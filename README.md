**# Camunda and Keycloak with MS SQL Server Integration**

**This project demonstrates how to:**

- Set up Camunda and Keycloak in a Docker Compose environment
- Integrate Camunda authentication with Keycloak
- Connect Camunda to an MS SQL Server database for data persistence
- Import realms and users into Keycloak

**## Quick Start:**

1. **Build and start the containers:**

   ```bash
   docker compose build
   docker compose up -d
   ```

2. **Access Camunda:**

   - Open `http://localhost:8085` in your browser.
   - Login with username `camunda` and password `camunda1!`.
   - Use Cockpit, Tasklist, and Admin tools.

3. **Access Keycloak:**

   - Open `https://localhost:9001/auth` in your browser.
   - Login with username `admin` and password `admin`.

4. **Configure admin-cli client:**

   - Navigate to `master realm > clients > admin-cli > settings`.
   - Enable client authentication and check the service account roles checkbox.
   - Assign the `create-user` role to the admin-cli client in `service account roles`.

**## Export:**
  ```bash
   docker exec -it keycloak_container /bin/sh
   /opt/keycloak/bin/kc.sh export --dir /opt/keycloak/data/import
   ```

**## Key Features:**

- **Docker Compose setup:** Easy deployment and management of containers.
- **Camunda and Keycloak integration:** Secure authentication for Camunda.
- **MS SQL Server database:** Data persistence for Camunda processes and tasks.
- **Realm and user import:** Streamlined setup for Keycloak.

**## Contributing:**

- Fork the repository on GitHub.
- Create a branch for your changes.
- Submit a pull request.

**## License:**

- This project is licensed under the MIT License.

**## Additional Information:**

- Camunda documentation: https://community.camunda.com/
- Keycloak documentation: https://www.keycloak.org/community
- MS SQL Server documentation: https://learn.microsoft.com/en-us/sql/connect/jdbc/understanding-xa-transactions?view=sql-server-ver16

**## Acknowledgements:**

- Camunda community: https://community.camunda.com/
- Keycloak community: https://www.keycloak.org/community
- Microsoft: https://learn.microsoft.com/en-us/sql/connect/jdbc/understanding-xa-transactions?view=sql-server-ver16
