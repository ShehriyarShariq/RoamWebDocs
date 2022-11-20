---
sidebar_position: 1
---

# Intro

The Web App is the main way of interacting with Roam, and is the user-facing part of the platform. It is meant to allow exploration, be part of a community and team-up with like-minded adventurers to explore uncharted territories together.

## Auxiliary Definitions

- **Experience**: A single location on the map, for eg: a lake, a mountain, a meadow, etc...
- **Adventure/Tour**: A combination of Experiences, with an order, a season, dates, and miscellaneous details.

## Features

The Web App supports the following features:

- **Authentication**: Access the platform as an authenticated user for a better experience.
  - **Login**: Login is indeed essential to the platform, however, most of the features on the platform can be utilized without logging in.
    - Email and Password
    - Social Logins
  - **Register**: Registration isn’t mandatory in order to use the platform. Registration can be done with either Email/Password or using social auth like Google, Facebook, etc.
  - **Change Password**: Changing the password is only performed in the scenario where a user wishes to change their password while already knowing the existing one and updating that to a newer password.
  - **Forgot Password**: When the user has forgotten their password and wants to re-login, the user can enter their email address and a link will be sent to them where they can enter their new password.
- **Explore**: Main attraction of the platform. Displays experiences on an easy-to-understand Map with the ability to explore and plan your trips.

  - **Map**
    - View Experiences from a Bird's-eye view
    - Filter Experiences
    - View Experience Details
    - View Routes between experiences
    - View Travel Plans of other Adventurers
    - Load Favorite Experiences
  - **Recommendations**
    - **Journeys**: Users are recommended trips/adventures based on their profile. This is done using NLP techniques.
    - **Dream/Wish Trip Input**: Users are recommended trips/adventures based on their input. This is done using NLP techniques.
      - Money
      - Time
      - Difficulty
      - Season
    - **People**: Users are shown other relevant profile members. This is done using NLP techniques.
      - Match based on Profile.
      - Match based on Input.
        - The user can input descriptions of the types of people they’re looking for on a trip.
    - **Upcoming Trips**: Users are able to view upcoming trips advertised by Roam or other platform members.

- **User Profile**: The user can read and update their profile from the User profile screen. The user can also add their adventure details, biography, profile picture and experiences.

  - Read/Update Profile
  - Add Profile Picture
  - Add Biography
  - Add Past Adventures
  - Add Services
  - Add Interests

- **Community**: build a tight-knit network of adventurers and guides.

  - **Forum**: A common place for all adventurers and guides to post their experiences and updates.
    - Ask Question
    - Upvote/Downvote Questions
    - Comment on Question
    - Add a Post
    - Comment on Posts
  - **Chat**: Communicate with other adventurers and guides.
  - **Meet**: Coordinate meetups with guides and adventurers.
  - **Updated Plans**: Be up-to-date on upcoming plans.

- **Messages**: Direct messaging to other users on the platform
- **Offer Trips**: Trips being created by guides and being viewed, reviewed and provided feedback for by the members on the platform.

  - **Packages**: Guides can create end-to-end tours from an Interactive Tour Builder.
  - **Offer Consultation**: Guide can provide consulting services to other adventurers.
  - **Misc Services**: Provide on-trip services to the adventurers.

- **Stories**: Articles posted by users that highlight their adventures.
- **Consult**: Consult the Roam team in terms of logistics, gear and adventure consultations.

## Directory Structure

Following are the directories that have a specific purpose and should only be used for that purpose only.

1. **Public**

```
/public
```

The public folder is for all the static elements of the platform, such as **images**.

2. **Pages**:

```
/pages
```

The pages folder defines the routing in the Next.js app and defines the actual pages that are visible on the folder-based hierarchical path.

3. **Components**

```
/components
```

The components folder contains all the JSX elements, where each folder within it represents either a Widget (re-usable component). This is the directory that is most often used for development.

4. **Contexts**

```
/contexts
```

The Contexts folder contains different kinds of Context API hooks that have been been placed at the root of the document tree. Following are the types of contexts currently present in the Tour Builder.

- Auth Context - For logging in, logging out, and getting the current user.
- Community Filters Context - For showing the Filters overlay.
- Experience Details Context - For showing the experience card as an overlay for the selected experience.
- Register Content Dialog Context - Show the Register content dialog.
- Search Context - Show the Search overlay.

5. **Utils**

```
/utils
```

The Utils folder contains constants and utility functions that perform a specific function, take in an input and return an output.

## Common Widgets

```
/components/common
```

1. **components/common/AutoTextArea** - Auto-resizing Text Area Widget
2. **components/common/Button** - Generic and Customizable Button Widget
3. **components/common/DropDown** - Generic DropDown
4. **components/common/IconButton** - Generic and Customizable Icon Button Widget
5. **components/common/InputField** - Generic Input Field
6. **components/common/Map** - Map Widget
7. **components/common/Tag** - Tag for Posts/Experiences/Stories

## 3rd Party Services Used

1. Firebase Client SDK
2. REST API (Django Rest Framework)
3. MapBox
