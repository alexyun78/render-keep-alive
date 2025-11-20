# Render Keep-Alive

Render 무료 플랜 서버를 15분마다 자동으로 깨워서 슬립 모드 방지

## 📋 관리 중인 서버

- Daily Coffee: https://your-daily-coffee-app.onrender.com

## ⏰ 실행 주기

- 자동: 15분마다 (GitHub Actions)
- 수동: Actions 탭에서 "Run workflow" 클릭

## 🔧 새 서버 추가 방법

`.github/workflows/keep-alive.yml` 파일에 새 step 추가:

\`\`\`yaml
- name: Ping New Server
  run: |
    echo "🔔 Pinging new server..."
    curl -f https://new-app.onrender.com || echo "⚠️ Ping failed"
\`\`\`

## 📊 실행 기록

GitHub Actions 탭에서 확인 가능
```

## 5. .gitignore
```
# macOS
.DS_Store

# Windows
Thumbs.db

# IDE
.vscode/
.idea/