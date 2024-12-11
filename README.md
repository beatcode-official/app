# BeatCode
BeatCode is a platform providing head-to-head LeetCode-like coding battles.

## Installation
Below are the commands to get the server up and running, for specific details please visit the README.md of each individual repo.

First clone this repo:
```bash
git clone https://github.com/beatcode-official/app.git
cd app
```

### 1. Frontend
#### Prerequisites
- Node.js v20.0+

#### Setup
Install dependencies
```bash
cd beatcode-client
npm install
```

#### Configuration
Copy the .env.example to a new file and name it .env (place in the same folder).

The default settings specified should have everything work out of the box, but if you need to change anything, the settings to change are pretty self-explanatory.

#### Running
```
npm build
npm run preview
```

#### Testing
**Unit Tests**
```bash
npm test
```

**End-to-end (E2E) Tests**
⚠️ Please have the frontend and backend running in another terminal before testing.
```bash
npm run test:e2e
```


### 2. Backend
#### Prerequisites
- Python v3.11
- PostgreSQL database installed and running
- Docker Engine installed and running

#### Setup
Navigate into the folder
```bash
cd beatcode-client
```

[OPTIONAL] Create a new Python virtual environment
```bash
python -m venv venv
venv/Scripts/Activate # For Windows
source venv/bin/activate # For Linux
```

Install the required Python dependencies
```bash
python -m pip install -r requirements.txt
```

Copy the .env.example to a new file and name it .env (place in the same folder).

Variables you'll likely need to change to match your system settings are:

```
1. DB_USER, DB_PASSWORD, DB_HOST
2. TEST_DB_USER, TEST_DB_PASSWORD, TEST_DB_HOST
3. RESEND_API_KEY (leave as default if you don't possess one)
4. FRONTEND_URL
5. SECRET_KEY
6. OPENAI_API_KEY (leave as default if you don't possess one)
```

Initialize the database
```bash
cd app
python -m db.init --drop --droptest
```

#### Running
Start the server
```bash
uvicorn main:app
```

#### Testing
Please set the .env variable `TESTING` to `True` before testing.
**Unit Test**
```bash
pytest tests/unit -sv # Test all components
pytest tests/unit/code_execution_test.py # Test a single component
pytest tests/unit/problem_test.py # Test a single component
```

**Integration Test**
```bash
python tests/integration/auth_test.py # Test authentication endpoints
python tests/integration/game_test.py # Test game endpoints
python tests/integration/room_test.py # Test room endpoints
```

## Other Notes
- We used for GPT-4o for test case generation and runtime analysis.
