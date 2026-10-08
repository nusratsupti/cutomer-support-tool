# Customer Support & Call Center Platform

A modern, full-featured customer support and call center application built for efficiency and scalability. This platform enables organizations to manage customer interactions through multiple channels including phone calls, SMS, and support tickets with comprehensive role-based access control.

## 🎯 Business Overview

### Purpose
This application provides a comprehensive solution for customer support operations, enabling teams to handle customer inquiries efficiently through integrated communication channels and robust ticket management systems.

### Key Features
- **Multi-Channel Communication**: Handle customer interactions via phone calls, SMS, and support tickets
- **Role-Based Access Control**: Three-tier permission system (Agent, Supervisor, Manager)
- **Real-Time Call Management**: Integrated Twilio-powered calling with call logging and status tracking
- **Ticket Management System**: Full-featured ticketing with priority levels, status tracking, and assignment workflows
- **Agent Performance Tracking**: Monitor agent availability, call times, and productivity metrics
- **SLA Management**: Track and monitor service level agreements with automated escalations
- **Real-Time Dashboard**: Live updates on ticket status, agent availability, and performance metrics

### Target Users
- **Agents**: Front-line support representatives handling customer interactions
- **Supervisors**: Team leads monitoring agent performance and managing workload distribution
- **Managers**: Senior leadership overseeing overall support operations and analytics

### Business Benefits
- Improved customer response times through efficient ticket routing
- Enhanced agent productivity with integrated communication tools
- Better visibility into support operations with real-time metrics
- Scalable architecture supporting growing support teams
- Compliance-ready with comprehensive audit trails

## 🏗️ Technical Architecture

### Technology Stack
- **Frontend**: React 18 with TypeScript
- **Build Tool**: Vite
- **UI Framework**: Tailwind CSS with shadcn/ui components
- **State Management**: React Context API with custom hooks
- **Backend**: Supabase (PostgreSQL database, Edge Functions, Authentication)
- **Communication**: Twilio API for voice and SMS
- **Real-Time**: Supabase Realtime subscriptions
- **Routing**: React Router DOM v6

### Core Dependencies
```json
{
  "react": "^18.3.1",
  "@supabase/supabase-js": "^2.52.1",
  "@tanstack/react-query": "^5.56.2",
  "react-router-dom": "^6.26.2",
  "tailwindcss": "latest",
  "typescript": "latest"
}
```

### Database Schema
The application uses Supabase PostgreSQL with the following key tables:
- `profiles`: User profile information and role assignments
- `tickets`: Customer support tickets with status, priority, and assignment
- `call_logs`: Call history and recordings with Twilio integration
- `agent_sessions`: Agent availability and performance tracking
- `agent_status`: Real-time agent availability status

### Security Features
- Row Level Security (RLS) policies for data isolation
- JWT-based authentication via Supabase Auth
- Role-based access control with granular permissions
- Secure API endpoints with proper authorization checks

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ and npm
- Supabase account and project
- Twilio account for communication features (optional for basic functionality)

### Installation

1. **Clone the repository**
   ```bash
   git clone <YOUR_GIT_URL>
   cd <YOUR_PROJECT_NAME>
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   The application uses Supabase for backend services. Configuration is handled automatically through the integrated Supabase client.

4. **Database Setup**
   - The database schema is automatically managed through Supabase migrations
   - All tables, functions, and policies are version-controlled in the `supabase/migrations/` directory

5. **Start Development Server**
   ```bash
   npm run dev
   ```

### Configuration

#### Twilio Integration (Optional)
For full communication features, configure Twilio secrets in your Supabase project:
- `TWILIO_ACCOUNT_SID`: Your Twilio Account SID
- `TWILIO_AUTH_TOKEN`: Your Twilio Auth Token  
- `TWILIO_PHONE_NUMBER`: Your Twilio phone number

#### User Roles
The system supports three user roles with different permissions:
- **Agent**: Can view and manage assigned tickets, make calls, send SMS
- **Supervisor**: Agent permissions + team management and performance monitoring
- **Manager**: Full system access including analytics and system configuration

## 📁 Project Structure

```
src/
├── components/
│   ├── auth/              # Authentication components
│   ├── call/              # Call and SMS interfaces
│   ├── dashboard/         # Dashboard and analytics
│   ├── layout/            # Layout components (navbar, etc.)
│   ├── support/           # Ticket management components
│   └── ui/                # Reusable UI components (shadcn/ui)
├── contexts/              # React Context providers
├── hooks/                 # Custom React hooks
├── pages/                 # Page components
├── services/              # Business logic and API services
└── lib/                   # Utilities and configurations

supabase/
├── functions/             # Edge Functions for Twilio integration
├── migrations/            # Database schema and migrations
└── config.toml           # Supabase configuration
```

## 🔧 Development

### Available Scripts
- `npm run dev`: Start development server
- `npm run build`: Build for production
- `npm run preview`: Preview production build locally
- `npm run lint`: Run ESLint

### Code Style
- TypeScript strict mode enabled
- ESLint configuration for React and TypeScript
- Tailwind CSS with semantic design tokens
- Component-based architecture with custom hooks

### Database Migrations
Database changes are managed through Supabase migrations:
- All schema changes are version-controlled
- Automatic deployment through Supabase CLI
- RLS policies ensure data security

## 🚀 Deployment

### Production Deployment
1. **Using Lovable**: Click the Publish button in the Lovable editor
2. **Manual Deployment**: 
   - Build the project: `npm run build`
   - Deploy the `dist` folder to your hosting platform
   - Ensure Supabase project is configured for production

### Custom Domain
Connect a custom domain through:
1. Project Settings → Domains in Lovable
2. Configure DNS records as instructed
3. SSL certificates are automatically provisioned

## 📊 Monitoring & Analytics

### Built-in Metrics
- Agent performance tracking (call duration, ticket resolution time)
- Real-time dashboard with live updates
- SLA compliance monitoring
- Customer satisfaction tracking

### Logging
- All user actions are logged for audit purposes
- Call logs include duration, outcome, and recordings
- Ticket history maintains complete interaction timeline

## 🔒 Security & Compliance

### Data Protection
- Row Level Security (RLS) ensures users only access authorized data
- All sensitive data encrypted at rest
- Audit trails for all user actions

### Authentication
- Secure JWT-based authentication
- Password policies enforced
- Multi-factor authentication support (via Supabase Auth)

## 🆘 Support & Documentation

### Getting Help
- **Lovable Community**: [Discord Server](https://discord.com/channels/1119885301872070706/1280461670979993613)
- **Documentation**: [Lovable Docs](https://docs.lovable.dev/)
- **Video Tutorials**: [YouTube Playlist](https://www.youtube.com/watch?v=9KHLTZaJcR8&list=PLbVHz4urQBZkJiAWdG8HWoJTdgEysigIO)

### Project Information
- **Lovable Project URL**: https://lovable.dev/projects/82c65cc6-bdf8-49d9-9e1c-1caaab52a3ce
- **Version**: 1.0.0
- **License**: MIT

### Contributing
1. Create feature branches from `main`
2. Follow existing code style and conventions
3. Ensure all tests pass before submitting
4. Document any new features or changes

---

Built with ❤️ using [Lovable](https://lovable.dev)
