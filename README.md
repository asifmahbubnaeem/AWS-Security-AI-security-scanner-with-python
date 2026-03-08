<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# AI Security Scanner for Python

**Project Link:** [View Project](http://learn.nextwork.org/projects/ai-security-audit)

**Author:** asif naeem  
**Email:** asifnaim0123@gmail.com

---

![Image](http://learn.nextwork.org/delighted_chartreuse_swift_buddha's_hand_citron/uploads/ai-security-audit_sec4e5f6)

---

## Introducing Today's Project!

In this project, I'm going to build a working CLI tool that helps to find security issues. This will help me learn sql injection, weak cryptography. I'm interested in this because I want to learn about security vulnerabilities.

### Key tools and concepts

Tools I used were python vertual environment, dotenv, google genai, gemini api, api key, text coloring library. Key concepts I learnt include security vulnarability using AI assitance, using api key to call gen ai api. The most important skill was to using prompt command effectively.

### Challenges and wins

This project took me approximately one hour.

### Why I did this project

I did this project today because I wanted to learn about using AI to code scanning.

---

## Connecting to Gemini API

In this step, I'm setting up the Gemini API connection. This involves steps:
1. create a new project folder and setup python environment.
2. get our google AI api key.
3. setup a .env file with our API key.
4. test our connection to gemini.

![Image](http://learn.nextwork.org/delighted_chartreuse_swift_buddha's_hand_citron/uploads/ai-security-audit_sec2c3d4)

I verified the connection by running the scanner python file:
python3 scanner.py
Gemini responded with
Hello, security scanner!
 which confirmed that our connection with gemini working fine.

![Image](http://learn.nextwork.org/delighted_chartreuse_swift_buddha's_hand_citron/uploads/ai-security-audit_sec4e5f6)

My scanner.py file works by using the gemini API request and getting back the response. When I ran it, Gemini identified
1.  **Hardcoding Sensitive Information (Cleartext Storage):**
2.  **Exposure in Memory:**
3.  **Weak Password (Content Issue):**
4.  **No Salting or Hashing (Implied):**
It also provides the recommedation to fix.
This shows that the Gemini API can detect vulnarabilities in code.

---

## Building the Vulnerability Scanner

In this step, I'm building a vulnerability scanner that
1. Add vulnerable code examples to test against
2. Create a detailed security prompt for Gemini
3. Test detection of SQL injection, hardcoded secrets, and weak passwords
This will allow me to do the code scan properly.

![Image](http://learn.nextwork.org/delighted_chartreuse_swift_buddha's_hand_citron/uploads/ai-security-audit_sec7h8i9)

The vulnerabilities Gemini detected were sql injection ,weak MD5 hashing, hardcoded secrets. The security prompt I crafted asked for categorized vulnarabilities.
This structured output helps me find the issues in a categorized way.

---

## Adding Severity Ratings

In this step, I'm adding severity ratings with updating the prompt to include severity ratings.
I'm also installing colorama to to show the colored output text based on severity rate.

![Image](http://learn.nextwork.org/delighted_chartreuse_swift_buddha's_hand_citron/uploads/ai-security-audit_sec0k1l2)

I updated the security prompt to include the severity ratings based on the risk severity. The add_colors_to_output function works by adding color based on the rating. When I see CRITICAL in red, it tells me immediate exploitation possible, could compromise the whole sytem.

---

## Scanning Real Python Files

In this secret mission, I'm adding the option to scan code from files. This lets the scanner read the python files. Professional tools do this because this can be used to check vulnabilities from files to a project.

![Image](http://learn.nextwork.org/delighted_chartreuse_swift_buddha's_hand_citron/uploads/ai-security-audit_sec3n4o5)

I scanned vulnerable.py by running command:
python3 scanner.py vulnerable.py
The vulnerabilities detected were
1. Hardcoded Credentials
2. SQL Injection
3. Use of Weak Cryptographic Hash
4. Command Injection

 The scan_file function works by scanning the files provided as a command line argument.

---

## Wrap-up

---

---
