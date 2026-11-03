# firewall_simulator
# Network Traffic & Firewall Rule Simulator

A lightweight Python simulation that models deterministic packet inspection and rule-based traffic filtering for a localized subnet (`192.168.1.0/24`). This project demonstrates core networking logic, packet triage, and pseudo-random network event simulation.

## 🚀 Features

- **Dynamic IP Generation:** Simulates incoming host traffic within a dedicated local IP range.
- **Rule-Based Triage:** Map-based firewall lookup matrix that instantaneously identifies and intercepts blacklisted IP addresses.
- **Traffic Logging:** Outputs real-time evaluation logs showing the origin IP, the enforced policy (`allow` or `block`), and a generated payload tracking ID.

## 🛠️ How It Works

1. **Firewall Rules Matrix:** The script initializes with a predefined dictionary mapping specific malicious or restricted IP addresses to a `block` state.
2. **Simulation Loop:** It spins up a traffic cycle modeling successive packet hits.
3. **Default-Allow Policy:** If an incoming IP address doesn't explicitly match a strict block rule, the traffic safely defaults to an `allow` status.

## 📋 Prerequisites

To run this script, you only need Python installed on your system (Python 3.x is recommended). No external libraries or dependencies are required.

```bash
python --version
```

## 💻 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com
cd YOUR_REPOSITORY_NAME
```

### 2. Run the script
```bash
python firewall_simulator.py
```

## 📊 Sample Output

```text
IP: 192.168.1.4, Action: block, Random: 4821
IP: 192.168.1.12, Action: allow, Random: 843
IP: 192.168.1.19, Action: block, Random: 7721
IP: 192.168.1.1, Action: block, Random: 1045
IP: 192.168.1.15, Action: allow, Random: 9231
```

## ⚖️ License
This project is open-source and available under the [MIT License](LICENSE).
