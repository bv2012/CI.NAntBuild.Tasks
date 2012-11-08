NAnt Task for MSTest Code Coverage Reporting
============================================

A NAnt task for transforming MSTest's binary code coverage report to XML. The task outputs a serialized DataSet; you will probably need to run an XSL transform to get it into a useful format. See `MSTestCoverageToEmma.xsl` for an example of converting to the format used by Jenkin's Emma plugin.

This NAnt task is forked from Gareth Redman's CI.MSBuild.Tasks project, which adapted the code provided by http://archive.msdn.microsoft.com/vscoveragetoxmltask and http://wiki.hudson-ci.org/display/HUDSON/MSTest+Coverage+Reports to permit the use of Visual Studio 2010.

See `Example.build` for usage.

Building
--------

Building this task requires the following dependencies:
* NAnt Core libraries
* Visual Studio 2010 Code Coverage Test library

These assemblies are not included as part of this project. The Visual Studio Code Coverage library should be provided as part of Visual Studio Premium or Ultimate (or whatever) and will be auto-magically detected as a project reference. The NAnt Core libraries can be provided by NuGet or the like.
