# CleanMe - Professional Cleaning Service Platform

## 1. Introduction

CleanMe is a modern web application built with Angular that connects clients with professional cleaners. The platform provides a streamlined booking experience, comprehensive dashboard management, and secure user interactions. The application features role-based navigation, dynamic user experiences, and a clean, modern UI built with Tailwind CSS.

## 2. Current Implementation Status

### ✅ **Fully Implemented Features**

- **User Registration & Authentication** – Complete dual-role system (CLIENT/CLEANER)
- **Dynamic Dashboard System** – Role-based dashboard routing and content
- **Cleaner Discovery** – Browse, filter, and search cleaners with advanced filtering
- **Booking System** – Complete reservation workflow with time slot management
- **Review System** – Rate and review cleaners after service completion
- **Favorites Management** – Save and manage favorite cleaners
- **Profile Management** – Comprehensive user and cleaner profile systems
- **Notification System** – Real-time booking updates and notifications
- **Responsive Design** – Mobile-first approach with Tailwind CSS

### 🚧 **Backend Integration Status**

- REST API integration with Spring Boot backend
- Authentication with JWT tokens
- Real-time data synchronization
- Error handling and fallback mechanisms

## 3. Application Architecture

### **Frontend Structure**

```
src/app/
├── core/
│   ├── services/ (auth, booking, reservation, review, etc.)
│   └── models/ (data transfer objects)
├── features/
│   ├── auth/ (login, register, user-info, cleaner-info)
│   ├── dashboard/ (user-dashboard, cleaner-dashboard)
│   ├── user/ (bookings-review, favorites, reviews)
│   ├── cleaner/ (browse-cleaners, cleaner-jobs, cleaner-services)
│   ├── shared-profile/ (profile management)
│   └── notifications/
├── shared/
│   └── components/ (reusable UI components)
└── environments/ (configuration)
```

### **Key Technical Improvements**

- **Component Consolidation**: Moved all reusable components to `shared/components`
- **Consistent Template Structure**: Separated HTML/CSS from TypeScript for maintainability
- **Dynamic Navigation**: Role-based dashboard routing and sidebar generation
- **Clean Codebase**: Removed debugging console logs for production readiness
- **Type Safety**: Comprehensive TypeScript interfaces and models

## 4. User Roles & Dashboards

### **CLIENT Dashboard**

- **Cleaner Discovery**: Browse available cleaners with advanced filtering
- **Booking Management**: View upcoming and past reservations
- **Favorites**: Manage saved cleaners
- **Review System**: Rate completed services
- **Profile Management**: Update personal information

**Navigation Features:**

- Browse Cleaners
- My Bookings
- Favorites
- Reviews
- Profile Settings

### **CLEANER Dashboard**

- **Job Management**: View and manage incoming booking requests
- **Service Configuration**: Set availability, services, and pricing
- **Booking History**: Track completed and ongoing jobs
- **Profile Optimization**: Manage public profile and services
- **Earnings Overview**: Track completed services

**Navigation Features:**

- My Jobs
- Services
- Availability
- Reviews
- Profile Settings

## 5. Core Features Implementation

### **5.1 Authentication System**

- **Registration**: Dual-role registration with toggle (CLIENT/CLEANER)
- **Login**: JWT-based authentication with role detection
- **Post-Registration**: Cleaner-specific onboarding flow
- **Role-based Routing**: Dynamic dashboard redirection

### **5.2 Booking Workflow**

```
1. Client browses cleaners → 2. Views cleaner profile →
3. Selects time slots → 4. Confirms booking →
5. Cleaner receives notification → 6. Accepts/Declines →
7. Service completion → 8. Review submission
```

### **5.3 Data Management**

- **Real-time Updates**: Automatic refresh of booking statuses
- **Local Storage**: Favorites and user preferences
- **API Integration**: RESTful communication with backend
- **Error Handling**: Graceful fallbacks and user feedback

## 6. Component Architecture

### **Shared Components** (19 components)

- `platform-layout` - Main application shell
- `booking-modal` - Service booking interface
- `cleaner-card` - Reusable cleaner display
- `booking-progress` - Status tracking
- `review-modal` - Rating and review system
- `notification-toast` - User feedback
- Plus 13 additional UI components

### **Feature-Specific Components**

- **User Features**: Booking management, favorites, reviews
- **Cleaner Features**: Job management, service configuration
- **Authentication**: Login, registration, onboarding flows

## 7. Technical Stack

### **Frontend**

- **Framework**: Angular 19+ (Standalone Components)
- **Styling**: Tailwind CSS 4+
- **Icons**: Material Icons, Heroicons
- **State Management**: Services with RxJS
- **Build Tool**: Angular CLI with Webpack
- **Hosting**: Netlify (Production Ready)

### **Backend Integration**

- **API**: Spring Boot REST API
- **Database**: PostgreSQL
- **Authentication**: JWT tokens
- **Hosting**: Heroku

### **Development Tools**

- **TypeScript**: Strict typing
- **ESLint**: Code quality
- **Prettier**: Code formatting
- **Environment Management**: Multi-environment configuration

