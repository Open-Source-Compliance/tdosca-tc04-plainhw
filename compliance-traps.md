# Compliance Traps of TDOSCA-TC04-PLAINHW

The test case input (= open source software)

* This app uses different licenses:
  - The class *Main* is licensed under the MIT license
  - The classes *Greeter* and *GreeterTest* are divergently licensed under the Apache-v2 license
  - The classs *Tipster* and *TipsterTest*a are divergently licensed under the BSD-3Clause license
  - The graddle elements are licensed under the the Apache-v2 license
* integrates the BSD-3-Clause license text into the file header
* delivers the other licensed as files
  - named LICENSE (MIT)
  - named LICENSE.apache-v2
* offers a NOTICE file for the class greeter (but devialty named it NOTICE.md)
* the file LICENSE  contains the text of the MIT license but does not declare to be the MIT license
* contains the gradle wrapper script, created by 'gradle wrapper' and the gradle-wrapper.jar  both licensed under the Apache-v2 license (= LICENSE.gradle) => A tool which automatically generates the sufficient compliance artifacts must/should create
  - the artifacts for the repository (= including the gradle artifacts)
  - the artifacts for the tdosca-tc04.jar file (= excluding the gradle artifacts)
* does not contain the gradle-NOTICE-file due to the fact, that the repository [https://github.com/gradle/gradle](https://github.com/gradle/gradle) itself does not contain such a file named NOTICE
