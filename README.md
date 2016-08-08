[![Codacy Badge](https://api.codacy.com/project/badge/Grade/5c2f9919b4de41349383b57b8e008dfd)](https://www.codacy.com/app/Codacy/codacy-csslint?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=codacy/codacy-csslint&amp;utm_campaign=Badge_Grade)
[![Build Status](https://circleci.com/gh/codacy/codacy-csslint.svg?style=shield&circle-token=:circle-token)](https://circleci.com/gh/codacy/codacy-csslint)

# Codacy CSSLint

This is the docker engine we use at Codacy to have [CSSLint](http://csslint.net/) support.
You can also create a docker to integrate the tool and language of your choice!
Check the **Docs** section for more information.

## Usage

You can create the docker by doing:

```
sbt docker:publishLocal
```

The docker is ran with the following command:

```
docker run -it -v $srcDir:/src  <DOCKER_NAME>:<DOCKER_VERSION>
```

## Docs

[Tool Developer Guide](https://support.codacy.com/hc/en-us/articles/207994725-Tool-Developer-Guide)

[Tool Developer Guide - Using Scala](https://support.codacy.com/hc/en-us/articles/207280379-Tool-Developer-Guide-Using-Scala)

## Test

We use the [codacy-plugins-test](https://github.com/codacy/codacy-plugins-test) to test our external tools integration.
You can follow the instructions there to make sure your tool is working as expected.
