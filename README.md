
smmn
====

**s(u)mm(o)n - mini xslt build.xml-processor** ( Version 1.0 )

smmn is a basic xml/xslt build system for small projects.
Place the smmn script in your project base folder, cobble up a build.xml and off you go.
See included sample build.xml to play around with.

## License ##

All source code is licensed under the open source BSD 2-clause license:
Copyright (c) 2014, Christian Himpe

## Dependencies ##

* libxslt

## Usage ##

`$ ./smmn RULENAME`

## build.xml ##

The build.xml is best easiest written obeying to the [MicroXML specification](https://www.ibm.com/developerworks/library/x-microxml1/).

### Structure + Tags ###

* project    ( *root tag* )
	* rule ( *each build rule is enclosed by this tag* )
		* name ( *the rule name identifier* )
		* compiler ( *binary name of the compiler to be used* )
		* sources ( *source group*)
			* source ( *each source file gets its own* )
		* path ( *path group* )
			* source ( *source path* )
			* include ( *library path* )
			* library ( *include path* )
		* libs ( *lib group* )
			* lib ( *each lib gets its own* )
		* defines ( *define group* )
			* define ( *each define gets its own* )
		* flags ( *flag group* )
			* flag ( *flags for compile and link steps* )
			* cflag ( *compile flags* )
			* lflag ( *link flags* )
		* binary ( *name of the binary* )
		* message ( *message to emit when done* )
		* action ( *some command to execute* )

