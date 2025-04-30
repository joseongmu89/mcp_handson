# mcp_handson

설치 과정 

1. Cursor AI 회원가입 및 설치 계정 확인후 체험판 2주

2. Python 사용을 위한 uv 설치
curl -LsSf https://astral.sh/uv/install.sh | sh
윈도우: powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
환경변수 설정

3. 파이썬 설치
환경변수 설정

4. npx 실행을 위한 Node 설치 
환경변수 설정

———실제 MCP 서버 개발———

1. uv 다운로드 
curl -LsSf https://astral.sh/uv/install.sh | sh

2. 프로젝트 생성
# Create a new directory for our project
uv init weather
cd weather

# Create virtual environment and activate it
uv venv
source .venv/bin/activate

# Install dependencies
uv add "mcp[cli]" httpx

# Create our server file
touch weather.py

<pre><code>
{
  "mcpServers": {
    "weather": {
      "command": "uv",
      "args": [
        "--directory",
        "/Users/joseongmu/Desktop/MCP_TEST/weather",
        "run",
        "weather.py"
      ]
    }
  }
}
</code></pre>
