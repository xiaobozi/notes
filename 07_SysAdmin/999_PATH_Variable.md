## What is the PATH variable?

When you run a command in the CL, it looks for the executable files using the directories listed in your *PATH variables* as a map. Given this, when you add a new executable, you may need to specify it's directory in your PATH variable. 


## View your current PATH

Mac users, this command will show you your PATH variable:

	echo $PATH
	
Windows users, this command will show you your PATH variables.

	PATH

## Edit your PATH

Mac users, follow these instructions: [Mac OSX Change Path Variables](http://www.tech-recipes.com/rx/2621/os_x_change_path_environment_variable/).

Windows users, to edit your PATH variables goto *My Computer* > *Properties* > *Advanced* > *Environment Variables* > *Path*.

Each path is separated by a semi-colon. Here's an example PATH variable:

	%SystemRoot%\system32;%SystemRoot%;%SystemRoot%\System32\Wbem;%SYSTEMROOT%\System32\WindowsPowerShell\v1.0\;C:\Program Files\Git\cmd;C:\Program Files\nodejs\;

Let's look at an example scenario where you want to add a php executable (`php.exe`) that comes with MAMP to your PATH variable. 

If you have MAMP installed, you should have a a `php.exe` file in `C:\MAMP\bin\php\php5.5.7\`, so this is the directory you'd want to add to your PATH.

<img src='http://making-the-internet.s3.amazonaws.com/laravel-setting-path-variable-on-windows.png?@2x' class='' style='max-width:1371px; width:75%' alt=''>

Make sure you end your path it with a trailing backslash. The idea is to point to the directory where `php.exe` can be found, not the actual `php.exe` file..

Ok/Save your changes.

Restart your Command Line.

Test it out:

	php -v
	
You should now see version information about PHP; you have confirmed that you can execute PHP from the command line.


### Reference
+ [SO: Adding directory to PATH Environment Variable in Windows](http://stackoverflow.com/questions/9546324/adding-directory-to-path-environment-variable-in-windows)
+ [How to set path and environment variables in Windows](http://www.computerhope.com/issues/ch000549.htm)
