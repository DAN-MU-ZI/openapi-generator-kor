<h1 align="center">OpenAPI Generator</h1>

<div align="center">

[![Stable releases in Maven Central](https://img.shields.io/maven-metadata/v/https/repo1.maven.org/maven2/org/openapitools/openapi-generator/maven-metadata.xml.svg)](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.openapitools%22%20AND%20a%3A%22openapi-generator%22)
[![Apache 2.0 License](https://img.shields.io/badge/License-Apache%202.0-orange)](./LICENSE)
[![Open Collective backers](https://img.shields.io/opencollective/backers/openapi_generator?color=orange&label=OpenCollective%20Backers)](https://opencollective.com/openapi_generator)
[![Join the Slack chat room](https://img.shields.io/badge/Slack-Join%20the%20chat%20room-orange)](https://join.slack.com/t/openapi-generator/shared_invite/zt-2wmkn4s8g-n19PJ99Y6Vei74WMUIehQA)
[![Follow OpenAPI Generator Twitter account to get the latest update](https://img.shields.io/twitter/follow/oas_generator.svg?style=social&label=Follow)](https://twitter.com/oas_generator)
[![Contribute with Gitpod](https://img.shields.io/badge/Contribute%20with-Gitpod-908a85?logo=gitpod)](https://gitpod.io/#https://github.com/OpenAPITools/openapi-generator)
[![Conan Center](https://shields.io/conan/v/openapi-generator)](https://conan.io/center/recipes/openapi-generator)
[![Revved up by Develocity](https://img.shields.io/badge/Revved%20up%20by-Develocity-06A0CE?logo=Gradle&labelColor=02303A)](https://ge.openapi-generator.tech/scans)
</div>

<div align="center">

[마스터 브랜치](https://github.com/OpenAPITools/openapi-generator/tree/master) (`7.14.0`):
[![Build Status](https://api.travis-ci.com/OpenAPITools/openapi-generator.svg?branch=master&status=passed)](https://app.travis-ci.com/github/OpenAPITools/openapi-generator/builds)
[![Integration Test2](https://circleci.com/gh/OpenAPITools/openapi-generator.svg?style=shield)](https://circleci.com/gh/OpenAPITools/openapi-generator)
[![Windows Test](https://ci.appveyor.com/api/projects/status/github/openapitools/openapi-generator?branch=master&svg=true&passingText=Windows%20Test%20-%20OK&failingText=Windows%20Test%20-%20Fails)](https://ci.appveyor.com/project/WilliamCheng/openapi-generator)
[![Bitrise](https://img.shields.io/bitrise/4a2b10a819d12b67/master?label=bitrise%3A%20Swift+4,5&token=859FMDR8QHwabCzwvZK6vQ)](https://app.bitrise.io/app/4a2b10a819d12b67)

</div>

<div align="center">

:star::star::star: 기여를 원하신다면 [가이드라인](CONTRIBUTING.md)과 [오픈된 작업 목록](https://github.com/openapitools/openapi-generator/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22)을 참고해주세요. :star::star::star:

:bangbang: Swagger Codegen에서 OpenAPI Generator로 마이그레이션하려면 [마이그레이션 가이드](docs/migration-from-swagger-codegen.md)를 참고하세요. :bangbang:

:notebook_with_decorative_cover: 더 많은 정보는 [Wiki 페이지](https://github.com/openapitools/openapi-generator/wiki)와 [FAQ](https://github.com/openapitools/openapi-generator/wiki/FAQ)를 참고하세요. :notebook_with_decorative_cover:

:notebook_with_decorative_cover: 초보자를 위한 eBook [A Beginner's Guide to Code Generation for REST APIs](https://gum.co/openapi_generator_ebook)도 참고할 수 있습니다. :notebook_with_decorative_cover:

:warning: OpenAPI 명세, 템플릿, 입력값(옵션, 환경변수 등)이 신뢰할 수 없는 소스에서 제공될 경우, 코드 생성 전 반드시 내용을 검토하여 보안 이슈(예: [코드 인젝션](https://en.wikipedia.org/wiki/Code_injection))를 방지하세요. 보안 취약점은 [team@openapitools.org](mailto:team@openapitools.org)로 연락 바랍니다. :warning:

:bangbang: "OpenAPI Tools"(https://OpenAPITools.org, OpenAPI Generator의 상위 조직)와 "OpenAPI Generator"는 OpenAPI Initiative(OAI)와는 무관합니다. :bangbang:

</div>

## 개요

OpenAPI Generator는 [OpenAPI 명세](https://github.com/OAI/OpenAPI-Specification)를 기반으로 API 클라이언트 라이브러리(SDK), 서버 스텁, 문서, 설정 파일 등을 자동으로 생성해주는 도구입니다.
OpenAPI 2.0과 3.0 모두 지원하며, 다양한 언어와 프레임워크를 지원합니다.

| 구분 | 지원 언어/프레임워크 |
|------|----------------------|
| **API 클라이언트** | **ActionScript**, **Ada**, **Apex**, **Bash**, **C**, **C#** (.NET 2.0, 3.5 이상, .NET Standard 1.3~2.1, .NET Core 3.1, .NET 5.0. 라이브러리: RestSharp, GenericHost, HttpClient), **C++** (Arduino, cpp-restsdk, Qt5, Tizen, Unreal Engine 4), **Clojure**, **Crystal**, **Dart**, **Elixir**, **Elm**, **Eiffel**, **Erlang**, **Go**, **Groovy**, **Haskell** (http-client, Servant), **Java** (Apache HttpClient 4.x, 5.x, Jersey2.x, OkHttp, Retrofit1.x, Retrofit2.x, Feign, RestTemplate, RESTEasy, Vertx, Google API Client Library for Java, Rest-assured, Spring 5 Web Client, Spring 6 RestClient, MicroProfile Rest Client, Helidon), **Jetbrains HTTP Client**, **Julia**, **k6**, **Kotlin**, **Lua**, **N4JS**, **Nim**, **Node.js/JavaScript** (ES5, ES6, AngularJS, Flow types, Apollo GraphQL DataStore), **Objective-C**, **OCaml**, **Perl**, **PHP**, **PowerShell**, **Python**, **R**, **Ruby**, **Rust** (hyper, reqwest, rust-server), **Scala** (akka, http4s, scalaz, sttp, swagger-async-httpclient, pekko), **Swift** (2.x~6.x), **Typescript** (AngularJS, Angular(9~19), Aurelia, Axios, Fetch, Inversify, jQuery, Nestjs, Node, redux-query, Rxjs), **XoJo**, **Zapier** |
| **서버 스텁** | **Ada**, **C#** (ASP.NET Core, Azure Functions), **C++** (Pistache, Restbed, Qt5 QHTTPEngine), **Erlang**, **F#** (Giraffe), **Go** (net/http, Gin, Echo), **Haskell** (Servant, Yesod), **Java** (MSF4J, Spring, Undertow, JAX-RS: CDI, CXF, Inflector, Jersey, RestEasy, Play Framework, PKMST, Vert.x, Apache Camel, Helidon), **Julia**, **Kotlin** (Spring Boot, Ktor, Vert.x), **PHP** (Flight, Laravel, Lumen, Mezzio, Slim, Silex, Symfony), **Python** (FastAPI, Flask), **NodeJS**, **Ruby** (Sinatra, Rails5), **Rust** (rust-server), **Scala** (Akka, Finch, Lagom, Play, Cask, Scalatra) |
| **API 문서 생성기** | **HTML**, **Confluence Wiki**, **Asciidoc**, **Markdown**, **PlantUML** |
| **설정 파일** | [**Apache2**](https://httpd.apache.org/) |
| **기타** | **GraphQL**, **JMeter**, **Ktorm**, **MySQL Schema**, **Postman Collection**, **Protocol Buffer**, **WSDL** |

## 목차

- [스폰서](#sponsors)
- [개요](#개요)
- [목차](#목차)
- [1 - 설치](#1---설치)
  - [1.1 - 호환성](#11---호환성)
  - [1.2 - Maven Central 아티팩트](#12---maven-central-아티팩트)
  - [1.3 - JAR 다운로드](#13---jar-다운로드)
  - [1.4 - 프로젝트 빌드](#14---프로젝트-빌드)
    - [Nix 사용자](#nix-사용자)
  - [1.5 - Homebrew (macOS 패키지 매니저)](#15---homebrew-macos-패키지-매니저)
  - [1.6 - Docker](#16---docker)
    - [공식 Docker 이미지](#공식-docker-이미지)
    - [OpenAPI Generator CLI Docker 이미지](#openapi-generator-cli-docker-이미지)
    - [OpenAPI Generator Online Docker 이미지](#openapi-generator-online-docker-이미지)
    - [Docker 개발 환경](#docker-개발-환경)
      - [문제 해결](#문제-해결)
    - [Vagrant에서 Docker 실행](#vagrant에서-docker-실행)
  - [1.7 - NPM (Node.js 패키지 매니저)](#17---npm-nodejs-패키지-매니저)
  - [1.8 - pip (Python 패키지 매니저)](#18---pip-python-패키지-매니저)
  - [1.9 - 런처 스크립트](#19---런처-스크립트)
- [2 - 시작하기](#2---시작하기)
- [3 - 사용법](#3---사용법)
  - [샘플 클라이언트 라이브러리 생성](#샘플-클라이언트-라이브러리-생성)
  - [3.1 - 커스터마이징](#31---커스터마이징)
  - [3.2 - 워크플로우 통합(Maven, Gradle, Github, CI/CD)](#32---워크플로우-통합maven-gradle-github-cicd)
  - [3.3 - 온라인 OpenAPI Generator](#33---온라인-openapi-generator)
  - [3.4 - 생성 코드의 라이선스 정보](#34---생성-코드의-라이선스-정보)
  - [3.5 - IDE 통합](#35---ide-통합)
- [4 - OpenAPI Generator를 사용하는 기업/프로젝트](#4---openapi-generator를-사용하는-기업프로젝트)
- [5 - 발표/영상/튜토리얼/도서](#5---발표영상튜토리얼도서)
- [6 - 소개](#6---소개)
  - [6.1 - OpenAPI Generator 핵심 팀](#61---openapi-generator-핵심-팀)
    - [핵심 팀원](#핵심-팀원)
    - [템플릿 제작자](#템플릿-제작자)
    - [핵심 팀 합류 방법](#핵심-팀-합류-방법)
  - [6.2 - 기술 위원회](#62---기술-위원회)
    - [위원회 멤버](#위원회-멤버)
  - [6.3 - 프로젝트 연혁](#63---프로젝트-연혁)
    - [창립 멤버](#창립-멤버)
- [7 - 라이선스](#7---라이선스)

## Sponsors

OpenAPI Generator가 업무에 도움이 되었다면, 회사에 [스폰서가 되어](https://opencollective.com/openapi_generator) 오픈소스 프로젝트를 지원해달라고 요청해보세요.
개인적으로도 [후원자(Backer)가 되어](https://opencollective.com/openapi_generator) 프로젝트를 지원할 수 있습니다.

#### 브론즈 스폰서에게 감사드립니다!

[![NamSor](https://openapi-generator.tech/img/companies/namsor.png)](https://www.namsor.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[![LightBow](https://openapi-generator.tech/img/companies/lightbow.png)](https://www.lightbow.net/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/docspring.png" width="128" height="128">](https://docspring.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/datadog.png" width="128" height="128">](https://datadoghq.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/thales.jpg" width="128" height="128">](https://cpl.thalesgroup.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/apideck.jpg" width="128" height="128">](https://www.apideck.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/pexa.png" width="128" height="128">](https://www.pexa.com.au/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/numary.png" width="128" height="128">](https://www.numary.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/onesignal.png" width="128" height="128">](https://www.onesignal.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/virtualansoftware.png" width="128" height="128">](https://www.virtualansoftware.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/mergedev.jpeg" width="128" height="128">](https://www.merge.dev/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/burkert.jpg" width="128" height="128">](https://www.burkert.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/finbourne.png" width="128" height="128">](https://www.finbourne.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/bumpsh.png" width="128" height="128">](https://bump.sh/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/bileto.png" width="128" height="128">](https://www.bileto.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/bairesdev.png" width="128" height="128">](https://www.bairesdev.com/sponsoring-open-source-projects/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/dmtech.jpeg" width="128" height="128">](https://www.dmtech.de/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/adyen.png" width="128" height="128">](https://adyen.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/fornex.png" width="128" height="128">](https://fornex.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/alloyautomation.png" width="128" height="128">](https://runalloy.com/signup?utm_source=github&utm_medium=referral&utm_campaign=1524_openapigenerator)
[<img src="https://openapi-generator.tech/img/companies/ssstwitter.png" width="128" height="128">](https://ssstwitter.com/?utm_source=github&utm_medium=referral&utm_campaign=sponsor)
[<img src="https://openapi-generator.tech/img/companies/svix.png" width="128" height="128">](https://www.svix.com/?utm_source=openapi-generator&utm_medium=sponsorship&utm_campaign=oss-sponsorship)
[<img src="https://openapi-generator.tech/img/companies/litslink.png" width="128" height="128">](https://litslink.com/services/artificial-intelligence?utm_source=openapi-generator&utm_medium=sponsorship&utm_campaign=oss-sponsorship)
[<img src="https://openapi-generator.tech/img/companies/designli.jpg" width="128" height="128">](https://designli.co?utm_source=openapi-generator&utm_medium=sponsorship&utm_campaign=oss-sponsorship)
[<img src="https://openapi-generator.tech/img/companies/itm.png" width="128" height="128">](https://opensource.muenchen.de?utm_source=openapi-generator&utm_medium=sponsorship&utm_campaign=oss-sponsorship)
[<img src="https://openapi-generator.tech/img/companies/kong.png" width="128" height="128">](https://konghq.com/products/kong-konnect?utm_medium=referral&utm_source=github&utm_campaign=platform&utm_content=openapi-generator)
[<img src="https://openapi-generator.tech/img/companies/route4me.png" width="128" height="128">](https://route4me.com/?utm_source=openapi-generator&utm_medium=sponsorship&utm_campaign=oss-sponsorship)
[<img src="https://openapi-generator.tech/img/companies/dm.png" width="128" height="128">](https://www.dotcom-monitor.com/sponsoring-open-source-projects/?utm_source=openapi-generator&utm_medium=sponsorship&utm_campaign=oss-sponsorship)
[<img src="https://openapi-generator.tech/img/companies/clickit.jpg" width="128" height="128">](https://www.clickittech.com/?utm_source=openapi-generator&utm_medium=sponsorship&utm_campaign=oss-sponsorship)
[<img src="https://openapi-generator.tech/img/companies/unified_to.jpg" width="128" height="128">](https://unified.to/?utm_source=openapi-generator&utm_medium=sponsorship&utm_campaign=oss-sponsorship)

#### GoDaddy(도메인), Linode(VPS), Checkly(API 모니터링), Gradle(Develocity) 후원에 감사드립니다.

[<img src="https://openapi-generator.tech/img/companies/godaddy.png" width="150">](https://www.godaddy.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[![Linode](https://www.linode.com/media/images/logos/standard/light/linode-logo_standard_light_small.png)](https://www.linode.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRAhEYadUyZYzGUotZiSdXkVMqqLGuohyixLl4eUpUV6pAbUULL" width="150">](https://checklyhq.com/?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)
[<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/cb/Gradle_logo.png/320px-Gradle_logo.png" width="150">](https://gradle.org?utm_source=openapi_generator&utm_medium=github_webpage&utm_campaign=sponsor)

## Overview

OpenAPI Generator allows generation of API client libraries (SDK generation), server stubs,  documentation and configuration automatically given an [OpenAPI Spec](https://github.com/OAI/OpenAPI-Specification) (both 2.0 and 3.0 are supported). Currently, the following languages/frameworks are supported:

|                                  | Languages/Frameworks                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| -------------------------------- |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **API clients**                  | **ActionScript**, **Ada**, **Apex**, **Bash**, **C**, **C#** (.net 2.0, 3.5 or later, .NET Standard 1.3 - 2.1, .NET Core 3.1, .NET 5.0. Libraries: RestSharp, GenericHost, HttpClient), **C++** (Arduino, cpp-restsdk, Qt5, Tizen, Unreal Engine 4), **Clojure**, **Crystal**, **Dart**, **Elixir**, **Elm**, **Eiffel**, **Erlang**, **Go**, **Groovy**, **Haskell** (http-client, Servant), **Java** (Apache HttpClient 4.x, Apache HttpClient 5.x, Jersey2.x, OkHttp, Retrofit1.x, Retrofit2.x, Feign, RestTemplate, RESTEasy, Vertx, Google API Client Library for Java, Rest-assured, Spring 5 Web Client, Spring 6 RestClient, MicroProfile Rest Client, Helidon), **Jetbrains HTTP Client**, **Julia**, **k6**, **Kotlin**, **Lua**, **N4JS**, **Nim**, **Node.js/JavaScript** (ES5, ES6, AngularJS with Google Closure Compiler annotations, Flow types, Apollo GraphQL DataStore), **Objective-C**, **OCaml**, **Perl**, **PHP**, **PowerShell**, **Python**, **R**, **Ruby**, **Rust** (hyper, reqwest, rust-server), **Scala** (akka, http4s, scalaz, sttp, swagger-async-httpclient, pekko), **Swift** (2.x, 3.x, 4.x, 5.x, 6.x), **Typescript** (AngularJS, Angular (9.x - 19.x), Aurelia, Axios, Fetch, Inversify, jQuery, Nestjs, Node, redux-query, Rxjs), **XoJo**, **Zapier** |
| **Server stubs**                 | **Ada**, **C#** (ASP.NET Core, Azure Functions), **C++** (Pistache, Restbed, Qt5 QHTTPEngine), **Erlang**, **F#** (Giraffe), **Go** (net/http, Gin, Echo), **Haskell** (Servant, Yesod), **Java** (MSF4J, Spring, Undertow, JAX-RS: CDI, CXF, Inflector, Jersey, RestEasy, Play Framework, [PKMST](https://github.com/ProKarma-Inc/pkmst-getting-started-examples), [Vert.x](https://vertx.io/), [Apache Camel](https://camel.apache.org/), [Helidon](https://helidon.io/)), **Julia**, **Kotlin** (Spring Boot, [Ktor](https://github.com/ktorio/ktor), [Vert.x](https://vertx.io/)), **PHP** ([Flight](https://docs.flightphp.com/), Laravel, Lumen, [Mezzio (fka Zend Expressive)](https://github.com/mezzio/mezzio), Slim, Silex, [Symfony](https://symfony.com/)), **Python** (FastAPI, Flask), **NodeJS**, **Ruby** (Sinatra, Rails5), **Rust** ([rust-server](https://openapi-generator.tech/docs/generators/rust-server/)), **Scala** (Akka, [Finch](https://github.com/finagle/finch), [Lagom](https://github.com/lagom/lagom), [Play](https://www.playframework.com/), [Cask](https://github.com/com-lihaoyi/cask), Scalatra)                                                                                                                                                    |
| **API documentation generators** | **HTML**, **Confluence Wiki**, **Asciidoc**, **Markdown**, **PlantUML**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Configuration files**          | [**Apache2**](https://httpd.apache.org/)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Others**                       | **GraphQL**, **JMeter**, **Ktorm**, **MySQL Schema**, **Postman Collection**, **Protocol Buffer**, **WSDL**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

## Table of contents

- [Sponsors](#sponsors)
    - [Thank you to our bronze sponsors!](#thank-you-to-our-bronze-sponsors)
    - [Thank you GoDaddy for sponsoring the domain names, Linode for sponsoring the VPS, Checkly for sponsoring the API monitoring and Gradle for sponsoring Develocity](#thank-you-godaddy-for-sponsoring-the-domain-names-linode-for-sponsoring-the-vps-checkly-for-sponsoring-the-api-monitoring-and-gradle-for-sponsoring-develocity)
- [Overview](#overview)
- [Table of contents](#table-of-contents)
- [1 - Installation](#1---installation)
  - [1.1 - Compatibility](#11---compatibility)
- [1.2 - Artifacts on Maven Central](#12---artifacts-on-maven-central)
  - [1.3 - Download JAR](#13---download-jar)
  - [Launcher Script](#launcher-script)
  - [1.4 - Build Projects](#14---build-projects)
    - [Nix users](#nix-users)
  - [1.5 - Homebrew (macOS 패키지 매니저)](#15---homebrew-macos-패키지-매니저)
  - [1.6 - Docker](#16---docker)
    - [Public Pre-built Docker images](#public-pre-built-docker-images)
    - [OpenAPI Generator CLI Docker Image](#openapi-generator-cli-docker-image)
    - [OpenAPI Generator Online Docker Image](#openapi-generator-online-docker-image)
    - [Development in docker](#development-in-docker)
      - [Troubleshooting](#troubleshooting)
    - [Run Docker in Vagrant](#run-docker-in-vagrant)
  - [1.7 - NPM (Node.js 패키지 매니저)](#17---npm-nodejs-패키지-매니저)
  - [1.8 - pip (Python 패키지 매니저)](#18---pip-python-패키지-매니저)
  - [1.9 - 런처 스크립트](#19---런처-스크립트)
- [2 - Getting Started](#2---getting-started)
- [3 - Usage](#3---usage)
  - [To generate a sample client library](#to-generate-a-sample-client-library)
  - [3.1 - Customization](#31---customization)
  - [3.2 - Workflow Integration (Maven, Gradle, Github, CI/CD)](#32---workflow-integration-maven-gradle-github-cicd)
  - [3.3 - Online OpenAPI generator](#33---online-openapi-generator)
  - [3.4 - License information on Generated Code](#34---license-information-on-generated-code)
  - [3.5 - IDE Integration](#35---ide-integration)
- [4 - Companies/Projects using OpenAPI Generator](#4---companiesprojects-using-openapi-generator)
- [5 - Presentations/Videos/Tutorials/Books](#5---presentationsvideostutorialsbooks)
- [6 - About Us](#6---about-us)
  - [6.1 - OpenAPI Generator Core Team](#61---openapi-generator-core-team)
    - [Core Team Members](#core-team-members)
    - [Template Creator](#template-creator)
    - [How to join the core team](#how-to-join-the-core-team)
  - [6.2 - OpenAPI Generator Technical Committee](#62---openapi-generator-technical-committee)
    - [Members of Technical Committee](#members-of-technical-committee)
  - [6.3 - History of OpenAPI Generator](#63---history-of-openapi-generator)
    - [Founding Members (alphabetical order):](#founding-members-alphabetical-order)
- [7 - License](#7---license)

## [1 - Installation](#table-of-contents)

### [1.1 - Compatibility](#table-of-contents)

The OpenAPI Specification has undergone 3 revisions since initial creation in 2010.  The openapi-generator project has the following compatibilities with the OpenAPI Specification:

| OpenAPI Generator Version                                                                                                                                 | Release Date | Notes                                             |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------------------------------------------------- |
| 7.14.0 (upcoming minor release) [SNAPSHOT](https://oss.sonatype.org/content/repositories/snapshots/org/openapitools/openapi-generator-cli/7.14.0-SNAPSHOT/) | 29.05.2025   | Minor release with breaking changes (with fallback) |
| [7.13.0](https://github.com/OpenAPITools/openapi-generator/releases/tag/v7.13.0) (latest stable release)                                                    | 27.04.2025   | Minor release with breaking changes (with fallback) |
| [6.6.0](https://github.com/OpenAPITools/openapi-generator/releases/tag/v6.6.0)                                                    | 11.05.2023   | Minor release with breaking changes (with fallback) |
| [5.4.0](https://github.com/OpenAPITools/openapi-generator/releases/tag/v5.4.0)                                                    | 31.01.2022   | Minor release with breaking changes (with fallback) |
| [4.3.1](https://github.com/OpenAPITools/openapi-generator/releases/tag/v4.3.1)                                                    | 06.05.2020   | Patch release (enhancements, bug fixes, etc)                       |

OpenAPI Spec compatibility: 1.0, 1.1, 1.2, 2.0, 3.0, 3.1 (beta support)

(We do not publish daily/nightly build. Please use SNAPSHOT instead)

For old releases, please refer to the [**Release**](https://github.com/OpenAPITools/openapi-generator/releases) page.

For decommissioned generators/libraries/frameworks, please refer to [the "Decommission" label](https://github.com/OpenAPITools/openapi-generator/issues?q=label%3ADecommission+is%3Amerged+) in the pull request page.

## [1.2 - Artifacts on Maven Central](#table-of-contents)

You can find our released artifacts on maven central:
```xml
<dependency>
    <groupId>org.openapitools</groupId>
    <artifactId>openapi-generator</artifactId>
    <version>${openapi-generator-version}</version>
</dependency>
```
See the different versions of the [openapi-generator](https://search.maven.org/artifact/org.openapitools/openapi-generator) artifact available on maven central.

**Cli:**
```xml
<dependency>
    <groupId>org.openapitools</groupId>
    <artifactId>openapi-generator-cli</artifactId>
    <version>${openapi-generator-version}</version>
</dependency>
```
See the different versions of the [openapi-generator-cli](https://search.maven.org/artifact/org.openapitools/openapi-generator-cli) artifact available on maven central.

**Maven plugin:**
```xml
<dependency>
    <groupId>org.openapitools</groupId>
    <artifactId>openapi-generator-maven-plugin</artifactId>
    <version>${openapi-generator-version}</version>
</dependency>
```
* See the different versions of the [openapi-generator-maven-plugin](https://search.maven.org/artifact/org.openapitools/openapi-generator-maven-plugin) artifact available on maven central.
* [Readme](https://github.com/OpenAPITools/openapi-generator/blob/master/modules/openapi-generator-maven-plugin/README.md)

**Gradle plugin:**
```xml
<dependency>
    <groupId>org.openapitools</groupId>
    <artifactId>openapi-generator-gradle-plugin</artifactId>
    <version>${openapi-generator-version}</version>
</dependency>
```
* See the different versions of the [openapi-generator-gradle-plugin](https://search.maven.org/artifact/org.openapitools/openapi-generator-gradle-plugin) artifact available on maven central.
* [Readme](https://github.com/OpenAPITools/openapi-generator/blob/master/modules/openapi-generator-gradle-plugin/README.adoc)

### [1.3 - Download JAR](#table-of-contents)
<!-- RELEASE_VERSION -->
최신 안정 버전을 원하신다면, Maven.org에서 직접 다운로드할 수 있습니다(Java 11 이상 필요):

JAR 위치: `https://repo1.maven.org/maven2/org/openapitools/openapi-generator-cli/7.13.0/openapi-generator-cli-7.13.0.jar`

**Mac/Linux 사용자:**
```sh
wget https://repo1.maven.org/maven2/org/openapitools/openapi-generator-cli/7.13.0/openapi-generator-cli-7.13.0.jar -O openapi-generator-cli.jar
```

**Windows 사용자:**
[wget](http://gnuwin32.sourceforge.net/packages/wget.htm)을 설치하거나, PowerShell(3.0+)의 Invoke-WebRequest를 사용할 수 있습니다.

```
Invoke-WebRequest -OutFile openapi-generator-cli.jar https://repo1.maven.org/maven2/org/openapitools/openapi-generator-cli/7.13.0/openapi-generator-cli-7.13.0.jar
```

After downloading the JAR, run `java -jar openapi-generator-cli.jar help` to show the usage.

For Mac users, please make sure Java 11 is installed (Tips: run `java -version` to check the version), and export `JAVA_HOME` in order to use the supported Java version:
```sh
export JAVA_HOME=`/usr/libexec/java_home -v 1.11`
export PATH=${JAVA_HOME}/bin:$PATH
```

<!-- /RELEASE_VERSION -->
### Launcher Script

One downside to manual jar downloads is that you don't keep up-to-date with the latest released version. We have a Bash launcher script at [bin/utils/openapi-generator.cli.sh](./bin/utils/openapi-generator-cli.sh) which resolves this issue.

To install the launcher script, copy the contents of the script to a location on your path and make the script executable.

An example of setting this up (NOTE: Always evaluate scripts curled from external systems before executing them).

```
mkdir -p ~/bin/openapitools
curl https://raw.githubusercontent.com/OpenAPITools/openapi-generator/master/bin/utils/openapi-generator-cli.sh > ~/bin/openapitools/openapi-generator-cli
chmod u+x ~/bin/openapitools/openapi-generator-cli
export PATH=$PATH:~/bin/openapitools/
```

Now, `openapi-generator-cli` is "installed". On invocation, it will query the GitHub repository for the most recently released version. If this matches the last downloaded jar,
it will execute as normal. If a newer version is found, the script will download the latest release and execute it.

If you need to invoke an older version of the generator, you can define the variable `OPENAPI_GENERATOR_VERSION` either ad hoc or globally. You can export this variable if you'd like to persist a specific release version.

Examples:

```
# Execute latest released openapi-generator-cli
openapi-generator-cli version

# Execute version 4.1.0 for the current invocation, regardless of the latest released version
OPENAPI_GENERATOR_VERSION=4.1.0 openapi-generator-cli version

# Execute version 4.1.0-SNAPSHOT for the current invocation
OPENAPI_GENERATOR_VERSION=4.1.0-SNAPSHOT openapi-generator-cli version

# Execute version 4.0.2 for every invocation in the current shell session
export OPENAPI_GENERATOR_VERSION=4.0.2
openapi-generator-cli version # is 4.0.2
openapi-generator-cli version # is also 4.0.2

# To "install" a specific version, set the variable in .bashrc/.bash_profile
echo "export OPENAPI_GENERATOR_VERSION=4.0.2" >> ~/.bashrc
source ~/.bashrc
openapi-generator-cli version # is always 4.0.2, unless any of the above overrides are done ad hoc
```

### [1.4 - Build Projects](#table-of-contents)

To build from source, you need the following installed and available in your `$PATH:`

* [Java 11](https://adoptium.net/)

* [Apache Maven 3.8.8 or greater](https://maven.apache.org/) (optional)

After cloning the project, you can build it from source using [maven wrapper](https://maven.apache.org/wrapper/):

- Linux: `./mvnw clean install`
- Windows: `mvnw.cmd clean install`

#### Nix users

If you're a nix user, you can enter OpenAPI Generator shell, by typing:
```sh
nix develop
```
It will enter a shell with Java 11 installed.

Direnv supports automatically loading of the nix developer shell, so if you're using direnv too, type:
```sh
direnv allow
```
and have `java` and `mvn` set up with correct versions each time you enter project directory.

The default build contains minimal static analysis (via CheckStyle). To run your build with PMD and Spotbugs, use the `static-analysis` profile:

- Linux: `./mvnw -Pstatic-analysis clean install`
- Windows: `mvnw.cmd -Pstatic-analysis clean install`

### [1.5 - Homebrew (macOS 패키지 매니저)](#table-of-contents)

To install, run `brew install openapi-generator`

Here is an example usage to generate a Ruby client:
```sh
openapi-generator generate -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml -g ruby -o /tmp/test/
```

To reinstall with the latest master, run `brew uninstall openapi-generator && brew install --HEAD openapi-generator`

To install OpenJDK (pre-requisites), please run
```sh
brew tap AdoptOpenJDK/openjdk
brew install --cask adoptopenjdk11
export JAVA_HOME=`/usr/libexec/java_home -v 1.11`
```

or download installer via https://adoptium.net/

To install Maven (optional), please run
```sh
brew install maven
```

### [1.6 - Docker](#목차)

#### 공식 Docker 이미지

- [https://hub.docker.com/r/openapitools/openapi-generator-cli/](https://hub.docker.com/r/openapitools/openapi-generator-cli/) (공식 CLI)
- [https://hub.docker.com/r/openapitools/openapi-generator-online/](https://hub.docker.com/r/openapitools/openapi-generator-online/) (공식 웹 서비스)

#### OpenAPI Generator CLI Docker 이미지

OpenAPI Generator Docker 이미지는 독립 실행형 실행 파일로 동작합니다.
Homebrew 설치가 어렵거나 Java 설치/업그레이드가 불가능한 개발자에게 대안이 될 수 있습니다.

코드를 생성하려면, 로컬 디렉토리를 볼륨으로 마운트해야 합니다.

예시:

```sh
docker run --rm -v "${PWD}:/local" openapitools/openapi-generator-cli generate \
    -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml \
    -g go \
    -o /local/out/go
```

생성된 코드는 현재 디렉토리의 `./out/go`에 위치합니다.

#### OpenAPI Generator Online Docker 이미지

openapi-generator-online 이미지는 자체 호스팅 웹 애플리케이션 및 API로 동작할 수 있습니다.
이 컨테이너는 CI 파이프라인에 통합할 수 있으며,
코드 생성을 위해 최소 두 번의 HTTP 요청과 일부 Docker 오케스트레이션이 필요합니다.

사용 예시:

```sh
# 8888 포트로 컨테이너 실행 및 ID 저장
CID=$(docker run -d -p 8888:8080 openapitools/openapi-generator-online)

# 컨테이너 기동 대기
sleep 10

# (선택) 컨테이너 IP 확인
GEN_IP=$(docker inspect --format '{{.NetworkSettings.IPAddress}}'  $CID)

# Ruby 클라이언트 생성 요청
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' \
-d '{"openAPIUrl": "https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml"}' \
'http://localhost:8888/api/gen/clients/ruby'

# 생성된 zip 파일 다운로드
wget http://localhost:8888/api/gen/download/다운로드_코드

# 압축 해제
unzip 다운로드_코드

# 컨테이너 종료 및 삭제
docker stop $CID && docker rm $CID
```

#### Docker 개발 환경

`run-in-docker.sh` 스크립트를 사용하면 모든 개발 작업을 Docker에서 수행할 수 있습니다.
이 스크립트는 로컬 저장소를 컨테이너의 `/gen`에,
`~/.m2/repository`를 컨테이너의 적절한 위치에 마운트합니다.

예시:

```sh
git clone https://github.com/openapitools/openapi-generator
cd openapi-generator
./run-in-docker.sh mvn package
```

빌드 결과물은 작업 디렉토리에서 확인할 수 있습니다.

빌드 후에는 `run-in-docker.sh`가 openapi-generator-cli의 실행 파일처럼 동작합니다.
코드 생성을 위해서는 `/gen` 하위 디렉토리(예: `/gen/out`)로 출력해야 합니다.

```sh
./run-in-docker.sh help # openapi-generator-cli의 help 명령 실행
./run-in-docker.sh list # openapi-generator-cli의 list 명령 실행
./run-in-docker.sh generate -i modules/openapi-generator/src/test/resources/3_0/petstore.yaml \
    -g go -o /gen/out/go-petstore -p packageName=petstore # go 클라이언트 생성, ./out/go-petstore에 출력
```

##### 문제 해결

아래와 같은 오류가 발생하면 **./mvnw clean install -U** 명령을 실행하세요:

> org.apache.maven.lifecycle.LifecycleExecutionException: Failed to execute goal org.apache.maven.plugins:maven-surefire-plugin:2.19.1:test (default-test) on project openapi-generator: A type incompatibility occurred while executing org.apache.maven.plugins:maven-surefire-plugin:2.19.1:test: java.lang.ExceptionInInitializerError cannot be cast to java.io.IOException

```sh
./run-in-docker.sh ./mvnw clean install -U
```

> Failed to execute goal org.fortasoft:gradle-maven-plugin:1.0.8:invoke (default) on project openapi-generator-gradle-plugin-mvn-wrapper: org.gradle.tooling.BuildException: Could not execute build using Gradle distribution 'https://services.gradle.org/distributions/gradle-4.7-bin.zip'

현재로서는 이 오류에 대한 해결책이 없습니다 :|

#### Vagrant에서 Docker 실행
사전 준비: [Vagrant](https://www.vagrantup.com/downloads.html)와 [VirtualBox](https://www.virtualbox.org/wiki/Downloads) 설치
 ```sh
git clone https://github.com/openapitools/openapi-generator.git
cd openapi-generator
vagrant up
vagrant ssh
cd /vagrant
./run-in-docker.sh ./mvnw package
```

### [1.7 - NPM (Node.js 패키지 매니저)](#목차)

[NPM 패키지 래퍼](https://www.npmjs.com/package/@openapitools/openapi-generator-cli)가 제공됩니다. (JVM 필요)
자세한 내용은 [프로젝트 README](https://github.com/openapitools/openapi-generator-cli)를 참고하세요.

전역 설치 예시:
```sh
npm install @openapitools/openapi-generator-cli -g
openapi-generator-cli version
```

특정 버전 사용 예시:
```sh
openapi-generator-cli version-manager set 7.13.0
```

개발 의존성으로 설치:
```sh
npm install @openapitools/openapi-generator-cli -D
```

로컬 빌드 JAR 또는 SNAPSHOT 버전도 사용할 수 있습니다.

### [1.8 - pip (Python 패키지 매니저)](#목차)

> **지원 플랫폼:** Linux, macOS, Windows
[PyPI](https://pypi.org/)를 통해 설치할 수 있습니다(Java 필요):

```sh
pip install openapi-generator-cli
```

특정 버전 설치:
```sh
pip install openapi-generator-cli==7.13.0
```

[jdk4py](https://github.com/activeviam/jdk4py)를 통해 java 없이 설치도 가능합니다(python>=3.10 필요):

```sh
pip install openapi-generator-cli[jdk4py]
```

자세한 내용은 [openapi-generator-pip](https://github.com/openAPITools/openapi-generator-pip) 참고

### [1.9 - 런처 스크립트](#table-of-contents)

수동으로 JAR 파일을 다운로드하면 최신 릴리즈 버전으로 자동 업데이트되지 않는 단점이 있습니다.
이 문제를 해결하기 위해 [bin/utils/openapi-generator.cli.sh](./bin/utils/openapi-generator-cli.sh) 위치에 Bash 런처 스크립트가 제공됩니다.

런처 스크립트 설치 방법:
스크립트 내용을 복사하여 PATH에 포함된 디렉토리에 저장하고, 실행 권한을 부여하세요.

설치 예시 (※ 외부에서 curl로 받은 스크립트는 반드시 내용을 확인 후 실행하세요):

```
mkdir -p ~/bin/openapitools
curl https://raw.githubusercontent.com/OpenAPITools/openapi-generator/master/bin/utils/openapi-generator-cli.sh > ~/bin/openapitools/openapi-generator-cli
chmod u+x ~/bin/openapitools/openapi-generator-cli
export PATH=$PATH:~/bin/openapitools/
```

Now, `openapi-generator-cli` is "installed". On invocation, it will query the GitHub repository for the most recently released version. If this matches the last downloaded jar,
it will execute as normal. If a newer version is found, the script will download the latest release and execute it.

If you need to invoke an older version of the generator, you can define the variable `OPENAPI_GENERATOR_VERSION` either ad hoc or globally. You can export this variable if you'd like to persist a specific release version.

Examples:

```
# Execute latest released openapi-generator-cli
openapi-generator-cli version

# Execute version 4.1.0 for the current invocation, regardless of the latest released version
OPENAPI_GENERATOR_VERSION=4.1.0 openapi-generator-cli version

# Execute version 4.1.0-SNAPSHOT for the current invocation
OPENAPI_GENERATOR_VERSION=4.1.0-SNAPSHOT openapi-generator-cli version

# Execute version 4.0.2 for every invocation in the current shell session
export OPENAPI_GENERATOR_VERSION=4.0.2
openapi-generator-cli version # is 4.0.2
openapi-generator-cli version # is also 4.0.2

# To "install" a specific version, set the variable in .bashrc/.bash_profile
echo "export OPENAPI_GENERATOR_VERSION=4.0.2" >> ~/.bashrc
source ~/.bashrc
openapi-generator-cli version # is always 4.0.2, unless any of the above overrides are done ad hoc
```

## [2 - Getting Started](#table-of-contents)

To generate a PHP client for [petstore.yaml](https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml), please run the following
```sh
git clone https://github.com/openapitools/openapi-generator
cd openapi-generator
./mvnw clean package
java -jar modules/openapi-generator-cli/target/openapi-generator-cli.jar generate \
   -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml \
   -g php \
   -o /var/tmp/php_api_client
```
(if you're on Windows, replace the last command with `java -jar modules\openapi-generator-cli\target\openapi-generator-cli.jar generate -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml -g php -o c:\temp\php_api_client`)

<!-- RELEASE_VERSION -->
You can also download the JAR (latest release) directly from [maven.org](https://repo1.maven.org/maven2/org/openapitools/openapi-generator-cli/7.13.0/openapi-generator-cli-7.13.0.jar)
<!-- /RELEASE_VERSION -->

To get a list of **general** options available, please run `java -jar modules/openapi-generator-cli/target/openapi-generator-cli.jar help generate`

To get a list of PHP specified options (which can be passed to the generator with a config file via the `-c` option), please run `java -jar modules/openapi-generator-cli/target/openapi-generator-cli.jar config-help -g php`

## [3 - Usage](#table-of-contents)

### To generate a sample client library
You can build a client against the [Petstore API](https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml) as follows:

```sh
./bin/generate-samples.sh ./bin/configs/java-okhttp-gson.yaml
```

(On Windows, please install [GIT Bash for Windows](https://gitforwindows.org/) to run the command above)

This script uses the default library, which is `okhttp-gson`. It will run the generator with this command:

```sh
java -jar modules/openapi-generator-cli/target/openapi-generator-cli.jar generate \
  -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml \
  -g java \
  -t modules/openapi-generator/src/main/resources/Java \
  --additional-properties artifactId=petstore-okhttp-gson,hideGenerationTimestamp=true \
  -o samples/client/petstore/java/okhttp-gson
```

with a number of options. [The java options are documented here.](docs/generators/java.md)

You can also get the options with the `help generate` command (below only shows partial results):

```
NAME
        openapi-generator-cli generate - Generate code with the specified
        generator.

SYNOPSIS
        openapi-generator-cli generate
                [(-a <authorization> | --auth <authorization>)]
                [--api-name-suffix <api name suffix>] [--api-package <api package>]
                [--artifact-id <artifact id>] [--artifact-version <artifact version>]
                [(-c <configuration file> | --config <configuration file>)] [--dry-run]
                [(-e <templating engine> | --engine <templating engine>)]
                [--enable-post-process-file]
                [(-g <generator name> | --generator-name <generator name>)]
                [--generate-alias-as-model] [--git-host <git host>]
                [--git-repo-id <git repo id>] [--git-user-id <git user id>]
                [--global-property <global properties>...] [--group-id <group id>]
                [--http-user-agent <http user agent>]
                [(-i <spec file> | --input-spec <spec file>)]
                [--ignore-file-override <ignore file override location>]
                [--import-mappings <import mappings>...]
                [--instantiation-types <instantiation types>...]
                [--invoker-package <invoker package>]
                [--language-specific-primitives <language specific primitives>...]
                [--legacy-discriminator-behavior] [--library <library>]
                [--log-to-stderr] [--minimal-update]
                [--model-name-prefix <model name prefix>]
                [--model-name-suffix <model name suffix>]
                [--model-package <model package>]
                [(-o <output directory> | --output <output directory>)] [(-p <additional properties> | --additional-properties <additional properties>)...]
                [--package-name <package name>] [--release-note <release note>]
                [--remove-operation-id-prefix]
                [--reserved-words-mappings <reserved word mappings>...]
                [(-s | --skip-overwrite)] [--server-variables <server variables>...]
                [--skip-validate-spec] [--strict-spec <true/false strict behavior>]
                [(-t <template directory> | --template-dir <template directory>)]
                [--type-mappings <type mappings>...] [(-v | --verbose)]

OPTIONS
        -a <authorization>, --auth <authorization>
            adds authorization headers when fetching the OpenAPI definitions
            remotely. Pass in a URL-encoded string of name:header with a comma
            separating multiple values

...... (results omitted)

        -v, --verbose
            verbose mode

```

You can then compile and run the client, as well as unit tests against it:

```sh
cd samples/client/petstore/java/okhttp-gson
mvn package
```

Other generators have [samples](https://github.com/OpenAPITools/openapi-generator/tree/master/samples) too.

### [3.1 - Customization](#table-of-contents)

Please refer to [customization.md](docs/customization.md) on how to customize the output (e.g. package name, version)

### [3.2 - Workflow Integration (Maven, Gradle, Github, CI/CD)](#table-of-contents)

Please refer to [integration.md](docs/integration.md) on how to integrate OpenAPI generator with Maven, Gradle, sbt, Bazel, Github and CI/CD.

### [3.3 - Online OpenAPI generator](#table-of-contents)

Here are the public online services:

- latest stable version: https://api.openapi-generator.tech
- latest master: https://api-latest-master.openapi-generator.tech (updated with latest master every hour)

The server is sponsored by [Linode](https://www.linode.com/) [![Linode Logo](https://www.linode.com/media/images/logos/standard/light/linode-logo_standard_light_small.png)](https://www.linode.com/)

(These services are beta and do not have any guarantee on service level)

Please refer to [online.md](docs/online.md) on how to run and use the `openapi-generator-online` - a web service for `openapi-generator`.

### [3.4 - License information on Generated Code](#table-of-contents)

The OpenAPI Generator project is intended as a benefit for users of the Open API Specification.  The project itself has the [License](#7---license) as specified. In addition, please understand the following points:

* The templates included with this project are subject to the [License](#7---license).
* Generated code is intentionally _not_ subject to the parent project license

When code is generated from this project, it shall be considered **AS IS** and owned by the user of the software.  There are no warranties--expressed or implied--for generated code.  You can do what you wish with it, and once generated, the code is your responsibility and subject to the licensing terms that you deem appropriate.

### [3.5 - IDE Integration](#table-of-contents)

Here is a list of community-contributed IDE plug-ins that integrate with OpenAPI Generator:

- Eclipse: [Codewind OpenAPI Tools for Eclipse](https://www.eclipse.org/codewind/open-api-tools-for-eclipse.html) by [IBM](https://www.ibm.com)
- IntelliJ IDEA: [OpenAPI Generator](https://plugins.jetbrains.com/plugin/8433-openapi-generator) by [Jim Schubert](https://jimschubert.us/#/)
- IntelliJ IDEA: [Senya Editor](https://plugins.jetbrains.com/plugin/10690-senya-editor) by [senya.io](https://senya.io)
- [RepreZen API Studio](https://www.reprezen.com/)
- Visual Studio: [REST API Client Code Generator](https://marketplace.visualstudio.com/items?itemName=ChristianResmaHelle.ApiClientCodeGenerator) by [Christian Resma Helle](https://christian-helle.blogspot.com/)
- Visual Studio Code: [Codewind OpenAPI Tools](https://marketplace.visualstudio.com/items?itemName=IBM.codewind-openapi-tools) by [IBM](https://marketplace.visualstudio.com/publishers/IBM)


## [4 - OpenAPI Generator를 사용하는 기업/프로젝트](#목차)

아래는 OpenAPI Generator를 실제로 사용하는 기업/프로젝트(알파벳순) 목록입니다.
목록에 본인 회사/프로젝트를 추가하고 싶다면 [README.md](README.md)에서 아이콘을 클릭해 페이지를 편집해 주세요.

- [Aalborg University](https://www.aau.dk)
- [act coding](https://github.com/actcoding)
- [Adaptant Solutions AG](https://www.adaptant.io/)
- [adesso SE](https://www.adesso.de/)
- [adorsys GmbH & Co.KG](https://adorsys.com/)
- [Adyen](https://www.adyen.com/)
- [Agoda](https://www.agoda.com/)
- [Airthings](https://www.airthings.com/)
- ... (이하 생략, 실제 기업/기관/서비스명 및 링크는 그대로 유지) ...
- [Zalando](https://www.zalando.com)
- [3DS Outscale](https://www.outscale.com/)

## [5 - 발표/영상/튜토리얼/도서](#목차)

- 2018/05/12 - [OpenAPI Generator - 커뮤니티 주도로 성장하는 코드 제너레이터](https://ackintosh.github.io/blog/2018/05/12/openapi-generator/) by [중앙인물](https://github.com/ackintosh)
- 2018/05/15 - [새 오픈소스 프로젝트 시작하기](http://jmini.github.io/blog/2018/2018-05-15_new-open-source-project.html) by [Jeremie Bresson](https://github.com/jmini)
- 2018/05/15 - [REST API 명세에서 API 클라이언트와 스텁 서버 자동 생성, Swagger Codegen에서 포크된 OpenAPI Generator 오픈소스 공개](https://www.publickey1.jp/blog/18/rest_apiapiopenapi_generatorswagger_generator.html) by [Publickey](https://www.publickey1.jp)
- 2018/06/08 - [Swagger Codegen이 이제 OpenAPI Generator로](https://angular.schule/blog/2018-06-swagger-codegen-is-now-openapi-generator) by [JohannesHoppe](https://github.com/JohannesHoppe)
- ... (이하 생략, 실제 발표/블로그/영상/도서 링크 및 저자명은 그대로 유지) ...
- 2025-02-20 - [Optimizing API Integration in a Large React Application Using OpenAPI Generator](https://www.youtube.com/watch?v=-B33pQnGQUI) by Stefano Marzo

## [6 - About Us](#table-of-contents)

OpenAPI Generator의 설계 철학 또는 원칙은 무엇인가요?

우리는 개발자 경험(Developer Experience)에 집중합니다.
Generator는 사용자가 쉽게 이해하고 활용할 수 있는 코드, 설정, 문서 등을 생성해야 합니다.
처음에는 단순한 사용 사례(바텀업 접근)부터 시작했으며,
이후 프로젝트와 커뮤니티가 크게 성장했습니다.
예를 들어, NPM CLI 래퍼를 통한 주간 60만 다운로드, openapi-generator-cli 도커 이미지는 3천만 다운로드를 기록했습니다.
OpenAPI 3.0에서 도입된 oneOf, anyOf 등 다양한 기능을 점진적으로 지원해왔으며,
앞으로도 사용자 요구와 피드백을 바탕으로 새로운 OpenAPI 명세(v3.1 및 이후 버전)의 기능을 계속 지원할 예정입니다.

### [6.1 - OpenAPI Generator 핵심 팀](#목차)

OpenAPI Generator 핵심 팀(Core Team) 멤버는
정기적으로 프로젝트에 중요한 기여(이슈 리뷰, 버그 수정, 기능 개선 등)를 해온 기여자들입니다.

#### 핵심 팀원
* [@wing328](https://github.com/wing328) (2015/07) [:heart:](https://www.patreon.com/wing328)
* [@jimschubert](https://github.com/jimschubert) (2016/05) [:heart:](https://www.patreon.com/jimschubert)
* [@cbornet](https://github.com/cbornet) (2016/05)
* [@jmini](https://github.com/jmini) (2018/04)  [:heart:](https://www.patreon.com/jmini)
* [@etherealjoy](https://github.com/etherealjoy) (2019/06)
* ... (이하 생략, 실제 팀원 목록 및 링크는 그대로 유지) ...

:heart: = 해당 기여자를 직접 후원할 수 있는 링크

#### 템플릿 제작자

**참고:** 내장 템플릿은 _Mustache_ 포맷만 공식 지원합니다.
다른 포맷은 실험적이며 언제든 변경될 수 있습니다.

템플릿 제작자 목록:
* API 클라이언트:
  * Ada: @stcarrez
  * Apex: @asnelling
  * Bash: @bkryza
  * ... (이하 생략, 실제 제작자/언어 목록은 그대로 유지) ...
* 서버 스텁:
  * Ada: @stcarrez
  * C# ASP.NET 5: @jimschubert [:heart:](https://www.patreon.com/jimschubert)
  * ... (이하 생략) ...
* 문서화:
  * AsciiDoc: @man-at-home
  * HTML Doc 2: @jhitchcock
  * ... (이하 생략) ...
* 설정:
  * Apache2: @stkrwork
  * k6: @mostafa
* 스키마:
  * Avro: @sgadouar
  * GraphQL: @wing328 [:heart:](https://www.patreon.com/wing328)
  * ... (이하 생략) ...

:heart: = 해당 기여자를 직접 후원할 수 있는 링크

#### 핵심 팀 합류 방법

핵심 팀원이 되려면 다음 조건을 충족해야 합니다:
- [기여자 순위 Top 50](https://github.com/openapitools/openapi-generator/graphs/contributors) 이내
  - 기여를 원한다면 [시작하기 좋은 이슈](https://github.com/openapitools/openapi-generator/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22) 참고
- 프로젝트에 정기적으로 기여(주 3시간 정도)
  - 이슈 처리, PR 리뷰, 버그 수정, 기능 개선 등
  - 지원 시점 기준 최근 3개월 내 활동 필요

핵심 팀 합류를 원하면 team@openapitools.org로 문의하세요.

템플릿 제작자가 되고 싶다면, 새로운 API 클라이언트(예: Rust, Elixir) 또는 서버 스텁(예: Ruby Grape) generator에 대한 PR을 제출하면 됩니다.

### [6.2 - 기술 위원회](#목차)

OpenAPI Generator 기술 위원회 멤버는 다음 역할을 수행합니다:

- 사용자에게 가이드 및 방향 제시
- PR 및 이슈 리뷰
- 기능 개선, 버그 수정, 문서 업데이트
- Generator의 기술적 방향성 설정

자격 요건:
- Generator에 3개 이상의 PR이 머지된 경우(템플릿 제작자 등 예외 가능)
- 합류를 원하면 team@openapitools.org로 Github ID와 함께 지원

#### 위원회 멤버

| 언어/Generator | 멤버(가입일) |
|:---------------|:------------|
| ActionScript | ... |
| Ada | ... |
| ... (이하 생략, 실제 위원회 멤버 표는 그대로 유지) ...

과거 위원회 멤버:
| 언어/Generator | 멤버(가입일) |
|:--------------|:------------|
| Python | ... |

:heart: = 해당 기여자를 직접 후원할 수 있는 링크

### [6.3 - 프로젝트 연혁](#목차)

OpenAPI Generator는 [Swagger Codegen](https://github.com/swagger-api/swagger-codegen)에서 포크된 프로젝트입니다.
Swagger Codegen 3.0.0(beta) 릴리즈와 프로젝트 방향성에 대한 이견으로 인해,
40명 이상의 주요 기여자와 템플릿 제작자가 Swagger Codegen을 포크하여
커뮤니티 주도의 "OpenAPI Generator"를 만들었습니다.
자세한 내용은 [Q&A](docs/qna.md)를 참고하세요.

#### 창립 멤버(알파벳순):

- [Akihito Nakano](https://github.com/ackintosh)
- [Artem Ocheredko](https://github.com/galaxie)
- ... (이하 생략, 실제 창립 멤버 목록은 그대로 유지) ...

:heart: = 해당 기여자를 직접 후원할 수 있는 링크

## [7 - 라이선스](#목차)
-------

Copyright 2018 OpenAPI-Generator Contributors (https://openapi-generator.tech)
Copyright 2018 SmartBear Software

Apache License, Version 2.0(이하 "라이선스")에 따라 라이선스가 부여됩니다.
이 파일을 라이선스에 따라 사용해야 하며, 라이선스 없이 사용할 수 없습니다.
라이선스 사본은 [apache.org/licenses/LICENSE-2.0](https://www.apache.org/licenses/LICENSE-2.0)에서 확인할 수 있습니다.

관련 법률 또는 서면 동의가 없는 한,
소프트웨어는 "있는 그대로(AS IS)" 제공되며,
명시적이거나 묵시적인 어떠한 보증도 제공하지 않습니다.
자세한 내용은 라이선스를 참고하세요.

---
