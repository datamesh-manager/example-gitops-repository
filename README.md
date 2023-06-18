# example-gitops-repository
Think of this as a repository which holds all the configuration to configure the the [Data Mesh Manager](https://www.datamesh-manager.com/) via GitHub Actions for a single domain team or a whole organization.

Teams, their operational systems and data products can just be put in their specific folders:

```
├── dataproducts
│   ├── shelf_warmers.yml
│   └── stock_updated.yml
├── operationalsystems
│   └── stock_service.yml
└── teams
    └── fulfillment.yml
```
Technically, all example configurations are transformed to json with yq and sent to the Data Mesh Manager with curl.

## GitHub
You can find the GitHub Action configuration [here](.github/workflows/push-to-dmm-action.yml).
The API key of the data mesh manager of the corresponding organization has be to set as a repository variable named `DMM_API_KEY`.

## GitLab
You can find the GitLab CI configuration [here](.gitlab-ci.yml).
The API key of the data mesh manager of the corresponding organization has be to set as a repository variable named `GITOPS_EXAMPLE_API_KEY`.
