---

copyright:
  years: 2015, 2018
lastupdated: "2018-05-25"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

<!-- 14/11/18: info moved to eventstreams099.md, moved because of doc app changes -->
# Using the MQ Light Ruby client
{: #mql_how}

** The MQ Light API is available as part of the Standard plan only.**
<br/>

To use the API, add a reference to the latest available {{site.data.keyword.mql}} client API for Ruby as follows:
{: shortdesc}

Add the following reference to the <code>Gemfile</code>:

```
gem 'mqlight', '~> 1.0'
```
{: codeblock}

And add the following require statement to your source file:

```
require ‘mqlight’
```
{: codeblock}

<!-- Comment from Andrew
Instructions for getting started, with links for more info
Simple send source and receive source in-line

-->


