FROM alpine:latest

# Set the environment variables for platform and build info
# The values are automatically set by 'docker buildx'
ARG TARGETPLATFORM
ARG TARGETARCH
ARG BUILDPLATFORM
ARG BUILDARCH

# Check tartet platform and build platform
RUN echo "TARGET_PLATFORM=${TARGETPLATFORM}, TARGET_ARCH=${TARGETARCH}" && \
    echo "BUILD_PLATFORM=${BUILDPLATFORM}, BUILD_ARCH=${BUILDARCH}" && \
    echo "BASE_IMAGE_ARG_NAME=${BASE_IMAGE_ARG_NAME}"

# Install command (just for sample)
WORKDIR /home
COPY ./install-${BUILDARCH}.sh /home
RUN echo "run /home/install-${BUILDARCH}.sh" && /home/install-${BUILDARCH}.sh \
    && rm /home/install-${BUILDARCH}.sh
