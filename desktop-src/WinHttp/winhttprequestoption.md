---
description: Comprend des options qui peuvent être définies ou récupérées pour la session active des services HTTP Microsoft Windows (WinHTTP).
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
ms.openlocfilehash: 32ae65f43cd04027027e43d29c49ed0f68f29c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526236"
---
# <a name="winhttprequestoption-enumeration"></a><span data-ttu-id="5586b-103">Énumération WinHttpRequestOption</span><span class="sxs-lookup"><span data-stu-id="5586b-103">WinHttpRequestOption enumeration</span></span>

<span data-ttu-id="5586b-104">L’énumération **WinHttpRequestOption** comprend des options qui peuvent être définies ou récupérées pour la session active des services http Microsoft Windows (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="5586b-104">The **WinHttpRequestOption** enumeration includes options that can be set or retrieved for the current Microsoft Windows HTTP Services (WinHTTP) session.</span></span>

## <a name="syntax"></a><span data-ttu-id="5586b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5586b-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="5586b-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="5586b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5586b-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption \_ UserAgentString**</span><span class="sxs-lookup"><span data-stu-id="5586b-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption\_UserAgentString**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-108">Définit ou récupère un **Variant** qui contient la chaîne de l' [*agent utilisateur*](glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="5586b-108">Sets or retrieves a **VARIANT** that contains the [*user agent*](glossary.md) string.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**\_URL WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="5586b-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**WinHttpRequestOption\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-110">Récupère une **variante** qui contient l’URL de la ressource.</span><span class="sxs-lookup"><span data-stu-id="5586b-110">Retrieves a **VARIANT** that contains the URL of the resource.</span></span> <span data-ttu-id="5586b-111">Cette valeur est en lecture seule ; vous ne pouvez pas définir l’URL à l’aide de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5586b-111">This value is read-only; you cannot set the URL using this property.</span></span> <span data-ttu-id="5586b-112">L’URL ne peut pas être lue tant que la méthode [**Open**](iwinhttprequest-open.md) n’a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="5586b-112">The URL cannot be read until the [**Open**](iwinhttprequest-open.md) method is called.</span></span> <span data-ttu-id="5586b-113">Cette option est utile pour vérifier l’URL une fois la méthode [**Send**](iwinhttprequest-send.md) terminée afin de vérifier si une redirection s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5586b-113">This option is useful for checking the URL after the [**Send**](iwinhttprequest-send.md) method is finished to verify that any redirection occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption \_ URLCodePage**</span><span class="sxs-lookup"><span data-stu-id="5586b-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption\_URLCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-115">Définit ou récupère une valeur de **type Variant** qui identifie la [*page de codes*](glossary.md) de la chaîne d’URL.</span><span class="sxs-lookup"><span data-stu-id="5586b-115">Sets or retrieves a **VARIANT** that identifies the [*code page*](glossary.md) for the URL string.</span></span> <span data-ttu-id="5586b-116">La valeur par défaut est la page de codes UTF-8.</span><span class="sxs-lookup"><span data-stu-id="5586b-116">The default value is the UTF-8 code page.</span></span> <span data-ttu-id="5586b-117">La page de codes est utilisée pour convertir la chaîne d’URL Unicode, transmise dans la méthode [**Open**](iwinhttprequest-open.md) , en une représentation sous forme de chaîne codée sur un octet.</span><span class="sxs-lookup"><span data-stu-id="5586b-117">The code page is used to convert the Unicode URL string, passed in the [**Open**](iwinhttprequest-open.md) method, to a single-byte string representation.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption \_ EscapePercentInURL**</span><span class="sxs-lookup"><span data-stu-id="5586b-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption\_EscapePercentInURL**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-119">Définit ou récupère une valeur de **type Variant** qui indique si les caractères de pourcentage de la chaîne d’URL sont convertis en séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="5586b-119">Sets or retrieves a **VARIANT** that indicates whether percent characters in the URL string are converted to an escape sequence.</span></span> <span data-ttu-id="5586b-120">La valeur par défaut de cette option **est \_ true** , qui spécifie tous les caractères non sécurisés American National Standards Institute (ANSI), sauf que le symbole de pourcentage est converti en séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="5586b-120">The default value of this option is **VARIANT\_TRUE** which specifies all unsafe American National Standards Institute (ANSI) characters except the percent symbol are converted to an escape sequence.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption \_ SslErrorIgnoreFlags**</span><span class="sxs-lookup"><span data-stu-id="5586b-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption\_SslErrorIgnoreFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-122">Définit ou récupère un **Variant** qui indique les erreurs de certificat de serveur qui doivent être ignorées.</span><span class="sxs-lookup"><span data-stu-id="5586b-122">Sets or retrieves a **VARIANT** that indicates which server certificate errors should be ignored.</span></span> <span data-ttu-id="5586b-123">Il peut s’agir d’une combinaison d’un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="5586b-123">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="5586b-124">Error</span><span class="sxs-lookup"><span data-stu-id="5586b-124">Error</span></span>                                                  | <span data-ttu-id="5586b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="5586b-125">Value</span></span>  |
|--------------------------------------------------------|--------|
| <span data-ttu-id="5586b-126">Autorité de certification inconnue ou racine non approuvée</span><span class="sxs-lookup"><span data-stu-id="5586b-126">Unknown certification authority (CA) or untrusted root</span></span> | <span data-ttu-id="5586b-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="5586b-127">0x0100</span></span> |
| <span data-ttu-id="5586b-128">Utilisation incorrecte</span><span class="sxs-lookup"><span data-stu-id="5586b-128">Wrong usage</span></span>                                            | <span data-ttu-id="5586b-129">0x0200</span><span class="sxs-lookup"><span data-stu-id="5586b-129">0x0200</span></span> |
| <span data-ttu-id="5586b-130">Nom commun non valide (CN)</span><span class="sxs-lookup"><span data-stu-id="5586b-130">Invalid common name (CN)</span></span>                               | <span data-ttu-id="5586b-131">0x1000</span><span class="sxs-lookup"><span data-stu-id="5586b-131">0x1000</span></span> |
| <span data-ttu-id="5586b-132">Date ou certificat non valide expiré</span><span class="sxs-lookup"><span data-stu-id="5586b-132">Invalid date or certificate expired</span></span>                    | <span data-ttu-id="5586b-133">0x2000</span><span class="sxs-lookup"><span data-stu-id="5586b-133">0x2000</span></span> |



 

<span data-ttu-id="5586b-134">La valeur par défaut de cette option dans la version 5,1 de WinHTTP est égale à zéro, ce qui entraîne l’ignorance d’aucune erreur.</span><span class="sxs-lookup"><span data-stu-id="5586b-134">The default value of this option in Version 5.1 of WinHTTP is zero, which results in no errors being ignored.</span></span> <span data-ttu-id="5586b-135">Dans les versions antérieures de WinHTTP, le paramètre par défaut était 0x3300, ce qui a entraîné l’ignorance de toutes les erreurs de certificat de serveur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5586b-135">In earlier versions of WinHTTP, the default setting was 0x3300, which resulted in all server certificate errors being ignored by default.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption \_ SelectCertificate**</span><span class="sxs-lookup"><span data-stu-id="5586b-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption\_SelectCertificate**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-137">Définit une **variante** qui spécifie le certificat client envoyé à un serveur à des fins d’authentification.</span><span class="sxs-lookup"><span data-stu-id="5586b-137">Sets a **VARIANT** that specifies the client certificate that is sent to a server for authentication.</span></span> <span data-ttu-id="5586b-138">Cette option indique l’emplacement, le [*magasin de certificats*](glossary.md)et l’objet d’un certificat client délimité par des barres obliques inverses.</span><span class="sxs-lookup"><span data-stu-id="5586b-138">This option indicates the location, [*certificate store*](glossary.md), and subject of a client certificate delimited with backslashes.</span></span> <span data-ttu-id="5586b-139">Pour plus d’informations sur la sélection d’un certificat client, consultez [SSL dans WinHTTP](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="5586b-139">For more information about selecting a client certificate, see [SSL in WinHTTP](ssl-in-winhttp.md).</span></span>

</dd> <dt>

<span data-ttu-id="5586b-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption \_ EnableRedirects**</span><span class="sxs-lookup"><span data-stu-id="5586b-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption\_EnableRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-141">Définit ou récupère une valeur de **type Variant** qui indique si les demandes sont redirigées automatiquement lorsque le serveur spécifie un nouvel emplacement pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="5586b-141">Sets or retrieves a **VARIANT** that indicates whether requests are automatically redirected when the server specifies a new location for the resource.</span></span> <span data-ttu-id="5586b-142">La valeur par défaut de cette option **est \_ true** pour indiquer que les demandes sont automatiquement redirigées.</span><span class="sxs-lookup"><span data-stu-id="5586b-142">The default value of this option is **VARIANT\_TRUE** to indicate that requests are automatically redirected.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption \_ UrlEscapeDisable**</span><span class="sxs-lookup"><span data-stu-id="5586b-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption\_UrlEscapeDisable**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-144">Définit ou récupère une valeur de **type Variant** qui indique si les caractères non sécurisés dans les composants de chemin d’accès et de requête d’une URL sont convertis en séquences d’échappement.</span><span class="sxs-lookup"><span data-stu-id="5586b-144">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the path and query components of a URL are converted to escape sequences.</span></span> <span data-ttu-id="5586b-145">La valeur par défaut de cette option **est \_ true**, qui spécifie que les caractères du chemin d’accès et de la requête sont convertis.</span><span class="sxs-lookup"><span data-stu-id="5586b-145">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the path and query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption \_ UrlEscapeDisableQuery**</span><span class="sxs-lookup"><span data-stu-id="5586b-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption\_UrlEscapeDisableQuery**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-147">Définit ou récupère une valeur de **type Variant** qui indique si les caractères non sécurisés dans le composant de requête de l’URL sont convertis en séquences d’échappement.</span><span class="sxs-lookup"><span data-stu-id="5586b-147">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the query component of the URL are converted to escape sequences.</span></span> <span data-ttu-id="5586b-148">La valeur par défaut de cette option **est \_ true**, qui spécifie que les caractères de la requête sont convertis.</span><span class="sxs-lookup"><span data-stu-id="5586b-148">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption \_ SecureProtocols**</span><span class="sxs-lookup"><span data-stu-id="5586b-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption\_SecureProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-150">Définit ou récupère un **Variant** qui indique les protocoles sécurisés qui peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="5586b-150">Sets or retrieves a **VARIANT** that indicates which secure protocols can be used.</span></span> <span data-ttu-id="5586b-151">Cette option sélectionne les protocoles acceptables pour le client.</span><span class="sxs-lookup"><span data-stu-id="5586b-151">This option selects the protocols acceptable to the client.</span></span> <span data-ttu-id="5586b-152">Le protocole est négocié au cours de la négociation de l’SSL (Secure Sockets Layer) (SSL).</span><span class="sxs-lookup"><span data-stu-id="5586b-152">The protocol is negotiated during the Secure Sockets Layer (SSL) handshake.</span></span> <span data-ttu-id="5586b-153">Il peut s’agir d’une combinaison d’un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="5586b-153">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="5586b-154">Protocol</span><span class="sxs-lookup"><span data-stu-id="5586b-154">Protocol</span></span>                           | <span data-ttu-id="5586b-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="5586b-155">Value</span></span>  |
|------------------------------------|--------|
| <span data-ttu-id="5586b-156">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="5586b-156">SSL 2.0</span></span>                            | <span data-ttu-id="5586b-157">0x0008</span><span class="sxs-lookup"><span data-stu-id="5586b-157">0x0008</span></span> |
| <span data-ttu-id="5586b-158">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="5586b-158">SSL 3.0</span></span>                            | <span data-ttu-id="5586b-159">0x0020</span><span class="sxs-lookup"><span data-stu-id="5586b-159">0x0020</span></span> |
| <span data-ttu-id="5586b-160">TLS (Transport Layer Security) 1,0</span><span class="sxs-lookup"><span data-stu-id="5586b-160">Transport Layer Security (TLS) 1.0</span></span> | <span data-ttu-id="5586b-161">0x0080</span><span class="sxs-lookup"><span data-stu-id="5586b-161">0x0080</span></span> |



 

<span data-ttu-id="5586b-162">La valeur par défaut de cette option est 0x0028, ce qui indique que SSL 2,0 ou SSL 3,0 peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="5586b-162">The default value of this option is 0x0028, which indicates that SSL 2.0 or SSL 3.0 can be used.</span></span> <span data-ttu-id="5586b-163">Si cette option a la valeur zéro, le client et le serveur ne sont pas en mesure de déterminer un protocole de sécurité acceptable et l' [**envoi**](iwinhttprequest-send.md) suivant génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="5586b-163">If this option is set to zero, the client and server are not able to determine an acceptable security protocol and the next [**Send**](iwinhttprequest-send.md) results in an error.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption \_ EnableTracing,**</span><span class="sxs-lookup"><span data-stu-id="5586b-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption\_EnableTracing**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-165">Définit ou récupère une valeur de **type Variant** qui indique si le traçage est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="5586b-165">Sets or retrieves a **VARIANT** that indicates whether tracing is currently enabled.</span></span> <span data-ttu-id="5586b-166">Pour plus d’informations sur la fonction de trace dans les services HTTP Microsoft Windows (WinHTTP), consultez [WinHTTP trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="5586b-166">For more information about the trace facility in Microsoft Windows HTTP Services (WinHTTP), see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span>

</dd> <dt>

<span data-ttu-id="5586b-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption \_ RevertImpersonationOverSsl**</span><span class="sxs-lookup"><span data-stu-id="5586b-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption\_RevertImpersonationOverSsl**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-168">Contrôle si l’objet [**WinHttpRequest**](winhttprequest.md) rétablit temporairement l’emprunt d’identité du client pendant la durée des opérations d’authentification du certificat SSL.</span><span class="sxs-lookup"><span data-stu-id="5586b-168">Controls whether the [**WinHttpRequest**](winhttprequest.md) object temporarily reverts client impersonation for the duration of the SSL certificate authentication operations.</span></span> <span data-ttu-id="5586b-169">Le paramètre par défaut de l’objet **WinHttpRequest** est **true**.</span><span class="sxs-lookup"><span data-stu-id="5586b-169">The default setting for the **WinHttpRequest** object is **TRUE**.</span></span> <span data-ttu-id="5586b-170">Affectez la valeur **false** à cette option pour conserver l’emprunt d’identité lors de l’exécution d’opérations d’authentification par certificat.</span><span class="sxs-lookup"><span data-stu-id="5586b-170">Set this option to **FALSE** to keep impersonation while performing certificate authentication operations.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption \_ EnableHttpsToHttpRedirects**</span><span class="sxs-lookup"><span data-stu-id="5586b-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption\_EnableHttpsToHttpRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-172">Contrôle si WinHTTP autorise ou non les redirections.</span><span class="sxs-lookup"><span data-stu-id="5586b-172">Controls whether or not WinHTTP allows redirects.</span></span> <span data-ttu-id="5586b-173">Par défaut, toutes les redirections sont automatiquement suivies, à l’exception de celles qui sont transférées d’une URL sécurisée (https) vers une URL non sécurisée (http).</span><span class="sxs-lookup"><span data-stu-id="5586b-173">By default, all redirects are automatically followed, except those that transfer from a secure (https) URL to an non-secure (http) URL.</span></span> <span data-ttu-id="5586b-174">Affectez la valeur **true** à cette option pour activer le protocole HTTPS sur les redirections http.</span><span class="sxs-lookup"><span data-stu-id="5586b-174">Set this option to **TRUE** to enable HTTPS to HTTP redirects.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption \_ EnablePassportAuthentication**</span><span class="sxs-lookup"><span data-stu-id="5586b-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption\_EnablePassportAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-176">Active ou désactive la prise en charge de l’authentification Passport.</span><span class="sxs-lookup"><span data-stu-id="5586b-176">Enables or disables support for Passport authentication.</span></span> <span data-ttu-id="5586b-177">Par défaut, la prise en charge automatique de l’authentification Passport est désactivée ; Affectez la valeur **true** à cette option pour activer la prise en charge de l’authentification Passport.</span><span class="sxs-lookup"><span data-stu-id="5586b-177">By default, automatic support for Passport authentication is disabled; set this option to **TRUE** to enable Passport authentication support.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption \_ MaxAutomaticRedirects**</span><span class="sxs-lookup"><span data-stu-id="5586b-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption\_MaxAutomaticRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-179">Définit ou récupère le nombre maximal de redirections que WinHTTP suit ; la valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="5586b-179">Sets or retrieves the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="5586b-180">Cette limite empêche les sites non autorisés de mettre le blocage du client WinHTTP à la suite d’un grand nombre de redirections.</span><span class="sxs-lookup"><span data-stu-id="5586b-180">This limit prevents unauthorized sites from making the WinHTTP client stall following a large number of redirects.</span></span>

<span data-ttu-id="5586b-181">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cette valeur d’énumération n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5586b-181">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption \_ MaxResponseHeaderSize**</span><span class="sxs-lookup"><span data-stu-id="5586b-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption\_MaxResponseHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-183">Définit ou récupère un jeu lié sur la taille maximale de la partie en-tête de la réponse du serveur.</span><span class="sxs-lookup"><span data-stu-id="5586b-183">Sets or retrieves a bound set on the maximum size of the header portion of the server's response.</span></span> <span data-ttu-id="5586b-184">Cette liaison protège le client contre un serveur malveillant tentant de bloquer le client en envoyant une réponse avec une quantité infinie de données d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="5586b-184">This bound protects the client from a malicious server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="5586b-185">La valeur par défaut est 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="5586b-185">The default value is 64 KB.</span></span>

<span data-ttu-id="5586b-186">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cette valeur d’énumération n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5586b-186">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption \_ MaxResponseDrainSize**</span><span class="sxs-lookup"><span data-stu-id="5586b-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption\_MaxResponseDrainSize**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-188">Définit ou récupère une limite sur la quantité de données qui seront vidées des réponses afin de réutiliser une connexion.</span><span class="sxs-lookup"><span data-stu-id="5586b-188">Sets or retrieves a bound on the amount of data that will be drained from responses in order to reuse a connection.</span></span> <span data-ttu-id="5586b-189">La valeur par défaut est 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="5586b-189">The default is 1 MB.</span></span>

<span data-ttu-id="5586b-190">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cette valeur d’énumération n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5586b-190">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="5586b-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption\_EnableHttp1\_1**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-192">Définit ou récupère une valeur booléenne qui indique si HTTP/1.1 ou HTTP/1.0 doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="5586b-192">Sets or retrieves a boolean value that indicates whether HTTP/1.1 or HTTP/1.0 should be used.</span></span> <span data-ttu-id="5586b-193">La valeur par défaut est **true**, de sorte que http/1.1 est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="5586b-193">The default is **TRUE**, so that HTTP/1.1 is used by default.</span></span>

<span data-ttu-id="5586b-194">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cette valeur d’énumération n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5586b-194">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption \_ EnableCertificateRevocationCheck**</span><span class="sxs-lookup"><span data-stu-id="5586b-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption\_EnableCertificateRevocationCheck**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-196">Active la vérification de la révocation des certificats du serveur pendant la négociation SSL.</span><span class="sxs-lookup"><span data-stu-id="5586b-196">Enables server certificate revocation checking during SSL negotiation.</span></span> <span data-ttu-id="5586b-197">Lorsque le serveur présente un certificat, une vérification est effectuée pour déterminer si le certificat a été révoqué par son émetteur.</span><span class="sxs-lookup"><span data-stu-id="5586b-197">When the server presents a certificate, a check is performed to determine whether the certificate has been revoked by its issuer.</span></span> <span data-ttu-id="5586b-198">Si le certificat est effectivement révoqué ou si la vérification de la révocation échoue parce que la liste de révocation de certificats (CRL) ne peut pas être téléchargée, la demande échoue ; ces erreurs de révocation ne peuvent pas être supprimées.</span><span class="sxs-lookup"><span data-stu-id="5586b-198">If the certificate is indeed revoked, or the revocation check fails because the Certificate Revocation List (CRL) cannot be downloaded, the request fails; such revocation errors cannot be suppressed.</span></span>

<span data-ttu-id="5586b-199">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cette valeur d’énumération n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5586b-199">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5586b-200">Notes</span><span class="sxs-lookup"><span data-stu-id="5586b-200">Remarks</span></span>

<span data-ttu-id="5586b-201">Définissez une option en spécifiant l’une des constantes précédentes comme paramètre de la propriété [**option**](iwinhttprequest-option.md) .</span><span class="sxs-lookup"><span data-stu-id="5586b-201">Set an option by specifying one of the preceding constants as the parameter of the [**Option**](iwinhttprequest-option.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="5586b-202">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="5586b-202">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5586b-203">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5586b-203">Requirements</span></span>



| <span data-ttu-id="5586b-204">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5586b-204">Requirement</span></span> | <span data-ttu-id="5586b-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="5586b-205">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5586b-206">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5586b-206">Minimum supported client</span></span><br/> | <span data-ttu-id="5586b-207">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5586b-207">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="5586b-208">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5586b-208">Minimum supported server</span></span><br/> | <span data-ttu-id="5586b-209">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5586b-209">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="5586b-210">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="5586b-210">Redistributable</span></span><br/>          | <span data-ttu-id="5586b-211">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5586b-211">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="5586b-212">MIDL</span><span class="sxs-lookup"><span data-stu-id="5586b-212">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5586b-213"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5586b-213"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5586b-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5586b-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5586b-215">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="5586b-215">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




