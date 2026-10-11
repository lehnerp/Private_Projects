# Private Projects
Projects that are (and will be) private by their nature.

1) Agregated Advanced Monitoring System of Technological Background
   
   An aggregated system for monitoring values, equipment states, and alerts across HVAC, air conditioning, ESS, lighting, and energy systems, primarily for diagnostic purposes.
   Some components support or previously supported long-term monitoring through an API → Zabbix → Grafana pipeline.
   Others use Python Flask dashboards with scraping, source-specific parsers, and graphical views.
   The consolidated application runs from a single Python file and provides one local-network dashboard with separate sections for each watcher.
   Each watcher preserves its own endpoints, polling intervals, data mappings, and alert rules, while similar alarm watchers share common logic.
   Monitoring includes environmental measurements, diagnostic signals, BMS alarm lifecycles, and selected access-control events, with selected values forwarded to ThingSpeak.
   Alerts are delivered through a shared SMTP relay as modern HTML emails with plain-text fallbacks.
   After three consecutive failures, the affected endpoint pauses for 24 hours before retrying automatically, while other endpoints continue monitoring.
   The dashboard displays alarms, observations, endpoint health, email statistics, and pause or retry times.
   Persistent state supports event tracking and reduces duplicate notifications, while endpoint pause timers reset when the application restarts.


3) Nearby Events Alert System
   Monitoring of nearby incidents, alerting if in nearby radius.

4) The Entra Analysis Suite

   It monitors Microsoft Entra ID sign-ins on tenants. It reads the Entra admin center's Sign-in logs in and shows the results on local dashboards. The Watcher collects foreign sign-ins, scores each one for risk, sends privacy-safe e-mail alerts and provides investigation, map and case views. The IP Hunter takes suspicious IP addresses from the watcher and checks each one in Entra for successful or password-valid sign-ins. The User Hunter does the same for accounts that were tried from several countries in the last week. Both hunters query Entra rate each target from "Quiet" to "Compromise likely", and e-mail you when a seriously compromised target signs in successfully from abroad. Each program has its own database, and the hunters feed each other the IPs and accounts they find compromised. Both hunters also offer a world map and a link view that shows which IPs are tied together by shared accounts and which accounts share the same IPs.
