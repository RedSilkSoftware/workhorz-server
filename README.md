# WorkHorz-Server

A web-application-framework in modern C++ with an integrated bare-essentials webserver and a LUA/Python3 and other scripting language plugin ability. Works best for middle- to enterprise-sized websites that need top performance, high speed, high security, easy integration into existing OS and libraries and full control over their web-app. Also it allows the users to hot-swap between version (on a component level or whole app) to test out things or make the deployment faster. The Open-Source version is of course free of charge. Business users should consider the commercial license which frees them to share the source code.

## Planning and Architecture
These are the modules that are planned for the first phase. Depending on the input and experience with it these may change over time. Docker and/or Kubernetes containers will make the deployment in enterprise servers easier so this is also a requirement now.
- [x] Modules and Components
  - [ ] Scalable by design (on components level), and easier to keep it scalable
  - [ ] Template Cacher
  - [ ] Webserver (HTTP/HTTPS)
    - [ ] Websockets-Server
    - [ ] Push-Server
  - [ ] LUA Plugin Mgmt. (later more interpreted languages like https://github.com/cesanta/mjs)
  - [ ] Security Mgmt. + securing scripts
  - [ ] MVC (Server) & MCCV (Server + Client) Paradigm
  - [ ] Load Balancing Mgmt.
  - [ ] OS & Utility Module
  - [ ] Session Mgmt.
  - [ ] Application API (for the customer WebApp)
  - [ ] Logging (to text files and InfluxDB)
  - [ ] REST-API construction and scaffolding
  - [ ] GraphQL queries
  - [ ] RDBMS ORM access to the most used database engines (https://github.com/SOCI/soci)
    - [ ] Active Records Pattern integrated for ease of use
  - [ ] Compression outside of HTTP (https://github.com/rikyoz/bit7z)
  - [ ] Easy to add new APIs to external web services
  - [ ] Apache and nginx compatible configuration of the integrated webserver (highest performance)
    - [ ] Webapps can also run under those with FastCGI if desired
  - [ ] Use of external caching like with Redis or memcached
  - [ ] Licensing server and management
  - [ ] Marketplace for 3rd party components
  - [ ] Easy integration into existing PHP web applications (as an extension)
  - [ ] Easy translation of webpages and content
  - [ ] Chatbots integration (like http://reo7sp.github.io/tgbot-cpp)
  - [ ] JWT Json Web Tokens
  - [ ] Login/Registration generation
  - [ ] Auth/Permission generation
  - [ ] ToolCase (mostly external units)
    - [ ] Scaffolding
    - [ ] WebApp Mgmt.
    - [ ] Build & Deployment Mgmt.
    - [ ] Unit-Testing
- [x] Adminstration and Monitorig
  - [ ] Qt desktop and mobile app for monitoring and configuration (remote access)
  - [ ] Integration or interconnection with monitoring tools like NagiosXI, Icinga, Monitis and the likes
  - [ ] Visual plugin management
  - [ ] Visual permission management
  - [ ] Browse log files easier with smart filtering to find what you need faster

## Technical Requirements
I want to use pure C++11/17 wherever possible and sound. I do this with the intention to make the development and maintenance easier and the resulting binaries faster. But it is also equally sensible to use good and well tested libraries that offer features which would otherwise be difficult or too lengthy to write myself. Out of all this I have the following list of required technical tools/libs:
* GCC >= 9.2 or CLANG >= 9.0, MSVC >= 2019 with C++17
* Intended OS platforms: Linux, OpenBSD, Windows, Mac OS X - (development as of now mainly on Windows)
* Boost >= 1.72 (to be tested once officially released)
  * Filesystem
  * Program Options
  * RegEx
  * Log
  * perhaps LockFree
* Catch2 >= 2.11.1 (testing framework, header-only)
* LUA >= 5.4 (cpp wrapper lib Sol2 https://github.com/ThePhD/sol2)
* OpenSSL >= 1.1.1
* dOxygen >= 1.8.18
* fmt (fast string formatting lib, https://github.com/fmtlib/fmt/)
* CMake >= 3.16.4
* Mongoose Embedded Webserver
* Monitoring integration (like https://prometheus.io/)
* Testing generation https://github.com/emil-e/rapidcheck
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
Docker/Kubernetes (or Lmctfy) will be a great way to make WorkHorz quickly available to admins. It is an ultimate goal of deliverables. Needs more research. 
* [Docker](https://www.docker.io/)
* [Let Me Contain That For You](https://github.com/google/lmctfy)
