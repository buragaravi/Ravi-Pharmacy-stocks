# Advanced Lab Inventory Management System

A comprehensive inventory management system for laboratory chemicals with role-based access control and advanced features.

## System Overview

The system manages laboratory chemical inventory with four distinct roles:
- Faculty
- Lab Assistant
- Central Lab Admin
- Admin

### Key Features

#### Faculty Features
- Create and manage chemical requests for experiments
- View experiment history and suggested chemicals
- Track request status in real-time
- Download request details and reports
- View notifications for request updates
- Update or delete pending requests

#### Lab Assistant Features
- Review and process faculty requests
- Handle partial fulfillment scenarios
- Manage lab-specific chemical inventory
- Track chemical stock levels
- Process chemical allocations
- View and manage lab-specific requests

#### Central Lab Admin Features
- Manage chemical master inventory
- Allocate chemicals to labs
- Monitor stock levels across labs
- Generate and manage quotations
- Access comprehensive analytics
- Manage chemical master data

#### Admin Features
- User management and role assignment
- System-wide configuration
- Access to all features
- Advanced analytics and reporting
- Audit logging and monitoring

- Downloadable PDF/Excel reports for requests and inventory
- Vendor management and budget tracking
- Regulatory compliance and lab safety protocols
- Team collaboration and communication tools
- Batch processing and expiry alerts
- API integration for external systems/ERPs

### Technical Architecture

#### Backend (Node.js/Express)
- RESTful API architecture
- MongoDB database with Mongoose ODM
- JWT-based authentication
- Role-based middleware
- Transaction logging
- Notification system
- Batch processing capabilities

#### Frontend (React)
- Modern React with hooks
- Role-specific dashboards
- Real-time updates
- Responsive Material-UI design
- Form validation
- Error handling
- Toast notifications

### Core Modules

#### Request Management
- Create, update, and delete requests
- Track request status (pending, approved, rejected, fulfilled, completed)
- Partial fulfillment handling
- Chemical allocation tracking
- Request history and analytics

#### Chemical Management
- Chemical master data management
- Lab-specific stock tracking
- Batch processing
- Stock level monitoring
- Chemical allocation
- Usage analytics

#### User Management
- Role-based access control
- User authentication
- Password management
- Profile management
- Activity logging

#### Notification System
- Real-time request updates
- Status change notifications
- System alerts
- Email notifications (if configured)

#### Quotation Management
- Create, review, and approve quotations
- Vendor and price management
- Status tracking (draft, pending, approved, purchased, allocated)
- Remarks and comments for chemicals
- Integration with chemical master and inventory

#### Transaction Management
- Track all stock movements (entry, issue, allocation, transfer)
- Transaction history and reporting
- Audit logging

### Data Models

#### ChemicalMaster
- Central repository for chemical data
- Batch information
- Supplier details
- Safety information
- Usage guidelines

#### ChemicalLive
- Lab-specific stock levels
- Real-time quantity tracking
- Allocation history
- Transaction records

#### Request
- Experiment details
- Chemical requirements
- Status tracking
- Allocation history
- Fulfillment records

#### Quotation
- Vendor details
- List of chemicals, quantities, prices
- Status tracking (draft, pending, approved, purchased, allocated)
- Comments and remarks
- Linked to user and lab

#### Transaction
- Chemical, quantity, unit, type (entry, issue, allocation, transfer)
- Source and destination labs
- User who performed the transaction
- Timestamped for audit

### Security Features
- JWT-based authentication
- Role-based access control
- Input validation
- Request sanitization
- Audit logging
- Secure password handling

### Analytics & Reporting
- Chemical usage patterns
- Stock level monitoring
- Request fulfillment rates
- Lab-wise analytics
- User activity tracking
- System performance metrics

### API & Integration
- RESTful API endpoints for all modules
- Supports integration with external laboratory management and ERP systems

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (v4.4 or higher)
- npm/yarn

### Installation
1. Clone the repository
2. Install dependencies:
   ```bash
   # Backend
   cd pharmacy-backend
   npm install
   
   # Frontend
   cd pharmacy-frontend
   npm install
   ```
3. Configure environment variables:
   - Create `.env` file in backend directory
   - Set required environment variables
4. Start the servers:
   ```bash
   # Backend
   cd pharmacy-backend
   npm start
   
   # Frontend
   cd pharmacy-frontend
   npm start
   ```

### Environment Variables
Required environment variables for backend:
```
PORT=5000
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
NODE_ENV=development
```

## API Documentation
The API documentation is available at `/api-docs` when running the backend server.

### Support
For support, contact:
- Email: support@pharmacylab.com
- Phone: (123) 456-7890

### FAQ
**Q: How secure is the platform?**
A: The platform uses industry-standard encryption, regular security audits, and complies with data protection regulations.

**Q: Can I integrate it with existing systems?**
A: Yes, robust API integration is supported for most laboratory and ERP systems.

**Q: What kind of support do you offer?**
A: 24/7 technical support, documentation, video tutorials, and dedicated account managers for enterprise clients.

## Contributing
Please read CONTRIBUTING.md for details on our code of conduct and the process for submitting pull requests.

## License
This project is licensed under the MIT License - see the LICENSE.md file for details