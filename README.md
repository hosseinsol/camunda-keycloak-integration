Usage:

1. `docker compose build`
2. `docker compose up -d`
3. Login at `http://localhost:8085` using `camunda` / `camunda1!` and use Cockpit / Tasklist / Admin.
4. Keycloak is available under `https://localhost:9001/auth`. Login with `admin` / `admin`.
5. In master realm > clients > admin-cli > settings ,enable client authentication and check service account roles checkbox
6. In master realm > clients > admin-cli > service account roles , assign roles , assign create-user role to admin-cli client
