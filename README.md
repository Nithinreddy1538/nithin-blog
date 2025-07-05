# User Data Fetcher

A modern, responsive web application that fetches and displays user data from the JSONPlaceholder API. Built with vanilla HTML, CSS, and JavaScript, featuring elegant UI design and comprehensive error handling.

## 🌟 Features

- **Real-time Data Fetching**: Retrieves user data from JSONPlaceholder API
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Modern UI**: Clean card-based layout with smooth animations
- **Error Handling**: Comprehensive error detection and user-friendly messages
- **Loading States**: Visual feedback during data fetching
- **Reload Functionality**: Easy data refresh with animated button
- **User-Friendly Display**: Shows complete user information including:
  - Name and username
  - Email and phone
  - Address details
  - Website links
  - Company information

## 🚀 Demo

The application displays user data in an elegant card layout with:
- User avatars with initials
- Hover effects and micro-interactions
- Smooth fade-in animations
- Professional gradient background

## 🛠️ Technologies Used

- **HTML5**: Semantic markup structure
- **CSS3**: Modern styling with Flexbox and Grid
- **JavaScript (ES6+)**: Fetch API and DOM manipulation
- **JSONPlaceholder API**: Public REST API for testing

## 📁 Project Structure

├── index.html          # Main HTML structure
├── styles.css          # CSS styling and animations
├── script.js           # JavaScript functionality
└── README.md           # Project documentation

## 🎯 Getting Started

### Prerequisites

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection for API requests

### Installation

1. Clone or download the project files
2. Open `index.html` in your web browser
3. The application will automatically load user data

### Local Development

For local development with live reload:

''bash
# Using Python (if installed)
python -m http.server 8000

# Using Node.js (if installed)
npx serve .

# Then open http://localhost:8000 in your browser
``

## 🔧 How It Works

### Data Fetching Process

1. **API Request**: Sends GET request to `https://jsonplaceholder.typicode.com/users`
2. **Response Handling**: Parses JSON response and validates data
3. **UI Update**: Dynamically creates user cards with fetched data
4. **Error Management**: Catches and displays user-friendly error messages

### Key Components

#### UserDataFetcher Class
- Manages all application functionality
- Handles API requests and responses
- Controls UI state (loading, error, success)
- Provides user interaction methods

#### Error Handling
- Network connectivity issues
- HTTP status errors
- JSON parsing errors
- User-friendly error messages with retry options

#### Responsive Design
- Mobile-first approach
- CSS Grid for flexible layouts
- Breakpoints for different screen sizes

## 🎨 UI Features

### Visual Elements
- **Gradient Background**: Modern purple-blue gradient
- **Card Design**: Clean white cards with subtle shadows
- **Typography**: Professional font stack with proper hierarchy
- **Icons**: Emoji-based icons for different data types
- **Animations**: Smooth transitions and hover effects

### Interactive Elements
- **Reload Button**: Animated reload with rotation effect
- **Hover States**: Card elevation and button transformations
- **Loading Spinner**: CSS-only spinning animation
- **Error Recovery**: Retry functionality with visual feedback

## 🧪 Testing Error Handling

To test the error handling functionality:

1. **Network Error**: Disable internet connection and click reload
2. **API Error**: The app handles various HTTP status codes
3. **Retry Functionality**: Use the retry button when errors occur

## 📱 Responsive Breakpoints

- **Desktop**: 1200px+ (Multi-column grid)
- **Tablet**: 768px-1199px (Flexible grid)
- **Mobile**: <768px (Single column)

## 🔍 Code Highlights

### Fetch Implementation
```javascript
async fetchUsers() {
    try {
        this.showLoading();
        const response = await fetch(this.apiUrl);
        
        if (!response.ok) {
            throw new Error(`HTTP error! status: ${response.status}`);
        }
        
        const users = await response.json();
        this.displayUsers(users);
    } catch (error) {
        this.handleError(error);
    }
}
```

### Dynamic Card Creation
```javascript
createUserCard(user) {
    const card = document.createElement('div');
    card.className = 'user-card fade-in';
    // Dynamic content generation with user data
    return card;
}
```

## 🌐 API Reference

**Endpoint**: `https://jsonplaceholder.typicode.com/users`

**Response Format**: Array of user objects containing:
- `id`: User identifier
- `name`: Full name
- `username`: Username
- `email`: Email address
- `phone`: Phone number
- `website`: Personal website
- `address`: Address object with street, city, zipcode
- `company`: Company object with name and catchphrase

## 🚀 Performance Features

- **Efficient DOM Manipulation**: Minimal reflows and repaints
- **CSS Animations**: Hardware-accelerated transitions
- **Lazy Loading**: Staggered card animations
- **Error Recovery**: Graceful degradation

## 🔮 Future Enhancements

- Search and filter functionality
- User detail modal views
- Data caching for offline viewing
- Pagination for large datasets
- Dark mode toggle
- Export user data functionality

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

If you encounter any issues or have questions, please open an issue in the project repository.

---

**Built with ❤️ using vanilla JavaScript and modern web technologies**
