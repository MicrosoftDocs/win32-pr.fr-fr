---
title: Cookies HTTP
description: Les cookies HTTP fournissent au serveur un mécanisme de stockage et de récupération des informations d’État sur le système de l’application cliente.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6855f0b105dc73760541bf9eb7a6da80dfb38e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513531"
---
# <a name="http-cookies"></a><span data-ttu-id="329f0-103">Cookies HTTP</span><span class="sxs-lookup"><span data-stu-id="329f0-103">HTTP Cookies</span></span>

<span data-ttu-id="329f0-104">Les cookies HTTP fournissent au serveur un mécanisme de stockage et de récupération des informations d’État sur le système de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="329f0-104">HTTP cookies provide the server with a mechanism to store and retrieve state information on the client application's system.</span></span> <span data-ttu-id="329f0-105">Ce mécanisme permet aux applications basées sur le Web de stocker des informations sur les éléments sélectionnés, les préférences de l’utilisateur, les informations d’enregistrement et d’autres informations qui peuvent être récupérées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="329f0-105">This mechanism allows web-based applications the ability to store information about selected items, user preferences, registration information, and other information that can be retrieved later.</span></span>

## <a name="cookie-related-headers"></a><span data-ttu-id="329f0-106">En-têtes de Cookie-Related</span><span class="sxs-lookup"><span data-stu-id="329f0-106">Cookie-Related Headers</span></span>

<span data-ttu-id="329f0-107">Il existe deux en-têtes, Set-Cookie et cookie, qui sont liés aux cookies.</span><span class="sxs-lookup"><span data-stu-id="329f0-107">There are two headers, Set-Cookie and Cookie, that are related to cookies.</span></span> <span data-ttu-id="329f0-108">L’en-tête Set-Cookie est envoyé par le serveur en réponse à une requête HTTP, qui est utilisée pour créer un cookie sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="329f0-108">The Set-Cookie header is sent by the server in response to an HTTP request, which is used to create a cookie on the user's system.</span></span> <span data-ttu-id="329f0-109">L’en-tête de cookie est inclus par l’application cliente avec une requête HTTP envoyée à un serveur, si un cookie a un domaine et un chemin d’accès correspondants.</span><span class="sxs-lookup"><span data-stu-id="329f0-109">The Cookie header is included by the client application with an HTTP request sent to a server, if there is a cookie that has a matching domain and path.</span></span>

### <a name="set-cookie-header"></a><span data-ttu-id="329f0-110">En-tête Set-Cookie</span><span class="sxs-lookup"><span data-stu-id="329f0-110">Set-Cookie Header</span></span>

<span data-ttu-id="329f0-111">L’en-tête de réponse Set-Cookie utilise le format suivant :</span><span class="sxs-lookup"><span data-stu-id="329f0-111">The Set-Cookie response header uses the following format:</span></span>

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

<span data-ttu-id="329f0-112">Une ou plusieurs séquences de chaînes (séparées par des points-virgules) qui suivent la = *valeur* de nom de modèle doivent être incluses dans l’en-tête de réponse Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="329f0-112">One or more string sequences (separated by semicolons) that follow the pattern *name*=*value* must be included in the Set-Cookie response header.</span></span> <span data-ttu-id="329f0-113">Le serveur peut utiliser ces séquences de chaînes pour stocker des données sur le système du client.</span><span class="sxs-lookup"><span data-stu-id="329f0-113">The server can use these string sequences to store data on the client's system.</span></span>

<span data-ttu-id="329f0-114">La date d’expiration est définie à l’aide du format Expires =*Date*, où *Date* est la date d’expiration à l’heure de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="329f0-114">The expiration date is set by using the format expires=*date*, where *date* is the expiration date in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="329f0-115">Si la date d’expiration n’est pas définie, le cookie expire après la fin de la session Internet.</span><span class="sxs-lookup"><span data-stu-id="329f0-115">If the expiration date is not set, the cookie expires after the Internet session ends.</span></span> <span data-ttu-id="329f0-116">Dans le cas contraire, le cookie est conservé dans le cache jusqu’à la date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="329f0-116">Otherwise, the cookie is persisted in the cache until the expiration date.</span></span> <span data-ttu-id="329f0-117">La date doit utiliser le format suivant :</span><span class="sxs-lookup"><span data-stu-id="329f0-117">The date must use the following format:</span></span>

