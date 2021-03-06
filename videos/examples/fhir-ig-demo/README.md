# FHIR IG demo playlist

The following subsections are based on the videos in the playlist. Each subsection outlines the steps for that video, links to resources, etc.

## Initial setup

* Create initial directories for the project.
  * A root directory for the overall project, `fhir-ig-demo` in this case.
  * A subdirectory for IG specific content. It's named `ig_root` in this example but it can be any name.
    * The `input` directory within this directory is the source code for the IG.
    * Other directories will be created within this directory as part of the build process.
* Download the latest IG publisher Jar file
  * From https://github.com/HL7/fhir-ig-publisher/releases
  * Occasionally the latest release might have a bug and you need to revert back to an older version.
  * Optionally tag the downloaded Jar file with the version number to keep them separate from each other if needed.
  * You can place this file anywhere. For this example it's located in the `ig_root` folder.
  * You will need Java installed on your machine. See https://adoptopenjdk.net/
  * You will also need Ruby and Jekyll installed according tho the following instructions https://jekyllrb.com/docs/installation/windows/
* Adjust .gitignore file in the root directory to ignore the large Jar files.
* Create the ig.ini publisher configuration file.
  * Name and directory can be changed but its location sets the root/working directory for the publisher tool.
  * The location of this file is considered to be the root of the IG working directory, `ig_root` in this example.
  * Other relative content/paths are relative to the location of this file.
* Create the ig.json ImplementationGuide instance
  * Place this file in the `input` directory.
  * Setup your IDE to support JSON Schema support to help with this step and later ones.
  * Name can be changed.
* Create the minimal needed structure and content under `ig_root`
  * The `input/resources` and `input/includes` folders
  * Populate the ig.json file with minimally needed content.
  * Create the `input/includes/menu.xml` file
* Open "Command Prompt" or "Windows PowerShell" and change to the project's `ig_root` directory by using the `cd` command.
  * Run `java -jar publisher_version.jar -ig ig.ini`
* The published site will be under `ig_root/output`
  * No index.html is created by default.
  * Open the toc.html file instead.
* See the following resources for additional documentation.
  * https://github.com/FHIR/sample-ig 
  * https://confluence.hl7.org/display/FHIR/IG+Publisher+Documentation
  * https://confluence.hl7.org/display/FHIR/Implementation+Guide+Parameters
  * https://build.fhir.org/ig/FHIR/ig-guidance/index.html
