* Defer
  * Used to delay the execution of a statement until function exits
  * Useful to group "open" and "close" function together
    * Be careful in loops
  * Run in LIFO(last-in, first-out) order
  * Arguments evaluated at time defer is executed not a time of called function execution
* Panic
  * Occur when program cannot continue at all
    * Don't use when file can't be opened, unless it is critical
    * Use for unrecoverable events - cannot obtain TCP port for web server
  * Funtion will stop executing
    * Deferred functions will still fire
  * If nothing handles panic, program will exit
* Recover
  * Used to recover from panics
  * Only useful in deferred functions
  * Current function will not attempt to continue, but higher functions in call stack will
