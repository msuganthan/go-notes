* Creating gorountines
  * Use go keyword in front of function call
  * When using anonymous functions, pass data as local variables
* Synchronization
  * Use sync.WaitGroup to wait for groups of gorountines to complete
  * Use sync.Mutex and sync.RWMutex to protect data access
* Parallelism
  * By default, Go will use CPU threads equal to available cores
  * Change with runtime.GOMAXPROCS
  * More threads can increase performance, but too many can slow it down
* Best Practices
  * Dont create gorountines in libraries
  * When creating a goroutine, know how it will end
    * Avoid subtle memory leaks
  * Check for race conditions at compile time.
