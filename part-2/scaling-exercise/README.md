## Scaling Exercise ##

The project https://github.com/docker-hy/material-applications/tree/main/scaling-exercise is a barely working application. Go ahead and clone it for yourself. The project already includes docker-compose.yml so you can start it by running docker compose up.

The application should be accessible through http://localhost:3000. However it doesn't work well enough and we've added a load balancer for scaling. Your task is to scale the compute containers so that the button in the application turns green.

The "calculator" service has a user interface to send calculations to the "compute" service.

The "compute" service calculates a solution to a problem.

Please return the used commands for this exercise.

**Solution**

```$ docker compose up --scale compute=3```