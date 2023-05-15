## Introduction to Stream Payment Plugins:

#### Receive payments on your Medusa applications using StreamPay.

Stream Payment Plugins offer a seamless solution for receiving payments on your Medusa application, specifically designed for integration with popular platforms like Medusa, WooCommerce (WordPress), Shopify, Magento, and Prestashop. With StreamPay, you can streamline your payment processes and provide a convenient and secure payment experience for your customers.

By integrating StreamPay into your Medusa application, you can offer a wide range of payment options to your customers, including traditional methods like credit cards, as well as emerging payment technologies like cryptocurrencies. This flexibility enables you to cater to a broader customer base and adapt to evolving payment trends.

Whether you're using Medusa Stream web3 Payments Plugins provide a seamless integration experience. You can easily configure and customize the plugins to match your specific business requirements, ensuring a seamless and consistent payment experience across your entire platform.

Stream Payment Plugins simplify the payment process by handling the necessary authentication, communication, and transaction management with the StreamPay payment system. This integration ensures that payment data is securely transmitted, processed, and validated, giving you and your customers peace of mind.

By leveraging StreamPay's robust features, such as real-time payment tracking, automatic order updates, and comprehensive reporting, you can gain valuable insights into your payment operations and streamline your business processes. With Stream Medusa Commerce Payment Plugin, you can focus on growing your business while StreamPay takes care of your payment needs.

Start accepting payments seamlessly on your Medusa e-commerce application with Stream Payment Plugins and empower your business with secure, flexible, and convenient payment solutions.

### Web3 payment features: 

Solana offers a range of powerful web3 features that enable StreamPay developers to build decentralized applications (dApps) and interact with the Solana blockchain. Here are some key web3 features provided by Solana:

Smart Contracts: Solana supports smart contracts through its programming language called "Rust." Developers can write and deploy smart contracts on the Solana blockchain, enabling the execution of decentralized applications and the automation of various operations.

Solana Web3 Libraries: Solana provides web3 libraries that simplify the interaction with the Solana blockchain. These libraries, such as SolanaJS and Anchor, offer APIs and tooling to connect to Solana nodes, sign transactions, deploy contracts, and interact with on-chain data.

Scalability and High Throughput: Solana is known for its high scalability and throughput. With its unique consensus mechanism called "Proof of History" (PoH), Solana can process thousands of transactions per second, making it suitable for high-performance decentralized applications.

Token Standards: Solana supports various token standards, including SPL (Solana Program Library) tokens. These standards allow developers to create and manage different types of tokens, such as fungible tokens (like cryptocurrencies) or non-fungible tokens (like digital collectibles).

Cross-Chain Interoperability: Solana aims to provide cross-chain interoperability, allowing assets and data to be transferred between different blockchains. Through projects like Wormhole, Solana enables the bridging of assets between Solana and other blockchains, expanding the possibilities for decentralized finance (DeFi) and cross-chain applications.

Wallet Integration: Solana integrates with web3 wallets, enabling users to interact with dApps and manage their Solana-based assets securely. Popular wallets like Sollet, Solflare, and Phantom provide seamless integration with the Solana blockchain, allowing users to send/receive transactions, stake tokens, and participate in governance activities.

Oracles and Decentralized Data Feeds: Solana supports the integration of oracles and decentralized data feeds. Oracles provide off-chain data to on-chain smart contracts, enabling dApps to access real-world information and make informed decisions based on external data sources.

These web3 features make Solana a robust blockchain platform for building decentralized applications with high performance, scalability, and interoperability. Developers can leverage Solana's capabilities to create innovative solutions, ranging from DeFi protocols and NFT marketplaces to gaming platforms and more.

## Creating and developing the "medusa-payment-streampay" plugin:

1. Plugin Creation: Start by creating a new plugin for Medusa called "medusa-payment-streampay." This plugin will handle the integration of StreamPay as a payment method within the Medusa platform.

2. Plugin Architecture: Design the plugin architecture, ensuring it follows the best practices and guidelines for Medusa plugin development. Consider the necessary components, such as payment gateways, configurations, and API interactions with StreamPay.

3. StreamPay Integration: Integrate the StreamPay payment system into the plugin. This includes establishing the necessary connections, authentication, and communication channels between Medusa and StreamPay's API.

4. Payment Configuration: Implement the configuration options for the "medusa-payment-streampay" plugin within the Medusa platform. This allows users to set up their StreamPay account credentials, configure payment settings, and customize the payment experience.

5. Payment Processing: Develop the functionality to handle payment processing using StreamPay. This involves capturing payment details, initiating payment requests, and handling callbacks and responses from StreamPay to update order statuses in the Medusa platform.

6. Error Handling: Implement error handling mechanisms to gracefully manage any issues or exceptions that may arise during payment processing. This ensures a smooth and reliable payment experience for users.

7. Testing and Quality Assurance: Conduct rigorous testing of the "medusa-payment-streampay" plugin to verify its functionality, compatibility, and security. Test various payment scenarios, error conditions, and edge cases to ensure the plugin performs as expected.

8. Documentation and Integration Guide: Create comprehensive documentation and integration guides that provide instructions on how to install, configure, and use the "medusa-payment-streampay" plugin within the Medusa platform. This helps users understand the setup process and utilize the plugin effectively.

9. Support and Maintenance: Offer ongoing support and maintenance for the "medusa-payment-streampay" plugin. Address user inquiries, bug reports, and feature requests to ensure the plugin remains up-to-date and compatible with future versions of Medusa.


### By creating and developing the "medusa-payment-streampay" plugin

By creating and developing the "medusa-payment-streampay" plugin, you enable seamless integration of StreamPay as a payment method within the Medusa platform, enhancing the payment options available to users and expanding the platform's capabilities.

#### Plugin name: medusa-payment-streampay

Receive payments on your Medusa commerce application using StreamPay.

How to Create a Plugin

In this document, you’ll learn how to create a plugin and some tips for development. If you’re interested to learn more about what plugins are and where to find available official and community plugins, check out the overview document.

### Develop, ToDo´s and Features:

1. Authorize payments on orders from any sales channel.
2. Support for SolanaPay, SEPA, Stripe, PayPal, ApplePay etc.
3. Capture payments from the admin "StreamPay" dashboard.
4. View payment analytics through StreamPay's dashboard.
5. Ready integration with Medusa's Next.js starter storefront.
6. Support for StreamPay Webhooks.

### Prerequisites

Medusa backend

StreamPay account

How to Install

Run the following command in the directory of the Medusa backend:

npm install medusa-payment-streampay


#### 2. Set the following environment variables in .env:

STREAMPAY_API_KEY=sk_...
# only necessary for production
STREAMPAY_WEBHOOK_SECRET=strm_...

In medusa-config.js add the following at the end of the plugins array:

const plugins = [
  // ...
  {
    resolve: `medusa-payment-streampay`,
    options: {
      api_key: process.env.STREAMPAY_API_KEY,
      webhook_secret: process.env.STREAMPAY_WEBHOOK_SECRET,
    },
  },
]

#### Test the Plugin

Run the following command in the directory of the Medusa backend to run the backend:

npm run start

Enable StreamPay in a region in the admin. You can refer to 

this User Guide to learn how to do that. Alternatively, you can use the Admin APIs.

Place an order using a storefront or the 

Store APIs. You should be able to use StreamPay as a payment method.
