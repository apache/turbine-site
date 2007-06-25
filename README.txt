$Id$

The Turbine Website Instructions
--------------------------------

The Turbine web site is based on .xml files which are transformed
into .html files using Maven.

<http://maven.apache.org/>

Once you have the site checked out locally, cd into your
turbine-site directory and execute:

maven site

This will build the documentation into the target/docs/ directory. The output
will show you which files got re-generated.

If you would like to make modifications to the web site documents,
you simply need to edit the files in the xdocs/ directory.

Once you have built your documentation and confirmed that your changes are
ok, you can check your .xml files back into Subversion.

To deploy the site execute:

maven site:deploy
To do this you need an account on the people.apache.org machine!!

