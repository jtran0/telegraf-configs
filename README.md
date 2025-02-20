# Overview

Configuration files for Telegraf 1.33.1

# Getting Started

1. Install Telegraf to `/opt/telegraf`

```bash
cd /opt
git clone https://github.com/jtran0/telegraf-configs.git
```

2. Download and install the Telegraf executable into `/opt/telegraf`

```bash
cd /tmp
wget https://dl.influxdata.com/telegraf/releases/telegraf-1.33.1_linux_amd64.tar.gz
tar xf ./telegraf-1.33.1_linux_amd64.tar.gz
cp /tmp/telegraf-1.33.1/usr/bin/telegraf /opt/telegraf/usr/bin
```

3. Configure Telegraf to startup on boot by configuring it as a systemd service

```bash
sudo cp /opt/telegraf/usr/lib/telegraf/scripts/telegraf.service /etc/systemd/system
sudo systemctl enable telegraf
```

4. Run Telegraf

```bash
sudo systemctl start telegraf

# Confirm it's running
systemctl status telegraf
```

5. (Optional) Observe its logs

```bash
journalctl -u telegraf -f
```
