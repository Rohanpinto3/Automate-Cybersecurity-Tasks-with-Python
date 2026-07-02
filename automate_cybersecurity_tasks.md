# Automate Cybersecurity Tasks with Python

---

### WHAT IS PROGRAMING ?

**Programming is the process of creating instructions that tell a computer what to do. It involves writing code in a programming language to solve problems, automate tasks, or build applications.**

---

### Why we use python in Cybersecurity ?

Its purpose is to automate tasks, analyze data, and build security tools—often gluing different systems together to make your job easier and more effective.

In cybersecurity, Python is used especially for automation. **Automation** is the use of technology to reduce human and manual effort to perform common and repetitive tasks. These are some specific areas of cybersecurity in which Python might be used to automate specific tasks:

- Log analysis
- Malware analysis
- Access control list management
- Intrusion detection
- Compliance checks
- Network scanning

---

# **Python Data Types**

### **1. Strings (`str`)**

Text data - enclosed in quotes.

String data is data consisting of an ordered sequence of characters. These characters could be letters, symbols, spaces, and even numbers.

## **2. Integers (`int`)**

 Integer data is data consisting of a number that does not include a decimal point. Numbers such as 0, -9, and 5,000 are valid integers. So far, we've used the print function to output a string. 

## **3. Floats (`float`)**

Numeric data includes floats and integers. Float data is data consisting of a number with a decimal point. This includes fractions like 2.1 or 10.5. 

## **4. Booleans (`bool`)**

True/False values - for conditions and flags.

Boolean data is data that can only be one of two values: either True or False. Booleans are useful for logic in our programs.

## **5. Lists data  (`list`)**

List data is a data structure that consists of a collection of data in sequential form. 

## **List**

In Python, **list data** is a data structure that consists of a collection of data in sequential form. Lists elements can be of any data type, such as strings, integers, Booleans, or even other lists. The elements of a list are placed within square brackets, and each element is separated by a comma. The following lists contains elements of various data types:

- **[12, 36, 54, 1, 7]**
- **["eraab", "arusso", "drosas"]**
- **[True, False, True, True]**
- **[15, "approved", True, 45.5, False]**

---

# **variables in Python**

A variable is a container that stores data.

```python
# Snake case (recommended)
malicious_ip = "10.0.0.5"
failed_attempts = 3

# Camel case (less common in Python)
threatLevel = "critical"

# UPPERCASE for constants
MAX_LOGIN_ATTEMPTS = 5
API_KEY = "abc123"

# Starting with underscore
_private_data = "sensitive"

# With numbers (but not starting)
attempt2 = 2
ip_address_2023 = "192.168.1.100"
```

## **Naming Rules**

### **✅ Allowed**

- Letters, numbers, underscores
- Start with letter/underscore
- Case sensitive (`ip ≠ IP`)
- Snake_case recommended

---

# **Conditional Statements**

### **What Are Conditional Statements?**

Conditional statements allow your program to **make decisions** based on conditions. They execute different code blocks depending on whether conditions are `True` or `False`.

### **Basic Structure of IF Statements**

python

```python
if condition:
    # body - code to run when condition is True
```

### **Key Components:**

### **1. Header Line**

python

```python
if failed_attempts > 5:
```

- **`if`** - keyword that starts the conditional
- **`condition`** - what we're checking (`failed_attempts > 5`)
- **`:`** - colon signals the body comes next

### **2. Body (Indented Code)**

python

```python
    print("Account locked")
```

- **Must be indented** (usually 4 spaces)
- **Only runs** when condition is `True`
- **Can have multiple lines** (all must be indented)

---

### **Complete Example Breakdown**

python

```python
# Variable assignment (happens BEFORE the if statement)
failed_attempts = 6

# Header - the condition check
if failed_attempts > 5:
    # Body - what happens when condition is True
    print("Account locked")
    send_security_alert()
```

**What happens:**

1. `failed_attempts` is assigned value `6`
2. Condition `failed_attempts > 5` evaluates to `6 > 5` which is `True`
3. Since condition is `True`, the indented body code runs
4. Output: "Account locked" and security alert is sent

---

activity :

python

