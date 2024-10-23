## Build a Stackoverflow app

Tech Stack:
Python 3.x, FastAPI, DB?, htmx, Ruff, Git, docker, pytest, CI/CD pipeline

Scope:
User should able to register/login to an account
User should able to Post a question
User should able to answer a question
User should able to vote(up/down) for an answer
User should able to add comments to an answer
User should able to search keywords(deferred for later use) for the topic of interest

Tables:
User:
    id
    full_name
    email
    password
    created_at
Question:
    id
    unique_id
    title
    description
    user(id)
    created_at
Answer:
    id
    question(id)
    description
    user(id)
    created_at
Vote:
    user(id)
    answer(id)
    type(up/down)
    created_at
Comment:
    user(id)
    answer(id)
    description
    created_at

# Code reference - https://github.com/fastapi/full-stack-fastapi-template/blob/master/backend
Steps:
    setup venv
    Install packages - fastapi "uvicorn[standard]" ruff pytest sqlmodel
    Initialize Git and repository
    Setup pre-commit (https://pre-commit.com/)
    create app package and core modules(db, config, api), follow main.py
    initialize app and run first sample api endpoint at home