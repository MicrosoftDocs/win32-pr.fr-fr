---
title: Gestion des cookies
description: Sous le protocole http, un serveur ou un script utilise des cookies pour conserver les informations d’État sur la station de travail cliente.
ms.assetid: c00279cf-9cdc-4caf-8549-af1851edfa25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0418442e961f6f4d3d2bcddb2c607ac9cf7928
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511305"
---
# <a name="managing-cookies"></a><span data-ttu-id="477fe-103">Gestion des cookies</span><span class="sxs-lookup"><span data-stu-id="477fe-103">Managing Cookies</span></span>

<span data-ttu-id="477fe-104">Sous le protocole http, un serveur ou un script utilise des cookies pour conserver les informations d’État sur la station de travail cliente.</span><span class="sxs-lookup"><span data-stu-id="477fe-104">Under the http protocol, a server or a script uses cookies to maintain state information on the client workstation.</span></span> <span data-ttu-id="477fe-105">Les fonctions WinINet ont implémenté une base de données de cookies persistante à cet effet.</span><span class="sxs-lookup"><span data-stu-id="477fe-105">The WinINet functions have implemented a persistent cookie database for this purpose.</span></span> <span data-ttu-id="477fe-106">Ils peuvent être utilisés pour définir des cookies dans et y accéder à partir de la base de données de cookies.</span><span class="sxs-lookup"><span data-stu-id="477fe-106">They can be used to set cookies in and access cookies from the cookie database.</span></span> <span data-ttu-id="477fe-107">Pour plus d’informations, consultez [cookies http](http-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="477fe-107">For more information, see [HTTP Cookies](http-cookies.md).</span></span>

<span data-ttu-id="477fe-108">Les fonctions [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) et [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) peuvent être utilisées pour gérer les cookies.</span><span class="sxs-lookup"><span data-stu-id="477fe-108">The [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) and [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) functions can be used to manage cookies.</span></span>

## <a name="using-cookie-functions"></a><span data-ttu-id="477fe-109">Utilisation des fonctions de cookie</span><span class="sxs-lookup"><span data-stu-id="477fe-109">Using Cookie Functions</span></span>

<span data-ttu-id="477fe-110">Les fonctions suivantes permettent à une application de créer ou de récupérer des cookies dans la base de données de cookies.</span><span class="sxs-lookup"><span data-stu-id="477fe-110">The following functions allow an application to create or retrieve cookies in the cookie database.</span></span>



| <span data-ttu-id="477fe-111">Fonction</span><span class="sxs-lookup"><span data-stu-id="477fe-111">Function</span></span>                                       | <span data-ttu-id="477fe-112">Description</span><span class="sxs-lookup"><span data-stu-id="477fe-112">Description</span></span>                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="477fe-113">**InternetGetCookie**</span><span class="sxs-lookup"><span data-stu-id="477fe-113">**InternetGetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | <span data-ttu-id="477fe-114">Récupère les cookies pour l’URL spécifiée et toutes ses URL parentes.</span><span class="sxs-lookup"><span data-stu-id="477fe-114">Retrieves cookies for the specified URL and all its parent URLs.</span></span> |
| [<span data-ttu-id="477fe-115">**InternetSetCookie**</span><span class="sxs-lookup"><span data-stu-id="477fe-115">**InternetSetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | <span data-ttu-id="477fe-116">Définit un cookie sur l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="477fe-116">Sets a cookie on the specified URL.</span></span>                              |



 

<span data-ttu-id="477fe-117">Notez que ces fonctions ne nécessitent pas d’appel à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="477fe-117">Note that these functions do not require a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="477fe-118">Les cookies qui ont une date d’expiration sont stockés dans le compte utilisateurs locaux sous utilisateurs \\ « nom d’utilisateur » \\ AppData \\ itinérant \\ Microsoft \\ Windows \\ cookies, et les utilisateurs \\ « nom d’utilisateur » \\ AppData \\ itinérants \\ Microsoft \\ Windows \\ cookies \\ bas Directory pour les applications qui s’exécutent avec des privilèges faibles.</span><span class="sxs-lookup"><span data-stu-id="477fe-118">Cookies that have an expiration date are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span> <span data-ttu-id="477fe-119">Les cookies qui n’ont pas de date d’expiration sont stockés en mémoire et ne sont disponibles que pour le processus dans lequel ils ont été créés.</span><span class="sxs-lookup"><span data-stu-id="477fe-119">Cookies that do not have an expiration date are stored in memory and are available only to the process in which they were created.</span></span>

<span data-ttu-id="477fe-120">Comme indiqué dans la rubrique [http cookies](http-cookies.md) , la fonction [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) ne retourne pas les cookies marqués par le serveur comme étant non scriptables avec l’attribut « HttpOnly » dans l’en-tête Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="477fe-120">As noted in the [HTTP Cookies](http-cookies.md) topic, the [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) function does not return cookies that have been marked by the server as non-scriptable with the "HttpOnly" attribute in the Set-Cookie header.</span></span>

### <a name="getting-a-cookie"></a><span data-ttu-id="477fe-121">Obtention d’un cookie</span><span class="sxs-lookup"><span data-stu-id="477fe-121">Getting a Cookie</span></span>

<span data-ttu-id="477fe-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) retourne les cookies pour l’URL spécifiée et toutes ses URL parentes.</span><span class="sxs-lookup"><span data-stu-id="477fe-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) returns the cookies for the specified URL and all its parent URLs.</span></span>

<span data-ttu-id="477fe-123">L’exemple suivant illustre un appel à [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span><span class="sxs-lookup"><span data-stu-id="477fe-123">The following example demonstrates a call to [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span></span>


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



### <a name="setting-a-cookie"></a><span data-ttu-id="477fe-124">Définition d’un cookie</span><span class="sxs-lookup"><span data-stu-id="477fe-124">Setting a Cookie</span></span>

<span data-ttu-id="477fe-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) est utilisé pour définir un cookie sur l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="477fe-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) is used to set a cookie on the specified URL.</span></span> <span data-ttu-id="477fe-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) peut créer des cookies persistants et de session.</span><span class="sxs-lookup"><span data-stu-id="477fe-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) can create both persistent and session cookies.</span></span>

<span data-ttu-id="477fe-127">Les cookies persistants ont une date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="477fe-127">Persistent cookies have an expiration date.</span></span> <span data-ttu-id="477fe-128">Ces cookies sont stockés dans le compte utilisateurs locaux sous utilisateurs \\ « nom d’utilisateur » \\ AppData \\ itinérant \\ Microsoft \\ Windows \\ cookies, et les utilisateurs \\ « nom d’utilisateur » \\ AppData \\ itinérants \\ Microsoft \\ Windows \\ cookies \\ bas Directory pour les applications qui s’exécutent avec des privilèges faibles.</span><span class="sxs-lookup"><span data-stu-id="477fe-128">These cookies are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span>

<span data-ttu-id="477fe-129">Les cookies de session sont stockés en mémoire et sont accessibles uniquement par le processus qui les a créés.</span><span class="sxs-lookup"><span data-stu-id="477fe-129">Session cookies are stored in memory and can be accessed only by the process that created them.</span></span>

<span data-ttu-id="477fe-130">Les données du cookie doivent être au format :</span><span class="sxs-lookup"><span data-stu-id="477fe-130">The data for the cookie should be in the format:</span></span>

``` syntax
NAME=VALUE
```

<span data-ttu-id="477fe-131">Pour la date d’expiration, le format doit être :</span><span class="sxs-lookup"><span data-stu-id="477fe-131">For the expiration date, the format must be:</span></span>

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

<span data-ttu-id="477fe-132">DAY est l’abréviation à trois lettres du jour de la semaine, DD est le jour du mois, MMM est l’abréviation à trois lettres du mois, YYYY est l’année et HH : MM : SS est l’heure de la journée en heure militaire.</span><span class="sxs-lookup"><span data-stu-id="477fe-132">DAY is the three-letter abbreviation for the day of the week, DD is the day of the month, MMM is the three-letter abbreviation for the month, YYYY is the year, and HH:MM:SS is the time of the day in military time.</span></span>

<span data-ttu-id="477fe-133">L’exemple suivant illustre deux appels à [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span><span class="sxs-lookup"><span data-stu-id="477fe-133">The following example demonstrates two calls to [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span></span> <span data-ttu-id="477fe-134">Le premier appel crée un cookie de session et le second crée un cookie persistant.</span><span class="sxs-lookup"><span data-stu-id="477fe-134">The first call creates a session cookie and the second creates a persistent cookie.</span></span>


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
> <span data-ttu-id="477fe-135">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="477fe-135">WinINet does not support server implementations.</span></span> <span data-ttu-id="477fe-136">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="477fe-136">In addition, it should not be used from a service.</span></span> <span data-ttu-id="477fe-137">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="477fe-137">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 