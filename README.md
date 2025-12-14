# GymBoy - Blockchain-Enabled Fitness Platform

A gamified fitness application that combines blockchain technology with AI-powered pose estimation to deliver real-time exercise feedback and NFT-based rewards for consistent workout habits.

## Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [System Architecture](#system-architecture)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Smart Contracts](#smart-contracts)
- [Contributing](#contributing)
- [License](#license)

## Overview

GymBoy is an innovative fitness platform that merges blockchain technology with TensorFlow-based pose estimation to create a comprehensive workout tracking and motivation system. The platform analyzes exercise form in real-time using computer vision, maintains detailed workout histories, and implements an NFT-based reward mechanism to gamify fitness achievements.

The system addresses proper exercise form maintenance through pose detection algorithms while leveraging Ethereum blockchain to create a unique incentive structure. Users can collect and develop virtual gear NFTs that unlock real-world fitness rewards, encouraging consistent exercise habits and proper technique.

## Key Features

### AI-Powered Pose Detection
Leverages TensorFlow.js and PoseNet models for real-time human pose estimation during workouts. The system tracks three core exercises:
- **Bicep Curls** - Monitors arm positioning and movement range
- **Push-ups** - Analyzes body alignment and form
- **Squats** - Evaluates posture and depth

Each exercise session records count and accuracy metrics to provide detailed performance feedback.

### Gamified NFT Gear System
Users collect and develop virtual fitness gear NFTs with unique characteristics:
- **Gear Categories**: Hair, tops, bottoms, and shoes with varying rarity levels
- **Experience System**: Gears gain experience based on workout completion and quality
- **Lucky Attributes**: Random multipliers (1.0x - 1.5x) affect reward progression
- **Customization**: Pixel editor for personalizing gear appearance
- **Rarity Tiers**: Regular, Advanced, High-tech, and Epic items with different drop rates

### Dual Orientation Training System
NFTs are categorized into two training orientations:
- **Health-Oriented NFTs** (Hair & Tops): Focus on consistent exercise habits with 14-day goal periods
- **Workout-Oriented NFTs** (Bottoms & Shoes): Emphasize intensive training with 7-day goal periods

Each orientation has tailored workout requirements and experience thresholds.

### Reward Redemption System
Fully developed NFTs can be exchanged for real-world fitness rewards:
- Partner brand coupons and discounts
- Fitness equipment and supplements
- Premium gym memberships
- Achievement-based rewards through smart contracts

### Comprehensive Progress Tracking
- Detailed exercise history with timestamp and accuracy records
- Weekly task system monitoring workout frequency
- Performance analytics and trend visualization
- Personal achievement milestones

## Technology Stack

### Backend
- **Django 4.2.3**: RESTful API framework and business logic
- **Django REST Framework**: API development with JWT authentication
- **SQLite**: Development database (production-ready for MySQL migration)
- **SIWE (Sign-In with Ethereum)**: Wallet-based authentication
- **Web3.py 6.6.1**: Ethereum blockchain interaction
- **Django CORS Headers**: Cross-origin resource sharing

### Frontend
- **React 18.2.0**: Component-based UI framework
- **React Router 6.14.0**: Client-side routing
- **Wagmi & Web3Modal**: Ethereum wallet connection and management
- **Ethers.js 6.6.7**: Ethereum library for smart contract interaction
- **Bootstrap 5.3.0**: Responsive UI components
- **Chart.js 4.4.0**: Data visualization for exercise analytics
- **Webpack 5**: Module bundler and build tool

### Machine Learning
- **TensorFlow.js**: Browser-based pose estimation
- **@tensorflow-models/pose-detection 2.1.2**: Pre-trained pose models
- **@tensorflow-models/posenet**: Real-time human pose tracking

### Blockchain
- **Ethereum**: NFT storage and smart contract execution
- **Web3 1.8.2**: Blockchain communication
- **MetaMask Integration**: Wallet management

### Additional Tools
- **Firebase**: Push notifications and cloud messaging
- **Axios**: HTTP client for API requests
- **NES UI React**: Retro gaming-style UI components

## System Architecture

The platform consists of four integrated layers:

### 1. Frontend Layer (React SPA)
- **Wallet Connection**: Web3Modal integration for MetaMask authentication
- **Exercise Interface**: Real-time camera feed with TensorFlow.js pose overlay
- **NFT Marketplace**: Browse, purchase, and manage gear collections
- **User Dashboard**: Profile management, workout history, and reward tracking
- **Pixel Editor**: Custom gear design tool

### 2. Backend API (Django REST)
- **Authentication**: JWT-based sessions with SIWE verification
- **User Management**: Account registration and profile handling
- **Gear Management**: NFT metadata, experience tracking, and ownership
- **Exercise Tracking**: Workout session recording and analytics
- **Reward System**: Coupon generation and redemption logic

### 3. Machine Learning Pipeline
- **Pose Detection**: Browser-based TensorFlow.js processing
- **Exercise Recognition**: Pattern matching for bicep curls, push-ups, squats
- **Accuracy Calculation**: Form quality assessment algorithms
- **Real-time Feedback**: Live posture correction guidance

### 4. Blockchain Layer
- **Smart Contracts**: NFT minting, transfers, and ownership verification
- **Wallet Integration**: Ethereum account connection via wagmi/ethers.js
- **Event Listening**: Backend listeners for blockchain events
- **NFT Metadata**: On-chain/off-chain data synchronization

## Project Structure

```
Information_Management_Capstone_Project/
├── client/                          # React frontend application
│   ├── public/                      # Static assets
│   ├── src/
│   │   ├── assets/                  # Images, fonts, gear icons
│   │   ├── components/              # React components
│   │   │   ├── PixelEditor/         # NFT customization tool
│   │   │   ├── WearCollect.js       # Gear collection display
│   │   │   └── translation.js       # i18n utilities
│   │   ├── contracts/               # Smart contract ABIs
│   │   ├── pages/                   # Route components
│   │   │   ├── Home.jsx
│   │   │   ├── Market.jsx
│   │   │   ├── Bag.jsx
│   │   │   ├── ExerciseRealtime.jsx
│   │   │   └── Profile.jsx
│   │   ├── providers/               # Context providers
│   │   └── App.jsx                  # Main application
│   ├── package.json
│   └── webpack.config.js
│
└── server/                          # Django backend application
    ├── accounts/                    # User authentication
    │   ├── models.py                # User model
    │   ├── views.py                 # Auth endpoints
    │   ├── backends.py              # SIWE authentication
    │   └── management/commands/     # Blockchain event listeners
    ├── api/                         # Core API logic
    │   ├── models.py                # Gear, Exercise, Thing, Wear models
    │   ├── views.py                 # API endpoints
    │   ├── serializers.py           # Data serialization
    │   └── utils/ethereum.py        # Web3 integration
    ├── dream/                       # Django project settings
    │   ├── settings.py
    │   └── urls.py
    ├── requirements.txt
    └── manage.py
```

## Getting Started

### Prerequisites
- **Python 3.8+**: Backend runtime environment
- **Node.js 14+**: Frontend build tools
- **MetaMask**: Browser extension for Ethereum wallet
- **Git**: Version control
- **Camera**: Webcam for pose detection exercises

### Installation

#### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/Information_Management_Capstone_Project.git
cd Information_Management_Capstone_Project
```

#### 2. Backend Setup
```bash
cd server

# Install Python dependencies
pip install -r requirements.txt

# Create environment file
# Create a .env file and add your Ethereum private key
echo "PRIVATE_KEY=your_ethereum_private_key" > .env

# Run database migrations
python manage.py migrate

# Create superuser (optional)
python manage.py createsuperuser

# Start Django development server
python manage.py runserver
```

The backend API will be available at `http://localhost:8000`

#### 3. Frontend Setup
```bash
cd client

# Install Node dependencies
npm install

# Start Webpack development server
npm start
```

The frontend application will be available at `http://localhost:8080`

### Configuration

#### Backend Configuration ([server/dream/settings.py](server/dream/settings.py))
```python
# Update for production deployment
DEBUG = False
SECRET_KEY = 'your-secret-key'
ALLOWED_HOSTS = ['your-domain.com']

# Configure database (currently SQLite)
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}

# Update API URL in server/api/models.py line 112
uri = f"http://your-domain.com:8000/api/gears/{self.token_id}"
```

#### Frontend Configuration
- Update smart contract addresses in [client/src/contracts/WearContract.js](client/src/contracts/WearContract.js)
- Configure Web3Modal project ID for wallet connection
- Update API endpoints if deploying to custom domain

#### Blockchain Setup
1. Deploy NFT smart contracts to Ethereum (mainnet/testnet)
2. Update contract addresses and ABIs in frontend
3. Fund deployer wallet with ETH for gas fees
4. Configure event listeners in `server/accounts/management/commands/listenEvent.py`

## Usage

### 1. Wallet Connection
- Open the application in a browser with MetaMask installed
- Click "Connect Wallet" and approve the connection
- Sign the SIWE message to authenticate your account

### 2. Profile Setup
- Complete your user profile with username and personal information
- View your wallet address and account details

### 3. Marketplace & NFT Purchase
- Browse available gear NFTs in the marketplace
- Purchase gear items using Ethereum (varies by rarity)
- View newly acquired items in your bag/collection

### 4. Gear Management
- Select target gear to train and develop
- Equip gear items (hair, top, bottom, shoes) to your avatar
- Customize gear appearance using the pixel editor
- Monitor experience progress toward goal thresholds

### 5. Exercise Sessions
- Choose from bicep curls, push-ups, or squats
- Grant camera permissions for pose detection
- Follow on-screen posture guidance in real-time
- Complete exercises to earn experience for equipped/targeted gear
- View session results showing count and accuracy

### 6. Progress Tracking
- Review exercise history with timestamps and performance data
- Track weekly workout completion goals
- Monitor gear experience and development
- Analyze workout trends and improvements

### 7. Reward Redemption
- Access fully developed gear NFTs (100% experience)
- Exchange NFTs for partner coupons (Adidas, Nike, etc.)
- View redemption history and coupon details
- Use QR codes or unique coupon codes at partner locations

## API Documentation

### Authentication Endpoints
- `POST /accounts/nonce/` - Request SIWE nonce
- `POST /accounts/verify/` - Verify signed message and login
- `POST /accounts/register/` - Register new user
- `GET /accounts/profile/` - Get user profile

### Gear Endpoints
- `GET /api/gears/` - List user's gear collection
- `GET /api/gears/{token_id}/` - Get gear details and metadata
- `POST /api/gears/target/` - Set target gear for training
- `POST /api/gears/dress/` - Equip gear to avatar
- `POST /api/gears/exchange/` - Redeem gear for coupon

### Exercise Endpoints
- `POST /api/exercises/` - Record exercise session
- `GET /api/exercises/history/` - Get workout history
- `GET /api/exercises/stats/` - Get performance analytics

### Marketplace Endpoints
- `GET /api/market/` - List available gear for purchase
- `POST /api/market/purchase/` - Purchase gear NFT

## Smart Contracts

### Gear NFT Contract
The platform uses ERC-721 compatible smart contracts for NFT management:

**Key Functions:**
- `mint(address to, uint256 tokenId)` - Mint new gear NFT
- `transfer(address to, uint256 tokenId)` - Transfer ownership
- `tokenURI(uint256 tokenId)` - Get metadata URI
- Event emission for ownership changes tracked by backend

**Metadata Structure:**
```json
{
  "name": "Gear #123",
  "description": "Fitness gear NFT",
  "image": "ipfs://...",
  "attributes": [
    {"trait_type": "Type", "value": "top"},
    {"trait_type": "Level", "value": "intermediate"},
    {"trait_type": "Lucky", "value": 1.25},
    {"trait_type": "Experience", "value": 450.0}
  ]
}
```

## Database Models

### Core Models
- **User**: Ethereum address-based authentication
- **Gear**: NFT metadata, experience, lucky multiplier, customization
- **Exercise**: Workout records with type, count, accuracy, timestamp
- **Thing**: Consumable items (dumbbells, protein, energy drinks)
- **Wear**: Avatar equipment configuration
- **WeekTask**: Weekly exercise goal tracking

## Contributing

This is an academic capstone project. Contributions, issues, and feature requests are welcome for educational purposes.

### Development Guidelines
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is developed for academic purposes as part of an Information Management capstone program. All rights reserved.

## Acknowledgments

- TensorFlow.js and PoseNet teams for pose estimation models
- Ethereum and Web3 communities for blockchain infrastructure
- Django and React communities for framework support
- NES UI React for retro gaming aesthetic components

## Contact & Support

For questions, issues, or collaboration inquiries:
- Open an issue in the GitHub repository
- Contact the development team through academic channels

---

**Note**: This is a prototype/academic project. For production deployment, ensure proper security audits, smart contract testing, and infrastructure hardening.