Greenlight Project
====

# Endpoint Overview

| Method | URL Pattern | Action |
| -- | -- | -- |
| GET | /v1/healthcheck | Show application health and version information | 
| GET | /v1/movies | Show the details of all movies | 
| POST | /v1/movies | Create a new movie | 
| GET | /v1/movies/:id | Show the details of a specific movie |
| PATCH | /v1/movies/:id | Update the details of a specific movie |
| DELETE | /v1/movies/:id | Delete a specific movie |
| POST | /v1/users | Register a new user |
| PUT | /v1/users/activated | Activate a specific user |
| PUT | /v1/users/password | Update the password for a specific user | 
| POST | /v1/tokens/authentication | Generate a new authentication token |
| POST | /v1/tokens/password-reset | Generate a new password-reset token |
| GET | /debug/vars | Display application metrics | 

# Lessons
1. Project Setup
  - Generate the  skeleton directory structure
    - bin contains binaries ready for deployment
    - cmd/api contains app-specific code
    - internal contains ancillary packages
    - migrations contain SQL mgiration files
    - remote contains config and setup scripts for prod
    - go.mod declare proj dependencies, versions, and module path
    - Makefiles contain recipes for automating admin tasks

  ```bash
  mkdir -p bin cmd/api internal migrations remote
  touch Makefile
  touch cmd/api/main.go

  ```
   
  - A Basic HTTP Server
    - Setup server
    - Setup healthcheck handler
    - ```httprouter``` handles request method compared to ```http.ServeMux```

# Notes
