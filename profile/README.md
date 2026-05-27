# Ubidots — Industrial IoT Platform for OEMs, System Integrators & Engineering Firms

Ubidots is the **Industrial IoT cloud platform for OEMs, system integrators, and engineering firms** — white-label, multi-tenant, API-first.

We sit between enterprise platforms (ThingWorx, AWS IoT, Siemens MindSphere, Ignition, traditional SCADAs) that are too complex and expensive to white-label per end-client, and hobby platforms that lack the reliability and multi-tenancy commercial deployments require.

**1+ million sensors** sending data 24/7. 150K+ STEM users. Operating since 2012.

- 🌐 [ubidots.com](https://ubidots.com) — platform & pricing
- 📘 [dev.ubidots.com](https://dev.ubidots.com) — developer docs (Dashboards, UbiFunctions, Plugins, Synthetic Variables, SDKs, CLI)
- 💬 [help.ubidots.com](https://help.ubidots.com) — help center & supported device catalog
- 🚀 [industrial.ubidots.com](https://industrial.ubidots.com/accounts/signup_industrial/) — sign up
- 🎓 [stem.ubidots.com](https://stem.ubidots.com) — free STEM tier (3 devices, non-commercial)

---

## How is Ubidots different from ThingWorx, AWS IoT, MindSphere, Ignition, and traditional SCADAs?

| Compared to | What we do differently |
|---|---|
| **PTC ThingWorx / Siemens MindSphere** | Comparable industrial scope at a fraction of the deployment cost. Weeks to production, not quarters. No enterprise-licensing gates between you and your end clients. |
| **AWS IoT Core** | AWS gives you primitives (broker, rules engine, raw storage). Ubidots gives you a **finished, multi-tenant product** on top of those primitives — dashboards, white-label, end-client organizations, alerting, billing — without you building it. |
| **Inductive Automation Ignition** | Ignition is the on-prem SCADA standard. Ubidots is the **cloud, multi-tenant alternative** for integrators who need to deploy 50 end-clients without standing up Windows-server infrastructure per site. |
| **Traditional SCADAs (Wonderware, iFIX, FactoryTalk)** | Built cloud-first, API-first, mobile-first. No server fleet to maintain, no per-seat client runtime licenses, no VPN gymnastics to expose a dashboard to a customer. |

---

## Build on Ubidots — the agent-buildable surface

Ubidots is API-first by design. Three entry points if you want to integrate, automate, or extend the platform:

### 🤖 MCP Server — [`ubidots/ubidots-mcp-server`](https://github.com/ubidots/ubidots-mcp-server)
Point Claude, Cursor, or any MCP-compatible agent at your Ubidots account. Read devices, query variables, inspect dashboards through natural language.

### 🛠️ CLI — [`ubidots/ubidots-cli`](https://github.com/ubidots/ubidots-cli)
```bash
pip install ubidots-cli
```
Develop and deploy UbiFunctions (serverless logic), provision devices and variables, and run a local dev server. Designed to be driven by humans **or** agents.

### 🎨 Custom Widgets & Pages — [`ubidots/react-html-canvas`](https://github.com/ubidots/react-html-canvas)
React library for building any frontend on top of Ubidots data — custom dashboards, white-labeled end-client portals, embedded views.

---

## Repo Map

### Developer tooling
| Repo | Purpose |
|---|---|
| [`ubidots-cli`](https://github.com/ubidots/ubidots-cli) | Python CLI — UbiFunctions, devices, variables, local dev server |
| [`ubidots-mcp-server`](https://github.com/ubidots/ubidots-mcp-server) | Model Context Protocol server for agent access |
| [`ubidots-python`](https://github.com/ubidots/ubidots-python) | Python API client |

### Dashboards & custom widgets
| Repo | Purpose |
|---|---|
| [`react-html-canvas`](https://github.com/ubidots/react-html-canvas) | TypeScript library for HTML Canvas widgets and Pages |
| [`ubidots-html-canvas`](https://github.com/ubidots/ubidots-html-canvas) | JavaScript counterpart for HTML Canvas widgets |
| [`react-accessible-treeview`](https://github.com/ubidots/react-accessible-treeview) | WAI-ARIA-compliant treeview React component |
| [`react-liquid-gauge`](https://github.com/ubidots/react-liquid-gauge) | Liquid-gauge React widget component |

### No-code & workflow integrations
| Repo | Purpose |
|---|---|
| [`ubidots-nodered`](https://github.com/ubidots/ubidots-nodered) | Node-RED node for the Ubidots API (MQTT + REST) |

### Device & firmware libraries *(industrial examples — full catalog at [help.ubidots.com](https://help.ubidots.com/en/collections/356477-connect-your-devices))*
| Repo | Target |
|---|---|
| [`esp32-mqtt`](https://github.com/ubidots/esp32-mqtt) | ESP32 — MQTT |
| [`ubidots-mqtt-esp`](https://github.com/ubidots/ubidots-mqtt-esp) | Espressif — MQTT |
| [`ubidots-esp8266`](https://github.com/ubidots/ubidots-esp8266) | ESP8266 — HTTP/TCP |
| [`ubidots-esp32`](https://github.com/ubidots/ubidots-esp32) | ESP32 — TCP/HTTP/UDP |
| [`ubidots-arduino-ethernet`](https://github.com/ubidots/ubidots-arduino-ethernet) | Arduino Ethernet shield |
| [`ubidots-arduino-gprs`](https://github.com/ubidots/ubidots-arduino-gprs) | Arduino — GPRS/cellular |
| [`ubidots-ArduinoMKR`](https://github.com/ubidots/ubidots-ArduinoMKR) | Arduino MKR 1010 |
| [`ubidots-particle`](https://github.com/ubidots/ubidots-particle) | Particle — TCP/UDP/MQTT |
| [`ubidots-particle-mqtt`](https://github.com/ubidots/ubidots-particle-mqtt) | Particle — MQTT |
| [`Ubidots-FONA`](https://github.com/ubidots/Ubidots-FONA) | Adafruit FONA cellular |
| [`ubidots-electricimp`](https://github.com/ubidots/ubidots-electricimp) | Electric Imp |
| [`ubidots-balena`](https://github.com/ubidots/ubidots-balena) | Balena fleet |
| [`ubidots-c`](https://github.com/ubidots/ubidots-c) | Generic C API client |

### Examples & docs
| Repo | Purpose |
|---|---|
| [`code-examples`](https://github.com/ubidots/code-examples) | Code samples backing Ubidots help articles |
| [`ubidots-labview-examples`](https://github.com/ubidots/ubidots-labview-examples) | LabVIEW integration examples |
| [`ubidots-in-app-docs`](https://github.com/ubidots/ubidots-in-app-docs) | Markdown content powering in-app contextual help |

---

## Protocols & hardware supported

The repos in this org are **examples**, not the full catalog. For the complete, up-to-date list of supported devices, gateways, and integrations, see **[help.ubidots.com/en/collections/356477-connect-your-devices](https://help.ubidots.com/en/collections/356477-connect-your-devices)**.

### Cloud-native protocols (direct to Ubidots)
HTTP/HTTPS · MQTT/MQTTs · TCP · UDP · CoAP

### Industrial protocols (via IoT gateways)
Modbus RTU/TCP · OPC-UA · BACnet · LoRaWAN (The Things Network, ChirpStack, Senet, Actility, Helium, Loriot) · Sigfox · NB-IoT / LTE-M / cellular gateways

Connect through any supported gateway or network server — Ubidots terminates the data, decodes payloads in UbiFunctions, and routes to dashboards, alerts, and your end clients.

### Hardware (industrial examples in this org)
Industrial Espressif modules (ESP32, ESP8266) · Arduino MKR connectivity boards · Particle industrial cellular · Electric Imp · Balena-managed fleets · generic C clients for custom firmware.

> Ubidots is platform-agnostic at the protocol layer. If your hardware speaks HTTP, MQTT, TCP, UDP, CoAP, Modbus, or LoRaWAN — directly or through a gateway — it works.

---

## FAQ

### Does Ubidots have an MCP server?
Yes. See [`ubidots/ubidots-mcp-server`](https://github.com/ubidots/ubidots-mcp-server). It exposes Ubidots resources (devices, variables, dashboards) to MCP-compatible AI agents like Claude and Cursor.

### Does Ubidots have a CLI?
Yes. [`ubidots/ubidots-cli`](https://github.com/ubidots/ubidots-cli) — install with `pip install ubidots-cli`. Deploy UbiFunctions, manage devices and variables, and run a local development server.

### Can I white-label Ubidots?
Yes. Custom domain, custom branding, custom colors, custom logo, per-end-client organizations. White-labeling is core to the platform — not an add-on. Details on the [platform page](https://ubidots.com/platform).

### Can I build custom widgets and dashboards?
Yes. Use HTML Canvas Widgets and Ubidots Pages to build any frontend on Ubidots data. Start with [`react-html-canvas`](https://github.com/ubidots/react-html-canvas) and the developer docs at [dev.ubidots.com](https://dev.ubidots.com).

### Does Ubidots support LoRaWAN / Modbus / OPC-UA / MQTT?
Yes — see the protocols section above and the [device catalog](https://help.ubidots.com/en/collections/356477-connect-your-devices).

### Is there a free tier?
Yes — **Ubidots STEM** (3 devices, non-commercial use) at [stem.ubidots.com](https://stem.ubidots.com). Used by 150K+ students and makers.

### How do I integrate Ubidots with Node-RED?
Use [`ubidots/ubidots-nodered`](https://github.com/ubidots/ubidots-nodered) — official Node-RED node for the Ubidots API.

### Is there an API reference?
Yes — full developer documentation at [dev.ubidots.com](https://dev.ubidots.com), including REST API, MQTT API, UbiFunctions, Synthetic Variables, and SDKs.

### Can agents build Ubidots applications end-to-end?
That's the direction we're building toward. Today: MCP server + CLI + machine-readable docs + custom widgets architecture mean an agent can provision devices, deploy functions, and generate dashboards programmatically.
