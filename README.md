# JMeter Assessment
Below is the run of the Project

[https://github.com/user-attachments/assets/c70cdf3d-a4a9-4201-9bbd-0facdcf1b9bd](https://github.com/user-attachments/assets/474cab9d-92e2-4950-8b80-56127fcb19a7)

## Overview
This project contains a JMeter test plan designed to evaluate the performance and functionality of a specific API. The test plan sends HTTP requests to an API endpoint, validates responses, and processes the data as needed. The test plan includes configurations for thread groups, HTTP request samplers, and assertions.

## Prerequisites
To run this test plan, ensure you have the following installed on your machine:

1. **Java Development Kit (JDK):** JMeter requires Java to run. Download and install the latest version of the JDK from [Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) or [OpenJDK](https://openjdk.org/).
2. **Apache JMeter:** Download the latest version of Apache JMeter from [JMeter Downloads](https://jmeter.apache.org/download_jmeter.cgi).
3. **Internet Access:** Ensure your machine has access to the internet to execute requests against online APIs.

## Setup Instructions
Follow these steps to set up the test plan:

1. **Download the JMX File:** Clone or download this repository to your local machine.
2. **Open JMeter:** Navigate to the JMeter installation directory and launch the `jmeter.bat` file (Windows) or `jmeter.sh` (Mac/Linux).
3. **Load the Test Plan:**
   - In JMeter, click on `File > Open`.
   - Browse to the location of the `.jmx` file and open it.

## Running the Test Plan
1. Configure any necessary variables or endpoints in the test plan:
   - Expand the `Thread Group` section to modify the number of users, ramp-up time, or loop count.
   - Edit the HTTP Request sampler to update the API endpoint or payload if needed.
2. Start the Test:
   - Click the green `Start` button (triangle icon) in the top toolbar.
   - Monitor test progress in the `View Results Tree` or `Summary Report` listeners.
  
## Explanation of Each Component and Post-Processor
1. I've used JSON Assertions for both of the API's(GET and POST) to validate the response key-values, for response code assertion I've used Response Assertions and in POST api I've used HTTP Header Manager to send the specific key-values in HTTP request header.
2. I've used JSON Extractor to extract user ID from the response of the POST request and store it in a variable(extracted_id) and to verify/check variable value I've used Debug Sampler. To use the extracted variable I've added JSR223 PostProcessor and print the variable you can see that in console.

## Results
The test plan includes listeners to display results:

- **View Results Tree:** Provides detailed request and response logs.
- **Summary Report:** Shows aggregated statistics such as average response time, throughput, and errors.
- **Log Files:**
  - Test logs will be saved in the `bin` folder of your JMeter installation or as configured in the test plan.

## Contact
If you encounter any issues or have questions, feel free to contact me at **adnanaashiq457@gmail.com** and WhatsApp me on **+92-302-2149193**.
