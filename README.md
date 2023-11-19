# Cloud Infrastructure Engineering - (6 Months) Entry Assessment

## Objective

This assessment aims to test your resourcefulness, the ability to understand IT concepts, and produce a viable answer to the problems listed.

---
## Submission

Use the registration form in NTU SCTP

---
## Expected Audience

- Individuals with an IT background to diversify/expand their skills and/or intending to switch to a cloud engineering role.
    - Those with IT or Engineering degree/diploma, or
    - Those with IT or Engineering experience professionally
- Individuals with systems and infrastructure administration background.
- Individuals who have attended basic infrastructure or cloud courses.
- Individuals without an IT background but want to expand their skills and/or intending to switch to a cloud engineering role.

---

## Problems

Please attempt the solve the problems described:

**Question 1 - IP Address**

What is the Bash command to discover the IP Address of `www.skillsunion.com`?

```sh
dig www.skillsunion.com +short
```

---

**Question 2 - Copy a Directory**

What is the command to copy a directory from `~/my_project` to `/etc/projects`?

```sh
sudo cp -r ~/my_project /etc/projects/
```
---

**Question 3 - Shell Scripting**

Implement a bash script that does the follow:
1. Convert a string "one,two,three" into an array delimited by comma (,).
1. Loop through the array and print each element.

```sh
#!/bin/bash

# The input string
input="one,two,three"

# Convert string into an array using comma as delimiter
IFS=',' read -r -a array <<< "$input"

# Loop through the array and print each element
for element in "${array[@]}"
do
    echo "$element"
done
```

---

**Question 4 - System Architecture Diagram**

Use [draw.io](draw.io) to draw a system architecture diagram as described below:

- A load balancer to manage request between 4 application servers.
- The load balancer is connected to the internet gateway.
- All application servers are connected to a cluster of database.
- The cluster of database contains an instance for reading and another instance for writing.
- The database must not be connected to the internet gateway.

Share the link to your image of diagram.  
https://drive.google.com/file/d/1oDBogflShyhLOrVyg4oUcgCusFXzHp-l/view?usp=sharing
---

**Question 5 - System Error Management**

Alan has deployed his web application to Amazon Web Service. Unfortunately, the web application encountered errors as complained by the customers (public users). Whenever there is a complaint, Alan would take a long time to trace the issue and get back to the customers. 

*Q5A: Which of the following described the scenario given?*

A - The principle of security is not applied.

B - The principle of observability is not applied.

C - The principle of availability is not applied.

D - The principle of performance is not applied.

*Q5B: What do you suggest could be done to improve the situation?*




Q5A:  

The described scenario most closely aligns with:  
B - The principle of observability is not applied.

Q5B: To improve the situation, Alan could implement several measures:  

1. **Logging**: Ensure comprehensive logging is in place so that errors can be quickly identified and traced back to their source. This includes application logs, server logs, and database logs.  

2. **Monitoring**: Use tools to monitor the application and infrastructure in real-time. AWS CloudWatch can be used to monitor AWS resources and applications.  

3. **Alerting**: Set up alerts for anomalies or errors so that Alan can be proactively notified of issues, rather than waiting for customer reports.  

4. **Tracing**: Implement distributed tracing to follow the path of a request through various services to find where failures occur and what their impacts are.  

5. **Performance Metrics**: Collect performance metrics to understand the health of the application and to spot trends that might indicate underlying issues.  

6. **Error Budgets**: Establish error budgets which can help prioritize work on stability vs new features.  

7. **Feedback Loops**: Create efficient feedback loops between the customer support and development teams to ensure that errors are reported and handled swiftly.  
By improving observability, Alan will be able to detect, diagnose, and respond to issues much more quickly, which will improve the overall reliability of the application and customer satisfaction.

---

END
