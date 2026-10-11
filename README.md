AWG Exit Nodes
===

Configure host as AWG server

Sample client
---

```yaml
awg_unmanaged_peers:
  vyatta_nubes:
  public_key: "Cp2Dz1YuAN9sMqtuABYAClgi7UTWR2HauSNdL8ByA2c="
    preshared_key: "openssl rand -base64 32"
    allowed_ips: "{{ awg_network | ansible.utils.ipaddr(1) | ansible.utils.ipaddr('address') }}"
    persistent_keepalive: "25"
    port: 44905
    endpoint: "{{ inventory['vyatta'].ansible_host }}"
```