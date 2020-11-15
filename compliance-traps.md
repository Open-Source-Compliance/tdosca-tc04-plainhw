# Compliance Traps of TDOSCA-TC04-PLAINHW

* This app licenses its internal classes deviantly:
  - Default License: M.I.T
  - Deviantly licensed:
    - Greeter.java :- A.p.a.c.h.e-2.0 (see LICENSE.A.p.a.c.h.e-2.0)
    - GreeterTest.java :- A.p.a.c.h.e-2.0 (see LICENSE.A.p.a.c.h.e-2.0)
    - Tipster.java :- B.S.D-3-Clause
    - TipsterTest.java :- B.S.D-3-Clause

* On the toplevel the App delivers two license files
  - named LICENSE (MIT = Default License)
  - named LICENSE.Apache-2.0 (= valid for Greeter)
  - Hence the scanning tools must not confound these two licenses
* On the top level, the source repo (= input-sources) offers a NOTICE.md file valid for Greeter
* The file LICENSE contains the text of the MIT license but does not explicitly declare to be the MIT license

* Additionally the software depends on the external 3rd party components
  * apache-log4j:
    - repository: https://logging.apache.org/log4j/2.x/download.html
    - license: Apache-2.0
    - NOTICE.txt: yes
  * joda-time
    - repository: https://github.com/JodaOrg/joda-time/releases
    - license: Apache-2.0
    - NOTICE.txt: yes
  - The graddle wrapper elements are licensed under the the Apache-v2 license


* Finally the software contains the gradle wrapper script, created by 'gradle wrapper' and the gradle-wrapper.jar  both licensed under the Apache-v2 license (= LICENSE.gradle) => A tool which automatically generates the sufficient compliance artifacts must/should create
  - the artifacts for the repository (= including the gradle artifacts)
  - the artifacts for the tdosca-tc04.jar file (= excluding the gradle artifacts)
* does not contain the gradle-NOTICE-file due to the fact, that the repository [https://github.com/gradle/gradle](https://github.com/gradle/gradle) itself does not contain such a file named NOTICE
