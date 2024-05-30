# ZBX-Draytek

## Overview
This repository contains a Zabbix template for monitoring Draytek routers and firewalls. 

## Requirements
- Zabbix 4.0 or higher
- Draytek router/firewall

## How to Use

### On Zabbix

1. **Import the zbx-draytek Template:**
   - Download the `zbx-draytek` template file from this repository.
   - Log in to your Zabbix server.
   - Navigate to `Configuration` > `Templates`.
   - Click on `Import` in the upper right corner.
   - Select the `zbx-draytek` template file and import it.

2. **Create a New Host:**
   - Navigate to `Configuration` > `Hosts`.
   - Click on `Create host`.
   - Fill in the host details, including the `Host name` and `Visible name`.
   - Under `Interfaces`, add an SNMP interface with the IP address or DNS name of your Draytek device.

3. **Link the Template:**
   - While still in the host configuration, navigate to the `Templates` tab.
   - Click on `Add` and select the `zbx-draytek` template from the list.

4. **Set the SNMP Community Macro:**
   - Navigate to the `Macros` tab within the host configuration.
   - Click on `Add`.
   - Set the macro `{$SNMP_COMMUNITY}` with the value of your desired community string (default is `public`).

5. **Save the Host Configuration:**
   - Click `Add` to save the new host configuration.

### On Draytek

1. **Enable SNMP:**
   - Log in to your Draytek router/firewall's web interface.
   - Navigate to the SNMP settings section (usually found under `System Maintenance` or `Management`).
   - Enable SNMP.

2. **Set the SNMP Community String:**
   - Set the community string to match the one you configured in the Zabbix macro (default is `public`).

## Support

For issues or feature requests, please open an issue on the GitHub repository. 

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contributing

We welcome contributions! Please see the `CONTRIBUTING.md` file for more details.

## Authors

- [Arnold Musembi](https://github.com/AnoldMusembi)

---

By following these steps, you will have successfully set up monitoring for your Draytek router/firewall using Zabbix. If you encounter any issues or have further questions, feel free to reach out via the issues section on GitHub.
