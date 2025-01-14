# Next.js Authentication & Power BI Dashboard

A modern web application built with Next.js 13, featuring user authentication and Power BI dashboard integration.

## Features

- 🔐 User Authentication (Login/Signup)
- 📊 Power BI Dashboard Integration
- 🎨 Modern UI with Tailwind CSS
- 🔄 Form Validation with Zod
- 📱 Fully Responsive Design
- ⚡ Server-Side Rendering with Next.js

## Tech Stack

- **Framework**: Next.js 13
- **Styling**: Tailwind CSS
- **UI Components**: shadcn/ui
- **Form Management**: React Hook Form
- **Validation**: Zod
- **Icons**: Lucide React
- **Authentication**: Custom JWT

## Getting Started

### Prerequisites

- Node.js 16.8 or later
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env.local` file in the root directory and add your environment variables:
```env
NEXT_PUBLIC_API_URL=http://www.tyji.in:5001
NEXT_PUBLIC_POWERBI_REPORT_ID=your_report_id
NEXT_PUBLIC_POWERBI_TENANT_ID=your_tenant_id
```

4. Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:3000`.

## Project Structure

```
├── app/
│   ├── auth/
│   │   ├── login/
│   │   └── signup/
│   ├── dashboard/
│   ├── layout.tsx
│   └── page.tsx
├── components/
│   └── ui/
├── hooks/
├── lib/
└── public/
```

## Authentication Flow

1. User enters credentials on the login page
2. Credentials are validated using Zod
3. POST request is sent to the authentication API
4. Upon successful authentication, JWT token is stored in localStorage
5. User is redirected to the dashboard
6. Protected routes check for token presence

## Power BI Integration

To integrate your Power BI dashboard:

1. Replace `YOUR_REPORT_ID` in `dashboard/page.tsx` with your actual Power BI report ID
2. Replace `YOUR_TENANT_ID` with your Azure AD tenant ID
3. Ensure proper authentication and permissions are set up in your Power BI workspace

## API Endpoints

### Login
- **URL**: `http://www.tyji.in:5001/login`
- **Method**: `POST`
- **Body**:
```json
{
  "email": "user@example.com",
  "password": "password"
}
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, email [your-email@example.com](mailto:your-email@example.com) or open an issue in the repository.