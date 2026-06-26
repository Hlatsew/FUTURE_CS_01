Browser Developer Tools:

purpose: Inspect HTTP security header and cookies configurations.

Evidance: [Browser Developer Tools] (evidence/missing headers using browser developer tools)

Nmap port scan:

purpose: perform basic network exposure analysis by scannong the target website for publicly accessible TCP ports.

Evidence:[Nmap scan](Evidence/Nmap output)

results: the scan found no open TCP ports. All 1000 scanned ports were filtered, indicating firewall or network filtering controls.


OWASP ZAP passive scan:

purpose: identify security configuration u=issues without attacking the website.

Evidence: [ OWSAP ZAP] (evidence/ zap-request-responce & zap_alert-details)

results: the passive scan identified missing HTTP security hearders, including content security policy (CSP) and strict-transport-security (HSTS) along with other low-risk configuration issues.
