FROM python:3.13.11-slim

COPY --from=ghcr.io/astral-sh/uv:latest uv/ /bin/

WORKDIR app/

ENV PATH="/app/.venv/bin:$PATH"

COPY ".python-version" "pyproject.toml" "uv.lock" ./

RUN uv sync --locked

COPY notebook_1.py ./

ENTRYPOINT ["python","notebook_1.py"]