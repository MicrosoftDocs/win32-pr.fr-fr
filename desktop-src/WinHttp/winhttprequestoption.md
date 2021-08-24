---
description: comprend des options qui peuvent être définies ou récupérées pour la session Microsoft Windows HTTP Services (WinHTTP) actuelle.
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: Énumération WinHttpRequestOption
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestOption
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: ff4112538aff4c76c02e251f45e9dc78e6778633de6a5d93f6892dd87ff70c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051877"
---
# <a name="winhttprequestoption-enumeration"></a>Énumération WinHttpRequestOption

l’énumération **WinHttpRequestOption** comprend des options qui peuvent être définies ou récupérées pour la session Microsoft Windows HTTP Services (WinHTTP) actuelle.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WinHttpRequestOption { 
  WinHttpRequestOption_UserAgentString,
  WinHttpRequestOption_URL,
  WinHttpRequestOption_URLCodePage,
  WinHttpRequestOption_EscapePercentInURL,
  WinHttpRequestOption_SslErrorIgnoreFlags,
  WinHttpRequestOption_SelectCertificate,
  WinHttpRequestOption_EnableRedirects,
  WinHttpRequestOption_UrlEscapeDisable,
  WinHttpRequestOption_UrlEscapeDisableQuery,
  WinHttpRequestOption_SecureProtocols,
  WinHttpRequestOption_EnableTracing,
  WinHttpRequestOption_RevertImpersonationOverSsl,
  WinHttpRequestOption_EnableHttpsToHttpRedirects,
  WinHttpRequestOption_EnablePassportAuthentication,
  WinHttpRequestOption_MaxAutomaticRedirects,
  WinHttpRequestOption_MaxResponseHeaderSize,
  WinHttpRequestOption_MaxResponseDrainSize,
  WinHttpRequestOption_EnableHttp1_1,
  WinHttpRequestOption_EnableCertificateRevocationCheck
} WinHttpRequestOption;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption \_ UserAgentString**
</dt> <dd>

Définit ou récupère un **Variant** qui contient la chaîne de l' [*agent utilisateur*](glossary.md) .

</dd> <dt>

<span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**\_URL WinHttpRequestOption**
</dt> <dd>

Récupère une **variante** qui contient l’URL de la ressource. Cette valeur est en lecture seule ; vous ne pouvez pas définir l’URL à l’aide de cette propriété. L’URL ne peut pas être lue tant que la méthode [**Open**](iwinhttprequest-open.md) n’a pas été appelée. Cette option est utile pour vérifier l’URL une fois la méthode [**Send**](iwinhttprequest-send.md) terminée afin de vérifier si une redirection s’est produite.

</dd> <dt>

<span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption \_ URLCodePage**
</dt> <dd>

Définit ou récupère une valeur de **type Variant** qui identifie la [*page de codes*](glossary.md) de la chaîne d’URL. La valeur par défaut est la page de codes UTF-8. La page de codes est utilisée pour convertir la chaîne d’URL Unicode, transmise dans la méthode [**Open**](iwinhttprequest-open.md) , en une représentation sous forme de chaîne codée sur un octet.

</dd> <dt>

<span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption \_ EscapePercentInURL**
</dt> <dd>

Définit ou récupère une valeur de **type Variant** qui indique si les caractères de pourcentage de la chaîne d’URL sont convertis en séquence d’échappement. La valeur par défaut de cette option **est \_ true** , qui spécifie tous les caractères non sécurisés American National Standards Institute (ANSI), sauf que le symbole de pourcentage est converti en séquence d’échappement.

</dd> <dt>

<span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption \_ SslErrorIgnoreFlags**
</dt> <dd>

Définit ou récupère un **Variant** qui indique les erreurs de certificat de serveur qui doivent être ignorées. Il peut s’agir d’une combinaison d’un ou plusieurs des indicateurs suivants.



| Erreur                                                  | Valeur  |
|--------------------------------------------------------|--------|
| Autorité de certification inconnue ou racine non approuvée | 0x0100 |
| Utilisation incorrecte                                            | 0x0200 |
| Nom commun non valide (CN)                               | 0x1000 |
| Date ou certificat non valide expiré                    | 0x2000 |



 

La valeur par défaut de cette option dans la version 5,1 de WinHTTP est égale à zéro, ce qui entraîne l’ignorance d’aucune erreur. Dans les versions antérieures de WinHTTP, le paramètre par défaut était 0x3300, ce qui a entraîné l’ignorance de toutes les erreurs de certificat de serveur par défaut.

</dd> <dt>

<span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption \_ SelectCertificate**
</dt> <dd>

Définit une **variante** qui spécifie le certificat client envoyé à un serveur à des fins d’authentification. Cette option indique l’emplacement, le [*magasin de certificats*](glossary.md)et l’objet d’un certificat client délimité par des barres obliques inverses. Pour plus d’informations sur la sélection d’un certificat client, consultez [SSL dans WinHTTP](ssl-in-winhttp.md).

</dd> <dt>

<span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption \_ EnableRedirects**
</dt> <dd>

Définit ou récupère une valeur de **type Variant** qui indique si les demandes sont redirigées automatiquement lorsque le serveur spécifie un nouvel emplacement pour la ressource. La valeur par défaut de cette option **est \_ true** pour indiquer que les demandes sont automatiquement redirigées.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption \_ UrlEscapeDisable**
</dt> <dd>

Définit ou récupère une valeur de **type Variant** qui indique si les caractères non sécurisés dans les composants de chemin d’accès et de requête d’une URL sont convertis en séquences d’échappement. La valeur par défaut de cette option **est \_ true**, qui spécifie que les caractères du chemin d’accès et de la requête sont convertis.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption \_ UrlEscapeDisableQuery**
</dt> <dd>

