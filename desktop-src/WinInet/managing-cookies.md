---
title: Gestion des cookies
description: Sous le protocole http, un serveur ou un script utilise des cookies pour conserver les informations d’État sur la station de travail cliente.
ms.assetid: c00279cf-9cdc-4caf-8549-af1851edfa25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0931de8b1d9d25862344658bddaacf5fd1d4325f9343176acb0206dcb3e1e383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113619"
---
# <a name="managing-cookies"></a>Gestion des cookies

Sous le protocole http, un serveur ou un script utilise des cookies pour conserver les informations d’État sur la station de travail cliente. Les fonctions WinINet ont implémenté une base de données de cookies persistante à cet effet. Ils peuvent être utilisés pour définir des cookies dans et y accéder à partir de la base de données de cookies. Pour plus d’informations, consultez [cookies http](http-cookies.md).

Les fonctions [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) et [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) peuvent être utilisées pour gérer les cookies.

## <a name="using-cookie-functions"></a>Utilisation des fonctions de cookie

Les fonctions suivantes permettent à une application de créer ou de récupérer des cookies dans la base de données de cookies.



| Fonction                                       | Description                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | Récupère les cookies pour l’URL spécifiée et toutes ses URL parentes. |
| [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | Définit un cookie sur l’URL spécifiée.                              |



 

Notez que ces fonctions ne nécessitent pas d’appel à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). les cookies qui ont une date d’expiration sont stockés dans le compte utilisateurs locaux sous les utilisateurs \\ « nom d’utilisateur » \\ AppData \\ itinérance \\ microsoft \\ Windows \\ les cookies, et les utilisateurs \\ « nom d’utilisateur » \\ appdata \\ itinérant \\ microsoft \\ Windows \\ cookies \\ bas répertoire pour les applications qui s’exécutent avec des privilèges faibles. Les cookies qui n’ont pas de date d’expiration sont stockés en mémoire et ne sont disponibles que pour le processus dans lequel ils ont été créés.

Comme indiqué dans la rubrique [http cookies](http-cookies.md) , la fonction [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) ne retourne pas les cookies marqués par le serveur comme étant non scriptables avec l’attribut « HttpOnly » dans l’en-tête Set-Cookie.

### <a name="getting-a-cookie"></a>Obtention d’un cookie

[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) retourne les cookies pour l’URL spécifiée et toutes ses URL parentes.

L’exemple suivant illustre un appel à [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).


```C++
TCHAR szURL[256];         // buffer to hold the URL
LPTSTR lpszData = NULL;   // buffer to hold the cookie data
DWORD dwSize=0;           // variable to get the buffer size needed

// Insert code to retrieve the URL.

retry:

// The first call to InternetGetCookie will get the required
// buffer size needed to download the cookie data.
if (!InternetGetCookie(szURL, NULL, lpszData, &dwSize))
{
    // Check for an insufficient buffer error.
    if (GetLastError()== ERROR_INSUFFICIENT_BUFFER)
    {
        // Allocate the necessary buffer.
        lpszData = new TCHAR[dwSize];

        // Try the call again.
        goto retry;
    }
    else
    {
        // Insert error handling code.
    }
}
else
{
    // Insert code to display the cookie data.

    // Release the memory allocated for the buffer.
    delete[]lpszData;
}
```



### <a name="setting-a-cookie"></a>Définition d’un cookie

[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) est utilisé pour définir un cookie sur l’URL spécifiée. [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) peut créer des cookies persistants et de session.

Les cookies persistants ont une date d’expiration. ces cookies sont stockés dans le compte utilisateurs locaux sous utilisateurs \\ « nom d’utilisateur » \\ appdata \\ itinérant \\ microsoft \\ Windows \\ les cookies, et les utilisateurs \\ « nom d’utilisateur » \\ appdata \\ itinérants \\ \\ de microsoft Windows \\ cookies \\ bas répertoire pour les applications qui s’exécutent avec des privilèges faibles.

Les cookies de session sont stockés en mémoire et sont accessibles uniquement par le processus qui les a créés.

Les données du cookie doivent être au format :

``` syntax
NAME=VALUE
```

Pour la date d’expiration, le format doit être :

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

DAY est l’abréviation à trois lettres du jour de la semaine, DD est le jour du mois, MMM est l’abréviation à trois lettres du mois, YYYY est l’année et HH : MM : SS est l’heure de la journée en heure militaire.

L’exemple suivant illustre deux appels à [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea). Le premier appel crée un cookie de session et le second crée un cookie persistant.


```C++
BOOL bReturn;

// Create a session cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
            TEXT("TestData = Test"));

// Create a persistent cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
           TEXT("TestData = Test; expires = Sat,01-Jan-2000 00:00:00 GMT"));

```



> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 