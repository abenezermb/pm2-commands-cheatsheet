# pm2-commands-cheatsheet
1. Get logs
pm2 logs my-app
pm2 logs my-app --lines 100    # show the last 100 lines
pm2 logs my-app --error        # only stderr
pm2 logs my-app --out          # only stdout

tail -f ~/.pm2/logs/my-app-out.log
tail -f ~/.pm2/logs/my-app-error.log

pm2 logs my-app --raw | jq .

2. Start app directly
pm2 start app.js --name my-app

3. Reload an app
pm2 reload my-app

4. Stop an app
pm2 stop my-app

5. Restart an app
pm2 restart my-app

6. Delete an app
pm2 delete my-app

