+++
date = "2016-01-06"
draft = true
weight = 09
title = "Lab 09 - Packet Capture"
+++

### Lab Objective

The objective of this lab is to introduce command line tools for inspecting network traffic.

#### 1. TCP Dump

0. Skim the `tcpdump` man file

    `$` `man tcpdump` 

0. Switch user to root to allow tcpdump to have permissions to capture traffic

   `$` `sudo su`

0. Run tcpdump with different flag settings:

  `#` `tcpdump -nS`
  `#` `tcpdump -nnvvS`
  `#` `tcpdump -nnvvXS`
  `#` `tcpdump -nnvvXSs 1514`

  > How do each of these modify the captured traffic

0. Add additional modifiers to limit captured traffic to specific hosts

  ```
  host x.x.x.x
  src x.x.x.x
  dst x.x.x.x
  net x.x.x.x/24
  ```

0. Add additional modifiers to limit captured traffic to specific protocols

  ```
  icmp
  udp
  tcp
  ```

0. Add additional modifiers to limit captured traffic to specific ports

  ```
  src port 22
  dest port 22
  ```

#### Sources:

* https://danielmiessler.com/study/tcpdump/
