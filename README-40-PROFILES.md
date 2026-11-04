# Super JinX: 40 subscription profiles

This edition retains the original Xray inbounds, Nginx routing, and database logic. It expands `METHODS` in `enforce_hosts.py` from 12 to 40 host profiles. These are **not 40 independent servers or inbounds**; multiple profiles share a transport and endpoint.

## Deploy
1. Back up the Railway volume and environment variables before replacing a running deployment.
2. Upload the repository contents to your own GitHub repository and connect that repository to Railway.
3. Keep the existing persistent volume mounted at `/var/lib/marzban` when migrating the service.
4. After deployment, inspect application logs and check the subscription link for 40 direct profiles (plus any configured relay, mirror, or Cloudflare routes).
5. Test connectivity on client applications. Some fingerprint and fragmentation variants may behave identically or be unsupported on particular clients.

The original project may regenerate settings at startup. Do not paste this code into the Marzban Core Settings editor.

Validation performed: Python syntax and JSON parsing; live Railway deployment and subscription functionality have not been tested.
