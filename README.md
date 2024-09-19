# Greenlight
Greenlight is a movie API similar to IMDb (albeit with far less information). This project was created in following Alex Edwards's Let's Go Further book.

## Sample response
```json
{
    "id": 1,
    "title": "The Breakfast Club",
    "year": 1985,
    "runtime": "97 mins",
    "genres": [
        "comedy"
    ]
}
```

## Features
- REST API supporting GET, POST, PUT, PATCH, and DELETE requests
- PostgreSQL database
- User accounts and automatic email activation using Mailtrap
- Token-based user authentication
- Multiple user permission levels for read/write
- API rate limiting
- Request pagination

## Command line
This application accepts several command line arguments to configure the program.
| Flag                 | Default value                             | Description                               |
|----------------------|-------------------------------------------|-------------------------------------------|
| `-port`              | `4000`                                    | API server port                           |
| `-env`               | `"development"`                           | Environment (`development`,`staging`,`production`) |
| `-db-dsn`            | `""`                                      | PostgreSQL DSN                            |
| `-db-max-open-conns` | `25`                                      | PostgreSQL max open connections           |
| `-db-max-idle-conns` | `25`                                      | PostgreSQL max idle connections           |
| `-db-max-idle-time`  | `"15m"`                                   | PostgreSQL max connection idle time       |
| `-limiter-rps`       | `2`                                       | Rate limiter maximum requests per second  |
| `-limiter-burst`     | `4`                                       | Rate limiter maximum burst                |
| `-limiter-enabled`   | `true`                                    | Enable rate limiter                       |
| `-smtp-host`         | `"sandbox.smtp.mailtrap.io"`              | SMTP host                                 |
| `-smtp-port`         | `25`                                      | SMTP port                                 |
| `-smtp-username`     | `""`                      | SMTP username                             |
| `-smtp-password`     | `""`                       | SMTP password                             |
| `-smtp-sender`       | `""` | SMTP sender                         |


## Deployment
This API was deployed using a Digital Ocean droplet, however the droplet is no longer active.