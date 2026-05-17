# 🦁 The Sunny Tavern - Restaurant CRM

A beautiful, One Piece-themed Restaurant Customer Relationship Management system built with vanilla HTML, CSS, and JavaScript.

Perfect for managing Japanese restaurants with a fun, pirate-inspired aesthetic.

## ✨ Features

- **🪑 Table Management** - Track table status (free/occupied/reserved) in real-time
- **👥 Customer Database** - Manage regular customers with visit history and loyalty tracking
- **🍜 Menu Management** - Add, edit, and display dishes with prices
- **📊 Dashboard** - Quick overview of today's revenue, reservations, and table availability
- **📱 Responsive Design** - Works seamlessly on desktop, tablet, and mobile
- **⚡ No Dependencies** - Pure vanilla JavaScript, no frameworks needed
- **🎨 One Piece Theme** - Vibrant colors and playful interactions inspired by One Piece

## 🎨 Design Philosophy

The Sunny Tavern features a One Piece-inspired design with:
- **Color Palette**: Orange (#FF6B35), Blue (#1E90FF), Green (#00D084), Yellow (#FFD700)
- **Typography**: Fredoka (headers), Inter (body text) for clean, friendly readability
- **Micro-interactions**: Smooth hover effects, toast notifications, and animations
- **Playful Elements**: Nautical emojis and adventure-themed messaging

## 🚀 Quick Start

1. **Download or clone the repository**
   ```bash
   git clone https://github.com/yourusername/the-sunny-tavern.git
   ```

2. **Open in browser**
   ```bash
   # Windows
   start index.html
   
   # macOS
   open index.html
   
   # Or simply drag index.html into your browser
   ```

3. **That's it!** No build step, no server, no dependencies needed.

## 📋 Pages

### 1. **Dashboard** 📊
- Daily revenue overview
- Available tables count
- Loyal customers count
- Today's reservations at a glance

### 2. **Tables** 🪑
- Visual grid of all restaurant tables
- Quick status updates (free/occupied/reserved)
- Add new tables to your restaurant
- Real-time availability tracking

### 3. **Customers** 👥
- Customer database with phone numbers
- Visit count and loyalty status
- Direct reservation from customer profile
- Add new customers easily

### 4. **Menu** 🍜
- Complete menu with descriptions
- Pricing displayed clearly
- Filter by category (Ramen, Sushi, Sides, etc.)
- Add new dishes on the fly

## 🛠️ Tech Stack

- **HTML5** - Semantic markup
- **CSS3** - Custom properties, Flexbox, CSS Grid, animations
- **Vanilla JavaScript** - No frameworks, pure ES6
- **Google Fonts** - Fredoka, Inter, Quicksand

## 💾 Data Management

All data is stored in-memory using JavaScript arrays:
- `tables` - Table status and capacity
- `customers` - Customer information and history
- `reservations` - Today's bookings
- `menu` - Menu items with prices

**Note**: Data resets on page reload. For persistence, integrate with a backend database.

## 🎮 Usage Examples

### Add a Table
1. Click "🪑 Tables" tab
2. Click "+ הוסף שולחן" (Add Table)
3. Enter table number and seat count
4. Submit

### Add a Customer
1. Go to "👥 Customers" tab
2. Click "+ לקוח חדש" (New Customer)
3. Enter name and phone number
4. Save to add to your database

### Add Menu Item
1. Navigate to "🍜 Menu" tab
2. Click "+ הוסף מנה" (Add Dish)
3. Fill in name, category, description, and price
4. Item appears immediately in menu

## 🌍 Internationalization

The app uses **Hebrew (RTL)** by default. Labels and interface text are in Hebrew with English menu items for flexibility.

To adapt for other languages, modify:
- Tab names and section titles
- Button labels in modals
- Placeholder text in form inputs

## 📱 Responsive Breakpoints

- **Desktop**: Full grid layouts (2-4 columns)
- **Tablet**: Adjusted grid (1-2 columns)
- **Mobile**: Single column, optimized for touch

## 🎯 Future Enhancements

- [ ] Backend integration for data persistence
- [ ] User authentication & multi-user support
- [ ] Order management & kitchen display system (KDS)
- [ ] Payment integration
- [ ] Customer loyalty rewards program
- [ ] Analytics & reporting dashboard
- [ ] Multi-language support (English, Japanese, etc.)
- [ ] Dark mode option
- [ ] Mobile app version

## 📝 License

This project is open source and available under the MIT License.

## 🏴‍☠️ Credits

Built with inspiration from One Piece's Thousand Sunny ship and restaurant management needs.

Designed for fun, adventure, and great food! ⛵🍜

---

**Made with ❤️ for restaurant crews everywhere**

*"Set sail with your restaurant management!" - Captain Design*