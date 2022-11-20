---
sidebar_position: 2
---

# Authentication

This page contains a high-level overview of the authentication process in the app.

## Working Directories/File(s)

```
pages/auth/*
contexts/AuthContext.js
```

## Functionality

1. Login is performed through the REST API.
2. Registration is performed through the API.
3. Login is based on Email and Password.
4. Registration requires the following properties: Email, and Password. All other properties asked afterwards as part of the registration as for the profile.
5. The Auth Context hook has been used to access the REST API to get the Access Token.
6. Account can be reclaimed by going through the _Forgot Password_ process in case one forgets their password.
