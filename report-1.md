# Report

**Date:** August 04, 2026

## Project Overview

In this lab, I set up a basic Security Information and Event Management (SIEM) environment using **Splunk Enterprise** and the **Splunk Universal Forwarder**.

The goal was to collect Windows logs from a client machine and forward them to a centralized Splunk server for indexing and analysis. This project demonstrates the fundamental process of log collection used in Security Operations Centers (SOCs).

## Objectives

* Install Splunk Enterprise
* Install Splunk Universal Forwarder
* Configure Splunk to receive forwarded data
* Connect the Windows endpoint to the Splunk server
* Import and index Windows logs
* Verify successful log collection

## Technologies Used

| **Category**     | **Tool**                   |
| ---------------- | -------------------------- |
| SIEM             | Splunk Enterprise          |
| Log Collection   | Splunk Universal Forwarder |
| Operating System | Windows 10                 |
| Protocol         | TCP                        |

## Implementation

{% stepper %}
{% step %}
## Installing Splunk Enterprise

Splunk Enterprise was installed on the Windows system. After the installation completed, the Splunk web interface was launched successfully.

Figure 1: Installation of Splunk enterprise

Figure 2: splunk Installed
{% endstep %}

{% step %}
## Installing the Universal Forwarder

The Splunk Universal Forwarder was installed on the client machine. During installation, the management server details were provided to enable communication with the Splunk instance.

Figure 3: Installation of Universal forwarder
{% endstep %}

{% step %}
## Configuring Data Receiving

The receiving port was configured on Splunk Enterprise to allow incoming connections from forwarders.

Figure 4: Configuring the receiving port
{% endstep %}

{% step %}
## Verifying Forwarder Connection

After configuration, the Universal Forwarder successfully appeared in the Splunk Forwarder Management page, confirming communication between the endpoint and the server.

Figure 5: Agent connected with splunk
{% endstep %}

{% step %}
## Importing Data

Using the Add Data wizard, the connected forwarder was selected as the source for collecting Windows log data.

Figure 6: Importing logs using forwarder

Figure 7: select Forwarder
{% endstep %}

{% step %}
## Configuring Data Input

The input type, source type, and destination index were configured before starting log collection.

Figure 8: Selecting the type of Data to import

Figure 9: Defining Source type and index
{% endstep %}

{% step %}
## Reviewing the Configuration

All settings were reviewed before submitting the configuration to begin indexing logs.

Figure 10: Review and Submit
{% endstep %}
{% endstepper %}

## Results

The Splunk Universal Forwarder successfully established communication with the Splunk Enterprise server. Windows log data was forwarded, indexed, and made available for searching through the Splunk interface.

## Skills Demonstrated

* SIEM deployment
* Splunk Enterprise installation
* Universal Forwarder configuration
* Windows log collection
* Log forwarding
* Data onboarding
* Log indexing
* Basic SOC operations

## Challenges

* Configuring the correct receiving port
* Ensuring successful communication between the forwarder and the Splunk server
* Verifying that logs were correctly indexed after onboarding

## Key Learnings

* Understood how Splunk Enterprise collects and indexes logs.
* Learned to install and configure the Splunk Universal Forwarder.
* Configured Splunk to receive logs over TCP.
* Learned the end-to-end workflow of Windows log collection.
* Gained hands-on experience with a basic SIEM environment.
