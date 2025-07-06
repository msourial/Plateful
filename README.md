# Plateful: AI-Powered Food Ordering via Telegram & Instagram

Plateful is a full-stack application that allows users to order food through a conversational AI interface on Telegram and Instagram. It features a web-based dashboard for restaurant owners to manage menus, track orders, and view analytics. The platform integrates with the Flow blockchain for a customer loyalty program and supports modern payment solutions.

## ✨ Features

- **Conversational Ordering:** AI-powered bots on Telegram and Instagram guide users through the ordering process.
- **Web Dashboard:** A comprehensive dashboard for restaurant staff to manage operations.
- **Menu Management:** Easily add, update, and remove menu items.
- **Order Tracking:** Real-time order tracking for both customers and staff.
- **Blockchain Loyalty Program:** A customer loyalty token system built on the Flow blockchain.
- **Secure Payments:** Integration with Coinbase Commerce for cryptocurrency payments.
- **User Authentication:** Secure user login for the management dashboard.
- **Responsive UI:** A modern and responsive user interface built with React and shadcn/ui.

## 🛠️ Tech Stack

| Category      | Technology                                                                                                  |
|---------------|-------------------------------------------------------------------------------------------------------------|
| **Frontend**  | [React](https://reactjs.org/), [Vite](https://vitejs.dev/), [TypeScript](https://www.typescriptlang.org/), [Tailwind CSS](https://tailwindcss.com/), [shadcn/ui](https://ui.shadcn.com/) |
| **Backend**   | [Node.js](https://nodejs.org/), [Express.js](https://expressjs.com/), [TypeScript](https://www.typescriptlang.org/)                                      |
| **Database**  | [PostgreSQL](https://www.postgresql.org/) with [Neon](https://neon.tech/), [Drizzle ORM](https://orm.drizzle.team/)                                |
| **AI**        | [OpenAI API](https://openai.com/docs), [Anthropic API](https://www.anthropic.com/)                                                                |
| **Blockchain**| [Flow](https://flow.com/), [Flow Client Library (FCL)](https://docs.onflow.org/fcl/)                                                              |
| **Bots**      | [node-telegram-bot-api](https://github.com/yagop/node-telegram-bot-api)                                       |
| **Payments**  | [Coinbase Commerce](https://commerce.coinbase.com/)                                                               |

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/en/) (v20.x or later)
- [npm](https://www.npmjs.com/)

### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/msourial/Plateful.git
    cd Plateful
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Set up environment variables:**
    Create a `.env` file in the root of the project and populate it with the necessary API keys and configuration details. See the `Environment Variables` section below for a template.

4.  **Push database schema:**
    This command will sync your database schema with the Drizzle ORM definitions.
    ```bash
    npm run db:push
    ```

5.  **Seed the database (optional):**
    If you want to populate your database with initial data, run the seed script.
    ```bash
    npm run db:seed
    ```

### Running the Application

- **Development:**
  To run the application in development mode with hot-reloading:
  ```bash
  npm run dev
  ```

- **Production:**
  To build and run the application for production:
  ```bash
  npm run build
  npm run start
  ```

## 📜 Available Scripts

- `npm run dev`: Starts the development server.
- `npm run build`: Bundles the application for production.
- `npm run start`: Runs the production build.
- `npm run check`: Runs the TypeScript compiler to check for type errors.
- `npm run db:push`: Pushes the Drizzle ORM schema to the database.
- `npm run db:seed`: Seeds the database with initial data.

## 📁 Project Structure

```
.
├── client/         # React frontend application
├── db/             # Drizzle ORM schema and seed scripts
├── server/         # Express.js backend server
│   ├── services/   # Business logic for various integrations (AI, Flow, etc.)
│   ├── telegram/   # Telegram bot logic
│   ├── instagram/  # Instagram bot logic
│   └── index.ts    # Main server entry point
├── shared/         # Shared types and schemas (e.g., Zod schemas)
├── drizzle.config.ts # Drizzle ORM configuration
├── package.json    # Project dependencies and scripts
└── tsconfig.json   # TypeScript configuration
```

## 🔑 Environment Variables

Create a `.env` file in the project root and add the following variables. Replace the placeholder values with your actual credentials.

```env
# Database
DATABASE_URL="your_neon_database_connection_string"

# Telegram Bot
TELEGRAM_BOT_TOKEN="your_telegram_bot_token"

# Instagram (if applicable)
INSTAGRAM_APP_ID="your_instagram_app_id"
INSTAGRAM_APP_SECRET="your_instagram_app_secret"

# AI Services
OPENAI_API_KEY="your_openai_api_key"
ANTHROPIC_API_KEY="your_anthropic_api_key"

# Flow Blockchain
FLOW_ACCESS_NODE="https://rest-testnet.onflow.org"
FLOW_PRIVATE_KEY="your_flow_account_private_key"
FLOW_ACCOUNT_ADDRESS="your_flow_account_address"

# Coinbase Commerce
COINBASE_COMMERCE_API_KEY="your_coinbase_commerce_api_key"

# Session
SESSION_SECRET="a_strong_random_secret_string"
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any bugs or feature requests.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
