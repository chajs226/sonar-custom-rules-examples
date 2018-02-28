

1. 소나 커스텀룰 프로젝트 다운받음. (https://github.com/SonarSource/sonar-custom-rules-examples)

2. sonarqube-5.6.7 다운로드 및 설치 (https://docs.sonarqube.org/display/SONAR/Get+Started+in+Two+Minutes)

3. Mysql 설치 및 설정 (https://gist.github.com/rasheedamir/11460beef67bc6b58d61)

4. Jenkins 에서 maven 빌드 + 소나 스캐너 설정


<Jenkins - Maven 빌드 설정>

구성 - JDK1.8, Maven3.0.5, Jekins2.89.4

(Jenkins의 Maven plugin 은 Maven 자체를 설치하는게 아니기 때문에, Maven bin은 별도로 설치를 해야함)

=====================================
Trouble Shooting

1. 소나 수행 시 아래와 같은 에러 발생

10:00:34.548 ERROR: Error during SonarQube Scanner execution
java.lang.IllegalStateException: Error when executing blame for file src/main/java/amis3/bp/bp/BpBpBgExtService.java

=> 소나큐브의 administrator - general 셋팅에 SCM Sensor 를 Disable 시킴. 프로젝트에 포함된 SVN 정보 파일이 문제를 일으키는 것 같음.

=====================================
Sonar Custom Rules Examples [![Build Status](https://travis-ci.org/SonarSource/sonar-custom-rules-examples.svg?branch=master)](https://travis-ci.org/SonarSource/sonar-custom-rules-examples)
==========

This repository contains project examples you can directly clone to bootstrap your own project to write custom rules for COBOL, Java, JavaScript, PHP, and RPG.

Related documentation is there: http://docs.sonarqube.org/display/DEV/Adding+Coding+Rules+using+Java

### License

Copyright 2016-2017 SonarSource.

Licensed under the [GNU Lesser General Public License, Version 3.0](http://www.gnu.org/licenses/lgpl.txt)
