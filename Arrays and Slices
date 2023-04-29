* Arrays
  * Collection of items with same type
  * Fixed size
  * Declaration styles
    * a := [3]int{1, 2, 3}
    * a := [...]int{1, 2, 3}
    * var a [3]int
  * Access via zero-based index
  * len function returns size of array
  * Copies refer to different underlying data
* Slice
  * Backed by array
  * Creation of slice
    * Slice existing array or slice
    * Literal style
    * Via make function
      * a := make([]int, 10) //create slice with capacity and length == 10
      * a := make([]int, 10, 100) // slice with length == 10 and capacity == 100
    * len function returns length of slice
    * cap function returns length of underlying array
    * append function to add elements to slice
      * May cause expensive copy operation if underlying array is too small
    * Copies refer to same underlying array