<span data-ttu-id="329f0-118">*jour*, *JJ* - *MMM* - *aaaa* *hh*:*mm*:*SS* GMT</span><span class="sxs-lookup"><span data-stu-id="329f0-118">*DAY*, *DD*-*MMM*-*YYYY* *HH*:*MM*:*SS* GMT</span></span>

<dl> <dt>

<span data-ttu-id="329f0-119"><span id="DAY"></span><span id="day"></span>*TEMPS*</span><span class="sxs-lookup"><span data-stu-id="329f0-119"><span id="DAY"></span><span id="day"></span>*DAY*</span></span>
</dt> <dd>

<span data-ttu-id="329f0-120">Jour de la semaine (Dim, Môn, Mar, Wed, Thou, Ven, SAT).</span><span class="sxs-lookup"><span data-stu-id="329f0-120">The day of the week (Sun, Mon, Tue, Wed, Thu, Fri, Sat).</span></span>

</dd> <dt>

<span data-ttu-id="329f0-121"><span id="DD"></span><span id="dd"></span>*JJ*</span><span class="sxs-lookup"><span data-stu-id="329f0-121"><span id="DD"></span><span id="dd"></span>*DD*</span></span>
</dt> <dd>

<span data-ttu-id="329f0-122">Jour du mois (par exemple, 01 pour le premier jour du mois).</span><span class="sxs-lookup"><span data-stu-id="329f0-122">The day in the month (such as 01 for the first day of the month).</span></span>

</dd> <dt>

<span data-ttu-id="329f0-123"><span id="MMM"></span><span id="mmm"></span>*MMM*</span><span class="sxs-lookup"><span data-stu-id="329f0-123"><span id="MMM"></span><span id="mmm"></span>*MMM*</span></span>
</dt> <dd>

<span data-ttu-id="329f0-124">Abréviation à trois lettres du mois (Jan, fév, Mar, avr, mai, juin, Jul, aoû, Sep, Oct, Nov, DEC).</span><span class="sxs-lookup"><span data-stu-id="329f0-124">The three-letter abbreviation for the month (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).</span></span>

</dd> <dt>

<span data-ttu-id="329f0-125"><span id="YYYY"></span><span id="yyyy"></span>*AAA*</span><span class="sxs-lookup"><span data-stu-id="329f0-125"><span id="YYYY"></span><span id="yyyy"></span>*YYYY*</span></span>
</dt> <dd>

<span data-ttu-id="329f0-126">Année.</span><span class="sxs-lookup"><span data-stu-id="329f0-126">The year.</span></span>

</dd> <dt>

<span data-ttu-id="329f0-127"><span id="HH"></span><span id="hh"></span>*HH*</span><span class="sxs-lookup"><span data-stu-id="329f0-127"><span id="HH"></span><span id="hh"></span>*HH*</span></span>
</dt> <dd>

<span data-ttu-id="329f0-128">La valeur de l’heure en heure militaire (22 serait de 10:00 P.M., par exemple).</span><span class="sxs-lookup"><span data-stu-id="329f0-128">The hour value in military time (22 would be 10:00 P.M., for example).</span></span>

</dd> <dt>

<span data-ttu-id="329f0-129"><span id="MM"></span><span id="mm"></span>*MM*</span><span class="sxs-lookup"><span data-stu-id="329f0-129"><span id="MM"></span><span id="mm"></span>*MM*</span></span>
</dt> <dd>

<span data-ttu-id="329f0-130">Valeur de minute.</span><span class="sxs-lookup"><span data-stu-id="329f0-130">The minute value.</span></span>

</dd> <dt>

<span data-ttu-id="329f0-131"><span id="SS"></span><span id="ss"></span>*SÉCURITÉ*</span><span class="sxs-lookup"><span data-stu-id="329f0-131"><span id="SS"></span><span id="ss"></span>*SS*</span></span>
</dt> <dd>

<span data-ttu-id="329f0-132">Seconde valeur.</span><span class="sxs-lookup"><span data-stu-id="329f0-132">The second value.</span></span>

</dd> </dl>

