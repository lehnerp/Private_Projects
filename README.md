# Private Projects

Projects that are—and will remain—private by their nature.

## 1. Aggregated Advanced Monitoring System of Technological Background

An aggregated system for monitoring values, equipment states, and alerts across HVAC, air conditioning, ESS, lighting, and energy systems, primarily for diagnostic purposes.

**Monitoring and dashboards**

Some components support, or previously supported, long-term monitoring through an **API → Zabbix → Grafana** pipeline. Others use Python Flask dashboards with scraping, source-specific parsers, and graphical views.

The consolidated application runs from a single Python file and provides one local-network dashboard with separate sections for each watcher. Each watcher preserves its own endpoints, polling intervals, data mappings, and alert rules, while similar alarm watchers share common logic.

**Data and alerts**

Monitoring includes environmental measurements, diagnostic signals, alarm lifecycles, and selected access-control events. Selected values are forwarded to ThingSpeak.

Alerts are delivered through a shared SMTP relay as modern HTML emails with plain-text fallbacks.

**Reliability and persistent state**

After three consecutive failures, the affected endpoint pauses for 24 hours before retrying automatically, while other endpoints continue monitoring.

The dashboard displays alarms, observations, endpoint health, email statistics, and pause or retry times. Persistent state supports event tracking and reduces duplicate notifications, while endpoint pause timers reset when the application restarts.

## 2. Nearby Events Alert System

A system that helps users stay informed about emergency incidents in a selected region. It reduces the need for manual checking and supports awareness of local emergencies.

**Monitoring and alerts**

The system regularly checks public incident information published by the fire and rescue service. Users can focus alerts on selected towns, neighbourhoods, or streets.

Email notifications highlight new incidents in those areas. Each notification summarises the incident and its reported location.

**Dashboard and overview**

A web dashboard brings current incidents and their history together in one place. Search and filters help users find relevant information quickly.

Maps and charts provide an overview of incident locations and activity. Users can mark incidents as reviewed, close them, or reopen them as needed.

## 3. The Entra Analysis Suite

A suite that monitors Microsoft Entra ID sign-ins across tenants. It reads sign-in logs from the Entra admin center and displays the results on local dashboards.

**The Watcher**

Collects foreign sign-ins, scores each one for risk, sends privacy-safe email alerts, and provides investigation, map, and case views.

**The IP Hunter**

Takes suspicious IP addresses from the Watcher and checks each one in Entra for successful or password-valid sign-ins.

**The User Hunter**

Performs the same checks for accounts that were tried from several countries during the previous week.

**Risk assessment and alerts**

Both hunters query Entra and rate each target from **“Quiet”** to **“Compromise likely.”** They send email alerts when a seriously compromised target signs in successfully from abroad.

**Databases and investigation views**

Each program has its own database. The hunters exchange the IP addresses and accounts they identify as compromised.

Both hunters also offer:

- A world map.
- A link view showing which IP addresses are connected through shared accounts and which accounts share the same IP addresses.
