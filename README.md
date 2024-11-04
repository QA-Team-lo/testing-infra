# testing-infra

Infra for testing team's projects.

This is a **MUST DO** for newcomers so please read thoroughly.

Currently we offer:

- x86_64 PVE based VMs/LXC containers
- RISC-V boards access¹
- Jumper host *Lancer*²
- x86_64 TrueNAS SCALE based VMs³
- Tailscale DERP server⁴
- HTTP/HTTPS reverse proxies for downloading files (outside Chinese Mainland, if it's too slow for you)
- Probably more

¹ ² ³ ⁴: hosted by @KevinMX at his home, for all boards here you're force to use *Lancer* as a jumper host. Security reasons, you know.

### Usage / SOP

1. Make sure you've configured a SSH key on GitHub.
2. Fork this repository.
3. Modifiy [user_map.json](./user_map.json), add your username:
    - "username": ["GitHub username"]
    - The CI only checks if you have a valid SSH key added.
4. PR your changes to this repo.
5. `/ping` @KevinMX_Neo on Telegram / @KevinMX_AC on WeChat.
6. Ask for what you need.
6. Wait for the `/pong` and login credentials.
7. Enjoy.

### Rules

- **DO NOT** use weak passwords.
- **DO NOT** expose ports to the internet with out permission.
    - Including things like: Tailscale, ZeroTier, or other similar tools.
    - Use jumper hosts.
- **DO NOT** share/expose login credentials outside testing team. Internal use only.
- Inform @KevinMX if you changed your GitHub username, or create a new PR here.

> We might do network security scans every month. If you have ports exposed to the public internet with weak passwords then good luck with that :)
>
> As for those hosted at my house with LAN access only, I don't really care but PLEASE at least don't screw up my home network.

### Other notes

The PVE host is using 4x SAS HDD RAID-5 setup, so do expect slow IO.

For more notes check pinned messages in the Telegram group.

Any other questions also please ask @KevinMX in the group, or via PM if you think it's necessary.

### Credits

Based on [isrc-cas/tarsier-infra](https://github.com/isrc-cas/tarsier-infra), licensed under Apache-2.0.
