# WorkHorz-Server

A web-application-framework in modern C++ with an integrated bare-essentials webserver and a Python3 plugin ability. Works best for middle- to enterprise-sized websites that need top performance, high security, easy integration into existing OS and libraries and full control over their web-app. The Open-Source version is of course free of charge. Business users should consider the commercial license which frees them to share the source code.

## Planning and Architecture
These are the modules that are planned for the first phase. Depending on the input and experience with it these may change over time.
- [x] Modules
  - [ ] Template Cacher
  - [ ] Webserver (HTTP/HTTPS)
    - [ ] Websockets-Server
  - [ ] Python3 Plugin Mgmt.
  - [ ] Security Mgmt.
  - [ ] MVC (Server) & MCCV (Server + Client) Paradigm
  - [ ] Balancing Mgmt.
  - [ ] OS & Utility Module
  - [ ] Session Mgmt.
  - [ ] Application API (for the customer WebApp)
  - [ ] ToolCase (mostly external units)
    - [ ] Scaffolding
    - [ ] WebApp Mgmt.
    - [ ] Build & Deployment Mgmt.
    - [ ] Unit-Testing

## Technical Requirements
I want to use pure C++11/14 wherever possible and sound. I do this with the intention to make the development and maintenance easier and the resulting binaries faster. But it is also equally sensible to use good and well tested libraries that offer features which would otherwise be difficult or too lengthy to write myself. Out of all this I have the following list of required technical tools/libs:
* GCC >= 4.8.2, MSVC >= 2013
* Intended OS platforms: Linux, OpenBSD, Windows, Mac OS X - (development as of now mainly on Windows)
* Boost >= 1.56 (to be tested once officially released)
  * Filesystem
  * Program Options
  * RegEx
  * Log
  * perhaps LockFree
* Google Test >= 1.7
* Python >= 3.4
* LibreSSL (probably)
* dOxygen >= 1.8.7
* CppFormat (fast string formatting lib, http://cppformat.github.io/)
* ...

## Help Needed
I will greatly welcome help at any stage of the process. If you have any expertise that would help make progress in a module, please do contact me.

## Planing
I try out the Kanbanery Integration in GitHub to plan the tasks at hand better.

## Integration & Development
I'm trying out Travis-CI and Coverity Scan.
* Travis-CI status: ![Build Status](https://travis-ci.org/RedSilkSoftware/workhorz-server.svg?branch=master) 
* Coverity Scan (Code Analysis) status: ...

### Development Process
Vagrant could be used as a development and/or platform-testing environment. Needs more research. 
* [Vagrant](http://docs.vagrantup.com/)

### Deployment
Docker or Lmctfy could be a great way to make WorkHorz quickly available to admins. Needs more research. 
* [Docker](https://www.docker.io/)
* [Let Me Contain That For You](https://github.com/google/lmctfy)