## 8. Current API Integration

### **Implemented Endpoints**

```typescript
// Authentication
POST /auth/login
POST /auth/register

// Users & Cleaners
GET /users/profile
PUT /users/profile
GET /cleaners
GET /cleaners/{id}

// Reservations
POST /reservation
GET /reservation/all
PUT /reservation/{id}
DELETE /reservation/{id}

// Reviews
POST /reviews
GET /reviews/cleaner/{cleanerId}
PUT /reviews/{id}

// Favorites (Frontend Service)
LocalStorage-based favorite management
```

## 9. Production Readiness

### **Code Quality**

- ✅ Console logs removed from production build
- ✅ Error handling implemented
- ✅ Loading states and user feedback
- ✅ Responsive design tested
- ✅ TypeScript strict mode enabled

### **Performance Optimizations**

- Bundle size: ~255 kB (gzipped)
- Lazy loading for feature modules
- Optimized asset delivery
- Clean component architecture

### **Security Features**

- JWT token management
- Route guards for protected pages
- Input validation and sanitization
- HTTPS enforcement ready

## 10. Deployment Status

### **Frontend Deployment**

- **Platform**: Netlify
- **Domain**: Ready for custom domain
- **Build**: Automated CI/CD
- **Environment**: Production configuration

### **Backend Integration**

- **API Base URL**: Configurable via environment
- **Authentication**: JWT token-based
- **Error Handling**: Comprehensive fallback mechanisms

## 11. Getting Started

### **Prerequisites**

- Node.js 18+ and npm
- Angular CLI (`npm install -g @angular/cli`)

### **Development Setup**

```bash
# Clone the repository
git clone <repository-url>
cd cleanme-frontend

# Install dependencies
npm install

# Start development server
npm run start

# Application runs on http://localhost:4200
```

### **Environment Configuration**

Create `.env` file in the frontend directory:

```bash
NG_APP_BASE_URL=http://localhost:8080/api
```

### **Production Build**

```bash
npm run build
# Optimized build in /dist/cleanme
```

### **Available Scripts**

```bash
npm run start          # Development server
npm run build          # Production build
npm run test           # Run unit tests
npm run lint           # Code linting
```

## 12. Project Structure

```
cleanme-ai/
├── cleanme-frontend/           # Angular frontend application
│   ├── src/
│   │   ├── app/
│   │   │   ├── core/          # Core services and models
│   │   │   ├── features/      # Feature modules
│   │   │   ├── shared/        # Shared components
│   │   │   └── environments/  # Environment configs
│   │   ├── assets/            # Static assets
│   │   └── styles/            # Global styles
│   ├── package.json
│   ├── angular.json
│   └── tailwind.config.js
├── docs/                      # Project documentation
└── README.md                  # This file
```

## 13. Key Features Showcase

### **Dynamic Role-Based Experience**

The application automatically detects user roles and provides tailored experiences:

- **Clients** see cleaner discovery, booking management, and review systems
- **Cleaners** access job management, service configuration, and earnings tracking

### **Advanced Booking System**

- Real-time availability checking
- Time slot management with conflict prevention
- Automated status updates and notifications
- Comprehensive booking history

### **Professional UI/UX**

- Modern, responsive design with Tailwind CSS
- Intuitive navigation with role-based menus
- Loading states and error handling
- Mobile-optimized interface

## 14. Future Enhancements (Roadmap)

### **Phase 2 Features**

- Real-time chat system between clients and cleaners
- Advanced payment integration (Stripe/PayPal)
- Progressive Web App (PWA) capabilities
- Enhanced analytics dashboard

### **Phase 3 Features**

- AI-powered cleaner matching algorithm
- Loyalty and referral programs
- Advanced scheduling automation
- Multi-language support
- Mobile app development

## 15. Contributing

### **Development Guidelines**

- Follow Angular style guide
- Use TypeScript strict mode
- Implement comprehensive error handling
- Write unit tests for new features
- Follow semantic commit conventions

### **Code Quality Standards**

- ESLint configuration enforcement
- Prettier code formatting
- Component-based architecture
- Service-oriented design patterns

## 16. API Documentation

### **Data Transfer Objects**

```typescript
interface UserDto {
  id: string;
  firstName: string;
  lastName: string;
  email: string;
  userType: "CLIENT" | "CLEANER";
}

interface CleanerDto {
  id: string;
  fullName: string;
  services: string[];
  hourlyRate: number;
  rating: number;
  reviewCount: number;
  location: string;
}

interface ReservationDto {
  id: string;
  userId: string;
  cleanerId: string;
  date: string;
  time: string;
  location: string;
  status: "PENDING" | "CONFIRMED" | "COMPLETED" | "CANCELLED";
  comment: string;
}
```

---

**CleanMe** represents a fully functional, production-ready cleaning service platform with modern architecture, clean code practices, and comprehensive user experience design. The application successfully bridges the gap between cleaning service providers and clients through an intuitive, feature-rich web interface.

---

## Contact

For questions or support, please contact the development team.
