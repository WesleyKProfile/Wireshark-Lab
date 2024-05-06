# Wireshark Lab

## Objective
The Wireshark lab aimed to enhance skills in capturing and analyzing network traffic, covering the use of Wireshark for both live captures and analysis of stored files. It included exploring various protocols like RADIUS, HTTP, DNS, and encrypted HTTPS, with a focus on decrypting RADIUS passwords and HTTPS traffic for deeper insights into network security.

### Skills Learned

- Advanced understanding of network traffic analysis concepts and practical application using Wireshark.
- Proficiency in capturing and analyzing various network protocols including RADIUS, HTTP, DNS, and encrypted HTTPS.
- Ability to decrypt RADIUS passwords and HTTPS traffic, demonstrating expertise in authentication mechanisms and encrypted communications.
- Development of critical thinking and problem-solving skills in cybersecurity through hands-on experience with real-world network traffic scenarios.

## Steps
**Capturing RADIUS Traffic**

1. Used a capture filter to filter for RADIUS traffic (port 1812).
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/68f6b484-fc92-4ab2-96cd-b4a4c05b4b53" alt="image">

<sub>*ref 1. a capture filter to show only traffic over port 1812*</sub>

2. Generated RADIUS traffic using NTRadPing Test Utility and ID Blender.
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/4003744d-fc8d-41bf-899f-c863e9dcf55b)" alt="image">

<sub>*ref 2. NTRadPing Test Utility being used to generate RADIUS traffic*</sub>

3. Captured RADIUS traffic, since the shared secret is known, both the username and password can be viewed in plain text.
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/2270d5df-48dc-453b-9d6c-6e7dd2c6adc0" alt="image">

<sub>*ref 3. captured RADIUS traffic*</sub>

<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/9f2bb18b-9a2a-410d-b94e-09ab00df6f28" alt="image">

<sub>*ref 4. cleartext username and password*</sub>

**Capturing HTTP Traffic**

1. Used a capture filter to filter for HTTP traffic (port 80).
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/6fa6401e-fea9-4707-accf-395d2614c965" alt="image">

<sub>*ref 5. a capture filter to show only traffic over port 80*</sub>

2. Generated HTTP traffic using httpbin for capture analysis.
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/e17c8838-43fa-4e40-b648-29c1c03e2db5" alt="image">

<sub>*ref 6. captured HTTP traffic*</sub>

3. Identify and select the authentication packet to access login credentials in plaintext.
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/6705a249-6c73-40fa-b701-251ae021e87f" alt="image">

<sub>*ref 7. credentials in the clear*</sub>

**Capturing Form Based Login Credentials**

1. Used a capture filter to filter for HTTP traffic (port 80).

2. Generated HTTP traffic using Web Scraper Testing Ground for analysis.

3. Identified password displayed in HTML format rather than Hypertext.
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/71c23bd6-ee72-4a58-9d83-e90f01ac74ee" alt="image">

<sub>*ref 8. form based credentials in the clear*</sub>

**Capturing DNS Traffic**

1. Use a capture filter to filter for DNS traffic (port 53).

2. Pinged Google to generate DNS traffic.

3. The captured DNS traffic is now available for analysis.
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/1c3fb3b7-16fe-402f-9d46-fa34c23803c7" alt="image">

<sub>*ref 9. captured DNS traffic*</sub>

**Capturing HTTPS Traffic**

1. Used a capture filter to filter for HTTPS traffic (port 443).

2. Examined TLS information within packets.
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/8b0e580b-ac1d-4fe1-864d-d55ba22661e1" alt="image">

<sub>*ref 10. TLS information*</sub>

3. Utilized environment variables to generate an SSL key log file.
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/711406bb-a1cf-46b7-9a56-d5dc9158f0dc" alt="image">

<sub>*ref 11. creation of new SSL key log file*</sub>

4. Integrated the SSL key log file into Wireshark for decryption.

5. Generated HTTPS traffic by browsing a website and obtained the website's IP address using the ping command.

6. Identified the IP address of the selected website using Wireshark's conversation feature, then proceeded to use 'Follow the Stream' for further analysis.
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/8fd4f518-99af-486d-a52c-3ca4b7311676" alt="image">

<sub>*ref 12. conversation in Wireshark*</sub>

<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/501ad04d-5a2b-4578-9bca-1bf0165325de)" alt="image">

<sub>*ref 13. result of Follow the Stream*</sub>

7. Examined the contents to view the decrypted data.
<img src="https://github.com/WesleyKProfile/Wireshark-Lab/assets/168662972/24d4cd93-d27c-4360-95cb-43fc6bb08cd7" alt="image">

<sub>*ref 14. decrypted packets*</sub>





