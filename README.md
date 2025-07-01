# TaskFlow - Advanced Task Management Application

*This project is a part of a hackathon run by https://www.katomaran.com*

## Overview

TaskFlow is a comprehensive full-stack task management application that revolutionizes productivity through advanced features including AI-powered suggestions, gamification, voice control, mood-based task assignment, and real-time analytics. Built with modern technologies, it provides an intuitive and engaging user experience for managing tasks efficiently.

## 🚀 Key Features

### Core Task Management
- **Complete CRUD Operations**: Create, read, update, and delete tasks with ease
- **Advanced Filtering & Sorting**: Filter by status, priority, category, and mood requirements
- **Task Sharing**: Collaborate by sharing tasks via email
- **Due Date Management**: Set and track due dates with overdue alerts
- **Priority System**: Organize tasks with high, medium, and low priority levels

### Advanced Features
- **🎮 Gamification System**: Earn points, level up, unlock achievements, and maintain streaks
- **🎙️ Voice Control**: Create and complete tasks using voice commands
- **🧠 Mood-Based Task Assignment**: Match tasks to your current mental state (focused, creative, energetic, calm)
- **🎊 Animated Task Completion**: Celebrate accomplishments with confetti and animations
- **📊 Analytics Dashboard**: Track productivity with charts, insights, and performance metrics
- **📅 Calendar View**: Visualize tasks in a calendar format with monthly summaries
- **🎨 Custom Themes**: Switch between minimal and full UI modes
- **📱 Responsive Design**: Works seamlessly across desktop, tablet, and mobile devices

### Technical Highlights
- **Authentication**: Secure login with Replit Auth (OpenID Connect)
- **Real-time Updates**: Live data synchronization with optimistic updates
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Modern UI**: Built with React 18, TypeScript, and Tailwind CSS
- **State Management**: TanStack Query for efficient server state management
- **Animations**: Framer Motion for smooth, engaging animations

## 🛠️ Technology Stack

### Frontend
- **React 18** with TypeScript for type-safe component development
- **Tailwind CSS** for utility-first styling
- **shadcn/ui** component library for consistent, accessible UI
- **TanStack Query** for powerful data fetching and caching
- **Framer Motion** for smooth animations and transitions
- **Chart.js** for data visualization and analytics
- **React Hook Form** with Zod validation for form management
- **Wouter** for lightweight client-side routing

### Backend
- **Node.js** with Express.js framework
- **TypeScript** for type safety across the stack
- **PostgreSQL** with Neon serverless database
- **Drizzle ORM** for type-safe database operations
- **Replit Auth** with OpenID Connect for secure authentication
- **Session Management** with PostgreSQL-backed sessions

## 🎯 User Experience Features

### Gamification Elements
- **Experience Points (XP)**: Earn points for completing tasks
- **Level System**: Progress through levels based on accumulated points
- **Achievements**: Unlock special badges for milestones
- **Streak Tracking**: Maintain daily task completion streaks
- **Progress Visualization**: Visual progress bars and indicators

### Voice Control Commands
- "Create task [task name]" - Create a new task
- "Complete task [task name]" - Mark task as completed
- "Add task [task name] with description [details]" - Create detailed tasks
- "Help" - Get available commands

### Mood-Based Productivity
- **Focused Mode**: Perfect for deep work, coding, and analysis
- **Creative Mode**: Ideal for brainstorming, design, and innovation
- **Energetic Mode**: Great for meetings, calls, and quick tasks
- **Calm Mode**: Best for organization, planning, and review

### Analytics & Insights
- **Completion Rate Tracking**: Monitor your productivity percentage
- **Priority Distribution**: Visualize task priorities with charts
- **Weekly Activity**: Track task creation and completion trends
- **Performance Recommendations**: Get personalized productivity tips

## 🎨 User Interface

### Modern Design
- **Clean, Minimalist Interface**: Focus on tasks without distractions
- **Gradient Backgrounds**: Beautiful color transitions
- **Card-Based Layout**: Organized information in digestible chunks
- **Responsive Grid System**: Adapts to any screen size

### Interactive Elements
- **Smooth Animations**: Engaging micro-interactions
- **Hover Effects**: Visual feedback for better usability
- **Loading States**: Clear progress indicators
- **Toast Notifications**: Immediate feedback for actions

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ installed
- PostgreSQL database (provided via Replit)
- Modern web browser with JavaScript enabled

