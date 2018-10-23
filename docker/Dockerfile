FROM ros:kinetic

RUN apt-get update && apt-get install -y \
  curl \
  netcat

EXPOSE 11311

# This container is healthy when the ROS port open is.
HEALTHCHECK --interval=5s --timeout=2s --retries=12 \
 CMD nc -z localhost 11311 || exit 1
