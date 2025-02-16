# Octavius

A TreeHacks 2025 submission. Check out our Devpost [here (TODO)]()!

TODO

## Technical Overview

One of our major challenges for this hackathon was obtaining the camera feed from the Apple Vision Pro. It's difficult to access this raw data due to privacy reasons, so there were multiple hoops to jump through to be able to tinker with it.

Pipeline
- Apple Vision Pro screen mirrors to Macbook.
- Macbook joins a Zoom call and screenshares (entire screen).
- Second laptop joins Zoom call and views the screenshared content full-screen.
- Second laptop streams via OBS RTSP to Jetson Nano.
- Jetson Nano takes the stream and handles object tracking.
- TODO: bounding boxes, coordinates, picking up the object
- TODO: InterSystems?

Why Jetson Nano?
- We decided to use the Jetson Nano because of its processing power. Although jumping through so many hoops to get the video input there resulted in very high latency, this project serves as a POC for our general idea.
- Nano Owl is very low latency, which makes it appropriate for this use case.
ElevenLabs?
- This was used as an additional feature for the user to speak with a remote agent who can help guide them or dispatch support depending on the situation.

## Hardware

TODO

## References
- [NanoOwl Tutorial](https://www.jetson-ai-lab.com/vit/tutorial_nanoowl.html)
- [ElevenLabs Documentation](https://elevenlabs.io/docs/conversational-ai/libraries/python)
