---
layout: default
---

The Bluetooth Low Energy (BLE) is regarded as the most popular short range wireless communication technology in the recent years. According to [reports](https://www.bluetooth.com/2022-market-update/), the number of BLE devices is expected to reach over 7 Billion in the next 4 years including mobile phones, IoT devices, computers, headphones, smart watches, etc. With this large attack surface, adversaries often target BLE devices to bypass security and privacy expectations. To ensure proper security measures, the Bluetooth Special Interest Group (SIG) actively works on updating the protocol specifications and maintaining standards. Despite the efforts, as BLE comprises a complex layered architecture and a plethora of different kinds of devices, having different capabilities and versions, implement the protocol, the implementations often fail to follow the specifications correctly and show noncompliant behavior.  

**BLEDiff** provides an automated black-box noncompliance checking framework for BLE devices and identifies several security issues in the tested devices.

## [BLEDiff has been accepted to IEEE S&P 2023](https://www.computer.org/csdl/proceedings-article/sp/2023/933600b082/1Js0DDrcl20)  



## Identified Vulnerabilities


<div align="center" data-include="assets/tables/identified-vulnerabilities.html">
    

<br> Tab.: Summary of identified issues (E: exploitable issue, I: interoperability issue, O: other issue)
</div>


<div align="center" data-include="assets/text/vulnerabilities.html"> </div>





<h2> Affected Devices  </h2>

<div align="center" data-include="assets/tables/affected-devices.html">
<br> Tab.: Summary of affected devices
</div>


<h2> Responsible Disclosure Progress </h2>


<div align="center" data-include="assets/tables/responsible-disclosure.html"></div>

<h2> Open Source Implementation </h2>

Due to responsible disclosure, we are not releasing the implementation of BLEDiff yet. We will provide the open sourced implementation at the [github repository](https://github.com/BLEDiff/BLEDiff) when the responsible disclosure process is complete.
