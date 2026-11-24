# Smart India Hackathon Workshop
# Date:
## Reference Number:
## Name:

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

## Problem Creater's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description

Farmers often sell produce through several intermediaries before it reaches consumers. Each intermediary adds a margin, which can reduce farmers’ earnings and raise the final price paid by consumers. The challenge is to connect farmers and Farmer Producer Organizations (FPOs) directly with consumers and bulk buyers, while providing dependable logistics and better demand information.


## Proposed Solution
FarmDirect is a digital marketplace that helps farmers and FPOs list available produce and sell directly to households, retailers, restaurants, and institutional buyers. Buyers can compare produce by variety, grade, quantity, location, price, and harvest or delivery date, then place orders through the platform.

The platform groups nearby orders and connects sellers with local transport providers, collection points, and cold-storage options where available. Order tracking and digital receipts make the movement of produce and payments easier to follow. A demand forecasting module uses past orders, seasonal patterns, and current listings to estimate demand and help farmers plan quantities and harvest timing. Route planning groups deliveries to reduce travel distance, delays, and spoilage.

FarmDirect addresses the problem by giving farmers access to more buyers and transparent price information, while buyers can source produce with fewer intermediary markups. Its distinguishing feature is combining direct discovery and ordering with local logistics coordination and practical demand forecasts in one workflow. The service is designed to complement existing FPOs and local markets rather than require farmers to work alone.



## Technical Approach

 **User interfaces:** Responsive web application for farmers, FPOs, buyers, and logistics partners; a lightweight mobile-friendly experience for low-bandwidth areas.
- **Application services:** REST API built with Python (FastAPI) or Node.js, with role-based access for sellers, buyers, and logistics partners.
- **Data storage:** PostgreSQL for users, listings, orders, and delivery records; object storage for produce photos and documents.
- **Marketplace workflow:** Seller registration and listing → buyer search and order → order confirmation → pickup and delivery assignment → status updates and payment record → feedback.
- **Forecasting:** Start with interpretable time-series and regression models using historical orders, seasonality, local prices, and listing data. Show forecast ranges and confidence so farmers can use them as guidance, not guarantees.
- **Route optimization:** Group deliveries by location and time window, then use a routing solver or mapping service to suggest efficient routes. Allow manual adjustment for road, vehicle, and produce-handling constraints.
- **Trust and safety:** Verify seller and buyer profiles through appropriate local processes, show clear units and grading details, retain order histories, and provide a dispute and support channel.
- **Prototype plan:** Build a pilot for one crop and one local market area; test listing, ordering, order aggregation, delivery assignment, and a basic demand dashboard before expanding.

## Feasibility and Viability

The solution can be prototyped with widely used web frameworks, a relational database, and existing mapping services. A pilot can begin with one FPO, a small group of farmers, a few local buyers, and a limited delivery area, which keeps onboarding and logistics manageable.

Key challenges include uneven internet access, limited digital familiarity, variable produce quality, unreliable supply estimates, delivery coordination, and buyer or seller trust. The platform can address these through assisted onboarding by FPO staff, a mobile-friendly low-data interface, local-language support, standardized listing fields, clear grading and cancellation rules, and manual support during the pilot. Forecasts should be introduced only after enough reliable order history is available, and should be displayed with uncertainty. Logistics can begin with partner coordination and grouped orders before investing in dedicated infrastructure.

Potential operating models include a small transparent transaction fee, subscriptions for larger buyers, or service partnerships with FPOs and logistics providers. The pilot should measure farmer net realization, buyer price, fulfillment rate, delivery cost, and spoilage before deciding which model is sustainable.

## Impact and Benefits

**For farmers and FPOs:** Access to a broader set of buyers, improved price visibility, potential for better net returns, and demand information to support production and sale planning.
- **For consumers and bulk buyers:** Easier discovery of local produce, clearer quality and price details, and the possibility of lower costs through more direct sourcing.
- **For the supply chain:** Better coordination of pickup and delivery, improved traceability of orders, and fewer avoidable delays.
- **For the environment and community:** Grouped deliveries and better matching of supply with demand may reduce unnecessary trips and food loss. These benefits should be measured during the pilot rather than assumed.


## Research and References
1. Ministry of Consumer Affairs, Food & Public Distribution — problem statement SIH 26033: “Multiple intermediaries reduce farmers earnings and increase consumer prices.” Smart India Hackathon workshop reference repository: https://github.com/selvasachein/SIH-26033
2. Food and Agriculture Organization of the United Nations (FAO) — Digital solutions and e-commerce in agriculture: https://www.fao.org/e-agriculture/
3. Food and Agriculture Organization of the United Nations (FAO) — Food loss and food waste: https://www.fao.org/food-loss-and-food-waste/
4. Government of India, Ministry of Agriculture & Farmers Welfare — e-NAM, National Agriculture Market: https://www.enam.gov.in/
