Ready-running Stack A lab:
- reverse-proxy (nginx)
- seafile
- seadoc
- elasticsearch
- mariadb
- redis

Start:
  docker compose up -d

Open:
  http://localhost/

Admin login:
  admin@example.com
  example-admin-password

Notes:
- This is intended for an isolated local lab only.
- ElasticSearch is included, but depending on the exact Seafile image/build, full-text indexing may still need an in-container Seafile config toggle/reindex after first boot.
- The reverse proxy targets seadoc on port 23333 because that matches the custom image behavior implied by the original compose provided by the user.
