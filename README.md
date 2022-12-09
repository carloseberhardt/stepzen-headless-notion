# StepZen Headless Notion

This is a StepZen schema to create a GraphQL API on top of the Notion API for the purpose of using Notion as a headless CMS.

## Getting Started
In order to use this schema with your Notion account, you will need to create a Notion Integration and get your API key. Learn more about Notion Integrations [here](https://developers.notion.com/docs/getting-started).

It is important to follow steps 2 and 3 in the [guide](https://developers.notion.com/docs/create-a-notion-integration#step-2-share-a-database-with-your-integration) to share a database with your integration, and save the database ID.

Once you have your Notion API key and database ID, create a `.env` file in the root of this project and add the following:

```
STEPZEN_NOTION_KEY=your-notion-api-key
STEPZEN_NOTION_DB_ID=your-database-id
```

The schema is designed to look for a Checkbox property in your Notion database called `published`. This is not required but is recommended. If you wish to use other properties, you will need to adjust the schema to match your database. Look at the `Properties` type in the schema to see which properties are currently supported.

## Deploying to StepZen
The config.yaml file is already set up to use the `.env` file for environment variables. You can deploy this schema to StepZen by running the following command:

```
stepzen start
```
