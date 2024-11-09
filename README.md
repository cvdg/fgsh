# Traefik with CloudFlare DNS challenge

I got tired of all the bogus HTTPS warnings in my homelab environment.
I also lost track of all the ports in my Docker services.

## CloudFlare DNS Token

CloudFlare -> My Profile -> API Tokens -> Create Token

Custom Token -> {name}

- Permissions:
  - Zone - Zone - Read
  - Zone - DNS  - Edit
- Zone Resources:
  - Include - All Zones
- TTL:
  - Start Date - {today}
  - End Date - {today + 1 year}

Save token as: `./secrets/cf_dns_api_token.secret`
