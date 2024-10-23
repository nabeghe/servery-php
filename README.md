# Servery for PHP.

> Provides easy access to certain details available in the global $_SERVER variable.

<hr>

## 🫡 Usage

### 🚀 Installation

You can install the package via composer:

```bash
composer require nabeghe/servery
```

<hr>

#### Example:

```php
use Nabeghe\Servery\Servery;
use Nabeghe\Servery\UserAgent;
use Nabeghe\Servery\WebServer;

echo "[[ Servery ]]\n<br>";
echo "Client IP = ".json_encode(Servery::getClientIP())."\n<br>";
echo "Server IP = ".json_encode(Servery::getServerIP())."\n<br>";
echo "Host Address = ".json_encode(Servery::getHostAddress())."\n<br>";
echo "Domain = ".json_encode(Servery::getDomain())."\n<br>";
echo "HTTPS = ".json_encode(Servery::isHttps())."\n<br>";
echo "URL Protocol = ".json_encode(Servery::getUrlProtocol())."\n<br>";
echo "Server Protocol = ".json_encode(Servery::getServerProtocol())."\n<br>";
echo "URL Scheme = ".json_encode(Servery::getUrlScheme())."\n<br>";
echo "Root URL = ".json_encode(Servery::getRootUrl())."\n<br>";
echo "Current URL = ".json_encode(Servery::getCurrentUrl())."\n<br>";
echo "Requested URL = ".json_encode(Servery::getRequestedUrl())."\n<br>"; // An alias for getRequestedUrl
echo "Requested Path = ".json_encode(Servery::getRequrestedPath())."\n<br>";
echo "Home URL = ".json_encode(Servery::getHomeUrl())."\n<br>";
echo "\n<br>";

echo "[[ UserAgent Handler ]]\n<br>";
echo "UserAgent = ".json_encode(UserAgent::getCurrent())."\n<br>";
echo "Browser Name = ".json_encode(UserAgent::detectBrowserName(UserAgent::getCurrent()))."\n<br>";
echo "Hash = ".json_encode(UserAgent::generateHash())."\n<br>";
echo "Simple Hash = ".json_encode(UserAgent::generateSimpleHash())."\n<br>";
echo "Is Bot = ".json_encode(UserAgent::detectBot())."\n<br>";
echo "Is Mobile = ".json_encode(UserAgent::detectMobile())."\n<br>";
echo "\n<br>";

echo "[[ UserAgent Handler Object ]]\n<br>";
echo "UserAgent = ".json_encode(UserAgent::instance()->getValue())."\n<br>";
echo "Browser Name = ".json_encode(UserAgent::instance()->getBrowserName())."\n<br>";
echo "Hash = ".json_encode(UserAgent::instance()->getHash())."\n<br>";
echo "Simple Hash = ".json_encode(UserAgent::instance()->getSimpleHash())."\n<br>";
echo "Is Bot = ".json_encode(UserAgent::instance()->isBot())."\n<br>";
echo "Is Mobile = ".json_encode(UserAgent::instance()->isMobile())."\n<br>";
echo "\n<br>";

echo "[[ WebServer Checker ]]\n<br>";
echo "Name = ".json_encode(WebServer::getName())."\n<br>";
echo "Is Apache = ".json_encode(WebServer::isApache())."\n<br>";
echo "Is IIS = ".json_encode(WebServer::isIIS())."\n<br>";
echo "Is IIS7 = ".json_encode(WebServer::isIIS7())."\n<br>";
echo "Is Litespeed = ".json_encode(WebServer::isLitespeed())."\n<br>";
echo "Is Nginx = ".json_encode(WebServer::isNginx())."\n<br>";
echo "Is PhpStorm = ".json_encode(WebServer::isPhpStorm())."\n<br>";
echo "\n<br>";
```

<hr>

## 📖 License

Copyright (c) Hadi Akbarzadeh

Licensed under the MIT license, see [LICENSE.md](LICENSE.md) for details.