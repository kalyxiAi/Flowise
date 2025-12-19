<!-- markdownlint-disable MD030 -->

<p align="center">
<img src="https://github.com/kalyxi/kalyxi-flow/blob/main/images/flowise_white.svg#gh-light-mode-only">
<img src="https://github.com/kalyxi/kalyxi-flow/blob/main/images/flowise_dark.svg#gh-dark-mode-only">
</p>

<div align="center">

[![Release Notes](https://img.shields.io/github/release/kalyxi/kalyxi-flow)](https://github.com/kalyxi/kalyxi-flow/releases)
[![GitHub star chart](https://img.shields.io/github/stars/kalyxi/kalyxi-flow?style=social)](https://star-history.com/#kalyxi/kalyxi-flow)
[![GitHub fork](https://img.shields.io/github/forks/kalyxi/kalyxi-flow?style=social)](https://github.com/kalyxi/kalyxi-flow/fork)

</div>

<h3>Build AI Agents, Visually</h3>
<a href="https://github.com/kalyxi/kalyxi-flow">
<img width="100%" src="https://github.com/kalyxi/kalyxi-flow/blob/main/images/flowise_agentflow.gif?raw=true"></a>

## 📚 Table of Contents

-   [⚡ Quick Start](#-quick-start)
-   [🐳 Docker](#-docker)
-   [👨‍💻 Developers](#-developers)
-   [🌱 Env Variables](#-env-variables)
-   [📖 Documentation](#-documentation)
-   [🌐 Self Host](#-self-host)
-   [☁️ Kalyxi Cloud](#️-kalyxi-cloud)
-   [🙋 Support](#-support)
-   [🙌 Contributing](#-contributing)
-   [📄 License](#-license)

## ⚡Quick Start

Download and Install [NodeJS](https://nodejs.org/en/download) >= 18.15.0

1. Install Kalyxi Flow
    ```bash
    npm install -g kalyxi-flow
    ```
2. Start Kalyxi Flow

    ```bash
    npx kalyxi-flow start
    ```

3. Open [http://localhost:3000](http://localhost:3000)

## 🐳 Docker

### Docker Compose

1. Clone the Kalyxi Flow project
2. Go to `docker` folder at the root of the project
3. Copy `.env.example` file, paste it into the same location, and rename to `.env` file
4. `docker compose up -d`
5. Open [http://localhost:3000](http://localhost:3000)
6. You can bring the containers down by `docker compose stop`

### Docker Image

1. Build the image locally:

    ```bash
    docker build --no-cache -t kalyxi-flow .
    ```

2. Run image:

    ```bash
    docker run -d --name kalyxi-flow -p 3000:3000 kalyxi-flow
    ```

3. Stop image:

    ```bash
    docker stop kalyxi-flow
    ```

## 👨‍💻 Developers

Kalyxi Flow has 3 different modules in a single mono repository.

-   `server`: Node backend to serve API logics
-   `ui`: React frontend
-   `components`: Third-party nodes integrations
-   `api-documentation`: Auto-generated swagger-ui API docs from express

### Prerequisite

-   Install [PNPM](https://pnpm.io/installation)
    ```bash
    npm i -g pnpm
    ```

### Setup

1.  Clone the repository:

    ```bash
    git clone https://github.com/kalyxi/kalyxi-flow.git
    ```

2.  Go into repository folder:

    ```bash
    cd kalyxi-flow
    ```

3.  Install all dependencies of all modules:

    ```bash
    pnpm install
    ```

4.  Build all the code:

    ```bash
    pnpm build
    ```

    <details>
    <summary>Exit code 134 (JavaScript heap out of memory)</summary>
    If you get this error when running the above `build` script, try increasing the Node.js heap size and run the script again:

    ```bash
    # macOS / Linux / Git Bash
    export NODE_OPTIONS="--max-old-space-size=4096"

    # Windows PowerShell
    $env:NODE_OPTIONS="--max-old-space-size=4096"

    # Windows CMD
    set NODE_OPTIONS=--max-old-space-size=4096
    ```

    Then run:

    ```bash
    pnpm build
    ```

    </details>

5.  Start the app:

    ```bash
    pnpm start
    ```

    You can now access the app on [http://localhost:3000](http://localhost:3000)

6.  For development build:

    -   Create `.env` file and specify the `VITE_PORT` (refer to `.env.example`) in `packages/ui`
    -   Create `.env` file and specify the `PORT` (refer to `.env.example`) in `packages/server`
    -   Run:

        ```bash
        pnpm dev
        ```

    Any code changes will reload the app automatically on [http://localhost:8080](http://localhost:8080)

## 🌱 Env Variables

Kalyxi Flow supports different environment variables to configure your instance. You can specify the following variables in the `.env` file inside `packages/server` folder. Read [more](https://github.com/kalyxi/kalyxi-flow/blob/main/CONTRIBUTING.md#-env-variables)

## 📖 Documentation

You can view the Kalyxi Flow documentation on our website at [https://kalyxi.ai/docs](https://kalyxi.ai/docs)

## 🌐 Self Host

Deploy Kalyxi Flow self-hosted in your existing infrastructure. We support various deployment options:

-   AWS
-   Azure
-   Digital Ocean
-   GCP
-   Railway
-   Render
-   And more...

Contact us at [support@kalyxi.ai](mailto:support@kalyxi.ai) for deployment assistance.

## ☁️ Kalyxi Cloud

Get Started with [Kalyxi Cloud](https://kalyxi.ai/).

## 🙋 Support

Feel free to ask any questions, raise problems, and request new features in [Discussion](https://github.com/kalyxi/kalyxi-flow/discussions) or contact us at [support@kalyxi.ai](mailto:support@kalyxi.ai).

## 🙌 Contributing

Thanks go to these awesome contributors

<a href="https://github.com/kalyxi/kalyxi-flow/graphs/contributors">
<img src="https://contrib.rocks/image?repo=kalyxi/kalyxi-flow" />
</a><br><br>

See [Contributing Guide](CONTRIBUTING.md).

[![Star History Chart](https://api.star-history.com/svg?repos=kalyxi/kalyxi-flow&type=Timeline)](https://star-history.com/#kalyxi/kalyxi-flow&Date)

## 📄 License

Source code in this repository is made available under the [Apache License Version 2.0](LICENSE.md).
