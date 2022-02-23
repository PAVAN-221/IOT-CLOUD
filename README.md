# The IoT cloud: Microsoft Azure vs. AWS vs. Google Cloud
<img width="700" alt="Capture" src=https://user-images.githubusercontent.com/52132063/155265416-50be6047-15f9-4493-b7a6-ef8ccfb4b572.png>

## In short
- **The three large hyperscalers collectively hold ~80% of the global IoT public cloud market.**
- **IoT is of high strategic importance to both Microsoft and AWS, while Google does not prioritize it as much.**

## Why it matters
- **Hyperscalers offer a large number of services in the public cloud that form the backbone of many IoT initiatives.**

The three leading global hyperscalers (**AWS, Microsoft**, and **Google Cloud**) hold more than 80% market share for global public cloud services specifically for IoT workloads according to the latest research from IoT Analytics: <ins>[ Cloud Computing for IoT Market Report 2021–2026](https://iot-analytics.com/product/cloud-computing-for-iot-market-report-2021-2026/)</ins>, a 135-page report on the current state and trends of the IoT cloud computing market.

Although offering public cloud services for connecting IoT devices is not (yet) a major driver for the businesses of these companies, IoT services and related cloud infrastructure investments are expected to grow faster than general public cloud spending and will thus increase in strategic importance during the coming years as public cloud becomes a <ins>[multi-trillion-dollar market.](https://iot-analytics.com/cloud-market/)<ins>

AWS had the first-mover advantage, introducing public cloud services in 2006 and adding IoT-specific services in 2015. Microsoft Azure, which launched its public cloud four years after AWS, introduced its IoT services only five months after AWS and has since managed to overtake AWS as the market leader for IoT-specific services thanks to its IoT-centric strategy, a $5 billion <ins>[investment](https://ciostory.com/business-platforms/microsoft-will-invest-5-billion-in-iot-over-the-next-4-years-globally/)</ins> in IoT in 2018, and its strong business footprint in the enterprise segment, which accounts for some of the biggest IoT deployments. GCP has managed to keep its position as a strong challenger to Azure and AWS due to its stronghold in data and analytics. However, Google’s focus on IoT to this date has not matched that of its major competitors.


## Typical IoT cloud services
Managing <ins>[billions](https://iot-analytics.com/number-connected-iot-devices/)</ins> of IoT devices requires a set of dedicated cloud services. IoT Analytics classifies IoT cloud offerings into three main categories (the same way we classify <ins>[IoT platform services](https://iot-analytics.com/5-things-to-know-about-iot-platforms-market/)</ins>, with the exception that IoT platform services can also reside in a private cloud or on other on-premises installations):<br/>
  
1. **IoT application management/enablement**<br/>
These include cloud services designed to enable the developer to make and manage IoT applications. IoT-specific application development and management services include rule engines, IoT development environments, and digital twins.
 
2. **IoT device management**<br/>
These include cloud services designed to ensure connected “things” are working properly by seamlessly running patches and updates for software and applications running on the device or edge gateways. Examples include device monitoring, firmware updates, or deployment configuration management.
  
3. **IoT data management/enablement**<br/>
These cloud services are designed for seamless asset/edge connectivity (e.g., drivers to connect devices) and for providing the capabilities to store and analyze IoT data.

## Comparing the three main IoT clouds

<img width="700" alt="Capture" src=https://user-images.githubusercontent.com/52132063/155267944-1c74a8bf-15d4-49c4-9e8e-180d28cddd41.png>
  
## 1.  **Microsoft Azure IoT**<br/>
  
Of the three major hyperscalers, Microsoft has the strongest enterprise customer base due to the wide adoption of Microsoft Windows, Microsoft 365 (formerly Office 365), and Microsoft Dynamics. For many customers, it has been easy to add new Microsoft Azure cloud services on top of already existing tools. Key differentiators for Microsoft Azure, in general, are its integration with business intelligence tools (particularly <ins>[Power BI](https://powerbi.microsoft.com/en-us/what-is-power-bi/)</ins>), its industry-specific solutions (e.g., Microsoft <ins>[Cloud for Retail](https://www.microsoft.com/en-us/industry/retail/microsoft-cloud-for-retail)</ins> or Microsoft <ins>[Cloud for Manufacturing](https://www.microsoft.com/en-us/industry/manufacturing/microsoft-cloud-for-manufacturing)</ins>), and the company’s strong focus on enterprise support.

Microsoft lists nine specific IoT cloud services on its websites. <ins>[IoT Hub](https://azure.microsoft.com/en-in/services/iot-hub/)</ins> is the most widely used Azure IoT service, based on an analysis of the 167 publicly available IoT case studies by Microsoft Azure, followed by <ins>[Azure IoT Edge](https://azure.microsoft.com/en-us/services/iot-edge/)</ins>. Azure IoT Hub is Microsoft’s core service for data ingestion into the cloud from IoT devices. The service provides secure communication to IoT devices and device management capabilities, such as device provisioning.

For Microsoft, IoT is a key priority. The company emphasizes that it aims to simplify the way IoT is used by enterprises and industries to achieve better interoperability and cohesion with other services in the IoT value chain. Microsoft has a specific focus on <ins>[Industrial IoT](https://azure.microsoft.com/en-us/solutions/industry/manufacturing/iot/#overview)</ins> and edge computing (e.g., through <ins>[Azure Sphere certified chips and operating systems or through its Azure Percept edge AI platform)](https://azure.microsoft.com/en-us/services/azure-sphere/)</ins>.

> *“From smart factories to smart buildings to smart cities, we are helping organizations use the combination of Azure IoT, Digital Twins, and Mesh to help digitize people, places, and things, in order to visualize, simulate, and analyze any business process. Ecolab, for example, is using these tools to build its own platform to model and optimize water management. …And so today, between Azure IoT, Digital Twins, and Mesh, we have many examples where customers are engaged with us. So that’s what will show up in Azure, and we’re investing significantly there.”*
**Satya Nadella, CEO of Microsoft, 25 January 2022**
 
## Azure IoT in action:

To understand how all the different Microsoft IoT components come together, consider the following reference architecture for condition monitoring for industrial IoT.
  
<img width="700" alt="Capture" src=https://user-images.githubusercontent.com/52132063/155269008-0ec02729-ef25-49ef-9bb8-93e6dd908b2d.png>

Source: https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/condition-monitoring
The picture demonstrates how manufacturers can connect their assets to the Microsoft Cloud using the Open Platform Communications Unified Architecture (OPC UA) protocol. Data are sent to edge devices that are running Azure IoT Edge. Industrial devices that cannot communicate through OPC UA need a third-party PLC adapter to connect to IoT Edge. Data are then sent on to IoT Hub, which ingests the data into the cloud and passes them on to industrial services hosted on Kubernetes container management. The industrial services are made up of several microservices exposing a REST API. All industrial services are deployed to an Azure Kubernetes Service cluster. Azure Event Hub is used to transform and distribute the data to other services, such as Azure IoT Time Series Insights, Data Storage, and Stream Analytics. With this architecture, customers can monitor their equipment’s key parameters to discover anomalies before they become critical issues.
  
**Kennametal**, a US-based supplier of industrial materials, is a known Microsoft IoT customer reference in this area. The company’s Orwell factory leverages <ins>[IoT and Microsoft cloud solutions](https://customers.microsoft.com/en-in/story/774902-kennametal-manufacturing-azure-iot-power-bi)</ins> to monitor and optimize the performance of its manufacturing operations.
  
## Azure’s IoT-specific services:

Microsoft lists eight specific IoT cloud services on its IoT products <ins>[page](https://azure.microsoft.com/en-us/overview/iot/#products)</ins>. (*Note: Some IoT services are missing on this page.*)
  
- **Application management/enablement:**<ins>[Azure IoT Central](https://azure.microsoft.com/en-us/services/iot-central/)</ins>, <ins>[Azure Digital Twins](https://azure.microsoft.com/en-us/services/digital-twins/)</ins><br/>
- **Device management:**<ins> [Azure IoT Hub](https://azure.microsoft.com/en-us/services/iot-hub/)</ins><br/>
- **Data management/enablement:** <ins>[Azure IoT Edge](https://azure.microsoft.com/en-us/services/iot-edge/)</ins><br/>
- **Other IoT offerings:** <ins>[Azure Percept](https://azure.microsoft.com/en-us/services/azure-percept/)</ins>, <ins>[Azure Sphere](https://azure.microsoft.com/en-us/services/azure-sphere/)</ins>, <ins>[Windows for IoT](https://azure.microsoft.com/en-us/services/windows-iot/)</ins>, <ins>[Azure RTOS](https://azure.microsoft.com/en-us/services/rtos/)</ins><br/>
  
## 2.  **AWS IoT**<br/>

AWS is the global public cloud <ins>[market leader](https://iot-analytics.com/cloud-market/)</ins> and was first to market with IoT-specific public cloud solutions. Its biggest strength is its sheer mass of specific public cloud services (the company lists a total of 227 different cloud services on its website as of February 2022) and the related customer footprint and developer ecosystem. Customers are often delighted with the ease of learning and setup, the usability of the offerings, and the helpful tutorials offered by the company. AWS is also seen as a leader in serverless computing with offerings such as <ins>[Lambda](https://aws.amazon.com/lambda/features/)</ins> and <ins>[Athena](https://aws.amazon.com/athena/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc)</ins>.

Our findings show that <ins>[IoT Core](https://docs.aws.amazon.com/iot/latest/developerguide/what-is-aws-iot.html)</ins> is the most popular AWS IoT service (based on public IoT case studies).

IoT Core for AWS is somewhat equivalent to IoT Hub for Microsoft. IoT Core is a data ingestion service that provides secure, bi-directional communication for IoT devices, using protocols such as MQTT or HTTPS. While Microsoft includes its device management capabilities as standard in its IoT Hub, an AWS customer has the flexibility to use IoT Core without some of the device management capabilities or add the AWS IoT Device Management service on top if needed. This is where the IoT strategies of AWS and Microsoft differ: AWS provides more services in total, but some of them have specialized features.
  
Therefore, it is not surprising that AWS has the largest portfolio of IoT-focused cloud services, with 13 offerings. And the company continues to add new services. At the December 2021 re: Invent conference, two new IoT services were launched: <ins>[AWS IoT TwinMaker](https://docs.aws.amazon.com/iot-twinmaker/latest/guide/what-is-twinmaker.html)</ins> and AWS IoT <ins>[FleetWise](https://docs.aws.amazon.com/iot-fleetwise/latest/developerguide/what-is-iotfleetwise.html)</ins>. The company also announced three other services with IoT relevance: AWS IoT <ins>[RoboRunner](https://aws.amazon.com/roborunner/)</ins>, a specific service for robotics, AWS IoT <ins>[ExpressLink](https://aws.amazon.com/iot-expresslink/)</ins>, a connectivity software that powers a range of hardware modules developed and offered by AWS Partners, and <ins>[AWS Private 5G](https://aws.amazon.com/private5g/)</ins>, a managed service that makes it easy to deploy, operate, and scale a private cellular network, with all required hardware and software provided by AWS. This could act as a catalyst for AWS’ industrial IoT and edge offerings.

The new CEO, Adam Selipsky’s, approach to tapping the cloud market differs from that of his predecessor, Andy Jassy. Selipsky’s strategy involves expanding AWS’ offerings beyond general-purpose cloud technologies into industry- and use-case-specific services. IoT is a key area of focus, as can be ascertained from the recent series of IoT-specific releases and his statements.
  
> *“We are going to work aggressively on ‘internet of things’ solutions, on ML solutions and these horizontal use cases and applications as well as bundle it together in ways that are attractive to solving customer problems.”*<br/>
**Adam Selipsky, CEO at AWS, 28 November 2021, to Silicon Angle**
  
> *“We’re building ever more powerful capabilities, pushing the edge of the cloud to new places with things like 5G and IoT. We’re driving towards seamless integration of data, analytics and machine learning that will be transformative. We’re tailoring services and applications to specific customer use cases and industries. The possibilities there are endless.”*<br/>
**Adam Selipsky, CEO at AWS, at AWS re:Invent 2021**
  
## AWS IoT in action:
  
To understand how all of the different AWS IoT components come together, consider the following reference architecture for smart products.
  
<img width="700" alt="Capture" src=https://user-images.githubusercontent.com/52132063/155271187-a9f403dc-e423-4b93-8262-2e947b6d004c.png>

Source: https://aws.amazon.com/solutions/implementations/smart-product-solution/
The reference architecture shows how AWS IoT Core authenticates messages from smart products and routes those messages to the solution’s microservices (AWS Lambda functions). AWS IoT Device Defender audits devices to ensure they do not deviate from security best practices. Finally, AWS IoT Analytics is used to analyze data from smart products. Non-IoT-specific AWS services, including Amplify, Amazon S3, and Amazon CloudFront, are also used.
  
**iRobot** is a known AWS IoT customer reference in this area. The global consumer robot company offers <ins>[connected vacuum and mopping robots.](https://aws.amazon.com/solutions/case-studies/irobot/)</ins>
  
## AWS’ IoT-specific services:
  
AWS lists 13 specific IoT cloud services in its <ins>[portfolio.](https://aws.amazon.com/iot/)</ins>
  
- **Application management/enablement:** <ins>[AWS IoT FleetWise](https://aws.amazon.com/iot-fleetwise/)</ins>, <ins>[AWS IoT TwinMaker](https://aws.amazon.com/iot-twinmaker/)</ins><br/>
- **Device management:** <ins>[AWS IoT Device Management](https://aws.amazon.com/iot-device-management/)</ins>, <ins>[AWS IoT Events](https://docs.aws.amazon.com/iotevents/latest/developerguide/what-is-iotevents.html)</ins>, <ins>[AWS IoT Device Defender](https://aws.amazon.com/iot-device-defender/)</ins>, <ins>[AWS IoT 1-Click](https://aws.amazon.com/iot-1-click/)</ins><br/>
- **Data management/enablement:** <ins>[AWS IoT Core](https://aws.amazon.com/iot-core/)</ins>, <ins>[AWS IoT Greengrass](https://docs.aws.amazon.com/greengrass/v1/developerguide/what-is-gg.html)</ins>, <ins>[AWS IoT SiteWise](https://aws.amazon.com/iot-sitewise/)</ins>, <ins>[AWS IoT Analytics](https://aws.amazon.com/iot-analytics/#:~:text=AWS%20IoT%20Analytics%20is%20a,build%20an%20IoT%20analytics%20platform.)</ins>, <ins>[AWS IoT ExpressLink](https://aws.amazon.com/iot-expresslink/)</ins>, <ins>[AWS IoT RoboRunner](https://aws.amazon.com/roborunner/)</ins><br/>
- **Other IoT offerings:** <ins>[FreeRTOS](https://www.freertos.org/)</ins><br/>
  
## 3.  **GCP IoT**<br/>
  
Although Google Cloud is a distant third in the global public cloud computing market, the company is behind some of the latest and most-adopted cloud technologies. The open-source container orchestration platform Kubernetes, for example, was designed by Google and has since become the de facto standard for managing containers in the cloud. Due to its heritage in organizing search and related data, Google has also maintained a strength in analytics, Big Data, and, more recently, AI and machine learning. According to our research,<ins>[Cloud IoT Core](https://cloud.google.com/iot-core)</ins> is the most popular Google Cloud IoT service (based on public IoT case studies). Cloud IoT Core is a fully managed service that is used to connect IoT devices. It can be combined with other services offered by Google Cloud to build an end-to-end IoT solution. Google’s IoT Core is very similar to Microsoft’s IoT Hub. For further data processing and management, Google integrates into its general blockbuster analytics tools (e.g., BigQuery) but, in contrast to its competitors, does not provide IoT-specific data services (e.g., AWS IoT Analytics).
  
With over 100 cloud services in total and only one dedicated to IoT, Google clearly is not prioritizing IoT in the same way as its two biggest rivals. Google’s IoT focus is very specialized, which also limits the company to some extent. Consider, for example, the emerging topic of digital twins, which plays a key role in many IoT scenarios. Azure has its <ins>[Digital Twin](https://azure.microsoft.com/en-us/services/digital-twins/)</ins> service for creating models of physical environments. AWS recently released <ins>[AWS IoT TwinMaker](https://aws.amazon.com/de/iot-twinmaker/)</ins> with a similar focus. Google, however, has no general digital twin service. (Note: <ins>[Google recently previewed Supply Chain](https://cloud.google.com/solutions/supply-chain-twin)</ins> Twin, a digital twin service for supply chain optimization.)

IoT seems to be missing as a strategic element for Google Cloud. Google Cloud CEO Thomas Kurian has not emphasized IoT as a priority in any of his appearances. Although Google has some prominent IoT customers, such as Philips, it seems as though Google is focused less on enterprises with an IoT element and more on companies such as Spotify, Snapchat, and Best Buy (all of which are well-known Google Cloud customers).
  
## Google Cloud IoT in action
 
*To understand how the Google Cloud Platform services work together consider the following (general) architecture for IoT.*
  
<img width="700" alt="Capture" src=https://user-images.githubusercontent.com/52132063/155272971-8c6f545a-a523-4a87-9c28-5fb2a9d4889f.jpg>

Source: https://cloud.google.com/iot-core/
The reference architecture shows how messages from devices are brokered as events into the Cloud Pub/Sub events stream manager through IoT Core, which acts as a gateway between devices and cloud services. The Cloud Pub/Sub message triggers a cloud function to run on it. Cloud Dataflow (a managed service) helps transform the incoming streams. It can be used to filter incoming data that are not needed in the final storage. Messages stay in Cloud Pub/Sub temporarily, and it stores the data for seven days. Dataflow shuttles the data to the storage and analytics section (Cloud Bigtable, BigQuery, and AI Platform). Google also offers data visualization tools, such as Datalab and DataStudio.
  
### GCP’s IoT-specific services
GCP lists IoT Core as its only IoT cloud service. It provides a list of other supportive capabilities that are not IoT-specific but add more functionalities.
  
# More information and further reading

## Are you interested in learning more about IoT cloud computing?
  
The <ins>[Cloud Computing for IoT Market Report 2021–2026](https://iot-analytics.com/product/cloud-computing-for-iot-market-report-2021-2026/)</ins> is a comprehensive 135-page report on the current state and trends of the IoT Cloud Computing Market. It is part of IoT Analytics’ ongoing coverage of <ins>[IoT Platforms & Software.](https://iot-analytics.com/our-coverage/iot-platforms-software/)</ins>

The report includes a detailed overview and explanation of the 6 main public cloud building blocks, competitive landscape analysis for the leading hyperscalers­ — with analysis of more than 250 IoT case studies and cloud services used, market sizing of the public cloud market for IoT PaaS and IoT IaaS including a forecast to 2026 and breakdown by country and segment. It also includes 24 public Cloud reference architectures for common IoT use cases, 7 recent trends & developments in the Cloud market for IoT, a separate project database in Excel with 130+ IoT cloud projects, and much more.
  
<img width="700" alt="Capture" src=https://user-images.githubusercontent.com/52132063/155273413-e38419b9-e93a-4c02-904a-dbff8056ed84.png>
  
This report provides answers to the following questions (among others):
- How big is the IoT Cloud computing market and how fast it is growing across the following dimensions?<br/>
  - By type: IoT PaaS vs. IoT IaaS<br/>
  - By vertical (13 segments)<br/>
  - By country/region (57 countries)<br/>
- What are some of the main trends and developments in the IoT cloud market?<br/>
- How big are the major hyperscalers in the IoT cloud segment?<br/>
- How do typical IoT public cloud architectures look like?<br/>
- How do IoT public cloud architectures look like in specific projects?<br/>
- And more…<br/>

  
## Sample
  
The sample of the report gives you a holistic overview of the available analysis (outline, key slides). The sample also provides additional context on the topic and describes the methodology of the analysis. You can download the sample here:\

[```Download Now```](https://iot-analytics.com/product/cloud-computing-for-iot-market-report-2021-2026/#request-form-cloud-computing-for-iot-market-report)
