---
title: Cookies HTTP
description: Les cookies HTTP fournissent au serveur un mécanisme de stockage et de récupération des informations d’État sur le système de l’application cliente.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ba5b2d3917ea8f140e334f5f78b1bd730908d25506d9023667403410833c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113713"
---
# <a name="http-cookies"></a>Cookies HTTP

Les cookies HTTP fournissent au serveur un mécanisme de stockage et de récupération des informations d’État sur le système de l’application cliente. Ce mécanisme permet aux applications basées sur le Web de stocker des informations sur les éléments sélectionnés, les préférences de l’utilisateur, les informations d’enregistrement et d’autres informations qui peuvent être récupérées ultérieurement.

## <a name="cookie-related-headers"></a>En-têtes de Cookie-Related

Il existe deux en-têtes, Set-Cookie et cookie, qui sont liés aux cookies. L’en-tête Set-Cookie est envoyé par le serveur en réponse à une requête HTTP, qui est utilisée pour créer un cookie sur le système de l’utilisateur. L’en-tête de cookie est inclus par l’application cliente avec une requête HTTP envoyée à un serveur, si un cookie a un domaine et un chemin d’accès correspondants.

### <a name="set-cookie-header"></a>En-tête Set-Cookie

L’en-tête de réponse Set-Cookie utilise le format suivant :

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

Une ou plusieurs séquences de chaînes (séparées par des points-virgules) qui suivent la = *valeur* de nom de modèle doivent être incluses dans l’en-tête de réponse Set-Cookie. Le serveur peut utiliser ces séquences de chaînes pour stocker des données sur le système du client.

La date d’expiration est définie à l’aide du format Expires =*Date*, où *Date* est la date d’expiration à l’heure de Greenwich (GMT). Si la date d’expiration n’est pas définie, le cookie expire après la fin de la session Internet. Dans le cas contraire, le cookie est conservé dans le cache jusqu’à la date d’expiration. La date doit utiliser le format suivant :

*jour*, *JJ* - *MMM* - *aaaa* *hh*:*mm*:*SS* GMT

<dl> <dt>

<span id="DAY"></span><span id="day"></span>*TEMPS*
</dt> <dd>

Jour de la semaine (Dim, Môn, Mar, Wed, Thou, Ven, SAT).

</dd> <dt>

<span id="DD"></span><span id="dd"></span>*JJ*
</dt> <dd>

Jour du mois (par exemple, 01 pour le premier jour du mois).

</dd> <dt>

<span id="MMM"></span><span id="mmm"></span>*MMM*
</dt> <dd>

Abréviation à trois lettres du mois (Jan, fév, Mar, avr, mai, juin, Jul, aoû, Sep, Oct, Nov, DEC).

</dd> <dt>

<span id="YYYY"></span><span id="yyyy"></span>*AAA*
</dt> <dd>

Année.

</dd> <dt>

<span id="HH"></span><span id="hh"></span>*HH*
</dt> <dd>

La valeur de l’heure en heure militaire (22 serait de 10:00 P.M., par exemple).

</dd> <dt>

<span id="MM"></span><span id="mm"></span>*MM*
</dt> <dd>

Valeur de minute.

</dd> <dt>

<span id="SS"></span><span id="ss"></span>*SÉCURITÉ*
</dt> <dd>

Seconde valeur.

</dd> </dl>

La spécification du nom de domaine, à l’aide du modèle domaine =*\_ nom de domaine*, est facultative pour les cookies persistants et est utilisée pour indiquer la fin du domaine pour lequel le cookie est valide. Les cookies de session qui spécifient un domaine sont rejetés. Si le nom de domaine spécifié se termine par la demande, le cookie tente de faire correspondre le chemin d’accès pour déterminer si le cookie doit être envoyé. Par exemple, si le nom de domaine se termine par. microsoft.com, les demandes adressées à home.microsoft.com et support.microsoft.com sont vérifiées pour voir si le modèle spécifié correspond à la requête. Le nom de domaine doit comporter au moins deux ou trois périodes pour empêcher la définition de cookies pour les fins de nom de domaine largement utilisées, telles que. com,. edu et co.jp. Les noms de domaine autorisés sont similaires à. microsoft.com,. someschool.edu et. someserver.co.jp. Seuls les hôtes au sein du domaine spécifié peuvent définir un cookie pour un domaine.

La définition du chemin d’accès, à l’aide du modèle Path =*some \_ path*, est facultative et peut être utilisée pour spécifier un sous-ensemble des URL pour lesquelles le cookie est valide. Si un chemin d’accès est spécifié, le cookie est considéré comme valide pour toutes les demandes qui correspondent à ce chemin d’accès. Par exemple, si le chemin d’accès spécifié est/example, les demandes avec les chemins d’accès/ExampleCode et/example/code.htm correspondent. Si aucun chemin d’accès n’est spécifié, le chemin d’accès est supposé être le chemin d’accès de la ressource associée à l’en-tête Set-Cookie.

Le cookie peut également être marqué comme sécurisé, ce qui indique que le cookie peut être envoyé uniquement aux serveurs HTTPS.

Enfin, un cookie peut être marqué comme HttpOnly (les attributs ne respectent pas la casse), pour indiquer que le cookie est non scriptable et ne doit pas être révélé à l’application cliente pour des raisons de sécurité. dans Windows Internet, cela signifie que le cookie ne peut pas être récupéré via la fonction **InternetGetCookie** .

### <a name="cookie-header"></a>En-tête de cookie

L’en-tête de cookie est inclus avec toutes les requêtes HTTP qui ont un cookie dont le domaine et le chemin d’accès correspondent à la demande. L’en-tête du cookie a le format suivant :

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

Une ou plusieurs séquences de chaînes, à l’aide de la valeur de *nom* de format = , contiennent les informations qui ont été définies dans le cookie.

## <a name="generating-cookies"></a>Génération de cookies

il existe trois méthodes pour générer des cookies pour microsoft Internet Explorer : à l’aide de microsoft JScript, à l’aide des fonctions WinINet et à l’aide d’un script CGI. Toutes les méthodes doivent définir les informations qui sont incluses dans l’en-tête Set-Cookie.

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a>Génération d’un cookie à l’aide du modèle objet DHTML

À l’aide du modèle objet DHTML (Dynamic HTML), les cookies peuvent être définis en appelant la propriété **cookie** de l’objet document, comme indiqué dans l’exemple suivant.

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a>Génération d’un cookie à l’aide des fonctions WinInet

Les cookies peuvent être créés par des applications à l’aide de la fonction [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) . Pour plus d’informations, consultez [définition d’un cookie](managing-cookies.md).

### <a name="generating-a-cookie-using-a-cgi-script"></a>Génération d’un cookie à l’aide d’un script CGI

Les cookies sont générés en incluant un en-tête Set-Cookie dans le cadre d’un script CGI inclus dans la réponse HTTP à une demande.

L’exemple suivant est un script CGI qui comprend un en-tête Set-Cookie à l’aide de Perl.

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 