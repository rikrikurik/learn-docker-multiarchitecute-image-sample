FROM alpine:latest

# Set the environment variables for platform and build info
# The values are automatically set by 'docker buildx'
ARG TARGETPLATFORM
ARG TARGETARCH
ARG BUILDPLATFORM
ARG BUILDARCH

# Check tartet platform and build platform
RUN echo "TARGET_PLATFORM=${TARGETPLATFORM}, TARGET_ARCH=${TARGETARCH}" && \
    echo "BUILD_PLATFORM=${BUILDPLATFORM}, BUILD_ARCH=${BUILDARCH}"

# Install g++ (just for sample)
RUN apk add --no-cache g++
