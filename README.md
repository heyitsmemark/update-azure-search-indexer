# `update-azure-search-indexer` GitHub Action

This repository contains an action for use with GitHub Actions, which updates an existing Indexer within an Azure Cognitive Search instance.

> :information_source: This action can be used to both create or update indexers.

## Usage

Update an indexer using a local definition file:

```yaml
- name: Update indexer
  uses: heyitsmemark/update-azure-search-indexer@1.0.0
  with:
    azureSearchInstance: plop
    azureSearchAdminKey: ${{ secrets.AZURE_SEARCH_ADMIN_KEY }}
    indexerName: indexer-plop
    indexerDefinitionFile: ./path/to/indexer.json
```

Update an indexer using a remote definition file:

```yaml
- name: Update indexer 
  uses: heyitsmemark/update-azure-search-indexer@1.0.0
  with:
    azureSearchInstance: plop
    azureSearchAdminKey: ${{ secrets.AZURE_SEARCH_ADMIN_KEY }}
    indexerName: indexer-plop
    indexerDefinitionUri: https://domain.com/path/to/indexer.json
```

## Samples

Sample workflows are available [here](.github/workflows/)