<span data-ttu-id="329f0-133">La spécification du nom de domaine, à l’aide du modèle domaine =*\_ nom de domaine*, est facultative pour les cookies persistants et est utilisée pour indiquer la fin du domaine pour lequel le cookie est valide.</span><span class="sxs-lookup"><span data-stu-id="329f0-133">Specifying the domain name, using the pattern domain=*domain\_name*, is optional for persistent cookies and is used to indicate the end of the domain for which the cookie is valid.</span></span> <span data-ttu-id="329f0-134">Les cookies de session qui spécifient un domaine sont rejetés.</span><span class="sxs-lookup"><span data-stu-id="329f0-134">Session cookies that specify a domain are rejected.</span></span> <span data-ttu-id="329f0-135">Si le nom de domaine spécifié se termine par la demande, le cookie tente de faire correspondre le chemin d’accès pour déterminer si le cookie doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="329f0-135">If the specified domain name ending matches the request, the cookie tries to match the path to determine if the cookie should be sent.</span></span> <span data-ttu-id="329f0-136">Par exemple, si le nom de domaine se termine par. microsoft.com, les demandes adressées à home.microsoft.com et support.microsoft.com sont vérifiées pour voir si le modèle spécifié correspond à la requête.</span><span class="sxs-lookup"><span data-stu-id="329f0-136">For example, if the domain name ending is .microsoft.com, requests to home.microsoft.com and support.microsoft.com would be checked to see if the specified pattern matches the request.</span></span> <span data-ttu-id="329f0-137">Le nom de domaine doit comporter au moins deux ou trois périodes pour empêcher la définition de cookies pour les fins de nom de domaine largement utilisées, telles que. com,. edu et co.jp.</span><span class="sxs-lookup"><span data-stu-id="329f0-137">The domain name must have at least two or three periods in it to prevent cookies from being set for widely used domain name endings, such as .com, .edu, and co.jp.</span></span> <span data-ttu-id="329f0-138">Les noms de domaine autorisés sont similaires à. microsoft.com,. someschool.edu et. someserver.co.jp.</span><span class="sxs-lookup"><span data-stu-id="329f0-138">Allowable domain names would be similar to .microsoft.com, .someschool.edu, and .someserver.co.jp.</span></span> <span data-ttu-id="329f0-139">Seuls les hôtes au sein du domaine spécifié peuvent définir un cookie pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="329f0-139">Only hosts within the specified domain can set a cookie for a domain.</span></span>

<span data-ttu-id="329f0-140">La définition du chemin d’accès, à l’aide du modèle Path =*some \_ path*, est facultative et peut être utilisée pour spécifier un sous-ensemble des URL pour lesquelles le cookie est valide.</span><span class="sxs-lookup"><span data-stu-id="329f0-140">Setting the path, using the pattern path=*some\_path*, is optional and can be used to specify a subset of the URLs for which the cookie is valid.</span></span> <span data-ttu-id="329f0-141">Si un chemin d’accès est spécifié, le cookie est considéré comme valide pour toutes les demandes qui correspondent à ce chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="329f0-141">If a path is specified, the cookie is considered valid for any requests that match that path.</span></span> <span data-ttu-id="329f0-142">Par exemple, si le chemin d’accès spécifié est/example, les demandes avec les chemins d’accès/ExampleCode et/example/code.htm correspondent.</span><span class="sxs-lookup"><span data-stu-id="329f0-142">For example, if the specified path is /example, requests with the paths /examplecode and /example/code.htm would match.</span></span> <span data-ttu-id="329f0-143">Si aucun chemin d’accès n’est spécifié, le chemin d’accès est supposé être le chemin d’accès de la ressource associée à l’en-tête Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="329f0-143">If no path is specified, the path is assumed to be the path of the resource associated with the Set-Cookie header.</span></span>

<span data-ttu-id="329f0-144">Le cookie peut également être marqué comme sécurisé, ce qui indique que le cookie peut être envoyé uniquement aux serveurs HTTPS.</span><span class="sxs-lookup"><span data-stu-id="329f0-144">The cookie can also be marked as secure, which specifies that the cookie can be sent only to https servers.</span></span>

<span data-ttu-id="329f0-145">Enfin, un cookie peut être marqué comme HttpOnly (les attributs ne respectent pas la casse), pour indiquer que le cookie est non scriptable et ne doit pas être révélé à l’application cliente pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="329f0-145">Finally, a cookie can be marked as HttpOnly (attributes are not case-sensitive), to indicate that the cookie is non-scriptable and should not be revealed to the client application, for security reasons.</span></span> <span data-ttu-id="329f0-146">Dans Windows Internet, cela signifie que le cookie ne peut pas être récupéré via la fonction **InternetGetCookie** .</span><span class="sxs-lookup"><span data-stu-id="329f0-146">Within Windows Internet, this means that the cookie cannot be retrieved through the **InternetGetCookie** function.</span></span>

