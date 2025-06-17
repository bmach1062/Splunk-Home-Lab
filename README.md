# 🧠 Splunk-Home-Lab

## 🎯 Objective
I will be using Splunk to analyze sample DNS logs by performing log parsing, field extraction, and writing SPL queries to detect anomalies and potential threats, supported by visual dashboards and alerts. 

## 🛠️ Environment and Tools Used
- Splunk
- DNS Log File Sample
- SPL (Search Processing Language)

## 🧭 Field Extraction Process
One great feature about Splunk is that you can create your own fields to organize the information within each log. Fields are simply labels for the information within a log. 

1. **Select any log to extract**  
   Pick any of the logs within the file of logs
2. **Select Method**  
There will be two options to choose from: Regex or Delimiters. For logs that are not structured, using Regex is the best option because unstructured logs will often have different lengths, missing fields, or extra spaces and Regex will offer the most flexibility to create fields. For logs that are structured (i.e. separated by a comma, space, or character), you should use Delimiters because they allow Splunk to easily split each log entry into fields without complex pattern matching, making extraction faster and simpler when the format is uniform.