### Installation & Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd taskflow
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   The following environment variables are automatically configured in Replit:
   - `DATABASE_URL` - PostgreSQL connection string
   - `SESSION_SECRET` - Session encryption key
   - `REPLIT_DOMAINS` - Allowed authentication domains

4. **Initialize the database**
   ```bash
   npm run db:push
   ```

5. **Start the development server**
   ```bash
   npm run dev
   ```

6. **Access the application**
   Open your browser and navigate to the provided Replit URL

## 📝 Usage Guide

### Getting Started
1. **Login**: Click "Login" to authenticate with your Replit account
2. **Create Your First Task**: Click the "Add Task" button or use voice control
3. **Set Your Mood**: Choose your current mental state for personalized task suggestions
4. **Track Progress**: Monitor your productivity through the analytics dashboard

### Task Management
- **Creating Tasks**: Use the form, voice commands, or quick-add features
- **Organizing**: Filter by status, priority, or mood requirements
- **Collaboration**: Share tasks with team members via email
- **Completion**: Mark tasks complete and enjoy the celebration animation

### Advanced Features
- **Voice Control**: Enable in settings and use voice commands
- **Calendar View**: Switch to calendar tab for timeline visualization
- **Analytics**: Check your productivity trends and insights
- **Gamification**: Track your level, points, and achievements

## 🔧 Development

### Project Structure
```
taskflow/
├── client/               # React frontend
│   ├── src/
│   │   ├── components/   # Reusable UI components
│   │   ├── pages/        # Page components
│   │   ├── hooks/        # Custom React hooks
│   │   └── lib/          # Utility functions
├── server/               # Express.js backend
│   ├── routes.ts         # API route definitions
│   ├── storage.ts        # Database operations
│   ├── replitAuth.ts     # Authentication logic
│   └── index.ts          # Server entry point
├── shared/               # Shared TypeScript types
│   └── schema.ts         # Database schema & types
└── README.md            # Project documentation
```

### Key Components
- **TaskForm**: Dynamic form for creating/editing tasks
- **TaskItem**: Individual task display with actions
- **GamificationPanel**: Points, levels, and achievements
- **VoiceControl**: Speech recognition integration
- **MoodSelector**: Mood-based task filtering
- **CalendarView**: Calendar visualization
- **AnalyticsDashboard**: Productivity insights

### Database Schema
The application uses a comprehensive PostgreSQL schema including:
- **Users**: Authentication and profile data
- **Tasks**: Core task information with extended fields
- **TaskShares**: Collaboration and sharing
- **UserPreferences**: Personal settings and preferences
- **Habits**: Habit tracking (extensible)
- **Analytics**: Performance tracking data

## 🎁 Future Enhancements

### Planned Features
- **AI Task Suggestions**: Machine learning-powered task recommendations
- **Habit Tracking**: Build and maintain productive habits
- **Team Collaboration**: Enhanced sharing and team features
- **Mobile App**: Native iOS and Android applications
- **API Integration**: Connect with external productivity tools
- **Custom Themes**: User-created color schemes and layouts
- **Offline Support**: Work without internet connectivity
- **Smart Notifications**: Context-aware reminders

### Technical Improvements
- **Real-time Collaboration**: WebSocket-based live updates
- **Advanced Analytics**: Machine learning insights
- **Performance Optimization**: Enhanced caching and lazy loading
- **Accessibility**: Full WCAG compliance
- **Internationalization**: Multi-language support
- **Dark Mode**: System-aware theme switching

## 🤝 Contributing

We welcome contributions! This project was built as part of a hackathon but is open for community improvements.

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow TypeScript best practices
- Write comprehensive tests for new features
- Maintain consistent code formatting
- Update documentation for significant changes
- Ensure responsive design compatibility

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🏆 Hackathon Attribution

*This project is a part of a hackathon run by https://www.katomaran.com*

## 🙏 Acknowledgments

- **Replit Platform**: For providing the development environment and authentication
- **shadcn/ui**: For the beautiful, accessible component library
- **Chart.js**: For powerful data visualization capabilities
- **Framer Motion**: For smooth, engaging animations
- **React Speech Recognition**: For voice control functionality
- **Drizzle ORM**: For type-safe database operations

## 📞 Support

For questions, issues, or suggestions:
- Open an issue on GitHub
- Check the documentation
- Review existing discussions

---

**Built with ❤️ for productivity enthusiasts**

Transform your task management experience with TaskFlow - where productivity meets innovation!