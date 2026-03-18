# CCNA-Lab-Network-Management-CDP-LLDP-NTP- 

## This lab demonstrates the configuration of network management protocols on Cisco routers including CDP, LLDP, NTP and Syslog.  

## Technologies used: - CDP for Cisco device discovery - LLDP for vendor-neutral discovery - NTP for time synchronization 

## All configurations were tested in Cisco Packet Tracer.

## Step 1 — Basic Configuration

📍 On R1 and R2

enable

configure terminal

hostname R1

no ip domain-lookup == "To disable DNS name resolution on the device itself."

## Configure interfaces

interface g0/0/0

ip address 192.168.1.1 255.255.255.0

no shutdown

exit

## Step 2 — Configure CDP

📍 On both routers

## Enable CDP globally

cdp run

## Enable CDP on interface

interface g0/0

cdp enable

## Verification

show cdp neighbors

## Step 3 — Configure LLDP

## Enable LLDP

lldp run

Enable LLDP on interface

interface g0/0/0

lldp transmit

lldp receive

### Verification

show lldp neighbors

## Step 4 — Configure NTP

## Configure NTP server

ntp server 192.168.1.10

## Verify

show ntp associations

## SANAA EL HABIB KAHLOUL :         https://www.linkedin.com/in/sanaa-el-habib-kahloul/ 
