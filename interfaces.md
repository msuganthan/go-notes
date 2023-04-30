* Basics
  ```
  type Writer interface {
    Write([]byte)(int, error)
  }
  
  type ConsoleWriter struct {}
  
  func(cw ConsoleWriter) Write(data []byte) (int, error) {
    n, err := fmt.Println(string(data))
    return n, err
  }
  ```
* Composing interfaces
  ```
  type Writer interface {
    Write([]byte) (int, error)
  }
  
  type Closer interface {
    Close() error
  }
  
  type WriterCloser interface {
    Writer
    Closer
  }
  ```
* Type conversion
 ```
  var wc WriterCloser = NewBufferedWriterCloser();
  bwc := wc.(*BufferedWriterCloser)
 ```
* Empty interface and type switches
  ```
  var i interface{} = 0
  switch i.(type) {
    case int:
      fmt.Println("i is an integer")
    case string:
      fmt.Prinln("i is a string")
    default:
      fmt.Println("I don't know what i is")
  }
  ```
 * Implementing with values vs. pointer
  * Method set of value is all methods with value receivers
  * Method set of pointer is all methods, regardless of receiver types.
* Best practices
  * Use many, small interfaces
    * Single method interface are some of the most powerful and flexible
      * io.Writer, io.Reader, interface{}
  * Don't export interfaces for types that will be consumed
  * Do export interfaces for types that will be used by package.
  * Design functions and methods to receive interface whenever possible.
