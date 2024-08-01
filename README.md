# Sanity-Nahla

![Sanity](https://img.shields.io/badge/Sanity-000000?style=for-the-badge&logo=sanity&logoColor=white)

## Overview

Sanity-Nahla is a content management system (CMS) built using Sanity.io, designed to manage and deploy content for the Nahla Naturals website. The CMS provides a structured and efficient way to handle content, enabling seamless updates and management of website data.

## Features

- **Content Management**: Create, update, and manage website content effortlessly.
- **Structured Content**: Organize content with a defined schema for consistency.
- **Plugins**: Utilize Sanity plugins for extended functionality, including vision tool for real-time data inspection.

## Technologies Used

- ![Sanity](https://img.shields.io/badge/Sanity-000000?style=for-the-badge&logo=sanity&logoColor=white)
- ![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
- ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
- ![Yarn](https://img.shields.io/badge/Yarn-2C8EBB?style=for-the-badge&logo=yarn&logoColor=white)

## Installation

### Prerequisites

- Node.js
- Yarn

### Steps

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/randy-kip/sanity-nahla.git
    cd sanity-nahla
    ```

2. **Install Dependencies**:
    ```bash
    yarn install
    ```

3. **Set Up Environment Variables**:
   Create a `.env` file in the root directory and add the following:
    ```plaintext
    SANITY_PROJECT_ID=your_project_id
    SANITY_DATASET=production
    ```

## Usage

### Running the Development Server

To start the development server, run:
```bash
yarn start
```
This will run Sanity Studio locally, allowing you to manage content from a local environment.

### Building for Production

To build the project for production, run:
```bash
yarn build
```

### Deploying

To deploy the project, run:
```bash
sanity deploy
```
This will deploy the Sanity Studio to the configured Sanity project.

## Configuration

### sanity.cli.js
```javascript
import { defineCliConfig } from 'sanity/cli'

export default defineCliConfig({
  api: {
    projectId: 'your-project-id',
    dataset: 'production'
  }
})
```

### sanity.config.js
```javascript
import { defineConfig } from 'sanity'
import { structureTool } from 'sanity/structure'
import { visionTool } from '@sanity/vision'
import { schemaTypes } from './schemaTypes'

export default defineConfig({
  name: 'default',
  title: 'your-sanity-title',

  projectId: 'your-project-id',
  dataset: 'production',

  plugins: [structureTool(), visionTool()],

  schema: {
    types: schemaTypes,
  },
})
```

## Deployment

### Deploying to Sanity

To deploy the Sanity Studio to Sanity.io:
1. Ensure you are logged into Sanity:
    ```bash
    sanity login
    ```

2. Deploy the Studio:
    ```bash
    sanity deploy
    ```

### Running in Production

To run the project in production, ensure you have built the project and then run:
```bash
yarn serve
```

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes. Ensure your code adheres to the existing style and add tests for any new features or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/randy-kip/sanity-nahla/blob/main/LICENSE.md) file for details.

<br>

---

By following this README file, you should be able to set up, run, and deploy the `sanity-nahla` project with ease. If you encounter any issues, please refer to the documentation or raise an issue on the repository.

<br>

# Sanity Clean Content Studio

For more information on the Sanity Content Studio, an open source real-time content editing environment connected to the Sanity backend, see the following:

- [Read “getting started” in the docs](https://www.sanity.io/docs/introduction/getting-started?utm_source=readme)
- [Join the community Slack](https://slack.sanity.io/?utm_source=readme)
- [Extend and build plugins](https://www.sanity.io/docs/content-studio/extending?utm_source=readme)
