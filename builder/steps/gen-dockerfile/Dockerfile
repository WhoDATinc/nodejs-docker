FROM nvidia/cuda:9.0-cudnn7-devel-ubuntu16.04

# Add the runtime builder code
ADD contents/ /opt/nodejs-runtime-builder

ENV NODE_ENV=development

# Setup the runtime builder code
RUN cd /opt/nodejs-runtime-builder && npm install && npm run compile

ENTRYPOINT ["node", "/opt/nodejs-runtime-builder/build/src/main.js", "--app-dir", "/workspace"]
