# ZapChat ⚡

A full-stack real-time messaging chat application powered by redis and pusher.

-----

## 📋 Table of Contents

  - [Features](https://www.google.com/search?q=%23-features)
  - [Demo](https://www.google.com/search?q=%23-demo)
  - [Tech Stack](https://www.google.com/search?q=%23-tech-stack)
  - [Architecture](https://www.google.com/search?q=%23%EF%B8%8F-architecture)
  - [Getting Started](https://www.google.com/search?q=%23-getting-started)
      - [Prerequisites](https://www.google.com/search?q=%23prerequisites)
      - [Installation](https://www.google.com/search?q=%23installation)
      - [Environment Variables](https://www.google.com/search?q=%23environment-variables)
  - [Usage](https://www.google.com/search?q=%23-usage)
  - [API Reference](https://www.google.com/search?q=%23-api-reference)
  - [Deployment](https://www.google.com/search?q=%23-deployment)
  - [Roadmap](https://www.google.com/search?q=%23%EF%B8%8F-roadmap)
  - [Contributing](https://www.google.com/search?q=%23-contributing)
  - [License](https://www.google.com/search?q=%23-license)
  - [Acknowledgements](https://www.google.com/search?q=%23-acknowledgements)
  - [Contact](https://www.google.com/search?q=%23-contact)

-----

## ✨ Features

  - **Real-time messaging** powered by Pusher
  - **Google authentication** for secure user management
  - **Friend system** with email-based friend requests
  - **Responsive design** that works on mobile and desktop
  - **Fast performance** with Redis database integration
  - **Message read receipts**
  - **User online/offline status**
  - **Image sharing** in messages
  - **Mobile-optimized layout** with slide-out navigation
  - **TypeScript** for type safety and better developer experience
  - **Protected routes** with NextAuth.js session management

-----

## 🚀 Demo

**Live Demo:** [https://zap-chat-seven.vercel.app](https://zap-chat-seven.vercel.app)

\<img alt="Dashboard Screenshot" src="[https://via.placeholder.com/800x400?text=ZapChat+Dashboard](https://via.placeholder.com/800x400?text=ZapChat+Dashboard)"\>

-----

## 🛠️ Tech Stack

### Frontend:

  - **Next.js 13** (App Router)
  - **React 18**
  - **TailwindCSS**
  - **Headless UI**
  - **Lucide Icons**

### Backend:

  - **Next.js API Routes**
  - **Upstash Redis**
  - **Pusher**

### Authentication:

  - **NextAuth.js**
  - **Google OAuth**

### Development Tools:

  - **TypeScript**
  - **ESLint**
  - **date-fns** for date formatting
  - **Zod** for validation

-----

## 🏗️ Architecture

ZapChat uses a modern architecture with:

  - **Server Components** for efficient rendering
  - **Redis** as the primary database for chat messages and user data
  - **Pusher** for real-time WebSocket communication
  - **NextAuth.js** for authentication and session management
  - **App Router** for improved routing and layouts

The app follows a modular component structure with:

  - Separate layouts for dashboard and authentication
  - Mobile-specific components for responsive design
  - Real-time message synchronization across devices
  - Optimistic UI updates for a snappy feel

-----

## 🚦 Getting Started

### Prerequisites

  - **Node.js** (v16.8 or newer)
  - **npm** or **yarn**
  - **Upstash Redis** account
  - **Pusher** account
  - **Google Cloud Console** project with OAuth credentials

### Installation

1.  Clone the repository:
    ```bash
    git clone https://github.com/yourusername/zap-chat.git
    cd zap-chat
    ```
2.  Install dependencies:
    ```bash
    npm install
    # or
    yarn
    ```
3.  Set up environment variables (see next section).
4.  Run the development server:
    ```bash
    npm run dev
    # or
    yarn dev
    ```
5.  Open [http://localhost:3000](https://www.google.com/search?q=http://localhost:3000) in your browser.

### Environment Variables

Create a `.env.local` file in the root directory with the following variables:

```env
# Redis
UPSTASH_REDIS_REST_URL="your-redis-url"
UPSTASH_REDIS_REST_TOKEN="your-redis-token"

# Google Auth
GOOGLE_CLIENT_ID="your-google-client-id"
GOOGLE_CLIENT_SECRET="your-google-client-secret"

# NextAuth
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="your-nextauth-secret"

# Pusher
PUSHER_APP_ID="your-pusher-app-id"
NEXT_PUBLIC_PUSHER_APP_KEY="your-pusher-key"
PUSHER_APP_SECRET="your-pusher-secret"
```

For production, update `NEXTAUTH_URL` to your deployed domain.

-----

## 📝 Usage

### Authentication

1.  Navigate to the homepage.
2.  Click "Sign In with Google".
3.  Follow the Google authentication flow.

### Adding Friends

1.  Navigate to the "Add Friend" page.
2.  Enter the email address of your friend.
3.  A friend request will be sent if they have an account.

### Chatting

1.  Select a friend from your chat list.
2.  Type your message in the input field.
3.  Press Enter or click the send button.

### Viewing Friend Requests

1.  Navigate to the "Friend Requests" page.
2.  Accept or decline pending requests.

-----

## 🔌 API Reference

### Chat Routes

  - `POST /api/message/send` - Send a new message
  - `GET /api/friends` - Get all friends
  - `POST /api/friends/add` - Send a friend request
  - `POST /api/friends/accept` - Accept a friend request
  - `POST /api/friends/deny` - Deny a friend request

### Authentication Routes

  - `GET/POST /api/auth/[...nextauth]` - NextAuth.js authentication routes

-----

## 📦 Deployment

### Deploying to Vercel

1.  Push your code to GitHub.
2.  Import the project in Vercel.
3.  Add all environment variables.
4.  Deploy\!

**Important:** Set `NEXTAUTH_URL` to your production URL.

### Configuring Google OAuth for Production

1.  Go to the Google Cloud Console.
2.  Add your production URL to the **Authorized redirect URIs**:
    `https://yourdomain.com/api/auth/callback/google`

-----

## 🗺️ Roadmap

  - [ ] Message reactions
  - [ ] Group chats
  - [ ] End-to-end encryption
  - [ ] Voice messages
  - [ ] Video calls
  - [ ] Message deletion
  - [ ] Message editing
  - [ ] Dark mode

-----

## 🤝 Contributing

Contributions are welcome\! Please feel free to submit a Pull Request.

1.  Fork the project
2.  Create your feature branch (`git checkout -b feature/amazing-feature`)
3.  Commit your changes (`git commit -m 'Add some amazing feature'`)
4.  Push to the branch (`git push origin feature/amazing-feature`)
5.  Open a Pull Request


-----


## 👏 Acknowledgements

  - [Next.js Documentation](https://nextjs.org/docs)
  - [TailwindCSS Documentation](https://tailwindcss.com/docs)
  - [Upstash Redis Documentation](https://upstash.com/docs)
  - [Pusher Documentation](https://pusher.com/docs)
  - [NextAuth.js Documentation](https://next-auth.js.org/getting-started/introduction)

-----



-----

Made with ❤️ by Pratik Sarangi
