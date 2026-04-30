# Student Certificate Verification System

A blockchain-based system for verifying and managing student certificates using Ethereum smart contracts, Ganache, and Node.js. This project provides a secure, transparent, and tamper-proof way to issue, store, and verify academic certificates.

## Features

- 🔐 **Blockchain-Based Verification**: Uses Ethereum smart contracts for immutable certificate storage
- 👨‍🎓 **Student Portal**: Secure login and certificate viewing for students
- 👩‍💼 **Admin Dashboard**: Interface for creating students and issuing certificates
- ✅ **Certificate Verification**: Public verification system with QR codes
- 🔒 **Secure Authentication**: Bcrypt password hashing for user security
- 📱 **Responsive Design**: Mobile-friendly UI with Tailwind CSS
- 🔗 **Web3 Integration**: Direct blockchain interaction using Web3.js

## Tech Stack

- **Backend**: Node.js with Express.js
- **Frontend**: HTML, CSS, JavaScript with Tailwind CSS
- **Blockchain**: Solidity smart contracts, Truffle framework
- **Local Blockchain**: Ganache (local Ethereum simulator)
- **Database**: JSON (student records)
- **Authentication**: Bcrypt for password hashing
- **QR Codes**: QRCode.js for certificate QR generation

## Prerequisites

Before running this project, ensure you have installed:

- [Node.js](https://nodejs.org/) (v14 or higher)
- [npm](https://www.npmjs.com/) or [Yarn](https://yarnpkg.com/)
- [Ganache](https://trufflesuite.com/ganache/) - Ganache CLI or Ganache GUI
- [Truffle](https://trufflesuite.com/truffle/) - Install globally with `npm install -g truffle`

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/student-certificate-verification.git
   cd student-certificate-verification
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Install Ganache CLI** (if not already installed)
   ```bash
   npm install -g ganache-cli
   ```

4. **Install Truffle globally** (if not already installed)
   ```bash
   npm install -g truffle
   ```

## Getting Started

### 1. Start Ganache

Start a local Ethereum blockchain using Ganache:

**Using Ganache CLI:**
```bash
ganache-cli --deterministic
```

**Or using Ganache GUI:**
- Open the Ganache application
- Create a new workspace or use the default one
- Ensure it's running on `127.0.0.1:7545`

### 2. Compile Smart Contracts

```bash
npm run compile
```

This compiles the Solidity contracts and generates the ABI files.

### 3. Deploy Smart Contracts

```bash
npm run migrate
```

This deploys the contracts to your local Ganache blockchain. Keep note of the contract address in the output.

### 4. Start the Server

```bash
npm start
```

For development with automatic restart on file changes:
```bash
npm run dev
```

The server will start on `http://localhost:3000`

## Project Structure

```
├── contracts/                 # Solidity smart contracts
│   └── CreatorChain.sol      # Certificate registry contract
├── migrations/               # Truffle migration scripts
│   └── 1_deploy_contracts.js # Contract deployment
├── public/                   # Frontend files
│   ├── app.js               # Main JavaScript application
│   ├── index.html           # Home page
│   ├── style.css            # Global styles
│   ├── admin/               # Admin dashboard pages
│   ├── student/             # Student portal pages
│   ├── verifier/            # Certificate verification pages
│   ├── assets/              # CSS and JavaScript assets
│   ├── certificates/        # Generated certificate files
│   └── imgs/                # Images and QR codes
├── build/                   # Compiled contracts (generated)
├── server.js                # Express server entry point
├── truffle-config.js        # Truffle configuration
├── package.json             # Project dependencies
└── student_db.json          # Student records storage
```

## Usage

### Admin Dashboard
1. Navigate to `http://localhost:3000/admin/`
2. Create a new student with email and password
3. Issue a certificate by selecting a student and filling in the certificate details
4. The certificate is stored on the blockchain and a QR code is generated

### Student Portal
1. Navigate to `http://localhost:3000/student/`
2. Login with your student credentials
3. View your issued certificates
4. Download or share your certificate verification link

### Public Verification
1. Navigate to `http://localhost:3000/verifier/`
2. Enter a certificate ID or scan the QR code
3. View the certificate details and verification status

## Smart Contract

### CertificateRegistry.sol

The main smart contract that stores and manages certificates:

- **issueCertificate**: Issues a new certificate to a student
- **verifyCertificate**: Verifies the authenticity of a certificate
- **getCertificate**: Retrieves certificate details
- **getCertificateCount**: Gets the total number of certificates

## Configuration

### Environment Variables

Create a `.env` file in the root directory (not included in version control):

```env
# Server configuration
PORT=3000
NODE_ENV=development

# Blockchain configuration
CONTRACT_ADDRESS=0x... # Update with your deployed contract address
```

### Truffle Configuration

The `truffle-config.js` file is pre-configured to connect to Ganache on `127.0.0.1:7545` with Network ID `5777`.

## Available npm Scripts

```bash
npm start          # Start the production server
npm run dev        # Start with Nodemon for development
npm run migrate    # Deploy contracts to blockchain
npm run compile    # Compile Solidity contracts
```

## Development Tips

- Check the browser console for debugging information
- View contract events in the Ganache GUI
- Use the Web3.js console in the browser to interact directly with contracts
- Student data is stored in `student_db.json`

## Security Considerations

⚠️ **This is a demonstration project. For production:**

- Store sensitive data securely (use environment variables and secrets management)
- Implement proper authentication and authorization
- Add input validation and sanitization
- Use HTTPS instead of HTTP
- Implement role-based access control
- Conduct security audits
- Use a real blockchain network with proper gas fee management

## Troubleshooting

### Port Already in Use
If port 3000 is already in use, you can specify a different port:
```bash
PORT=3001 npm start
```

### Ganache Connection Issues
- Ensure Ganache is running on `127.0.0.1:7545`
- Check that the Network ID matches (should be 5777)
- Restart Ganache and redeploy contracts

### Contract Deployment Issues
- Clear the `build/` folder: `rm -rf build/`
- Recompile: `npm run compile`
- Redeploy: `npm run migrate`

### Student DB Corruption
- Delete `student_db.json` to reset student records
- The file will be recreated automatically

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## Support

For support, please open an issue on GitHub or contact the project maintainers.

## Disclaimer

This is a proof-of-concept project for educational purposes. Always verify academic credentials through official channels before making important decisions based on this system.

---

**Last Updated**: 2026
