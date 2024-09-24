# The Turbine Website Instructions
--------------------------------

The Turbine web site is based on .xml files which are transformed
into .html files using Maven.

<http://maven.apache.org/>

This is the wrapper site for the released Turbine builds. New/Changed Turbine builds should be added/updated here: 
- xdocs/index.xml
- xdocs/news.xml
- xdocs/turbine/index.xml
- src/site/site.xml
- doap/doap_Turbine.rdf


Once you have the site checked out locally, cd into your
turbine-site directory and execute:

    mvn site

This will build the documentation into the target/site/ directory. The output
will show you which files got re-generated.

If you would like to make modifications to the web site documents,
you simply need to edit the files in the xdocs/ directory.

Once you have built your documentation and confirmed that your changes are
ok, you can check your .xml files back into Git.

## Deployment

To deploy the site execute:

Either save the content from target/site, switch to branch asf-site, copy the saved content to the root, add missing files, commit and push the changes.

Or:

    mvn clean site site:stage
    
    mvn scm-publish:publish-scm


