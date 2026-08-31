---
layout:
  width: wide
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# Windows Attack Simulation and Event Investigation

#### Project Overview <a href="#r25p" id="r25p"></a>

In this lab, I simulated a Windows endpoint compromise using Metasploit and investigated the resulting activity through Windows Event Logs.The lab involved generating a test payload, transferring it to the Windows machine, establishing a Meterpreter session, performing several post-exploitation activities, and then examining the Windows logs generated during the activity.The investigation was performed using Windows Event Viewer and Sysmon-related event data.

#### Objectives <a href="#r25t" id="r25t"></a>

Generate and deliver a test payload to a Windows endpointEstablish a Meterpreter sessionPerform basic post-exploitation activitiesGenerate security-relevant Windows eventsInvestigate the activity using Windows Event ViewerIdentify evidence of process execution, account changes, and other system activityUnderstand how endpoint activity can be detected through Windows logs

#### Technologies Used <a href="#r265" id="r265"></a>

| Category         | Tool                 |
| ---------------- | -------------------- |
| Attacker Machine | Kali Linux           |
| Framework        | Metasploit           |
| Endpoint         | Windows 10           |
| Monitoring       | Sysmon               |
| Log Analysis     | Windows Event Viewer |
| Payload          | Windows executable   |
| Network          | HTTP                 |

#### Implementation <a href="#r26p" id="r26p"></a>

**Step 1: Creating the Test Payload**

Metasploit was used on the Kali Linux machine to configure a Windows reverse HTTP payload.The listener was configured to communicate with the Windows endpoint, and an executable payload namednetflixmod.exewas generated for the lab.

<div><figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption><p>Figure 1: Configuring the Metasploit payload</p></figcaption></figure> <figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption><p><strong>Step 2: Starting the Metasploit Handler</strong></p></figcaption></figure></div>

A Metasploit handler was started to listen for the incoming connection from the Windows endpoint.The handler successfully started and waited for the Windows system to execute the payload.

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption><p>Figure 2: Metasploit handler</p></figcaption></figure>

**Step 3: Transferring the Payload**

A temporary HTTP server was started on the Kali machine to make the test executable available to the Windows endpoint.The Windows machine accessed the server and displayed the directory containing the executable.

<div><figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure></div>

<figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption><p>Figure 3: Hosting and accessing the test payload</p></figcaption></figure>

**Step 4: Executing the Payload**

The test executable was downloaded to the Windows machine and executed.After execution, the Metasploit handler received a connection and established a Meterpreter session with the Windows endpoint.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption><p>Figure 4: Meterpreter session established</p></figcaption></figure>

**Step 5: Accessing the Windows System**

After establishing the session, commands were executed to interact with the Windows system and inspect the environment.The activity included accessing the user's Downloads directory and interacting with the Windows command shell.

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption><p>Figure 5: Interaction with the Windows endpoint</p></figcaption></figure>

**Step 6: Performing Post-Exploitation Activity**

Additional commands were executed on the Windows endpoint as part of the lab.The activity included modifying local account configuration and creating a scheduled task. These actions were intentionally performed to generate security-relevant events that could later be investigated.

<div><figure><img src="../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption><p>Figure 6: Post-exploitation activity</p></figcaption></figure></div>

**Step 7: Investigating Windows Event Logs**

Windows Event Viewer was used to investigate the events generated during the activity.The relevant Windows event logs were reviewed to identify activity associated with the simulated compromise.

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption><p>Figure 7: Reviewing Windows Event Logs</p></figcaption></figure>

**Step 8: Investigating Event Details**

Individual events were opened to examine their details, including timestamps, event IDs, event sources, and other available information.This helped connect the observed system activity with the actions performed during the simulation.

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption><p>Figure 8: Windows event details</p></figcaption></figure>

**Step 9: Reviewing Sysmon Events**

Sysmon-related events were examined in Event Viewer to identify additional information about activity on the Windows endpoint.The events provided visibility into system activity generated during the lab.

<div><figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption><p>Figure 9: Sysmon event investigation</p></figcaption></figure></div>

**Step 10: Reviewing Additional Event Evidence**

Additional Windows events were reviewed to correlate the activity performed during the simulation with the logs generated on the endpoint.The investigation included examining event details and identifying information useful for understanding the sequence of activity.

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption><p>Figure 10: Correlating Windows event activityConverted to Divider</p></figcaption></figure>
