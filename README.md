# Sara: Creator's Love

Sara: Creator's Love is an AI agent designed to revolutionize digital content monetization by creating a decentralized, self-sovereign economy for creators and traders. By transforming online engagement into tradable tokens, Sara empowers creators to monetize their influence directly—bypassing traditional ad-based revenue models.

---

## Project Overview

Sara monitors YouTube for trending creators and automatically mints unique creator coins based on real-time engagement data. When a creator’s metrics spike, Sara calculates a new token price using a weighted formula and updates the decentralized exchange (DEX) for trading. Verified creators also earn royalties from each trade, ensuring a continuous passive income stream.

---

## Key Features

- **Real-Time YouTube Monitoring**  
  Continuously tracks trending YouTube creators using advanced APIs and scrapers.

- **Automatic Token Minting**  
  Mints a unique creator coin (e.g., `$MRBEAST` for MrBeast) based on real-time engagement metrics such as views, likes, comments, and shares.

- **Dynamic Token Pricing**  
  Calculates the initial token price using a weighted formula:  
  **P = (V × 0.4) + (L × 0.3) + (C × 0.2) + (S × 0.1)**  
  where **V** = views, **L** = likes, **C** = comments, and **S** = shares. Prices are continuously adjusted as engagement changes.

- **Decentralized Trading Platform (DEX)**  
  Users can buy and sell creator tokens on a DEX-like interface where prices reflect live market dynamics.

- **Creator Royalties**  
  When creators verify their accounts, a percentage (e.g., 1% per trade) of every token transaction is automatically directed to them as royalties.

- **Social Integrations**  
  Expands beyond YouTube by integrating with platforms such as Discord, Instagram, Twitter, and YouTube livestreams for comprehensive coin insights.

---

## Architecture & Workflow

1. **Monitoring**  
   Sara continuously scans YouTube for trending creators using APIs and scrapers.

2. **Minting**  
   When a creator’s engagement reaches a defined threshold, Sara mints a new creator coin based on the collected metrics.

3. **Pricing**  
   The token's price is determined using a weighted formula that reflects real-time engagement, ensuring the token value rises or falls according to market demand.

4. **Trading**  
   Users interact with these tokens on our decentralized exchange-like platform, buying or selling based on the current market price.

5. **Royalties**  
   Verified creators automatically receive a set percentage of the token transaction volume, providing them with continuous passive income.

---

## YouTube Engagement Metrics Plugin

A critical component of Sara: Creator's Love is the YouTube Engagement Metrics plugin, which:

- Fetches YouTube engagement data (views, likes, comments, video title, etc.) using the YouTube Data API.
- Processes and formats the data into actionable metrics.
- Exposes an action that Sara can call to update token prices or mint new coins based on the latest data.

The plugin is organized into three main files:

- **action.ts** – Defines the action that fetches and processes YouTube metrics.
- **provider.ts** – Handles API calls to the YouTube Data API (using axios) and parses the response.
- **index.ts** – Initializes the plugin within the Eliza framework and registers the action.

---

## Installation & Setup

1. **Clone the Repository**  
   Clone the project repository to your local machine:

       git clone <repository_url>
       cd yt-metrics-plugin

2. **Install Dependencies**  
   Run the following command to install all required packages:

       npm install

3. **Configure Environment Variables**  
   Create a `.env` file in the project root and add your credentials:

       YT_API_KEY=your_youtube_api_key_here
       YT_VIDEO_ID=default_video_id_here

4. **Build the Plugin**  
   Compile the TypeScript files using:

       npm run build

5. **Run the Plugin**  
   For testing purposes, run:

       npm start

---

## Build Tools & Testing

- **Tsup** is used for bundling the plugin. The tsup configuration specifies entry points, output directory, sourcemap generation, and external dependencies.
- **Vitest** is used for running tests. The vitest configuration sets the testing environment to Node, includes coverage reports, and defines file inclusions/exclusions.
- **TypeScript** ensures type safety and supports modern JavaScript features.

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and add relevant tests.
4. Submit a pull request with a detailed description of your modifications.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

## Acknowledgments

- Thanks to the Eliza framework for providing the foundation for our plugin system.
- Inspiration is drawn from the Coinbase AgentKit plugin architecture.
- Special thanks to the creator community for pushing the boundaries of digital monetization.

---

Sara: Creator's Love isn’t just an AI agent—it’s a movement toward a transparent, creator-first digital economy. Join us in redefining how digital influence is valued and monetized!
