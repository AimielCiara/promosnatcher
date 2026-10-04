# Promo Snatcher — Coolify demo

This repository serves the public, **saved-case demo** of Promo Snatcher. It replays three researched U.S. event examples and lists U.S. coupon sources. It does not run live ZooWork/Tavily searches or verify codes at checkout. No API keys are included or required.

## Deploy on Coolify

1. Create an application from this GitHub repository: `https://github.com/AimielCiara/promosnatcher`.
2. Select the **Dockerfile** build pack. Use `/` as the base directory and `/Dockerfile` as the Dockerfile location.
3. Set **Ports Exposes** to `8080`, assign a domain (or use Coolify's test domain), and deploy.
4. Open the deployment URL and try the three saved cases. The container health check requests `/` on port `8080`.

The Docker build copies only `dist/` and the Nginx config. If live search is added later, keep ZooWork and Tavily credentials in Coolify runtime secrets, add stronger usage controls before enabling public requests, and never commit keys to Git.
