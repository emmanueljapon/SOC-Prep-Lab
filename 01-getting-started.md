Homelab Log — Entry 1: Getting Started

Date: July 4, 2026
Goal: Build a cybersecurity homelab to prep for the BTL1 (Blue Team Level 1) certification, focused on Active Directory, detection, and SOC-style workflows.

Why This Lab Exists

I currently work as an IT Support Specialist, and I would like to transition into a SOC Analyst role. BTL1 is my next certification target, and hands-on practice with a realistic environment is the goal. This repo will document my progress as I work on this project and the lessons I am learning. 

After gaining some theoretical knowledge, this lab project will help me gain hands-on experience with situations that SOC analysts commonly face and prepare me for a transition into a SOC Analyst role.

The Hardware

I'm running this lab on a GMKtec M7 Ultra Mini PC:

ComponentSpecCPUAMD Ryzen 7 PRO 6850U (8 cores / 16 threads, up to 4.7GHz)RAM32GB DDR5Storage1TB PCIe SSDNetworkingDual 2.5G LANOtherOCuLink support

32GB of RAM gives enough headroom to run several VMs concurrently — a Windows Server domain controller, an attacker box, a Windows victim machine, and eventually a SIEM (likely Security Onion), without having to constantly power VMs on and off.

The Plan (Month 1)

The roadmap starts with core Active Directory infrastructure before layering in offensive and defensive tooling:


Download and install Windows Server 2022 on a VM
Promote it to a domain controller — hostname DC01, domain lab.local
Configure basic AD structure (OUs, a few test user accounts, group policy basics)
Get a Windows client VM joined to the domain
From there, start layering in Kali Linux, pfSense, and Security Onion in later phases


Today's Step: Downloading Windows Server

Today I'm downloading the Windows Server 2022 ISO to start building DC01.



