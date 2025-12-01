FROM mcr.microsoft.com/devcontainers/ruby:1-3.2-bullseye

# Install Node.js (needed for some Jekyll plugins)
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && curl -fsSL https://deb.nodesource.com/setup_18.x | bash - \
    && apt-get install -y nodejs \
    && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Install Jekyll and Bundler
RUN gem install jekyll bundler

# Set working directory
WORKDIR /workspace

# Expose Jekyll server port
EXPOSE 4000 35729