# Information Management Capstone Project

A blockchain-enabled fitness platform that leverages deep learning for real-time exercise posture correction and performance tracking.

## Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [System Architecture](#system-architecture)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview

This capstone project presents an innovative fitness platform that combines blockchain technology with deep learning-based human pose estimation to revolutionize workout quality tracking. The system provides real-time feedback on exercise form, maintains comprehensive workout history, and implements a blockchain-based NFT reward system to enhance user motivation and engagement.

The platform addresses the common challenge of maintaining proper exercise form by leveraging computer vision and pose estimation algorithms to detect and correct postural errors in real-time. By integrating blockchain technology and NFTs, the system creates a unique incentive structure that encourages consistent exercise habits while providing tangible rewards for fitness achievements.

## Key Features

### Real-Time Posture Correction
Utilizing advanced deep learning algorithms for human pose estimation, the platform analyzes user movements during workouts and provides immediate feedback on form and technique. The system detects postural errors in real-time, enabling users to make instant corrections and reduce the risk of injury.

### Comprehensive Exercise History Tracking
The platform maintains detailed logs of all workout sessions, allowing users to:
- Review past exercise performance
- Track progress over time
- Identify patterns and trends in their fitness journey
- Monitor improvements in form and consistency

### Blockchain-Based NFT Integration
Users interact with two categories of NFTs built on the Ethereum blockchain:

- **Fitness-Oriented NFTs**: Guide users through structured exercise routines with specific form requirements
- **Health-Oriented NFTs**: Promote consistent exercise habits and long-term wellness goals

NFTs must be unlocked through the completion of prescribed exercise routines, creating a gamified fitness experience.

### Smart Contract Reward System
Upon reaching specific milestones, fully-developed NFTs can be exchanged for real-world rewards through smart contracts. This feature creates tangible incentives for maintaining proper form and consistent exercise habits.

## Technology Stack

### Backend
- **Django**: Web framework for backend API and business logic
- **MySQL**: Relational database for user data and exercise history

### Frontend
- **React.js**: Modern UI library for responsive and interactive user interface

### Machine Learning
- **TensorFlow**: Deep learning framework for pose estimation and movement analysis

### Blockchain
- **Ethereum**: Blockchain platform for NFT creation and smart contract execution

## System Architecture

The platform consists of four primary components:

1. **Frontend Application**: React-based user interface for workout sessions and data visualization
2. **Backend API**: Django REST framework handling business logic and data management
3. **ML Pipeline**: TensorFlow-based pose estimation system for real-time movement analysis
4. **Blockchain Layer**: Ethereum smart contracts managing NFT lifecycle and reward distribution

## Getting Started

### Prerequisites
- Python 3.8+
- Node.js 14+
- MySQL 8.0+
- MetaMask or compatible Ethereum wallet

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/Information_Management_Capstone_Project.git
cd Information_Management_Capstone_Project

# Backend setup
cd backend
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

# Frontend setup
cd ../frontend
npm install
npm start
```

### Configuration

1. Configure database settings in `backend/settings.py`
2. Set up Ethereum wallet connection in the frontend configuration
3. Configure TensorFlow model paths and parameters

## Usage

1. **Account Creation**: Register and connect your Ethereum wallet
2. **NFT Purchase**: Select and purchase fitness or health-oriented NFTs
3. **Workout Session**: Start a session and follow real-time posture guidance
4. **Progress Tracking**: Review your exercise history and performance metrics
5. **Reward Redemption**: Exchange fully-developed NFTs for real-world rewards

## Contributing

This is a capstone project developed as part of academic requirements. For questions or collaboration inquiries, please open an issue or contact the development team.

## License

This project is developed for academic purposes. Please contact the authors for licensing information.