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
   ![select_sample_method](https://github.com/bmach1062/Splunk-Home-Lab/blob/main/Splunk_Pictures/1.%20Select_Sample_Event.png)
   
2. **Select Method**  
   There will be two options to choose from: Regex or Delimiters. For logs that are not structured, using Regex is the best option because unstructured logs will often have different lengths, missing fields, or extra spaces and Regex will offer the most flexibility to create fields. For logs that are structured (i.e. separated by a comma, space, or character), you should use Delimiters because they allow Splunk to easily split each log entry into fields without complex pattern matching, making extraction faster and simpler when the format is uniform.

   We will choose Regex in this case because the sample DNS Log File I used has unstructured logs.

 ![select_method](https://github.com/bmach1062/Splunk-Home-Lab/blob/main/Splunk_Pictures/2.%20Select_Method.png)

3. **Select Fields**  
   After choosing the method of extraction, I will highlight any of the fields in the sample log and assign them a name. For example, the first field I extract is the timestamp, which is stored in Unix epoch time (also called epoch or Enoch), a format that represents the number of seconds since January 1, 1970. Keep in mind that it is best practice to extract fields one at a time, rather than extracting multiple fields all at once. When you try to highlight and extract several fields together, Splunk may generate a complex regex pattern that is too rigid or breaks easily if the log format varies slightly across entries. Extracting one field at a time ensures better accuracy, flexibility, and control over the pattern being used, helping you avoid mislabeling or missed data.
![select_fields](https://github.com/bmach1062/Splunk-Home-Lab/blob/main/Splunk_Pictures/3.%20Select_Fields.png)

4. **Field Validation**  
That said, in this case, I selected multiple fields at once since it’s a controlled lab setting and I wanted to move quickly through the process. This approach works here because I know the log format is consistent and I’m only working with a small, predictable dataset.
