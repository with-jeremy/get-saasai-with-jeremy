# AI-Assisted Social Media Video SaaS

This project is an AI-assisted tool for automated, yet curated, social media short-form video creation. Built using **Nuxt.js**, **Pinia**, **Vuetify**, and **Firebase**, it offers users an intuitive interface to generate engaging content for platforms like Instagram Reels and YouTube Shorts.

## Project Progress

### Sprint 1: Firebase Setup and Nuxt Project Initialization

- **Initialized Firebase project** with Authentication, Firestore Database, and Storage.
- **Set up Nuxt.js project** with Pinia for state management.
- **Installed Vuetify** and configured the design system with predefined colors, typography, and layouts.
- **Created foundational files** including plugins for Vuetify and Firebase.
- **Defined data models** for Users, Projects, and Transactions.

### Upcoming Sprints

1. **Sprint 2: Authentication and User Onboarding**
   - Build user authentication flow with Firebase Auth.
   - Create onboarding flow where users select their plan/tier.
   - Initialize user profiles in Firestore, including credits based on tier.

2. **Sprint 3: Dashboard Layout and Design System Implementation**
   - Design the user dashboard.
   - Implement reusable components using Vuetify.
   - Create style collections for common UI elements.

3. **Sprint 4: Credits and Usage Management**
   - Implement the credits system.
   - Display remaining credits in the dashboard.
   - Add admin interface to adjust user credits.

4. **Sprint 5: AI Product Integration (Social Media Video Tool)**
   - Setup API integrations for script generation, text-to-speech, and video assembly.
   - Create guided workflows for users.

5. **Sprint 6: Stripe Payment Integration**
   - Integrate Stripe for subscription plans and credit purchasing.
   - Create a billing page in the user’s dashboard.

6. **Sprint 7: User Settings and Customization**
   - Add pages for users to update their account settings.
   - Implement tier management.

7. **Sprint 8: Video Review and Publishing**
   - Allow users to preview generated videos.
   - Integrate Instagram Reels and YouTube Shorts APIs for direct publishing.

8. **Sprint 9: Final Design and UI Refinements**
   - Focus on responsive design.
   - Polish the visual layout and interactions.

9. **Sprint 10: Testing and Deployment**
   - Conduct end-to-end testing.
   - Deploy on Firebase Hosting.

## Getting Started

### Prerequisites

- **Node.js** and **npm** installed.
- **Firebase** account with a project set up.
- **Git** installed.

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name

[Users] Collection
  |
  |--- [userId] Document
          |--- email: string
          |--- name: string
          |--- tier: string
          |--- credits: number
          |--- createdAt: timestamp
          |--- updatedAt: timestamp

[Projects] Collection
  |
  |--- [projectId] Document
          |--- userId: reference to Users/userId
          |--- title: string
          |--- status: string
          |--- platform: string
          |--- script: string
          |--- videoUrl: string
          |--- createdAt: timestamp
          |--- updatedAt: timestamp

[Transactions] Collection
  |
  |--- [transactionId] Document
          |--- userId: reference to Users/userId
          |--- type: string
          |--- amount: number
          |--- creditsAdded: number
          |--- createdAt: timestamp
