![Image Placememt](img/Arista_Logo_copy.png)

# Arista Southwest Region Newsletter

Welcome to the January 2026 Newsletter for Arista customers in the U.S. Southwest Region! 

We welcome your feedback on the newsletter. If you have any ideas or suggestions on how to improve the newsletter, please reach out to [southwest@arista.com](mailto:southwest@arista.com){: target="_blank" }.  

## Leadership Perspectives — Recent Blogs from Arista Leadership
---
<div class="grid cards" markdown>

-   **Delivering Reliable AI and Cloud Networking**
    ---
    *Dec 18, 2025: Hugh Holbrook and Kamal Sharma explore the infrastructure requirements for massive-scale GenAI.*
    
    [Read Blog](https://blogs.arista.com/blog/delivering-reliable-ai-and-cloud-networking){: target="_blank" }

-   **The Cognitive Campus Blueprint**
    ---
    *Dec 10, 2025: A guide to navigating the "all-wireless office" transformation with AI-driven operations.*
    
    [Read Blog](https://blogs.arista.com/blog/cognitive-campus-blueprint){: target="_blank" }

-   **CloudVision: The First Decade**
    ---
    *Dec 3, 2025: Reflecting on ten years of innovation as CloudVision evolves into a full network operating system.*
    
    [Read Blog](https://blogs.arista.com/blog/cloudvision-the-first-decade-2025){: target="_blank" }

-   **Arista and Palo Alto Networks Partnership**
    ---
    *Nov 12, 2025: Strengthening the bond between networking and security in the new age of AI-driven threats.*
    
    [Read Blog](https://blogs.arista.com/blog/arista-and-palo-alto-networks-strengthen-partnership-in-the-new-age-of-ai-security){: target="_blank" }

</div>

[Explore All Blogs](https://blogs.arista.com/blog){: target="_blank" }


---


## 🛠️ Southwest Region Tech Tip of the Month

!!! info "The 'Pre-Game' Safety Net: CloudVision Snapshots"
    <div style="font-size: 1.15em; line-height: 1.5;" markdown>
    Before pushing a major config change to your network, use the **CloudVision Snapshot** tool to capture the exact state of your routing tables and interface counters.
    
    **Why it matters:** If things go sideways, you aren't just looking at logs—you can "diff" the network state before and after the change to see exactly which routes dropped, further simplifying complex changes.
    
    **Pro Tip:** Pair this with CloudVision Change Control Rollbacks, which allow you to revert to the previous state prior to the change, for a 100% stress-free maintenance window. 
    </div>
  

---
## 📚 Articles

### Unlocking Continuous Network Uptime: The Power of Arista SSU Hitless Upgrade
By: Alex Bojko, Advisory Systems Engineer 

The words "it's time to upgrade the network" can send shivers down even the most seasoned network engineers' spine. The term software upgrade is synonymous with network downtime in the realm of network engineering. Schedules must be adjusted, clients and customers alerted, and downtime, or planned outages, must be scheduled to complete these tedious procedures. Even a few seconds of downtime can have a real operational and financial impact on many organizations. For certain domains, like healthcare, network downtime is unacceptable.  

Arista aims to flip the script on software upgrades by delivering game-changing hitless upgrades that result in minimal to no packet loss and no impact to end users. Yes, you read that correctly, leveraging the power of Arista SSU (Smart System Upgrade), an EOS switch supporting Access Points, PC's, IP Phones, IP Cameras, and any other end device can undergo a software upgrade without any impact to client traffic.  

In this article, we will highlight how the hitless upgrade procedure works, and how you can complete the upgrade solely through CloudVision.   

SSU, or Arista's hitless upgrade, works by forwarding data plane traffic based on the last known state of the device's control plane as it appeared prior to the upgrade. All PoE (Power over Ethernet) devices connected to the switch will continue to receive power throughout the entirety of the upgrade. The below image depicts a comparison of what occurs during a normal software upgrade vs the Arista SSU hitless upgrade.   


<figure markdown="span">
  ![First Pic](img/November25Pic8.png)
  <figcaption>Traditional Upgrade</figcaption>
</figure>  


<figure markdown="span">
  ![First Pic](img/November25Pic9.png)
  <figcaption>SSU Smart System Upgrade</figcaption>
</figure>  

The only observed packet loss, if any, occurs during the sub-second timeframe where the device's control plane comes back online, and re-syncs with the data plane.  

SSU is the perfect solution for single-homed endpoints, which encompass the vast majority of campus end devices. These devices rely on a single connection to a switch for uptime, and with the introduction of SSU hitless upgrades, are now able to achieve continuous network uptime even during software upgrades. An access point, which can service hundreds of clients, can maintain power and internet connectivity while the access switch it's connected to undergoes a software upgrade. This is applicable to all access devices that service our network users.   

As mentioned above, hitless upgrades can be executed entirely through CloudVision using the Software Management Studio. Simply assign a new version of EOS to your Arista switch and submit the workspace. You can directly download the desired EOS image without ever leaving CloudVision. Downloading the image will make it accessible in CloudVision for the current and all future devices to use.  

After selecting the desired image and submitting the Workspace, within the Change Control tab, select the device, followed by the arguments tab, and under the "Reload-Mode" dropdown, select "SSU Only". This will instruct CloudVision to proceed with a hitless upgrade, as opposed to a standard software upgrade. The last step is the Approve and Execute the Change Control, and the device will begin the SSU process. You can view the logs associated with the change directly through the Change Control screen as well.   

<figure markdown="span">
  ![First Pic](img/November25Pic13.png)
  <figcaption>SSU Smart System Upgrade</figcaption>
</figure>   


The Arista SSU Hitless upgrade is a game-changer for network engineers who once feared the task of completing  software upgrades. For more information on hitless upgrades, please click on the links below.   

[Tech Library: Hitless Upgrade](https://tech-library.arista.com/solution_guides/ssu/){: target="_blank" }  


---

### A More Simple View of Network Metrics
By: Akashdeep Takhar, Advanced Services Engineer, Southwest Region   

A more efficient approach to monitoring network traffic metrics not only helps in identifying issues in production, it can also lead to a significantly faster time to troubleshooting. Although the CLI is great at quickly gathering information, utilizing graphs and charts to visually represent that data allows for an illustrative way to measure network information. That’s where the Dashboards tool in CloudVision is ready to help.  

Dashboards give the ability for network data to be visually represented in graphs, charts, interactive menus, and customizable layouts. Rather than navigating across multiple devices, you can gather both summaries and in depth views of the entire network. CloudVision provides pre-built Dashboards for you to view. However, in addition to that, you have the ability to become creative and customize these Dashboards to your liking. Let’s take a look at some examples of Dashboards.  

<figure markdown="span">
  ![Pic2](img/November25Pic10.png)
  <figcaption>Network Health Dashboard</figcaption>
</figure>  

In the example above, we have a dashboard that lists events that impact the health of the networks. The left hand horizontal bar chart works like this: the x-axis identifies a number of devices, the y-axis lists type of events that are harmful to given device, the colors of the bar categorize the event types as critical, error, or warning. By viewing this, we are informed that many devices in the network are exposed to potential harm. To further elaborate on those warning, take a look at the table located to the right.  

The table on the right lists the events and the message associated with that event. By looking at these two side by side, we now know of potential issues that are impactful to the device. Had that not been there, we would not be able to identify issues early on before scaling out the production for future use. At the bottom of the dashboard, we see a timeline of critical issues for the untagged devices, further providing us with information necessary to fix.  

<figure markdown="span">
  ![Pic2](img/November25Pic11.png)
  <figcaption>Device Power Consumption Dashboard</figcaption>
</figure>   

Another Dashboard that is pre-built into your CloudVision instance is the Device Power Consumption board. A method of analyzing devices for troubleshooting problems, could be to view this dashboard for an overall view of input and output wattage use. If you suspect that there are power issues that are causing network disruptions, simply navigate to this page to see all the devices and their power consumption.  

In addition to the graph, the bar at the top labeled “devices device*” allows for you to view the metrics, specified for a particular device. In the case where you would prefer to view the power use of multiple devices, you can select those devices within the top drop down bar as well. The graphs readjust to the chosen device. Take a look below as we select a device:  

<figure markdown="span">
  ![Pic2](img/November25Pic12.png)
  <figcaption>Device Power Consumption Dashboard</figcaption>
</figure>  

These are examples of pre-built dashboards. CloudVision allows for you to also create many customizable dashboards to specific metric views that are of interest to you. If you would like any assistance on how to begin this step, contact your ASE or SE to set up a meeting.  

For more information on dashboards in CloudVision, click the link below:  
[CloudVision Dashboard Guide](https://www.arista.io/help/articles/ZGFzaGJvYXJkcy5BbGwuZGFzaGJvYXJkcw==){: target="_blank" }   


---

## __*Upcoming Events*__  
Arista hosts various events throughout the year for you! Members of our team organize these informative events to showcase Arista's ability to not only help improve your network, but to also assist by providing a set of tools to improve your operations!  

Click on the boxes below to be directed to Arista's website for additional lists of Webinars and Events.


<div class="grid cards" markdown>

-   __Webinars__  

    --- 

    We make it easy for you to view products that are of interest, all virtually! Technical members of the team showcase outstanding explanations of the products. Click below to see our list of Webinars. 

    [Arista Webinars](https://www.arista.com/en/company/news/webinars){.md-button target="_blank"}

-   __Events__ 

    ---
    Join us in person to get a closer look at our list of products and solutions, as well as get the chance to meet members of the team. Click below to see our list of upcoming Events. 

    [Upcoming Events](https://www.arista.com/en/company/news/events){ .md-button target="_blank" }


</div>

--- 

## __*Software Updates*__
![Image Placememt](img/software_upgrades_condensed.png)

For new code releases, click [here](https://www.arista.com/en/support/software-download){: target="_blank" } 


|  Software    | Version      |  Release Date |
| :-----------: | :-----------: | :-----------:
| __EOS__           | 4.34.3.1M <br>4.32.8M <br> 4.34.3M <br> 4.35.0F <br>  | November 4th, 2025 <br>October 27th, 2025 <br> October 6th, 2025 <br> October 6th, 2025 <br> 
| __CVP__           | Portal 2025.2.1 <br> Appliance 7.0.1 <br> Sensor 1.2.0 <br>    | August 21st, 2025 <br> January 28th, 2025<br> September 8th, 2025 <br>
| __DMF__           | 8.8.0 <br >| August 15th, 2025 <br> 
| __WLAN__ <br>CV-CUE<br> | <br> 19.0.0 <br>      | <br> July 25th, 2025<br>  
| __Arista NDR__         | 5.3.5         | July 16th, 2025
| __TerminAttr__    | 1.39.1 <br>       | July 18th, 2025 <br>  
| __VeloCloud SD-WAN__  <br>Orchestrator/ Gateway / Edge<br>  | <br>6.4.0 <br>       | <br> May 2nd, 2025 <br> 




---

## __*Security Advisories and Field Notices*__

![Image Placememt](img/Security_image.png)

Below is a list of advisories that are announced by Arista. To view more details on the specific advisories, please click the links in the middle row.

| Name          | Advisory Link           | Date of Advisory Notice  |
| :-----------: |:-------------:| :-----:|
|  __Arista DANZ Monitoring Fabric__   | [Security Advisory 0124](https://www.arista.com/en/support/advisories-notices/security-advisory/22538-security-advisory-0124){: target="_blank" }  | October 22nd, 2025   |  
|  __Arista Edge Threat Management NGFW__   | [Security Advisory 0123](https://www.arista.com/en/support/advisories-notices/security-advisory/22535-security-advisory-0123){: target="_blank" }  | October 21st, 2025   |  
|  __WiFi 7 Access Points Firmware Version 21.0__   | [Field Notice 0117](https://www.arista.com/en/support/advisories-notices/field-notice/22534-field-notice-0117){: target="_blank" }  | October 16th, 2025   |  
|  __SwitchApp Interfaces starting with EOS 4.35.0F__   | [Field Notice 0116](https://www.arista.com/en/support/advisories-notices/field-notice/22528-field-notice-0116){: target="_blank" }  | October 14th, 2025   |  

 


For a list of the most current advisories and notices, click [Here](https://www.arista.com/en/support/advisories-notices){: target="_blank" }

---

## __*Product Updates - New Releases and End of Sale Notices *__

![Image Placememt](img/Product_image.png)



**New Releases** of Arista's devices are listed below 

|  Device       | More Information |  Release Date 
    | :-----------: | :-----------:    | :-----------:
    | Arista VeloCloud | [VeloCloud Acquisition](https://www.arista.com/en/company/news/press-release/21646-pr-07012025){: target="_blank" } | Q3 2025
    |  Arista SWAG    |   [Modern Stacking for Campus](https://www.arista.com/en/company/news/press-release/20693-pr-12032024){: target="_blank" }                | Q1 2025 
    | Arista Multi-Domain Segmentation Service  | [Arista MSS](https://www.arista.com/en/company/news/press-release/19297-pr-20240430){: target="_blank" }         | Q3 2024
    | Arista CV UNO  | [CloudVision Universal Network Observability](https://www.arista.com/en/company/news/press-release/19195-pr-20240305){: target="_blank" }  | Q1 2024



**End of Sale** notices are listed below.

| Device        | Name           | End Of Sale Date  |
| :-----------: |:-------------: |     :----:        |
| Software      | [End of Software for CloudVision Portal 2023.2](https://www.arista.com/en/support/advisories-notices/end-of-support/21412-end-of-software-support-for-cloudvision-portal-2023-2-release-train){: target="_blank" }<br>[End of Software Support for EOS 4.28](https://www.arista.com/en/support/advisories-notices/end-of-support/21275-end-of-software-support-for-eos-4-28){: target="_blank" }<br>[DMF and CCF Deployments on Accton/ Edgecore Switches](https://www.arista.com/en/support/advisories-notices/end-of-support/21094-end-of-support-for-dmf-and-ccf-deployments-on-accton-edgecore-switches){: target="_blank" }<br>[EOS-4.34 and later no longer supported on select switches](https://www.arista.com/en/support/advisories-notices/end-of-support/21089-end-of-software-support-for-7280r-r2-7500r-r2-and-7020r-series){: target="_blank" }<br> | May 27th, 2025 <br> March 14, 2025 <br>January 31st, 2025 <br>January 15th, 2025 <br> |
| CVP           | [CVP IPAM Application](https://www.arista.com/en/support/advisories-notices/endofsupport){: target="_blank" } <br> [CVP 2023.3](https://www.arista.com/en/support/advisories-notices/end-of-support/21627-end-of-software-support-for-cloudvision-portal-2023-3-release-train){: target="_blank" }          |  July 14th, 2025 <br> June 17th, 2025   |
| DMF           | [DMF Service Node DCA-DM-SC2](https://www.arista.com/en/support/advisories-notices/end-of-sale/22537-end-of-sale-end-of-life-for-arista-service-node-appliance-dca-dm-sc2){: target="_blank" }          |  October 22nd, 2025           |  
| CCF           | [CCF Product Line](https://www.arista.com/en/support/advisories-notices/end-of-sale/22430-end-of-sale-end-of-life-for-arista-ccf-product-line){: target="_blank" }          |  October 1st, 2025           |  
| Switches      | [7010TX-48-DC Switch](https://www.arista.com/en/support/advisories-notices/end-of-sale/22421-end-of-sale-of-the-arista-7010tx-48-dc-switches){: target="_blank" }<br> [7050CX3-32S Switch](https://www.arista.com/en/support/advisories-notices/end-of-sale/22419-end-of-sale-of-the-arista-7050cx3-32s-switches){: target="_blank" }<br> [CCS-720XP-96ZC2 Switch with 4GB DRAM](https://www.arista.com/en/support/advisories-notices/end-of-sale/22403-end-of-sale-of-the-arista-ccs-720xp-96zc2-switches-with-4gb-dram){: target="_blank" }<br> [CCS-720D Switches with 4GB DRAM](https://www.arista.com/en/support/advisories-notices/end-of-sale/22402-end-of-sale-of-the-arista-ccs-720d-switches-with-4gb-dram){: target="_blank" }<br> [CCS-710P-12 Switch](https://www.arista.com/en/support/advisories-notices/end-of-sale/22401-end-of-sale-of-the-arista-ccs-710p-12-switch){: target="_blank" } |  September 19th, 2025<br> September 19th, 2025<br> September 12th, 2025<br> September 12th, 2025<br> September 12th, 2025 |
| Access Points      | [AP Mounts](https://www.arista.com/en/support/advisories-notices/end-of-sale/22536-end-of-sale-of-ap-mounts-mnt-ap-flat-c130-mnt-ap-flat-c100-mnt-ap-flat-14cm-a){: target="_blank" }<br> |  October 22nd, 2025 <br> | 
| VeloCloud      | [SASE Secured by Symantec](https://www.arista.com/en/support/advisories-notices/end-of-sale/22072-end-of-sale-life-velocloud-sase-secured-symantec){: target="_blank" }<br> [Software Defined (SD) Access](https://www.arista.com/en/support/advisories-notices/end-of-sale/21653-end-of-sale-end-of-life-for-velocloud-software-defined-sd-access){: target="_blank" } <br> |  August 20th, 2024 <br> July 1st, 2025 | 



---
## *Your Southwest Regional Team is Here to Support Your Success.* 

![Image Placememt](img/Arista_Banner.png)


---
<div style="background-color: #f8f9fa; border-left: 5px solid #004a99; padding: 20px; margin-top: 30px;">
  <h3 style="color: #004a99; margin-top: 0;">Let's Connect</h3>
  <p>Thanks for reading! Your local Arista team is here to help you navigate your evolving network needs. Reach out anytime to southwest@arista.com for more information or technical guidance. Until next month—stay connected!</p>
  <a href="mailto:southwest@arista.com" class="md-button md-button--primary">Contact Your Local Team</a>
</div>