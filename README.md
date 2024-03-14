## Remote Debugging and Logging Prework

### Using `grep` and `less` to examine logs
In this activity you will use the commands you've just learned about to look at some real logs. These log files are
pulled from an example web application, for which the main page will not load. The user is seeing an unfriendly error
message "Encountered exception".
 
You are tasked with figuring out what's gone wrong.
 
1. Check out the contents of the project directory.
2. In your terminal, change directories into the `logs` subdirectory - in the same directory as this README.
3. First, we should find out what logs contain information about the error we’re seeing. 
  * Use `grep` in the log directory to find files containing the error exception message.
    * [How do I use grep with a directory?](./hints/hint_01.md)
  * Next, let’s find the error message in the logs.
    * Use `less` to open one of the files found above. Resist the urge to open the file in a text editor!
    * Search the file for the error message by typing `/Encountered exception` and hitting enter.
  * Reading through the logs, you'll encounter an exception message, "I'm responsible for your woes," followed by a
      stack trace.
 
In that stack trace, you will be able to see what class the error occurred in (usually the very first class listed in
the stack trace). Go back to the Canvas quiz and enter that class name as the answer to the quiz question.
 
If this were a real Amazon application, you could then go find the source code of that class and see if you are able to 
identify the problem. You would just check out the code and use your IDE debugger to do some remote debugging.