### <a name="cookie-header"></a><span data-ttu-id="329f0-147">En-tête de cookie</span><span class="sxs-lookup"><span data-stu-id="329f0-147">Cookie Header</span></span>

<span data-ttu-id="329f0-148">L’en-tête de cookie est inclus avec toutes les requêtes HTTP qui ont un cookie dont le domaine et le chemin d’accès correspondent à la demande.</span><span class="sxs-lookup"><span data-stu-id="329f0-148">The Cookie header is included with any HTTP requests that have a cookie whose domain and path match the request.</span></span> <span data-ttu-id="329f0-149">L’en-tête du cookie a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="329f0-149">The Cookie header has the following format:</span></span>

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

<span data-ttu-id="329f0-150">Une ou plusieurs séquences de chaînes, à l’aide de la valeur de *nom* de format = , contiennent les informations qui ont été définies dans le cookie.</span><span class="sxs-lookup"><span data-stu-id="329f0-150">One or more string sequences, using the format *name*=*value*, contain the information that was set in the cookie.</span></span>

## <a name="generating-cookies"></a><span data-ttu-id="329f0-151">Génération de cookies</span><span class="sxs-lookup"><span data-stu-id="329f0-151">Generating Cookies</span></span>

<span data-ttu-id="329f0-152">Il existe trois méthodes pour générer des cookies pour Microsoft Internet Explorer : à l’aide de Microsoft JScript, à l’aide des fonctions WinINet et à l’aide d’un script CGI.</span><span class="sxs-lookup"><span data-stu-id="329f0-152">There are three methods for generating cookies for Microsoft Internet Explorer: using Microsoft JScript, using the WinINet functions, and using a CGI script.</span></span> <span data-ttu-id="329f0-153">Toutes les méthodes doivent définir les informations qui sont incluses dans l’en-tête Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="329f0-153">All of the methods need to set the information that is included in the Set-Cookie header.</span></span>

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a><span data-ttu-id="329f0-154">Génération d’un cookie à l’aide du modèle objet DHTML</span><span class="sxs-lookup"><span data-stu-id="329f0-154">Generating a Cookie Using the DHTML Object Model</span></span>

<span data-ttu-id="329f0-155">À l’aide du modèle objet DHTML (Dynamic HTML), les cookies peuvent être définis en appelant la propriété **cookie** de l’objet document, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="329f0-155">Using the Dynamic HTML (DHTML) object model, cookies can be set by calling the **cookie** property of the document object, as shown in the following example.</span></span>

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a><span data-ttu-id="329f0-156">Génération d’un cookie à l’aide des fonctions WinInet</span><span class="sxs-lookup"><span data-stu-id="329f0-156">Generating a Cookie Using the WinInet Functions</span></span>

<span data-ttu-id="329f0-157">Les cookies peuvent être créés par des applications à l’aide de la fonction [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) .</span><span class="sxs-lookup"><span data-stu-id="329f0-157">Cookies can be created by applications using the [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) function.</span></span> <span data-ttu-id="329f0-158">Pour plus d’informations, consultez [définition d’un cookie](managing-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="329f0-158">For more information, see [Setting a Cookie](managing-cookies.md).</span></span>

### <a name="generating-a-cookie-using-a-cgi-script"></a><span data-ttu-id="329f0-159">Génération d’un cookie à l’aide d’un script CGI</span><span class="sxs-lookup"><span data-stu-id="329f0-159">Generating a Cookie Using a CGI Script</span></span>

<span data-ttu-id="329f0-160">Les cookies sont générés en incluant un en-tête Set-Cookie dans le cadre d’un script CGI inclus dans la réponse HTTP à une demande.</span><span class="sxs-lookup"><span data-stu-id="329f0-160">Cookies are generated by including a Set-Cookie header as part of a CGI script included in the HTTP response to a request.</span></span>

<span data-ttu-id="329f0-161">L’exemple suivant est un script CGI qui comprend un en-tête Set-Cookie à l’aide de Perl.</span><span class="sxs-lookup"><span data-stu-id="329f0-161">The following example is a CGI script that includes a Set-Cookie header using Perl.</span></span>

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> <span data-ttu-id="329f0-162">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="329f0-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="329f0-163">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="329f0-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="329f0-164">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="329f0-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 