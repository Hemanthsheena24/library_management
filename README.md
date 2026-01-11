
# Frontend - GyaanKosh Library Management

The frontend client for the GyaanKosh library management system, built with vanilla HTML, CSS, and JavaScript.

## Overview

A responsive, modern web application that provides user interfaces for students, librarians, and public users to interact with the library management system.

## Features

- **Responsive Design**: Works on desktop, tablet, and mobile
- **User Authentication**: Login and registration forms
- **Role-based Dashboards**: Different interfaces for students and admins
- **Book Catalog**: Browse and search available books
- **Borrowing System**: Request books and track status
- **Admin Panel**: Manage books, users, and requests
- **Modern UI**: Clean, intuitive design with smooth animations

## Technology Stack

- **HTML5**: Semantic markup and accessibility
- **CSS3**: Modern styling with Flexbox and Grid
- **Vanilla JavaScript**: No frameworks, pure ES6+ JavaScript
- **Font Awesome**: Icon library
- **Google Fonts**: Typography (Poppins)
- **Local Storage**: Client-side data persistence

## Project Structure

```
frontend/
├── Dockerfile              # Container configuration
├── index.html             # Landing page
├── login.html             # Authentication page
├── signup.html            # Registration page
├── public-catalog.html    # Public book catalog
├── student-dashboard.html # Student interface
├── librarian-dashboard.html # Admin interface
├── style.css              # Global styles
├── script.js              # Shared utilities
├── login.js               # Login functionality
├── student.js             # Student dashboard logic
├── librarian.js           # Admin dashboard logic
├── public-catalog.js      # Catalog browsing
└── hello.txt              # Placeholder file
```

## Pages

### Public Pages
- **index.html**: Landing page with hero section and navigation
- **public-catalog.html**: Browse available books without login
- **login.html**: User authentication
- **signup.html**: New user registration

### Protected Pages
- **student-dashboard.html**: Student interface for managing requests
- **librarian-dashboard.html**: Admin interface for system management

## Key Components

### Navigation
Responsive navbar with mobile menu toggle, search functionality, and user authentication status.

### Authentication
- JWT token-based authentication
- Automatic token refresh
- Role-based access control
- Secure logout functionality

### Book Catalog
- Grid/list view toggle
- Search and filter capabilities
- Book details modal
- Availability status

### Dashboards
- **Student Dashboard**: Personal requests, profile management
- **Admin Dashboard**: User management, book inventory, request approval

## API Integration

The frontend communicates with the backend API using fetch requests:

```javascript
// Example API call
const response = await fetch('/api/books', {
  headers: {
    'Authorization': `Bearer ${token}`,
    'Content-Type': 'application/json'
  }
});
```

## Styling

- **CSS Variables**: Consistent theming and easy customization
- **Responsive Breakpoints**: Mobile-first design approach
- **Animations**: Smooth transitions and hover effects
- **Typography**: Google Fonts for modern, readable text

## JavaScript Architecture

- **Modular Code**: Separate files for different functionalities
- **Event Delegation**: Efficient event handling
- **Async/Await**: Modern asynchronous programming
- **Error Handling**: User-friendly error messages

## Development

### Local Development
```bash
# Serve with any static server
npx http-server -p 8080

# Or use Python
python -m http.server 8080
```

### Docker
```bash
docker build -t library-frontend:latest .
```

## Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## Performance

- Optimized images and assets
- Minimal JavaScript bundle
- Efficient CSS with no unused styles
- Fast loading times

## Accessibility

- Semantic HTML structure
- Keyboard navigation support
- Screen reader friendly
- High contrast ratios

## Deployment

The frontend is served as static files through an Nginx container in production, configured via the Dockerfile for optimal performance and security.
