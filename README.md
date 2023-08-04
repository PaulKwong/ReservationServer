## Intro
The reservation system was originally designed and developed because the school activity room reservation process hopes to change from the previous cumbersome and inefficient completely offline reservation
It was modified to online reservation + offline stamp approval to reserve school activity rooms, which gradually evolved.

Currently developed with ASP.NET Core, deployed on Kubernetes

- Demo address: <https://reservation.weihanli.xyz>
- New version reservation client demo address: <https://reservation-client.weihanli.xyz> (angular + material SPA)
- REST API Swagger: <https://reservation.weihanli.xyz/swagger>

- Background login address: <https://reservation.weihanli.xyz/Admin/>

   Background login account:

   Administrator username: admin Password: Admin@888

   Ordinary user: Alice Password: Test@1234

   Administrators have more permissions, can set more system-related configurations, and can also add general system administrators

## About technology

Evolution of technology used:

ASP.NET WebForm => ASP.NET MVC => ASP.NET Core

Deployment method:

IIS => `Docker`+`nginx` => `kubernetes`+`nginx`

CI/CD:

appveyor => travis => Azure Pipeline

[Deployment Documentation](./docs/README.md)

## Roadmap

### 1.0

- [x] Event Room Reservations
- [x] Appointment Management
- [x] Event room management
- [x] Announcement management
- [x] User Management
- [x] Reservation blacklist management
- [x] System settings management
- [x] Appointments are disabled for a certain period of time, such as holidays/cold (summer) vacations, etc.

### 2.0

- [x] Event Room Reservation SPA <https://github.com/OpenReservation/ReservationServer/tree/dev/OpenReservation.Clients/ReservationClient> (angular8 + material)
- [x] WeChat Mini Program Reservation <https://github.com/OpenReservation/ReservationServer/tree/dev/OpenReservation.Clients/WxAppClient>
- [x] From stand-alone to cluster, detailed modification reference: <https://www.cnblogs.com/weihanli/p/aspnetcore-migrate-standalone-to-cluster.html>

### 3.0

- [x] Multilingual support
- [x] user system (requires login to make an appointment, login supports Github login)
- [x] My Appointment Records
- [x] cancel appointment

### 4.0

- [ ] A more general booking process
- [ ] Add the concept of organization, multi-tenancy
- [ ] ReservationService as a Service, creating a Saas reservation service platform

## Contact

Contact me if you need: <paulkwong622@gmail.com>

# OpenReservation [![Build Status](https://weihanli.visualstudio.com/Pipelines/_apis/build/status/OpenReservation.ReservationServer?branchName=dev)](https://weihanli.visualstudio.com/Pipelines/_build /latest?definitionId=7&branchName=dev)
