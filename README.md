# example-gitops-repository
Think of this as a repository which holds all the configuration to configure the the [data mesh manager](https://www.datamesh-manager.com/) via GitHub Actions for a single domain team.

Using this approach, data contracts could be requested by other teams by using pull requests containing new data contract files inside `./datacontracts`.

You can find the GitHub Action configuration [here](.github/workflows/push-to-dmm-action.yml).
Technically, all example configurations are transformed to json with yq and sent to the data mesh manager with curl.

The API key of the data mesh manager of the corresponding organization has be to set as a repository variable named `DMM_API_KEY`.
