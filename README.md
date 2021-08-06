# SteamFlaskLogin

Небольшой класс позволяющий добавить вход на сайт с помощью сервиса Steam

Quick start
```pytohn
from steamlogin import SteamLogin
```
main func
```python
shouldLogin = request.args.get('login')

if shouldlogin is not None:
	steamlogin = SteamLoginn()
	return steamlogin.RedirectUser(steamlogin.ConstructURL('http://127.0.0.1:5000/login'))
return 'Click <a href="/?login=true">to login</a>'
```

login func
```python
returnData = request.values
steamlogin = SteamLogin()
steamID = steamlogin.ValidateResults(returnData)

if steamID is not False:
	return redirect(url_for('profile'))
else:
	return 'Failed to login'
```

Данный код представлен для личного использования
