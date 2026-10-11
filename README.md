# Private Projects
Projects that are (and will be) private by their nature.

1) Agregated Advanced Monitoring System of Technological Background
   Monitoring of values, states, alerts of various things (HVAC, AC, ESS, lights, energy) primarily for diagnostic purposes ...
   Some of them are/were implemented for a long-term monitoring (API (Text, JSON, ...) -> Zabbix -> Grafana), others were based on Python Flask Dashboards with use of scraping, parsers and graphs.

3) Nearby Events Alert System
   Monitoring of nearby incidents, alerting if in nearby radius.

4) The Entra Analysis Suite

   It monitors Microsoft Entra ID sign-ins on tenants. It reads the Entra admin center's Sign-in logs in and shows the results on local dashboards. The Watcher collects foreign sign-ins, scores each one for risk, sends privacy-safe e-mail alerts and provides investigation, map and case views. The IP Hunter takes suspicious IP addresses from the watcher and checks each one in Entra for successful or password-valid sign-ins. The User Hunter does the same for accounts that were tried from several countries in the last week. Both hunters query Entra rate each target from "Quiet" to "Compromise likely", and e-mail you when a seriously compromised target signs in successfully from abroad. Each program has its own database, and the hunters feed each other the IPs and accounts they find compromised. Both hunters also offer a world map and a link view that shows which IPs are tied together by shared accounts and which accounts share the same IPs.