Définit ou récupère une valeur de **type Variant** qui indique si les caractères non sécurisés dans le composant de requête de l’URL sont convertis en séquences d’échappement. La valeur par défaut de cette option **est \_ true**, qui spécifie que les caractères de la requête sont convertis.

</dd> <dt>

<span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption \_ SecureProtocols**
</dt> <dd>

Définit ou récupère un **Variant** qui indique les protocoles sécurisés qui peuvent être utilisés. Cette option sélectionne les protocoles acceptables pour le client. Le protocole est négocié au cours de la négociation de l’SSL (Secure Sockets Layer) (SSL). Il peut s’agir d’une combinaison d’un ou plusieurs des indicateurs suivants.



| Protocol                           | Valeur  |
|------------------------------------|--------|
| SSL 2.0                            | 0x0008 |
| SSL 3.0                            | 0x0020 |
| TLS (Transport Layer Security) 1,0 | 0x0080 |



 

La valeur par défaut de cette option est 0x0028, ce qui indique que SSL 2,0 ou SSL 3,0 peut être utilisé. Si cette option a la valeur zéro, le client et le serveur ne sont pas en mesure de déterminer un protocole de sécurité acceptable et l' [**envoi**](iwinhttprequest-send.md) suivant génère une erreur.

</dd> <dt>

<span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption \_ EnableTracing,**
</dt> <dd>

Définit ou récupère une valeur de **type Variant** qui indique si le traçage est actuellement activé. pour plus d’informations sur la fonction de trace dans Microsoft Windows HTTP Services (winhttp), consultez [winhttp trace facility](winhttptracecfg-exe--a-trace-configuration-tool.md).

</dd> <dt>

<span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption \_ RevertImpersonationOverSsl**
</dt> <dd>

Contrôle si l’objet [**WinHttpRequest**](winhttprequest.md) rétablit temporairement l’emprunt d’identité du client pendant la durée des opérations d’authentification du certificat SSL. Le paramètre par défaut de l’objet **WinHttpRequest** est **true**. Affectez la valeur **false** à cette option pour conserver l’emprunt d’identité lors de l’exécution d’opérations d’authentification par certificat.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption \_ EnableHttpsToHttpRedirects**
</dt> <dd>

Contrôle si WinHTTP autorise ou non les redirections. Par défaut, toutes les redirections sont automatiquement suivies, à l’exception de celles qui sont transférées d’une URL sécurisée (https) vers une URL non sécurisée (http). Affectez la valeur **true** à cette option pour activer le protocole HTTPS sur les redirections http.

</dd> <dt>

<span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption \_ EnablePassportAuthentication**
</dt> <dd>

Active ou désactive la prise en charge de l’authentification Passport. Par défaut, la prise en charge automatique de l’authentification Passport est désactivée ; Affectez la valeur **true** à cette option pour activer la prise en charge de l’authentification Passport.

</dd> <dt>

<span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption \_ MaxAutomaticRedirects**
</dt> <dd>

Définit ou récupère le nombre maximal de redirections que WinHTTP suit ; la valeur par défaut est 10. Cette limite empêche les sites non autorisés de mettre le blocage du client WinHTTP à la suite d’un grand nombre de redirections.

**Windows XP avec SP1 et Windows 2000 avec SP3 :** Cette valeur d’énumération n’est pas prise en charge.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption \_ MaxResponseHeaderSize**
</dt> <dd>

Définit ou récupère un jeu lié sur la taille maximale de la partie en-tête de la réponse du serveur. Cette liaison protège le client contre un serveur malveillant tentant de bloquer le client en envoyant une réponse avec une quantité infinie de données d’en-tête. La valeur par défaut est 64 Ko.

**Windows XP avec SP1 et Windows 2000 avec SP3 :** Cette valeur d’énumération n’est pas prise en charge.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption \_ MaxResponseDrainSize**
</dt> <dd>

Définit ou récupère une limite sur la quantité de données qui seront vidées des réponses afin de réutiliser une connexion. La valeur par défaut est 1 Mo.

**Windows XP avec SP1 et Windows 2000 avec SP3 :** Cette valeur d’énumération n’est pas prise en charge.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**
</dt> <dd>

Définit ou récupère une valeur booléenne qui indique si HTTP/1.1 ou HTTP/1.0 doit être utilisé. La valeur par défaut est **true**, de sorte que http/1.1 est utilisé par défaut.

**Windows XP avec SP1 et Windows 2000 avec SP3 :** Cette valeur d’énumération n’est pas prise en charge.

</dd> <dt>

<span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption \_ EnableCertificateRevocationCheck**
</dt> <dd>

Active la vérification de la révocation des certificats du serveur pendant la négociation SSL. Lorsque le serveur présente un certificat, une vérification est effectuée pour déterminer si le certificat a été révoqué par son émetteur. Si le certificat est effectivement révoqué ou si la vérification de la révocation échoue parce que la liste de révocation de certificats (CRL) ne peut pas être téléchargée, la demande échoue ; ces erreurs de révocation ne peuvent pas être supprimées.

**Windows XP avec SP1 et Windows 2000 avec SP3 :** Cette valeur d’énumération n’est pas prise en charge.

</dd> </dl>

## <a name="remarks"></a>Remarques

Définissez une option en spécifiant l’une des constantes précédentes comme paramètre de la propriété [**option**](iwinhttprequest-option.md) .

> [!Note]  
> pour Windows XP et Windows 2000, consultez la section [configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHttp.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>            |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>         |
| Composant redistribuable<br/>          | WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.<br/> |
| MIDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




