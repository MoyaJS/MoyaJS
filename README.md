# MoyaJS
Network abstraction layer written in Javascript.

[![CircleCI](https://circleci.com/gh/MoyaJS/MoyaJS/tree/master.svg?style=svg)](https://circleci.com/gh/MoyaJS/MoyaJS/tree/master)
[![codecov.io](https://codecov.io/github/MoyaJS/MoyaJS/coverage.svg?branch=master)](https://codecov.io/github/MoyaJS/MoyaJS?branch=master)

<p align="center">
  <img height="160" src="web/logo_github.png" />
</p>

You're a smart developer. You probably use [Axios](https://github.com/mzabriskie/axios) to abstract away access to
`http` and all those nasty details you don't really care about. But then,
like lots of smart developers, you write ad hoc network abstraction layers. They
are probably called "APIManager" or "NetworkModel", and they always end in tears:
[React-redux-axios-example](https://github.com/oviava/react-redux-axios-example)

Well the Swift guys over at [Moya](https://github.com/Moya/Moya) finally got it right.  So, taking Moya's basic princeple's and applying Atwood's Law: any application that can be written in JavaScript, will eventually be written in JavaScript.  We introduce MoyaJS.

![MoyaJS Overview](web/diagram.png)

Ad hoc network layers are common in web apps. They're bad for a few reasons:

- Makes it hard to write new apps ("where do I begin?")
- Makes it hard to maintain existing apps ("oh my god, this mess...")
- Makes it hard to write unit tests ("how do I do this again?")

So the basic idea of Moya is that we want some network abstraction layer that
sufficiently encapsulates actually calling Alamofire directly. It should be simple
enough that common things are easy, but comprehensive enough that complicated things
are also easy.

> If you use Axios, Fetch, or Ajax to abstract away `http`, why not use something
to abstract away the nitty gritty of URLs, parameters, etc?

Some awesome features of MoyaJS:

- Compile-time checking for correct API endpoint accesses.
- Lets you define a clear usage of different endpoints with associated enum values.
- Treats test stubs as first-class citizens so unit testing is super-easy.