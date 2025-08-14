## Compile and install the application

3. Discover the Go install path, where the go command will install the current package.
You can discover the install path by running the go list command, as in the following example:

$ go list -f '{{.Target}}'

4. Add the Go install directory to your system's shell path.
That way, you'll be able to run your program's executable without specifying where the executable is.

On Linux or Mac, run the following command:
$ export PATH=$PATH:/path/to/your/install/directory
On Windows, run the following command:
$ set PATH=%PATH%;C:\path\to\your\install\directory
As an alternative, if you already have a directory like $HOME/bin in your shell path and you'd like to install your Go programs there, you can change the install target by setting the GOBIN variable using the go env command:

$ go env -w GOBIN=/path/to/your/bin
or

$ go env -w GOBIN=C:\path\to\your\bin

## Result of step 3 command:
PS C:\Users\Ricardo\Documents\GitHub\hello> go list -f '{{.Target}}'
C:\Users\Ricardo\go\bin\hello.exe

## Question:

What should be my go env command to install this application?
