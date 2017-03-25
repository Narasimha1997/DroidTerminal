# DroidTerminal
A simple terminal emulator for Android. Upgrading in process

<h2>What can this app do?</h2>
<p> The app is basically a terminal emulator used for executing Linux command, Since Android is based on a Linux Kernel it can execute basic
shell commands, but shell is not visible to the userland, But internally it is the feature of all Linux based systems.</p>

<h2>How user can access the Linux Shell in Android? </h2>
<p>For every app there is a process which is created when it is opened, The Unix and Unix like Process has the ability to create a new Process
with the help of kernel by using fork and exec mechanism, So here using a Java package Runtime and Process (java.lang.Process) we are creating
a new process of the shell by passing command as an argument to exec() function. So now an instance of shell is created in the background.
Since android does not provide any interface for interacting with the shell directly we use getInputStream() method. This method just
extracts the data produced by the shell instance or any process which is created using java.lang.Process object.</p>
<p>   Once the execution is complete getInputStream() provides data to the BufferedReader we can extract the data in the form of Strings,
This string be displayed or any operation can be performed on it, here we just display it on the TextView. The code is really simple!! </p>

<h2>By: Narasimha Prasanna HN, KSIT</h2>
<h2>9611818690</h2>
