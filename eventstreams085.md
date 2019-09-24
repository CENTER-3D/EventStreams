---

copyright:
  years: 2015, 2019
lastupdated: "2019-08-30"

keywords: IBM Event Streams, Kafka as a service, managed Apache Kafka

subcollection: eventstreams

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# Choosing your plan 
{: #plan_choose}

{{site.data.keyword.messagehub}} is available as different plans depending on your requirements: Lite, Standard, Enterprise, and Classic. 

<!--
For information about the Classic plan, see
[Classic plan](/docs/services/EventStreams?topic=eventstreams-plan_choose_classic#plan_choose_classic).
-->
{: shortdesc}
## Lite plan
{: #plan_lite}

The Lite plan is free for users who want to try out {{site.data.keyword.messagehub}} or build a proof-of-concept. We do not recommend the Lite plan for production use. The Lite plan offers shared access to a multi-tenant {{site.data.keyword.messagehub}} cluster.

## Standard plan
{: #plan_standard}

The Standard plan is appropriate if you require event ingest and distribution capabilities but do not require any additional benefits of the Enterprise plan. The Standard plan offers shared access to a multi-tenant {{site.data.keyword.messagehub}} cluster.

## Enterprise plan 
{: #plan_enterprise}

The Enterprise plan is appropriate if data isolation, guaranteed performance, and increased retention are important considerations. The Enterprise plan offers exclusive access to a dedicated {{site.data.keyword.messagehub}} cluster. You can also provision an {{site.data.keyword.messagehub}} cluster in a geographically local but [single zone location (SZR)](/docs/services/EventStreams?topic=eventstreams-sla#sla_szr).

## Classic plan
{: #plan_classic}

The Classic plan gives access to the previous edition of the Standard plan and is provided for existing workloads and backward compatibility only. You should provision new workloads against the Standard plan.


## What's supported by the Lite, Standard, Enterprise, and Classic plans

The following table summarizes what is supported by the plans:

<table>
    <caption>Table 1. Support in Lite, Standard, Enterprise, and Classic plans</caption>
      <tr>
	        <th></th>
		    <th>Lite Plan</th>
		    <th>Standard Plan</th>
		    <th>Enterprise Plan</th>
		    <th>Classic Plan</th>
        </tr>
		<tr>
			<td>**Tenancy**</td>
			<td>Multi-tenant </td>
			<td>Multi-tenant </td>
			<td>Single tenant</td>
			<td>Multi-tenant</td>
		</tr>
        <tr>
			<td>**Availability zones**</td>
			<td>3</td>
			<td>3</td>
			<td>3<br/>(1 in single zone locations)
			</td>
			<td>Not supported</td>
		</tr>
        <tr>
			<td>**Availability**</td>
			<td>99.95% [<sup>1</sup>](/docs/services/EventStreams?topic=eventstreams-plan_choose#footnote_lite)</td>
			<td>99.95%</td>
			<td>99.95%<br/>(99.5% in single zone locations)  [<sup>2</sup>](/docs/services/EventStreams?topic=eventstreams-plan_choose#footnote_plans)</td>
			<td>99.5%</td>
		</tr>
	  		<tr>
			<td>**Kafka version on cluster**</td>
			<td>Kafka 2.2</td>
			<td>Kafka 2.2</td>
			<td>Kafka 2.2</td>
			<td>Kafka 1.1</td>
		</tr>
		<tr>
			<td>**Fine-grained access control**</td>
			<td>Yes</td>
			<td>Yes</td>
			<td>Yes</td>
			<td>No</td>
		</tr>
				<tr>
			<td>**Cloud Service Endpoint support**</td>
			<td>No</td>
			<td>No</td>
			<td>Yes</td>
			<td>No</td>
		</tr>
		<tr>
			<td>**Kafka Connect and Kafka Streams supported **</td>
			<td>No</td>
			<td>Yes</td>
			<td>Yes</td>
			<td>Yes</td>
		</tr>
		<tr>
			<td>**Maximum number of partitions per topic**</td>
			<td>1</td>
			<td>100</td>
			<td>3000</td>
			<td>100</td>
		</tr>
		<tr>
			<td>**Maximum retention period**</td>
			<td>100 MB for the partition for up to 30 days </td>
			<td>1 GB per partition for up to 30 days </td>
			<td>2 TB of usable storage<!--Unlimited up to the storage limit of your plan --></td>
			<td>1 GB per partition for up to 30 days </td>
		</tr>
		<tr>
			<td>**Maximum throughput**</td>
			<td>100 KB per second per partition</td>
			<td>1 MB per second per partition (20 MB per service instance) </td>
			<td>40 MB per second per cluster (peak throughput of 75 MB per second)</td>
			<td>1 MB per second per partition</td>
		</tr>
		<tr>
			<td>**Maximum message size**</td>
			<td>1 MB</td>
			<td>1 MB</td>
			<td>1 MB</td>
			<td>1 MB</td>
		</tr>
		<tr>
			<td>**Maximum number of connected clients**</td>
			<td>5</td>
			<td>100</td>
			<td>10 000</td>
			<td>100</td>
		</tr>
		<tr>
			<td>**Location (region) availability**</td>
			<td>Dallas (us-south)</br>
			<br/>
			</td>
			<td>**Multizone location (MZR)**<br/>
			Dallas (us-south)</br>
			Washington (us-east)<br/>
			London (eu-gb)<br/>
			Sydney (au-syd)</br>
			Frankfurt (eu-de)<br/>
			Tokyo (jp-tok)<br/>
			<br/>
			</td>
			<td>**Multizone location (MZR)**</br>
			Dallas (us-south)</br>
			Washington (us-east)<br/>
			London (eu-gb)<br/>
			Sydney (au-syd)</br>
			Frankfurt (eu-de)<br/>
			Tokyo (jp-tok)<br/>
			<br/>
			**Single zone location (SZR)**</br>
			Seoul (seo01)<br/>
			<br/>
			</td>
			<td>Dallas (us-south)</br>
			London (eu-gb)</br>
			Sydney (au-syd)</br>
			Frankfurt (eu-de) - no {{site.data.keyword.mql}} API </td>
		</tr>
		<tr>
     	    <td>**APIs supported**</td>
			<td>Kafka API</br>
			Admin REST API<br/>
			REST Producer API</br>
		    </td>
			<td>Kafka API<br/>
			Admin REST API</br>
			REST Producer API</br>
			</td>
			<td>Kafka API</br>
			Admin REST API<br/>
			REST Producer API</br>
		    </td>
			<td>Kafka API</br>
			Admin REST API<br/>
			Kafka REST API</br>
			MQ Light API</br>
		    </td>
		</tr>
		</tr>
			<td>**Cloud Object Storage bridge and<br/>
			MQ bridge supported**</td>
			<td>No</td>
			<td>No</td>
			<td>No</td>
			<td>Yes</td>
		</tr>
		<tr>
			<td>**Deployment timeframe**</td>
			<td>Instantaneous provisioning</td>
			<td>Instantaneous provisioning</td>
			<td>Expect provisioning to take up to 3 hours. Because Enterprise has its own dedicated resources for each cluster, it requires more time for provisioning</td>
			<td>Instantaneous provisioning</td>
		</tr>

</table>
### Footnotes
{: #footnote_plans notoc}

1. {: #footnote_lite notoc} Note that after 30 days of inactivity, your instance is deleted.
2. {: #footnote_szr notoc} For more information about availability, see [single zone location deployments](/docs/services/EventStreams?topic=eventstreams-sla#sla_szr).



<!--
## {{site.data.keyword.Bluemix_notm}} Public environment
{: notoc}

{{site.data.keyword.Bluemix_notm}} Public provides an
economical public cloud service where you pay for what you use and share infrastructure with
others.

In {{site.data.keyword.Bluemix_notm}} Public, the cost of
{{site.data.keyword.messagehub}} is determined by two factors: the
number of partitions that you use and the number of messages that you send and receive. There is no
charge for message data while it is retained on the topics, but the data that each partition retains
is capped at 1 GB.

For more information, see [{{site.data.keyword.Bluemix_notm}} Public ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud/free/){:new_window}.
-->

