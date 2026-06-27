Future_CS_01 - passive cybersecurity audit

overview

This repository showcases the cybersecurity Task 1(2026) from the future interns internship program. A passive vulnerability assessment was performed on testphp.vulweb.com(https://testphp.vulnweb.com) to identify security weaknesses without exploitation.

Tools Used

1. Google chrome
2. Browser Developer Tools
3. Nmap
4. OWASP ZAP


key findings

1. missing content security policy(CSP) - Medium risk
2. missing strict-transport-security (HSTS)- Medium risk
3. missing Anti-Clickjacking Protection- Medium risk
4. missing X-content-type-options- Low risk
5. Timestamp disclosure-Low risk
6. Network exposure- Low risk

Recommendations

1. implement CSP & HSTS headers
2. configure anti-clickjacking nosniff
3. remove unnecessary timestamp disclosures
4. continue firewall monitoring & regular assessments

Deliverables

1. Vulnerability Assessment Report
2. Evidence screenshots & tool output(/evidence)
3. README summarizing scope, findings and recommendations

conclusion

this assessment highlights medium-risk gaps in HTTP security headers and confirms effective firewall controls by applying the recommended fixes, the website's security posture will be strengthened against common web threats.
