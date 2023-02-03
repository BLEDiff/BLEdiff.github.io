---
layout: default
---

The Bluetooth Low Energy (BLE) is regarded as the most popular short range wireless communication technology in the recent years. According to [reports](https://www.bluetooth.com/2022-market-update/), the number of BLE devices is expected to reach over 7 Billion in the next 4 years including mobile phones, IoT devices, computers, headphones, smart watches, etc. With this large attack surface, adversaries often target BLE devices to bypass security and privacy expectations. To ensure proper security measures, the Bluetooth Special Interest Group (SIG) actively works on updating the protocol specifications and maintaining standards. Despite the efforts, as BLE comprises a complex layered architecture and a plethora of different kinds of devices, having different capabilities and versions, implement the protocol, the implementations often fail to follow the specifications correctly and show noncompliant behavior.  

**BLEDiff** provides an automated black-box noncompliance checking framework for BLE devices and identifies several security issues in the tested devices.

## BLEDiff has been accepted to IEEE S&P 2023  


## CVE Updates
### CVE-2022-45190
- Affected Product: Microchip Technology BLE peripheral implementation.
- Version: RN4870 - v1.43
- CVE ID: CVE-2022-45190
- Description: An attacker within BLE radio range can bypass passkey entry in the legacy pairing of the device.
- Root Cause: The root cause of this issue can be attributed to implementation deviating from the specification. The BLE specification clearly states that if the confirm values do not match, the peripheral should not proceed with pairing.
- Impact: Due to this passkey entry bypass, it is possible for the attacker to perform a MitM attack on the vulnerable BLE devices.


### CVE-2022-40480
- Affected Product: Nordic Semiconductor, Microchip Technology
- Version: NRF5340-DK - DT100112
- CVE ID: CVE-2022-40480
- Description:  Nordic Semiconductor, Microchip Technology NRF5340-DK DT100112 was discovered to contain an issue which allows attackers to cause a Denial of Service (DoS) via a crafted ConReq packet.
- Root Cause: The root cause of this issue can be attributed to implementation deviating from the specification. 
- Impact: An attacker in the radio range can exploit the issue to cause a surreptitious denial of service of the Bluetooth. Though this attack is on BLE, the smartphone turns off both BLE and BR/EDR without notifying the user. To resolve this, the user has to manually restart BLE and, in some cases, the smartphone altogether.

### CVE-2022-45192
- Affected Product: Microchip Technology BLE peripheral implementation.
- Version: RN4870 - v1.43
- CVE ID: CVE-2022-45192
- Description: An attacker within BLE radio range can cause a denial of service by sending a cleartext encryption pause request.
- Root Cause: The root cause of this issue can be attributed to implementation deviating from the specification. 
- Impact: The implementation goes to an incorrect state and discards subsequent messages from the central. The deviation thus enables an attacker to induce DoS attacks on the affected devices. An correctly implemented device ignores plaintext PauseEncReq messages and does not change state.


### CVE-2022-45191
- Affected Product: Microchip Technology BLE peripheral implementation.
- Version: RN4870 - v1.43
- CVE ID: CVE-2022-45191
- Description:  An attacker within BLE radio range can cause a denial of service by sending a pair confirm message with wrong values.
- Root Cause: The root cause of this issue can be attributed to implementation deviating from the specification. 
- Impact: An attacker within the radio range of another BLE implementation can cause a denial of service by sending a pair confirm message with wrong values.


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
