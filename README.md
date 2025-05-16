Here’s a clean, well-formatted reference for your PM2 commands:

---

## 1. Viewing Logs for a Specific Process

```bash
# Tail both stdout + stderr
pm2 logs my-app

# Tail last 100 lines
pm2 logs my-app --lines 100

# Tail stderr only
pm2 logs my-app --error

# Tail stdout only
pm2 logs my-app --out

# Follow stdout log file directly
tail -f ~/.pm2/logs/my-app-out.log

# Follow stderr log file directly
tail -f ~/.pm2/logs/my-app-error.log

# Stream raw logs and pretty-print JSON entries
pm2 logs my-app --raw | jq .
```

---

## 2. Managing Your App

```bash
# Start the app
pm2 start app.js --name my-app

# Reload (zero-downtime)
pm2 reload my-app

# Stop the app
pm2 stop my-app

# Restart the app
pm2 restart my-app

# Delete the app from PM2 process list
pm2 delete my-app
```
