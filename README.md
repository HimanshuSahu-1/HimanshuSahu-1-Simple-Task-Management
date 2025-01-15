 # Authenticated Task App with TRPC, Next.js, Prisma, and Tailwind

This application is built using the T3 Stack, combining TRPC for API communication, Next.js for the frontend and backend, Prisma for database access, and Tailwind CSS for styling. It features authenticated user access via magic link emails and optimistic updates for a smooth user experience.

## Video Demonstration



Click the image above or [watch the video here](https://drive.google.com/file/d/1wZJXBQMeVnO8HOnN59Z-BrIgQGFlC5hT/view?usp=sharing) to see a walkthrough of the app.

## Technologies Used

*   [Next.js](https://nextjs.org): React framework for server-side rendering and more.
*   [NextAuth.js](https://next-auth.js.org): Authentication library.
*   [Prisma](https://prisma.io): ORM for database access.
*   [Tailwind CSS](https://tailwindcss.com): Utility-first CSS framework.
*   [tRPC](https://trpc.io): End-to-end typesafe APIs.

## Installation and Setup

1.  **Clone the Repository:**

    ```bash
    git clone [https://github.com/HimanshuSahu-1/HimanshuSahu-1-Simple-Task-Management.git](https://github.com/HimanshuSahu-1/HimanshuSahu-1-Simple-Task-Management.git)
    cd HimanshuSahu-1-Simple-Task-Management
    ```

2.  **Install Dependencies:**

    Make sure you have Node.js and npm (or yarn) installed. Then, run:

    ```bash
    npm install
    # or
    yarn install
    ```

3.  **Environment Variables:**

    Create a `.env` file in the root of your project and add the following environment variables. **Replace the placeholder values with your actual credentials.**

    ```
    DATABASE_URL="your-database-connection-url" # e.g., postgresql://user:password@host:port/database
    NEXTAUTH_URL="http://localhost:3000" # Or your production URL
    NEXTAUTH_SECRET="a-very-long-and-random-secret-key" # Generate a strong secret
    EMAIL_SERVER="smtp://your-email-server:port" # e.g., smtp://[invalid URL removed]
    EMAIL_FROM="your-email@example.com"
    EMAIL_PASSWORD="your-email-password" # if needed by email server
    ```
    *   **DATABASE_URL:** This is your database connection string. For PostgreSQL, it typically looks like `postgresql://user:password@host:port/database`. For other databases, consult Prisma's documentation.
    *   **NEXTAUTH_SECRET:** This is crucial for NextAuth.js security. Generate a long, random string. You can use online tools or the command `openssl rand -base64 32` (on Linux/macOS) to generate one.
    *   **Email Configuration:** The `EMAIL_SERVER` and `EMAIL_FROM` settings are required for the magic link email authentication to function. You will need an email service provider (like Gmail, SendGrid, Mailgun, etc.) to configure these correctly.

4.  **Prisma Setup:**

    *   Generate the Prisma client:

        ```bash
        npx prisma generate
        ```

    *   Apply the database migrations:

        ```bash
        npx prisma migrate dev
        ```

5.  **Run the Development Server:**

    ```bash
    npm run dev
    # or
    yarn dev
    ```

6.  **Open in Browser:**

    Navigate to `http://localhost:3000` in your web browser to view the application.

