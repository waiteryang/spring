MyBatis Spring Adapter
======================

[![Build Status](https://travis-ci.org/mybatis/spring.svg?branch=master)](https://travis-ci.org/mybatis/spring)
[![Coverage Status](https://coveralls.io/repos/mybatis/spring/badge.svg?branch=master&service=github)](https://coveralls.io/github/mybatis/spring?branch=master)
[![Maven central](https://maven-badges.herokuapp.com/maven-central/org.mybatis/mybatis-spring/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.mybatis/mybatis-spring)
[![Sonatype Nexus (Snapshots)](https://img.shields.io/nexus/s/https/oss.sonatype.org/org.mybatis/mybatis-spring.svg)](https://oss.sonatype.org/content/repositories/snapshots/org/mybatis/mybatis-spring/)
[![License](http://img.shields.io/:license-apache-brightgreen.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)

![mybatis-spring](http://mybatis.github.io/images/mybatis-logo.png)

MyBatis-Spring adapter is an easy-to-use Spring bridge for MyBatis sql mapping framework.

Supported Versions
------------------

- 1.3.x - Continued support for Java 6 and 7
- master (2.0.x) - Support for Java 8, Spring 5, and Junit 5 plus other java 8 requirements

Essentials
----------

* [See the docs](http://mybatis.github.io/spring/)

# 源码阅读
使用@MapperScan指定了mapper接口之后, 触发调用AutoConfiguredMapperScannerRegistrar, 注册MapperScannerConfigurer Bean 定义之后, 委派ClassPathMapperScanner将扫描的mapper接口, 注册成MapperFactoryBean, 最后由MapperFactoryBean生成mapper对象.
