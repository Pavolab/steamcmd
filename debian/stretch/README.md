[![MicroBadger Size](https://img.shields.io/microbadger/image-size/pavolab/steamcmd/stretch.svg?style=for-the-badge)](https://microbadger.com/#/images/pavolab/steamcmd)
[![Docker Automated build](https://img.shields.io/docker/automated/pavolab/steamcmd.svg?style=for-the-badge)](https://hub.docker.com/r/pavolab/steamcmd/)
[![Docker Build Status](https://img.shields.io/docker/build/pavolab/steamcmd.svg?style=for-the-badge)](https://hub.docker.com/r/pavolab/steamcmd/)
[![GitHub](https://img.shields.io/github/license/pavolab/steamcmd.svg?style=for-the-badge)](https://github.com/pavolab/steamcmd/blob/master/LICENSE)

# Supported tags and respective `Dockerfile` links

-	[`bionic` (ubuntu/bionic/Dockerfile)](https://github.com/pavolab/steamcmd/blob/master/ubuntu/bionic/Dockerfile)
-	[`stretch`, `debian` (*debian/stretch/Dockerfile*)](https://github.com/pavolab/steamcmd/blob/master/debian/stretch/Dockerfile)

----------------

# SteamCMD
![SteamCMD](../../docs/logo.png)

The Steam Console Client or SteamCMD is a command-line version of the Steam client. Its primary use is to install and update various dedicated servers available on Steam using a command-line interface. It works with games that use the SteamPipe content system. All games have been migrated from the deprecated HLDSUpdateTool to SteamCMD.

----------------

# Get Image

```bash
docker pull pavolab/steamcmd
```

----------------

# How to use this image

```bash
$ docker run -it pavolab/steamcmd
```

----------------

# Required Ports for Steam
Which ports do I need to open for Steam?

| To log into Steam and download content |
|----------------------------------------|
| HTTP (TCP port 80) and HTTPS (443)     |
| UDP 27015 through 27030                |
| TCP 27015 through 27030                |

| Steam Client                                                  |
|---------------------------------------------------------------|
| UDP 27000 to 27015 inclusive (Game client traffic)            |
| UDP 27015 to 27030 inclusive (Typically Matchmaking and HLTV) |
| UDP 27031 and 27036 (incoming, for In-Home Streaming)         |
| TCP 27036 and 27037 (incoming, for In-Home Streaming)         |
| UDP 4380                                                      |

| Dedicated or Listen Servers |
|-----------------------------|
|TCP 27015 (SRCDS Rcon port)  |

| Streamworks P2P Networking and Steam Voice Chat |
|-------------------------------------------------|
| UDP 3478 (Outbound)                             |
| UDP 4379 (Outbound)                             |
| UDP 4380 (Outbound)                             |

----------------

# Package: steamcmd
Steam (http://www.steampowered.com) is a software content delivery system developed by Valve software (http://www.valvesoftware.com). There is some free software available, but for the most part the content delivered is non-free.

The Steam Console Client or SteamCMD is a command-line version of the Steam client. Its primary use is to install and update various dedicated servers available on Steam using a command-line interface.

This package comes with a fairly substantial non-free license agreement that must be accepted before installing the software.