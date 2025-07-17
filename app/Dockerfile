# syntax=docker/dockerfile:1.7-labs
ARG LANG=C.UTF-8
ARG NODE_VERSION=24.4.1
FROM node:${NODE_VERSION} AS base

ENV PNPM_HOME="/pnpm"
ENV PATH="$PNPM_HOME:$PATH"

RUN corepack enable
COPY . /app
WORKDIR /app

FROM base AS prod-deps
RUN --mount=type=cache,id=pnpm,target=/pnpm/store pnpm install --prod --frozen-lockfile

FROM base AS dev-deps
RUN --mount=type=cache,id=pnpm,target=/pnpm/store pnpm install --frozen-lockfile

FROM base
COPY --from=prod-deps /app/node_modules /app/node_modules

CMD [ "pnpm", "run", "start" ]
