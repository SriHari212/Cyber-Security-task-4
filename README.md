# Cyber-Security-task-4

# Task 4: Windows Firewall Configuration

This repository documents the process of setting up and testing a basic firewall rule on Windows 10/11 using the Windows Defender Firewall with Advanced Security.

---

## 1. Summary of How a Firewall Filters Traffic

*(Here, you will write the summary you created. For example:)*

A firewall acts as a digital security guard for a computer network. It inspects all incoming and outgoing data and decides whether to allow it or block it based on a set of security rules. It filters traffic by looking at information like the source/destination IP address, the protocol (TCP/UDP), and the specific port number. By creating rules to allow or deny traffic for specific ports, a firewall protects the system from unauthorized access.

---

## 2. Documentation of GUI Steps Used
1.  Opened **Windows Defender Firewall with Advanced Security** from the Start Menu.
2.  Navigated to the **Inbound Rules** section.
3.  Clicked **New Rule...** to start the wizard.
4.  Selected **Rule Type:** Port.
5.  Specified **Protocol and Ports:** TCP, Port 23.
6.  Chose the **Action:** Block the connection.
7.  Applied the rule to all **Profiles** (Domain, Private, Public).
8.  Named the rule "Block Telnet (Port 23)" and saved it.
9.  Tested the block using the `Test-NetConnection -ComputerName localhost -Port 23` command in PowerShell, which failed as expected.
10. Deleted the rule to restore the original state.

---

## 3. Deliverable: Screenshot of the Applied Rule

The following screenshot shows the "Block Telnet (Port 23)" rule active in the Windows Defender Firewall.

![Screenshot of the new firewall rule](firewall-rule-screenshot.png)
