My DUL Utilities Home
---------------------

This folder contains a number of utilities that can be helpful during a DUL engagement.

1) mpdriver

	This driver utility will work from a set of commands and execute them in parallel
	using the parallelism specified in the initialization file.

2) inifile

	This initialization file sets the parameters for the "mpdriver" script.  The
	currently supported parameters are "parallelism" and "debug".

3) dul_it

	The "mpdriver" script accepts a file that contains commands.  Each command must
	be contained in a single line.  More complex processing requires the use of a
	second script that embodies these details.  The "dul_it" script is such a script
	and invokes the DUL "unload table" command for the table specified on argument 1.

4) cmdfile

	The "mpdriver" script accepts a command file called "cmdfile".  This script is an
	example of such a command file.

5) dul.deny

	The "dul.deny" initialization file is used by the genMPDrvrCmdFile script to
	exclude non-application tables from the unload.

5) genMPDrvrCmdFile

	The "genMPDrvrCmdFile" script generates the "cmdfile" that controls the execution
	of mpdriver, by reading the USER.dat and TAB.dat files that are produced when
	the DUL utility extracts information from the system catalog tables.
