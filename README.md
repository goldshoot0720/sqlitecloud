# SQLiteCloud scheduled exports

This repository combines two GitHub Actions workflows that export data from a
SQLiteCloud database:

- **Food**: queries the `food` table every five hours and uploads `food.json`.
- **Subscription**: queries the `subscription` table every six hours and uploads
  `subscription.json`.

## Configuration

Add a repository secret named `SQLITECLOUD_URL` containing the connection URL
for the SQLiteCloud database.

Both workflows can also be started manually from the Actions tab. Each run
uploads the exported JSON file as a workflow artifact.
