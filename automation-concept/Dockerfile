FROM python:3.12-slim-bookworm

COPY --from=ghcr.io/astral-sh/uv:0.8.2 /uv /uvx /bin/

ADD . /api

WORKDIR /api

RUN uv sync --locked

CMD ["uv", "run", "uvicorn", "src.main:api", "--host", "0.0.0.0", "--port", "8080"]
