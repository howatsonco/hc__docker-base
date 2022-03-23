# Base Docker Images

This docker houses a bunch of base images - those taking a long time to build especially for `arm64` cross architectural build.

Currently there are two Base Containers:

`php8_node16__arm64`:
- PHP 8.0 FPM on Debian.
- Node 16 (for SSR rendering in the same container).
- Nginx (for built-in reverse proxying - container can be served immediately).
- Composer.
- WP-CLI.

Mounts:
- Web path is mounted on `/var/www/html`.

`node-lts__arm64`:
- Node LTS (tracking the latest `node-lts-slim` image).
- Yarn and pnpm package managers for different project types.
- AWS CLI

Mounts:

- Suggested app path is mounted on `/app`.