```python
# ===  VARIABLES ===
compromised_host = "WEB-SRV-02"
attacker_ip = "95.161.222.78"
failed_login_attempts = 4
max_allowed_attempts = 3
is_account_locked = False

# ===  CONDITIONAL CHECKS ===
print("=== INCIDENT REPORT ===")
print("Compromised Host:", compromised_host)
print("Attacker IP:", attacker_ip)
print("Failed Login Attempts:", failed_login_attempts)
print("Max Allowed Attempts:", max_allowed_attempts)
print("Is Account Locked:", is_account_locked)

print("\n=== SECURITY ANALYSIS ===")

# Check 1: Login Attempts
if failed_login_attempts > max_allowed_attempts:
    print("🚨 ALERT: Too many login attempts!")
    print(f"   ⚠️  {failed_login_attempts} attempts exceeds maximum of {max_allowed_attempts}")
    # Auto-lock the account
    is_account_locked = True
    print("   🔒 Account has been automatically locked")
else:
    print("✅ Login attempts within acceptable limits")

# Check 2: Account Status
if is_account_locked:
    print("🚨 ACCOUNT STATUS: LOCKED - requires admin intervention")
else:
    print("✅ ACCOUNT STATUS: ACTIVE - no intervention needed")

# Check 3: Risk Assessment
if failed_login_attempts >= 4:
    risk_level = "CRITICAL"
elif failed_login_attempts >= 2:
    risk_level = "HIGH"
else:
    risk_level = "LOW"

print(f"📊 RISK LEVEL: {risk_level}")

print("\n=== RECOMMENDED ACTIONS ===")
if failed_login_attempts > max_allowed_attempts:
    print("1. 🔒 Keep account locked")
    print("2. 📧 Notify security team")
    print("3. 🔍 Investigate source IP:", attacker_ip)
else:
    print("1. 👀 Continue monitoring")
    print("2. 📝 Log incident for records")
```

## **Output:**

```
=== INCIDENT REPORT ===
Compromised Host: WEB-SRV-02
Attacker IP: 95.161.222.78
Failed Login Attempts: 4
Max Allowed Attempts: 3
Is Account Locked: False

=== SECURITY ANALYSIS ===
🚨 ALERT: Too many login attempts!
   ⚠️  4 attempts exceeds maximum of 3
   🔒 Account has been automatically locked
🚨 ACCOUNT STATUS: LOCKED - requires admin intervention
📊 RISK LEVEL: CRITICAL

=== RECOMMENDED ACTIONS ===
1. 🔒 Keep account locked
2. 📧 Notify security team
3. 🔍 Investigate source IP: 95.161.222.78
```

---

![image.png](image.png)

![image.png](image%201.png)

![image.png](image%202.png)

![image.png](image%203.png)

![image.png](image%204.png)

![image.png](image%205.png)

![image.png](image%206.png)

![image.png](image%207.png)

![image.png](image%208.png)

![image.png](image%209.png)

---

# **Iterative Statements**

## **What are Iterative Statements?**

**Iterative statements** (also called **loops**) allow you to **repeat code multiple times**. Think of them as automation tools that do repetitive work for you.

### There are two types of loops in python :

- FOR loop
- WHILE loop

### **1. For Loops - When you know how many times to repeat**

### **Syntax:**

python

```python
for variable in sequence:
    # code to repeat
```

### **Cybersecurity Examples:**

### **Scan Multiple IPs:**

```python
# Check multiple IP addresses for suspicious activity
suspicious_ips = ["192.168.1.100", "10.0.0.5", "203.0.113.10"]

for ip in suspicious_ips:
    print(f"🔍 Scanning IP: {ip}")
    print(f"📊 Checking for malicious activity...")
```

**Output:**

```
🔍 Scanning IP: 192.168.1.100
📊 Checking for malicious activity...
🔍 Scanning IP: 10.0.0.5
📊 Checking for malicious activity...
🔍 Scanning IP: 203.0.113.10
📊 Checking for malicious activity...
```

### **Check Multiple Ports:**

```python
# Scan common ports for security assessment
common_ports = [22, 80, 443, 3389, 8080]

for port in common_ports:
    print(f"🔒 Checking port {port} for vulnerabilities")
```

### **2. While Loops - When you don't know how many times to repeat**

### **Syntax:**

```python
while condition:
    # code to repeat while condition is True
```

### **Cybersecurity Examples:**

### **Monitor Login Attempts:**

```python
# Monitor until too many failed attempts
failed_attempts = 0
max_attempts = 3

while failed_attempts < max_attempts:
    print(f"⚠️ Failed login attempt #{failed_attempts + 1}")
    failed_attempts += 1

print("🚨 Account locked: Too many failed attempts!")
```

**Output:**

```
⚠️ Failed login attempt #1
⚠️ Failed login attempt #2
⚠️ Failed login attempt #3
🚨 Account locked: Too many failed attempts!
```

### **Continuous Security Monitoring:**

```python
# Simulate continuous monitoring
monitoring = True
threat_detected = False

while monitoring and not threat_detected:
    print("👀 Monitoring network traffic...")
    # In real system, this would check for threats
    # For demo, we'll stop after one iteration
    threat_detected = True

print("✅ Monitoring complete - no threats detected")
```