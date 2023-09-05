RSTF - Robust Systems Test Framework
Version 1.0beta

The Robust Systems Test Framework (RSTF) provides a means of
specifying and running test programs on various computation
platforms. RSTF provides a level of specification above standard
scripting languages. During a set of runs, standard timing information
is collected. The RSTF specification can also gather job-specific
information, and can include ways to characterize test outcomes. All
results and scripts can be stored into and retrieved from an SQL
database for later data analysis. RSTF also provides operations for
managing the script and result files, and for compiling applications
and gathering compilation information such as optimization flags.

RSTF was developed to support comparative benchmarking.
Other users  are interested in adopting the software for managing their own
benchmarking runs. Future enhancements would allow RSTF to be used for
automated testing of large systems.

RSTF tests are specified using an XML-based markup language. The file
can be parsed and either entered into an SQL database or converted
into an executable PERL script for later execution. When the PERL
script is run, timing and other data is gathered from the test case in
question, and the results are placed back into an XML file that can be
imported into the database. The underlying database is PostgreSQL. A
standard XML parsing library is used for reading the XML
files. Database updates are handled using standard techniques. The
database schema is delivered with the system.

DOCUMENTATION

Two PDF files contain the bulk of the documentation:

	cmd_ref.pdf documents the 'rst' command line interface
	refman.pdf  documents the XML markup language and it use.

In this release, refman.pdf only touches on many aspects of the language
and the markup. 

FILES & DIRECTORIES:
	./Makefile.PL - MakeMaker input to generate Makefile
	./README    - This file.
	./INSTALL   - Installation instructions
	./MANIFEST  - list of all files in distribution

	./doc - documentation files
	./scripts - rst command line
	./etc     - DTD files for XML
	./lib     - Perl Code
	./toolinfo_scripts - scripts for parsing compiler output produced by 'rst make' command

INSTALLATION

See the INSTALL file in this directory.

DEPENDENCIES

RSTF uses the following open source components:
	PostgreSQL database  -- http://www.postgresql.org
	Expat XML parser     -- http://expat.sourceforge.net
	Perl modules         -- http://www.cpan.org

The installer itself uses the AppConfig module, so install it first. The installer requires 
the following Perl modules:

	AppConfig
	Class::MethodMaker
	Cwd
	DBI
	DBD::Pg
	Data::Dumper
	Date::Manip
	Fcntl
	File::Copy
	File::Path
	Getopt::Long
	IO::File
	IPC::Run
	POSIX
	Sys::Hostname
	Time::HiRes
	XML::Twig

COPYRIGHT AND LICENCE

Copyright (c) 2004, Sandia Corporation. 
Under the terms of Contract DE-AC04-94AL85000 with Sandia Corporation, the
U.S. Government retains certain rights in this software.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are
met:

    * Redistributions of source code must retain the above copyright
      notice, this list of conditions and the following disclaimer.

    * Redistributions in binary form must reproduce the above
      copyright notice, this list of conditions and the following disclaimer
      in the documentation and/or other materials provided with the
      distribution.

    * Neither the name of the Sandia Corporation nor the names of its
      contributors may be used to endorse or promote products derived from
      this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
