# OPA Server Agent – Sample Configuration

This repository contains a sample configuration file for `sftd`, the [Okta Privileged Access](https://help.okta.com/oie/en-us/content/topics/privileged-access/pam-overview.htm) Server Agent.

## Usage

1. Copy `sftd.sample.yaml` to `/etc/sft/sftd.yaml` on your server.
2. Uncomment and set any options you need.
3. Restart the `sftd` service to apply changes.

```bash
sudo cp sftd.sample.yaml /etc/sft/sftd.yaml
sudo systemctl restart sftd
```

## Comment Convention

The file uses a two-tier comment style:

| Prefix | Meaning |
|--------|---------|
| `##` | Description or section header — for reference only |
| `#key: value` | Disabled option — uncomment to enable |

**Example:**
```yaml
## Automatically enrolls the server on initial startup.
#AutoEnroll: true
```

## Configuration Sections

| Section | Description |
|---------|-------------|
| Enrollment Options | Controls how the server agent enrolls with the OPA platform |
| Log Options | Controls log verbosity |
| Connection Options | Network settings, proxies, SSH configuration |
| Access Broker Options | Access broker ports and behavior |
| Domain Controller Options | Account management overrides for domain controllers |
| Labels | Custom key:value metadata for access control and targeting |

## Reference

Full documentation for all options:
https://help.okta.com/oie/en-us/content/topics/privileged-access/server-agent/pam-configure-server-agent.htm
