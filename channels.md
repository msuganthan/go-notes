* Channel basics
  * create a channel with `make` command
    * make(chan int)
  * Send message into channel
    * ch <- val
  * Receive message from channel 
    * val := <-ch
  * Can have multiple senders and receivers
* Restricting data flow
  * Channel can be cast into send-only or receive only versions
    * Send-only: chan <- int
    * Receive-only <- chan int
* Buffered channels
  * Channels block sender side till receiver is available
  * Block receiver side till message is available 
  * Can decouple sender and receiver with buffered channel 
    * make(chan int, 50)
  * Use buffered channels when send and receive have assymmetric loading
* For..range loops with channel
  * Use to monitor channel and process messages as they arrive.
  * Loop exits when channel is closed
* Select statements
  * Allows gorountine to monitor several channels at once.
    * Blocks if all channels block
    * If multiple channels receive value simultaneously, behavior is undefined. 
