--------------------------------------------------------------------------
 Licensed to the Apache Software Foundation (ASF) under one
 or more contributor license agreements.  See the NOTICE file
 distributed with this work for additional information
 regarding copyright ownership.  The ASF licenses this file
 to you under the Apache License, Version 2.0 (the
 "License"); you may not use this file except in compliance
 with the License.  You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing,
 software distributed under the License is distributed on an
 "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
 KIND, either express or implied.  See the License for the
 specific language governing permissions and limitations
 under the License.
--------------------------------------------------------------------------
$Id$
--------------------------------------------------------------------------

The Turbine Website Instructions
--------------------------------

The Turbine web site is based on .xml files which are transformed
into .html files using Maven.

<http://maven.apache.org/>

This is the wrapper site for the released Turbine builds. New/Changed Turbine builds should be added/updated here: 
- xdocs/index.xml
- xdocs/news.xml
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
ok, you can check your .xml files back into Subversion.

To deploy the site execute:

mvn site-deploy

To do this you need an account on the people.apache.org machine!!

- after deployment check/cleanup local deployment path as defined in turbine.site.cache. By default it's in user.home/turbine-sites/site.

