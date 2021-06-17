---
Description: Les indicateurs d’option suivants sont pris en charge par WinHttpQueryOption et WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Indicateurs d’option (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 91a9506225c53893990d4dcdc534293daa6c8e00
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262061"
---
# <a name="option-flags"></a><span data-ttu-id="7ee00-103">Indicateurs d’option</span><span class="sxs-lookup"><span data-stu-id="7ee00-103">Option Flags</span></span>

<span data-ttu-id="7ee00-104">Les indicateurs d’option suivants sont pris en charge par [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) et [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="7ee00-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="7ee00-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**OPTION WINHTTP assurée par les \_ \_ \_ \_ rappels non bloquants \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-106">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="7ee00-106">The default is FALSE.</span></span> <span data-ttu-id="7ee00-107">Si la valeur est TRUE, WinHTTP ne garantit pas la progression si les rappels d’État sont bloqués par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="7ee00-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="7ee00-108">L’application cliente doit être particulièrement prudente pour effectuer des opérations minimales dans le rappel sans blocage, ce qui revient le plus rapidement possible et, en particulier, ne doit pas attendre d’appels WinHTTP ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="7ee00-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="7ee00-109">S’il ne suit pas ces instructions, il est probable qu’il y ait un impact négatif sur les performances ou qu’une application potentielle se bloque.</span><span class="sxs-lookup"><span data-stu-id="7ee00-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="7ee00-110">Si elle est utilisée de la manière prescrite, cette option peut améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="7ee00-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**stratégie d’accès automatique aux \_ options WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-112">Définit une valeur d’entier long non signé qui spécifie la [stratégie d’ouverture de session automatique](authentication-in-winhttp.md) avec l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="7ee00-113">Terme</span><span class="sxs-lookup"><span data-stu-id="7ee00-113">Term</span></span> | <span data-ttu-id="7ee00-114">Description</span><span class="sxs-lookup"><span data-stu-id="7ee00-114">Description</span></span> |
|-|-|
| <span data-ttu-id="7ee00-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>niveau de sécurité de l' \_ AUTOLOGO WINHTTP WinHTTP \_ \_ \_ élevé</span><span class="sxs-lookup"><span data-stu-id="7ee00-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="7ee00-116">Les informations d’identification par défaut ne sont pas utilisées.</span><span class="sxs-lookup"><span data-stu-id="7ee00-116">Default credentials are not used.</span></span> <span data-ttu-id="7ee00-117">Notez que cet indicateur prend effet uniquement si vous spécifiez le serveur par le nom de l’ordinateur réel.</span><span class="sxs-lookup"><span data-stu-id="7ee00-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="7ee00-118">Elle ne prend pas effet si vous spécifiez le serveur par « localhost » ou par adresse IP.</span><span class="sxs-lookup"><span data-stu-id="7ee00-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="7ee00-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>niveau de sécurité de l’ouverture de certification WINHTTP \_ \_ \_ \_ bas</span><span class="sxs-lookup"><span data-stu-id="7ee00-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="7ee00-120">Une ouverture de session authentifiée à l’aide des informations d’identification par défaut est effectuée pour toutes les demandes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="7ee00-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>niveau de sécurité de la \_ protection d’accès réseau WinHTTP \_ \_ \_ moyen</span><span class="sxs-lookup"><span data-stu-id="7ee00-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="7ee00-122">Une connexion authentifiée à l’aide des informations d’identification par défaut est exécutée uniquement pour les demandes sur l’intranet local.</span><span class="sxs-lookup"><span data-stu-id="7ee00-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7ee00-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_rappel d’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-124">Récupère le pointeur vers la fonction de rappel définie avec [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="7ee00-124">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_contexte de \_ \_ certificat client \_ de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-126">Définit le contexte du certificat client.</span><span class="sxs-lookup"><span data-stu-id="7ee00-126">Sets the client certificate context.</span></span> <span data-ttu-id="7ee00-127">Si une application reçoit un certificat d' [**\_ authentification de \_ client WinHTTP \_ \_ \_ nécessaire**](error-messages.md), elle doit appeler [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) pour fournir un certificat avant de retenter la demande.</span><span class="sxs-lookup"><span data-stu-id="7ee00-127">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="7ee00-128">Dans le cadre du traitement de cette option, WinHttp appelle [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) sur le contexte de certificat fourni par l’appelant afin que le contexte de certificat puisse être libéré indépendamment par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7ee00-128">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="7ee00-129">L’application ne doit pas tenter de fermer le magasin de certificats avec l’indicateur de fermeture de l' \_ \_ indicateur de fin de magasin de certificats \_ de l' \_ appel à [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) sur le magasin de certificats à partir duquel le contexte de certificat a été récupéré.</span><span class="sxs-lookup"><span data-stu-id="7ee00-129">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="7ee00-130">Une violation d’accès peut se produire.</span><span class="sxs-lookup"><span data-stu-id="7ee00-130">An access violation may occur.</span></span>

<span data-ttu-id="7ee00-131">Lorsque le serveur demande un certificat client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retourne une erreur message d' [**authentification du \_ \_ client WinHTTP \_ \_ \_ requis**](error-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="7ee00-131">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="7ee00-132">Si le serveur demande le certificat mais n’en a pas besoin, l’application peut spécifier cette option pour indiquer qu’elle n’a pas de certificat.</span><span class="sxs-lookup"><span data-stu-id="7ee00-132">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="7ee00-133">Le serveur peut choisir un autre schéma d’authentification ou autoriser un accès anonyme au serveur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-133">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="7ee00-134">L’application fournit la macro de **contexte de certificat du \_ client WinHTTP no \_ client \_ \_** dans le paramètre *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7ee00-134">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="7ee00-135">Si le serveur a besoin d’un certificat client, il peut envoyer un code d’état HTTP 403 en réponse.</span><span class="sxs-lookup"><span data-stu-id="7ee00-135">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="7ee00-136">Pour plus d’informations, consultez l’option **WinHTTP \_ \_ liste d' \_ \_ émetteurs \_ de certificats client** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-136">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_option WinHTTP \_ \_ liste d’émetteurs de certificats client \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-138">Récupère une structure [**SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) lorsque l’erreur de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) est un **\_ certificat d' \_ authentification client WinHTTP \_ \_ \_ nécessaire**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-138">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="7ee00-139">La liste d’émetteurs de la structure contient une liste d’autorités de certification (CA) acceptables du serveur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-139">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="7ee00-140">L’application cliente peut filtrer la liste des autorités de certification pour récupérer le certificat client pour l’authentification SSL.</span><span class="sxs-lookup"><span data-stu-id="7ee00-140">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="7ee00-141">En revanche, si le serveur demande le certificat client, mais ne l’exige pas, l’application peut appeler [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avec l' **option \_ WinHTTP \_ \_ \_ contexte de certificat client CERT** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-141">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="7ee00-142">Pour plus d’informations, consultez l’option de **\_ \_ \_ \_ contexte certificat du client de l’option WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-142">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**page de codes de l' \_ option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-144">Définit la [*page de codes*](glossary.md) utilisée pour traiter l’URL (c’est-à-dire, la chaîne de requête).</span><span class="sxs-lookup"><span data-stu-id="7ee00-144">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="7ee00-145">La valeur par défaut est UTF-8.</span><span class="sxs-lookup"><span data-stu-id="7ee00-145">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_option WinHTTP \_ configurer \_ l' \_ authentification Passport**</span><span class="sxs-lookup"><span data-stu-id="7ee00-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-147">Définit une valeur d’entier long non signé qui spécifie si [l’authentification Passport dans](passport-authentication-in-winhttp.md) l’authentification WinHTTP est activée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-147">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="7ee00-148">Il peut s'agir de l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ee00-148">The value can be one of the following:</span></span>

| <span data-ttu-id="7ee00-149">Terme</span><span class="sxs-lookup"><span data-stu-id="7ee00-149">Term</span></span> | <span data-ttu-id="7ee00-150">Description</span><span class="sxs-lookup"><span data-stu-id="7ee00-150">Description</span></span> |
|-|-|
| <span data-ttu-id="7ee00-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP- \_ désactiver l' \_ \_ authentification Passport</span><span class="sxs-lookup"><span data-stu-id="7ee00-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="7ee00-152">L’authentification Microsoft Passport est désactivée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-152">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="7ee00-153">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ee00-153">This is the default.</span></span> |
| <span data-ttu-id="7ee00-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP-désactiver le porte- \_ \_ \_ clés Passport</span><span class="sxs-lookup"><span data-stu-id="7ee00-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="7ee00-155">Le porte-clés Passport est désactivé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-155">The Passport keyring is disabled.</span></span> <span data-ttu-id="7ee00-156">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ee00-156">This is the default.</span></span> |
| <span data-ttu-id="7ee00-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>activation de WINHTTP avec l' \_ \_ \_ authentification Passport</span><span class="sxs-lookup"><span data-stu-id="7ee00-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="7ee00-158">L’authentification Passport est activée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-158">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="7ee00-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP activer le porte- \_ \_ \_ clés Passport</span><span class="sxs-lookup"><span data-stu-id="7ee00-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="7ee00-160">Le porte-clés Passport est activé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-160">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="7ee00-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_ \_ nouvelles tentatives de connexion de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-162">Définit ou récupère une valeur d’entier long non signé qui contient le nombre de tentatives de connexion de timesWinHTTP à un hôte.</span><span class="sxs-lookup"><span data-stu-id="7ee00-162">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="7ee00-163">Les services HTTP Microsoft Windows (WinHTTP) ne tentent qu’une seule fois par adresse IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="7ee00-163">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="7ee00-164">Par exemple, si vous tentez de vous connecter à un hôte multirésident qui a 10 adresses IP et que les **\_ \_ \_ nouvelles tentatives de connexion de l’option WinHTTP** ont la valeur 7, WinHTTP tente uniquement de se connecter aux sept premières adresses IP.</span><span class="sxs-lookup"><span data-stu-id="7ee00-164">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="7ee00-165">Étant donné le même jeu de 10 adresses IP, si l' **\_ option de connexion des \_ \_ nouvelles tentatives WinHTTP** est définie sur 20, WinHTTP tente chacune des 10 une seule fois.</span><span class="sxs-lookup"><span data-stu-id="7ee00-165">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="7ee00-166">Si une tentative de connexion échoue encore après le nombre spécifié de tentatives, ou si le délai de connexion a expiré avant, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-166">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="7ee00-167">La valeur par défaut pour les **\_ \_ \_ nouvelles tentatives de connexion de l’option WinHTTP** est de cinq tentatives.</span><span class="sxs-lookup"><span data-stu-id="7ee00-167">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**délai de connexion de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-169">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-169">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="7ee00-170">La définition de cette option sur Infinite (0xFFFFFFFF) désactive ce minuteur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-170">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="7ee00-171">Si une demande de connexion TCP prend plus de temps que cette valeur de délai d’attente, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-171">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="7ee00-172">Le délai d’attente par défaut est de 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-172">The default timeout is 60 seconds.</span></span> <span data-ttu-id="7ee00-173">Lorsque vous tentez de vous connecter à plusieurs adresses IP pour un seul hôte (un hôte multirésident), le délai d’expiration est fixé pour chaque connexion individuelle.</span><span class="sxs-lookup"><span data-stu-id="7ee00-173">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**informations de connexion de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-175">Récupère l’adresse IP source et de destination, ainsi que le port de la demande qui a généré la réponse quand [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retourne.</span><span class="sxs-lookup"><span data-stu-id="7ee00-175">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="7ee00-176">L’application appelle [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) avec l’option **WinHTTP \_ option \_ Connection \_ info** , et fournit la structure des [**\_ \_ informations de connexion WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) dans le paramètre *lpBuffer* .</span><span class="sxs-lookup"><span data-stu-id="7ee00-176">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="7ee00-177">Pour plus d’informations, **consultez \_ \_ informations de connexion WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-177">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="7ee00-178">**Windows Server 2003 avec SP1 et Windows XP avec SP2 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="7ee00-178">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_Statistiques de connexion des options WinHTTP \_ \_ \_ v0**</span><span class="sxs-lookup"><span data-stu-id="7ee00-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-180">Extrait le struct d' [**\_ informations TCP \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) pour la connexion sous-jacente utilisée par la demande.</span><span class="sxs-lookup"><span data-stu-id="7ee00-180">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="7ee00-181">La structure retournée peut contenir des statistiques des requêtes précédentes envoyées sur la même connexion.</span><span class="sxs-lookup"><span data-stu-id="7ee00-181">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="7ee00-182">Cette option a été remplacée par les **statistiques de connexion de l' \_ option WinHTTP \_ \_ \_ v1**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-182">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Statistiques de connexion des options WinHTTP \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="7ee00-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-184">Extrait le struct d' [**\_ informations TCP \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) pour la connexion sous-jacente utilisée par la demande.</span><span class="sxs-lookup"><span data-stu-id="7ee00-184">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="7ee00-185">La structure retournée peut contenir des statistiques des requêtes précédentes envoyées sur la même connexion.</span><span class="sxs-lookup"><span data-stu-id="7ee00-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**valeur de contexte de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-187">Définit ou récupère un **\_ ptr DWORD** qui contient un pointeur vers la valeur de contexte associée à ce handle [HINTERNET](hinternet-handles-in-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="7ee00-187">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="7ee00-188">La valeur stockée dans la mémoire tampon est utilisée et la nouvelle valeur est assignée à l’indicateur d’option de la valeur de contexte de l' **\_ option \_ \_ WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-188">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**décompression des \_ options WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-190">Définit un DWORD d’indicateurs qui déterminent si WinHTTP décompresse automatiquement les corps de réponse avec les encodages de contenu compressés.</span><span class="sxs-lookup"><span data-stu-id="7ee00-190">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="7ee00-191">WinHTTP définira également un en-tête de Accept-Encoding approprié, en remplaçant tout fourni par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7ee00-191">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="7ee00-192">Les valeurs prises en charge sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ee00-192">Supported values are:</span></span>

| <span data-ttu-id="7ee00-193">Terme</span><span class="sxs-lookup"><span data-stu-id="7ee00-193">Term</span></span> | <span data-ttu-id="7ee00-194">Description</span><span class="sxs-lookup"><span data-stu-id="7ee00-194">Description</span></span> |
|-|-|
| <span data-ttu-id="7ee00-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_indicateur de décompression WinHTTP, \_ \_ gzip</span><span class="sxs-lookup"><span data-stu-id="7ee00-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="7ee00-196">Décompresser Content-Encoding : réponses gzip.</span><span class="sxs-lookup"><span data-stu-id="7ee00-196">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="7ee00-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_indicateur de décompression WinHTTP \_ \_ deflate</span><span class="sxs-lookup"><span data-stu-id="7ee00-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="7ee00-198">Décompresser le contenu-encodage : réponses décompressées.</span><span class="sxs-lookup"><span data-stu-id="7ee00-198">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="7ee00-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_indicateur de décompression WinHTTP \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="7ee00-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="7ee00-200">Décompressez les réponses avec tout encodage de contenu pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ee00-200">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="7ee00-201">Par défaut, WinHTTP remet les réponses compressées à l’appelant sans les modifier.</span><span class="sxs-lookup"><span data-stu-id="7ee00-201">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**\_fonctionnalité de \_ désactivation de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-203">Définit une valeur d’entier long non signé qui spécifie les fonctionnalités qui sont désactivées avec un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="7ee00-203">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="7ee00-204">N’oubliez pas que cette fonctionnalité doit être transmise uniquement à [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) sur les handles de requête après la création du handle de demande avec [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), et avant l’envoi de la demande avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="7ee00-204">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="7ee00-205">Terme</span><span class="sxs-lookup"><span data-stu-id="7ee00-205">Term</span></span> | <span data-ttu-id="7ee00-206">Description</span><span class="sxs-lookup"><span data-stu-id="7ee00-206">Description</span></span> |
|-|-|
| <span data-ttu-id="7ee00-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>\_désactiver \_ l’authentification WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="7ee00-208">L’authentification automatique est désactivée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-208">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="7ee00-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>désactivation des \_ \_ cookies WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="7ee00-210">L’ajout automatique d’en-têtes de cookie aux demandes est désactivé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-210">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="7ee00-211">En outre, les cookies retournés ne sont pas automatiquement ajoutés à la base de données de cookies.</span><span class="sxs-lookup"><span data-stu-id="7ee00-211">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="7ee00-212">La désactivation des cookies peut entraîner des performances médiocres pour l’authentification Passport.</span><span class="sxs-lookup"><span data-stu-id="7ee00-212">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="7ee00-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>\_désactiver \_ Keep \_ Alive dans WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="7ee00-214">Désactive la sémantique Keep-Alive pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="7ee00-214">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="7ee00-215">La sémantique Keep-Alive est requise pour MSN, NTLM et d’autres types d’authentification.</span><span class="sxs-lookup"><span data-stu-id="7ee00-215">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="7ee00-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>désactivation des \_ \_ redirections WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="7ee00-217">La redirection automatique est désactivée lors de l’envoi de demandes avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="7ee00-217">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="7ee00-218">Si la redirection automatique est désactivée, une application doit inscrire une fonction de rappel pour que l’authentification Passport aboutisse.</span><span class="sxs-lookup"><span data-stu-id="7ee00-218">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7ee00-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_option WinHTTP \_ désactiver \_ le \_ protocole sécurisé de \_ secours**</span><span class="sxs-lookup"><span data-stu-id="7ee00-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-220">Empêche WinHTTP de retenter une connexion avec une version antérieure du protocole de sécurité en cas d’échec de la négociation de protocole initiale.</span><span class="sxs-lookup"><span data-stu-id="7ee00-220">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPTION WINHTTP- \_ \_ désactiver la \_ \_ file d’attente de flux**</span><span class="sxs-lookup"><span data-stu-id="7ee00-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-222">Autorise les nouvelles demandes à ouvrir une connexion HTTP/2 supplémentaire lorsque la limite de flux simultané maximale est atteinte, plutôt que d’attendre le flux disponible suivant sur une connexion existante.</span><span class="sxs-lookup"><span data-stu-id="7ee00-222">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**\_option WinHTTP \_ activer la \_ fonctionnalité**</span><span class="sxs-lookup"><span data-stu-id="7ee00-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-224">Définit une valeur d’entier long non signé qui spécifie les fonctionnalités actuellement activées.</span><span class="sxs-lookup"><span data-stu-id="7ee00-224">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="7ee00-225">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-225">Can be one of the following values.</span></span>

| <span data-ttu-id="7ee00-226">Terme</span><span class="sxs-lookup"><span data-stu-id="7ee00-226">Term</span></span> | <span data-ttu-id="7ee00-227">Description</span><span class="sxs-lookup"><span data-stu-id="7ee00-227">Description</span></span> |
|-|-|
| <span data-ttu-id="7ee00-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ activer \_ l' \_ emprunt d' \_ identité par le biais de SSL</span><span class="sxs-lookup"><span data-stu-id="7ee00-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="7ee00-229">S’il est activé, WinHTTP rétablit temporairement l’emprunt d’identité du client pendant la durée des opérations d’authentification du certificat SSL.</span><span class="sxs-lookup"><span data-stu-id="7ee00-229">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="7ee00-230">Cette valeur ne peut être définie que sur le descripteur de session.</span><span class="sxs-lookup"><span data-stu-id="7ee00-230">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="7ee00-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ activer \_ la \_ révocation SSL</span><span class="sxs-lookup"><span data-stu-id="7ee00-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="7ee00-232">Si cette option est activée, WinHTTP autorise la révocation SSL.</span><span class="sxs-lookup"><span data-stu-id="7ee00-232">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="7ee00-233">Cette valeur peut être définie uniquement sur le handle de demande.</span><span class="sxs-lookup"><span data-stu-id="7ee00-233">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_option WinHTTP \_ activer \_ le \_ protocole http**</span><span class="sxs-lookup"><span data-stu-id="7ee00-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-235">Définit un masque de réinitialisation DWORD des versions HTTP avancées acceptables.</span><span class="sxs-lookup"><span data-stu-id="7ee00-235">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="7ee00-236">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ee00-236">Possible values are:</span></span>

| <span data-ttu-id="7ee00-237">Terme</span><span class="sxs-lookup"><span data-stu-id="7ee00-237">Term</span></span> | <span data-ttu-id="7ee00-238">Description</span><span class="sxs-lookup"><span data-stu-id="7ee00-238">Description</span></span> |
|-|-|
| <span data-ttu-id="7ee00-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_ \_ Indicateur de protocole WinHTTP \_ http2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="7ee00-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="7ee00-240">Active HTTP/2 pour la requête.</span><span class="sxs-lookup"><span data-stu-id="7ee00-240">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="7ee00-241">Aucun (0x0)</span><span class="sxs-lookup"><span data-stu-id="7ee00-241">None (0x0)</span></span> | <span data-ttu-id="7ee00-242">Limite la demande à HTTP/1.1 et antérieur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-242">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="7ee00-243">Les versions héritées de HTTP (1,1 et versions antérieures) ne peuvent pas être désactivées à l’aide de cette option.</span><span class="sxs-lookup"><span data-stu-id="7ee00-243">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="7ee00-244">La valeur par défaut est 0x0.</span><span class="sxs-lookup"><span data-stu-id="7ee00-244">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-245"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**\_Option WinHTTP \_ activer \_ le \_ certificat du client http2 plus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-245"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7ee00-246">Cette option peut être définie sur un handle de session WinHttp pour permettre à WinHttp d’utiliser le contexte de certificat client fourni par l’appelant lorsque le protocole HTTP/2 est utilisé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-246">This option can be set on a WinHttp session handle to allow WinHttp to use the caller-provided client certificate context when HTTP/2 is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-247"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_option WinHTTP \_ EnableTracing,**</span><span class="sxs-lookup"><span data-stu-id="7ee00-247"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-248">Définit une valeur **bool** qui spécifie si le traçage est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-248">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="7ee00-249">Pour plus d’informations sur la fonctionnalité de trace dans WinHTTP, consultez [WinHTTP trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="7ee00-249">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="7ee00-250">Cette option ne peut être définie que sur un handle **HINTERNET** **null** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-250">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="7ee00-251"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**\_option WinHTTP \_ coder \_ extra**</span><span class="sxs-lookup"><span data-stu-id="7ee00-251"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-252">Active l’encodage de pourcentage d’URL pour le chemin d’accès et la chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="7ee00-252">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="7ee00-253">Vous pouvez également encoder en pourcentage avant d’appeler WinHttp.</span><span class="sxs-lookup"><span data-stu-id="7ee00-253">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="7ee00-254"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**expiration de la connexion de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-254"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-255">Cette option ne peut être définie que sur un handle de demande qui est toujours actif (envoi ou réception).</span><span class="sxs-lookup"><span data-stu-id="7ee00-255">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="7ee00-256">La définition de cette option indique à WinHttp d’arrêter de servir les demandes sur la connexion associée au handle de demande passé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-256">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="7ee00-257">La connexion sera fermée après le handle de requête. cette option est appelée avec est terminée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-257">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="7ee00-258">Cette option ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7ee00-258">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-259"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ erreur étendue de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-259"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-260">Récupère une valeur d’entier long non signé qui contient un code d’erreur Microsoft Windows Sockets qui a été mappé à l’erreur \_ WinHTTP \_ \* messages d’erreur retournés dans ce contexte de thread.</span><span class="sxs-lookup"><span data-stu-id="7ee00-260">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="7ee00-261">Vous pouvez passer **null** comme valeur de handle.</span><span class="sxs-lookup"><span data-stu-id="7ee00-261">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-262"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**identification \_ du \_ proxy global des options \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-262"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-263">Prend un pointeur vers une structure d' [**\_ CREDS \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) d’identification WinHTTP avec le paramètre de fonction *hInternet* ayant la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-263">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="7ee00-264">Cette option requiert la clé de Registre **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings ! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-264">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="7ee00-265">Si cette clé de Registre n’est pas définie, WinHTTP retourne l' **\_ option erreur WinHTTP \_ non valide \_**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-265">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="7ee00-266">Cette clé de Registre n’est pas présente par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ee00-266">This registry key is not present by default.</span></span> <span data-ttu-id="7ee00-267">Lorsqu’il est défini, WinINet envoie les informations d’identification vers WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7ee00-267">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="7ee00-268">Chaque fois que WinHttp reçoit une demande d’authentification et si aucune information d’identification n’est définie sur le handle actuel, il utilise les informations d’identification fournies par WinINet.</span><span class="sxs-lookup"><span data-stu-id="7ee00-268">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="7ee00-269">Pour partager des informations d’identification de serveur en plus des informations d’identification de proxy, les utilisateurs doivent définir l' **\_ option WinHTTP utiliser les \_ \_ \_ \_ informations d’identification du serveur global** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-269">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-270"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_options WinHTTP \_ - \_ CREDS de serveur global \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-270"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-271">Prend un pointeur vers une structure d' [**\_ CREDS \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) d’identification WinHTTP avec le paramètre de fonction *hInternet* ayant la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-271">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="7ee00-272">Cette option requiert la clé de Registre **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings ! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-272">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="7ee00-273">Si cette clé de Registre n’est pas définie, WinHTTP retourne l' **\_ option erreur WinHTTP \_ non valide \_**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-273">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="7ee00-274">Cette clé de Registre n’est pas présente par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ee00-274">This registry key is not present by default.</span></span> <span data-ttu-id="7ee00-275">Lorsqu’il est défini, WinINet envoie les informations d’identification vers WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7ee00-275">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="7ee00-276">Chaque fois que WinHttp reçoit une demande d’authentification et si aucune information d’identification n’est définie sur le handle actuel, il utilise les informations d’identification fournies par WinINet.</span><span class="sxs-lookup"><span data-stu-id="7ee00-276">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="7ee00-277">Pour partager des informations d’identification de serveur en plus des informations d’identification de proxy, les utilisateurs doivent définir l' **\_ option WinHTTP utiliser les \_ \_ \_ \_ informations d’identification du serveur global** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-277">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-278"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TYPE de handle de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-278"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-279">Récupère une valeur d’entier long non signé qui contient le type du handle [HINTERNET](hinternet-handles-in-winhttp.md) passé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-279">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="7ee00-280">La valeur de retour peut être une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ee00-280">The return value can be one of the following:</span></span>

| <span data-ttu-id="7ee00-281">Terme</span><span class="sxs-lookup"><span data-stu-id="7ee00-281">Term</span></span> | <span data-ttu-id="7ee00-282">Description</span><span class="sxs-lookup"><span data-stu-id="7ee00-282">Description</span></span> |
|-|-|
| <span data-ttu-id="7ee00-283"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>\_connexion au \_ type de handle WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-283"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="7ee00-284">Le descripteur est un handle de connexion.</span><span class="sxs-lookup"><span data-stu-id="7ee00-284">The handle is a connection handle.</span></span> |
| <span data-ttu-id="7ee00-285"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_demande de \_ type de handle WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-285"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="7ee00-286">Le descripteur est un handle de demande.</span><span class="sxs-lookup"><span data-stu-id="7ee00-286">The handle is a request handle.</span></span> |
| <span data-ttu-id="7ee00-287"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_session de \_ type de handle WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-287"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="7ee00-288">Le descripteur est un handle de session.</span><span class="sxs-lookup"><span data-stu-id="7ee00-288">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7ee00-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_option WinHTTP \_ \_ protocole http \_ requis**</span><span class="sxs-lookup"><span data-stu-id="7ee00-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-290">Empêche l’utilisation de versions de protocole autres que celles activées par l' **\_ option WinHTTP activer le \_ \_ \_ protocole http** pour la demande.</span><span class="sxs-lookup"><span data-stu-id="7ee00-290">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-291"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**\_option WinHTTP \_ \_ protocole http \_ utilisé**</span><span class="sxs-lookup"><span data-stu-id="7ee00-291"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-292">Obtient une valeur DWORD qui indique quelle version HTTP avancée a été utilisée sur une demande donnée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-292">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="7ee00-293">Pour obtenir la liste des valeurs possibles, **consultez \_ option WinHTTP \_ activer le \_ \_ protocole http**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-293">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-294"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_ \_ version http de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-294"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-295">Définit ou récupère une structure [**d' \_ \_ informations de version http**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) qui contient la version http prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7ee00-295">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="7ee00-296">Il s’agit d’une option à l’ensemble du processus ; Utilisez la **valeur null** pour le descripteur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-296">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-297"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**\_Option WinHTTP \_ http2 \_ KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="7ee00-297"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP\_OPTION\_HTTP2\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7ee00-298">Cette option peut être définie sur un handle de session pour que WinHttp utilise des trames PING HTTP/2 comme mécanisme KeepAlive.</span><span class="sxs-lookup"><span data-stu-id="7ee00-298">This option can be set on a session handle to have WinHttp use HTTP/2 PING frames as a keepalive mechanism.</span></span> <span data-ttu-id="7ee00-299">Les appelants spécifient un délai d’expiration en millisecondes et, après l’absence d’activité sur une connexion pour ce délai, WinHttp commence à envoyer des trames PING HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="7ee00-299">Callers specify a timeout in milliseconds, and after there is no activity on a connection for that timeout period, WinHttp will begin to send HTTP/2 PING frames.</span></span> <span data-ttu-id="7ee00-300">Les appelants ne peuvent pas définir une valeur de délai d’expiration inférieure à 5000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-300">Callers cannot set a timeout value less than 5000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-301"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**\_Option WinHTTP \_ http2 \_ plus \_ \_ encodage de transfert**</span><span class="sxs-lookup"><span data-stu-id="7ee00-301"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7ee00-302">Cette option peut être définie sur un handle de demande WinHttp pour contrôler la façon dont WinHttp se comporte lorsqu’une réponse HTTP/2 contient un en-tête « Transfer-Encoding ».</span><span class="sxs-lookup"><span data-stu-id="7ee00-302">This option can be set on a WinHttp request handle to control how WinHttp behaves when an HTTP/2 response contains a "Transfer-Encoding" header.</span></span> <span data-ttu-id="7ee00-303">Dans ce cas, WinHttp retourne une erreur si cette option a la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-303">In such a case, WinHttp will return an error if this option is set to **FALSE**.</span></span>


</dt> </dl> </dd> <dt>


<span data-ttu-id="7ee00-304"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_option WinHTTP \_ Ignorer \_ la \_ révocation de certificat \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="7ee00-304"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-305">Autorise les connexions sécurisées à utiliser des certificats de sécurité pour lesquels la liste de révocation de certificats n’a pas pu être téléchargée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-305">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-306"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_Option WinHTTP \_ \_ Fast \_ Fallback IPv6**</span><span class="sxs-lookup"><span data-stu-id="7ee00-306"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-307">Active la connexion Fast de secours IPv6 (les yeux plus heureux) pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="7ee00-307">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="7ee00-308">Ce comportement est similaire au comportement de l’œil heureux décrit dans le [document RFC 6555](https://tools.ietf.org/html/rfc6555) pour améliorer les temps de connexion sur les réseaux où IPv6 n’est pas fiable.</span><span class="sxs-lookup"><span data-stu-id="7ee00-308">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="7ee00-309">Si les adresses IPv6 et IPv4 sont résolues pour un hôte donné, WinHttp commence par se connecter à la première adresse IPv6 résolue avec un délai d’expiration court (300 mètres).</span><span class="sxs-lookup"><span data-stu-id="7ee00-309">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="7ee00-310">En cas d’échec de cette connexion, WinHttp tente de se connecter à la première adresse IPv4 résolue avec le délai d’attente standard.</span><span class="sxs-lookup"><span data-stu-id="7ee00-310">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="7ee00-311">En cas d’échec de la deuxième connexion, WinHttp réessaiera la première adresse IPv6 résolue avec le délai d’expiration standard.</span><span class="sxs-lookup"><span data-stu-id="7ee00-311">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="7ee00-312">En cas d’échec de la troisième connexion, WinHttp rétablit le comportement par défaut pour toutes les adresses restantes, en tentant une connexion avec le délai d’expiration standard jusqu’à ce qu’une connexion soit établie ou qu’aucune adresse ne soit conservée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-312">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-313"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**l' \_ option WinHTTP \_ est une \_ \_ réponse de connexion proxy \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-313"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-314">Obtient une valeur indiquant si une réponse de connexion de retour de proxy peut être récupérée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-314">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-315"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_Option WinHTTP \_ nombre de Conn. \_ \_ par \_ \_ serveur 1 0 \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-315"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-316">Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par serveur HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="7ee00-316">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="7ee00-317">La valeur par défaut est **infinite**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-317">The default value is **INFINITE**.</span></span>

<span data-ttu-id="7ee00-318">**Windows Vista avec SP1 et Windows Server 2008 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="7ee00-318">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-319"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_option WinHTTP \_ nombre maximal de \_ conn. \_ par \_ serveur**</span><span class="sxs-lookup"><span data-stu-id="7ee00-319"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-320">Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par serveur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-320">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="7ee00-321">La valeur par défaut est **infinite**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-321">The default value is **INFINITE**.</span></span>

<span data-ttu-id="7ee00-322">Lorsque cette option a la valeur zéro, WinHTTP définit la limite du nombre de connexions à 2.</span><span class="sxs-lookup"><span data-stu-id="7ee00-322">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-323"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**\_option WinHTTP \_ nombre maximal de \_ \_ \_ redirections http automatiques**</span><span class="sxs-lookup"><span data-stu-id="7ee00-323"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-324">Définit le nombre maximal de redirections que WinHTTP suit ; la valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="7ee00-324">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="7ee00-325">Cette limite empêche les sites non autorisés de suspendre le client WinHTTP après un grand nombre de redirections.</span><span class="sxs-lookup"><span data-stu-id="7ee00-325">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="7ee00-326">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="7ee00-326">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-327"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_ \_ État http max de l’option WinHTTP \_ \_ \_ continue**</span><span class="sxs-lookup"><span data-stu-id="7ee00-327"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-328">Le nombre maximal de réponses du code d’État 100-199 est ignoré avant de renvoyer le code d’état final au client WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7ee00-328">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="7ee00-329">Les codes d’État informations 100-199 peuvent être envoyés par le serveur avant le code d’état final et sont décrits dans la spécification pour HTTP/1.1 (pour plus d’informations, consultez [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="7ee00-329">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="7ee00-330">La valeur par défaut est de 10.</span><span class="sxs-lookup"><span data-stu-id="7ee00-330">The default is 10.</span></span>

<span data-ttu-id="7ee00-331">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="7ee00-331">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-332"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**\_option WinHTTP \_ taille maximale de \_ \_ drainage \_ de la réponse**</span><span class="sxs-lookup"><span data-stu-id="7ee00-332"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-333">Lié sur la quantité de données vidées des réponses afin de réutiliser une connexion, spécifiée en octets.</span><span class="sxs-lookup"><span data-stu-id="7ee00-333">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="7ee00-334">La valeur par défaut est 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="7ee00-334">The default is 1MB.</span></span>

<span data-ttu-id="7ee00-335">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="7ee00-335">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-336"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_ \_ taille maximale d' \_ \_ en-tête de réponse \_ de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-336"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-337">Une limite définie sur la taille maximale de la partie en-tête de la réponse du serveur, spécifiée en octets.</span><span class="sxs-lookup"><span data-stu-id="7ee00-337">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="7ee00-338">Cette liaison protège le client contre les tentatives de blocage du client par un serveur non autorisé en envoyant une réponse avec une quantité infinie de données d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="7ee00-338">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="7ee00-339">La valeur par défaut est 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="7ee00-339">The default value is 64KB.</span></span>

<span data-ttu-id="7ee00-340">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="7ee00-340">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-341"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ handle parent de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-341"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-342">Récupère le handle parent de ce handle.</span><span class="sxs-lookup"><span data-stu-id="7ee00-342">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-343"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**OPTION WINHTTP du texte de la \_ \_ \_ comarketingisation Passport \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-343"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-344">Récupère une chaîne qui contient le texte de [*copersonnalisation*](glossary.md) fourni par le serveur d’ouverture de session Passport.</span><span class="sxs-lookup"><span data-stu-id="7ee00-344">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="7ee00-345">Cette option doit être récupérée immédiatement après que le serveur d’ouverture de session a répondu avec un code d’état 401.</span><span class="sxs-lookup"><span data-stu-id="7ee00-345">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="7ee00-346">Une application doit passer une taille de mémoire tampon, en octets, qui est suffisamment grande pour contenir la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-346">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-347"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_URL de \_ la \_ comarketing de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-347"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-348">Récupère une chaîne qui contient une URL pour un graphique de [*copersonnalisation*](glossary.md) fourni par le serveur d’ouverture de session Passport.</span><span class="sxs-lookup"><span data-stu-id="7ee00-348">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="7ee00-349">Cette option doit être récupérée immédiatement après que le serveur d’ouverture de session a répondu avec un code d’état 401.</span><span class="sxs-lookup"><span data-stu-id="7ee00-349">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="7ee00-350">Une application doit passer une taille de mémoire tampon, en octets, qui est suffisamment grande pour contenir la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-350">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-351"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_URL de \_ \_ retour Passport \_ de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-351"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-352">Définit une option en lecture seule sur un handle de demande qui récupère l’URL de retour Passport.</span><span class="sxs-lookup"><span data-stu-id="7ee00-352">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-353"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**déconnexion de l’option WINHTTP de \_ \_ Passport \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-353"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-354">Définit l’option sur un handle de session pour se déconnecter de toutes les connexions Passport.</span><span class="sxs-lookup"><span data-stu-id="7ee00-354">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="7ee00-355">Une application doit transmettre l’URL de retour Passport qui a été récupérée avec l' **\_ option WinHTTP \_ \_ \_ URL de renvoi Passport**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-355">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="7ee00-356">Tous les cookies associés à l’URL de renvoi sont effacés.</span><span class="sxs-lookup"><span data-stu-id="7ee00-356">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-357"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_ \_ mot de passe de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-357"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-358">Définit ou récupère une valeur de chaîne qui contient le mot de passe associé à un handle de demande.</span><span class="sxs-lookup"><span data-stu-id="7ee00-358">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-359"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_proxy d’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-359"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-360">Définit ou récupère une structure [**d' \_ \_ informations de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) qui contient les données de proxy sur un handle de session ou un handle de demande existant.</span><span class="sxs-lookup"><span data-stu-id="7ee00-360">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="7ee00-361">Lors de la récupération de données de proxy, une application doit libérer les chaînes **lpszProxy** et **lpszProxyBypass** contenues dans cette structure (si elles n’ont pas la **valeur null**) à l’aide de la fonction [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="7ee00-361">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="7ee00-362">Une application peut interroger les données de proxy globales (le proxy par défaut) en passant un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-362">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-363"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_ \_ \_ mot de passe proxy de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-363"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-364">Définit ou récupère une valeur de chaîne qui contient le mot de passe utilisé pour accéder au proxy.</span><span class="sxs-lookup"><span data-stu-id="7ee00-364">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-365"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**nom de principal du proxy de l' \_ option WinHTTP \_ \_ \_ utilisé**</span><span class="sxs-lookup"><span data-stu-id="7ee00-365"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-366">Obtient le nom principal du serveur proxy que WinHTTP a fourni à SSPI pendant l’authentification.</span><span class="sxs-lookup"><span data-stu-id="7ee00-366">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="7ee00-367">Cette valeur de chaîne est usefor transmettant à [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) après un échec d’authentification.</span><span class="sxs-lookup"><span data-stu-id="7ee00-367">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-368"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_ \_ \_ nom d’utilisateur proxy de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-368"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-369">Définit ou récupère une valeur de chaîne qui contient le nom d’utilisateur utilisé pour accéder au proxy.</span><span class="sxs-lookup"><span data-stu-id="7ee00-369">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-370"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_taille de \_ la \_ mémoire tampon de lecture de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-370"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-371">Cette option est dépréciée ; elle n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="7ee00-371">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-372"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**réponse de la connexion du proxy de réception de l' \_ option WinHTTP \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-372"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-373">Définit si l’entité de réponse du proxy peut être récupérée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-373">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="7ee00-374">Cette option est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ee00-374">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-375"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**\_délai de \_ réponse de réception \_ \_ de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-375"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-376">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, à attendre pour recevoir tous les en-têtes de réponse d’une demande.</span><span class="sxs-lookup"><span data-stu-id="7ee00-376">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="7ee00-377">Si WinHTTP ne parvient pas à recevoir tous les en-têtes dans ce délai, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-377">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="7ee00-378">La valeur du délai d’attente par défaut est de 90 secondes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-378">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="7ee00-379">Ce délai d’expiration est vérifié uniquement lorsque des données sont reçues du Socket.</span><span class="sxs-lookup"><span data-stu-id="7ee00-379">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="7ee00-380">Par conséquent, lorsque le délai d’attente expire, l’application cliente n’est pas notifiée tant que davantage de données n’arrivent pas sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-380">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="7ee00-381">Si aucune donnée n’arrive à partir du serveur, le délai entre l’expiration du délai d’attente et la notification de l’application cliente peut être aussi important que celui défini à l’aide du paramètre *dwReceiveTimeout* de la fonction [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .</span><span class="sxs-lookup"><span data-stu-id="7ee00-381">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-382"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_délai de \_ réception des options WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-382"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-383">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour recevoir une réponse partielle à une demande ou lire des données.</span><span class="sxs-lookup"><span data-stu-id="7ee00-383">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="7ee00-384">Si la réponse prend plus de temps que cette valeur de délai d’attente, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-384">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="7ee00-385">La valeur de délai d'attente par défaut est de 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-385">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-386"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_stratégie de \_ redirection des options WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-386"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-387">Définit le comportement de WinHTTP en ce qui concerne la gestion d’un code d’état de redirection HTTP 30.</span><span class="sxs-lookup"><span data-stu-id="7ee00-387">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="7ee00-388">Cette option peut être définie sur une session ou un handle de demande sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ee00-388">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="7ee00-389">Terme</span><span class="sxs-lookup"><span data-stu-id="7ee00-389">Term</span></span> | <span data-ttu-id="7ee00-390">Description</span><span class="sxs-lookup"><span data-stu-id="7ee00-390">Description</span></span> |
|-|-|
| <span data-ttu-id="7ee00-391"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_la stratégie de REdirection de l’option WinHTTP est \_ \_ \_ toujours</span><span class="sxs-lookup"><span data-stu-id="7ee00-391"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="7ee00-392">Toutes les redirections sont suivies automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7ee00-392">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="7ee00-393"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_ \_ la stratégie de redirection des options WinHTTP \_ \_ interdit \_ https \_ à \_ http</span><span class="sxs-lookup"><span data-stu-id="7ee00-393"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="7ee00-394">Toutes les redirections sont suivies, à l’exception de celles qui proviennent d’une URL sécurisée (https) vers une URL non sécurisée (http).</span><span class="sxs-lookup"><span data-stu-id="7ee00-394">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="7ee00-395">Il s'agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ee00-395">This is the default setting.</span></span> |
| <span data-ttu-id="7ee00-396"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>\_stratégie de \_ redirection des options WinHTTP \_ \_ jamais</span><span class="sxs-lookup"><span data-stu-id="7ee00-396"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="7ee00-397">Les redirections ne sont jamais suivies.</span><span class="sxs-lookup"><span data-stu-id="7ee00-397">Redirects are never followed.</span></span> <span data-ttu-id="7ee00-398">L’état de 30 est renvoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="7ee00-398">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-399"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_option WinHTTP \_ Reject \_ USERPWD \_ dans l' \_ URL**</span><span class="sxs-lookup"><span data-stu-id="7ee00-399"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-400">Rejette les URL qui contiennent un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7ee00-400">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="7ee00-401">Cette option rejette également les URL qui contiennent la sémantique *username : password* , même si aucun nom d’utilisateur ou mot de passe n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ee00-401">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="7ee00-402">Par exemple, « u:p@hostname », « :@hostname », « u:@hostname » et « :p@hostname » sont tous marqués comme étant non valides.</span><span class="sxs-lookup"><span data-stu-id="7ee00-402">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="7ee00-403">Si une URL non valide est transmise à la fonction, elle retourne l' [erreur \_ WinHTTP \_ \_ URL non valide](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="7ee00-403">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="7ee00-404">Cette option est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ee00-404">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-405"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**priorité des demandes de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-405"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-406">Cette option est dépréciée ; elle n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="7ee00-406">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-407"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_statistiques des \_ demandes d’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-407"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-408">Extrait les statistiques de la demande.</span><span class="sxs-lookup"><span data-stu-id="7ee00-408">Retreives statistics for the request.</span></span>  <span data-ttu-id="7ee00-409">Pour obtenir la liste des statistiques disponibles, consultez [**\_ \_ statistiques des demandes WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="7ee00-409">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-410"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**\_ \_ durées de demande de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-410"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-411">Informations de minutage extrait pour la requête.</span><span class="sxs-lookup"><span data-stu-id="7ee00-411">Retreives timing information for the request.</span></span> <span data-ttu-id="7ee00-412">Pour obtenir la liste des minutages disponibles, consultez [**\_ \_ durée des requêtes WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="7ee00-412">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-413"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**l' \_ option WinHTTP \_ nécessite une \_ fin de flux \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-413"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP\_OPTION\_REQUIRE\_STREAM\_END**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7ee00-414">Cette option indique à WinHttp d’ignorer les en-têtes de réponse « Content-Length » et de continuer à recevoir sur un flux jusqu’à ce que l’indicateur END_STREAM soit reçu.</span><span class="sxs-lookup"><span data-stu-id="7ee00-414">This option tells WinHttp to ignore "Content-Length" response headers, and continue receiving on a stream until the END_STREAM flag is received.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-415"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**\_nom d' \_ hôte de résolution de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-415"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7ee00-416">Cette option peut être définie sur un handle de demande WinHttp avant son envoi.</span><span class="sxs-lookup"><span data-stu-id="7ee00-416">This option can be set on a WinHttp request handle before it has been sent.</span></span> <span data-ttu-id="7ee00-417">Si cette valeur est définie, WinHttp utilise la chaîne fournie par l’appelant comme nom d’hôte pour la résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="7ee00-417">If set, WinHttp will use the caller-provided string as the hostname for DNS resolution.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-418"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**délai de résolution de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-418"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-419">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour résoudre un nom d’hôte.</span><span class="sxs-lookup"><span data-stu-id="7ee00-419">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="7ee00-420">La valeur par défaut du délai d’attente est **infinie**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-420">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="7ee00-421">Si une valeur non définie par défaut est spécifiée, il existe une surcharge liée à la création d’un thread par la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="7ee00-421">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-422"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**\_ \_ protocoles sécurisés option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-422"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-423">Définit une valeur d’entier long non signé qui spécifie les protocoles sécurisés qui sont acceptables.</span><span class="sxs-lookup"><span data-stu-id="7ee00-423">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="7ee00-424">Par défaut, les paramètres SSL3 et TLS1 sont activés uniquement dans Windows 7 et Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7ee00-424">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="7ee00-425">Par défaut, les protocoles SSL3, TLS 1.0, TLS 1.1 et TLS 1.2 sont activés dans Windows 8.1 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7ee00-425">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="7ee00-426">La valeur peut être une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-426">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="7ee00-427">Terme</span><span class="sxs-lookup"><span data-stu-id="7ee00-427">Term</span></span> | <span data-ttu-id="7ee00-428">Description</span><span class="sxs-lookup"><span data-stu-id="7ee00-428">Description</span></span> |
|-|-|
| <span data-ttu-id="7ee00-429"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>\_indicateur WinHTTP \_ \_ tout protocole \_ sécurisé</span><span class="sxs-lookup"><span data-stu-id="7ee00-429"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="7ee00-430">Les protocoles SSL (Secure Sockets Layer) (SSL) 2,0, SSL 3,0 et TLS (Transport Layer Security) 1,0 peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="7ee00-430">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="7ee00-431"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>\_SSL2 de \_ \_ protocole sécurisé d’indicateur \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-431"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="7ee00-432">Le protocole SSL 2,0 peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-432">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="7ee00-433"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>\_Indicateur WinHTTP \_ \_ protocole sécurisé \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="7ee00-433"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="7ee00-434">Le protocole SSL 3,0 peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-434">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="7ee00-435"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>\_TLS1 de \_ \_ protocole sécurisé d’indicateur \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-435"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="7ee00-436">Le protocole TLS 1,0 peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-436">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="7ee00-437"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>\_Protocole sécurisé d’indicateur WinHTTP \_ \_ \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="7ee00-437"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="7ee00-438">Le protocole TLS 1,1 peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-438">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="7ee00-439"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>\_Indicateur WinHTTP \_ \_ protocole sécurisé \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="7ee00-439"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="7ee00-440">Le protocole TLS 1,2 peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-440">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7ee00-441"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_structure de \_ certificat de sécurité option \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-441"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-442">Récupère le certificat pour un serveur SSL/TLS dans la structure [**des \_ \_ informations de certificat WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) .</span><span class="sxs-lookup"><span data-stu-id="7ee00-442">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="7ee00-443">L’application doit libérer les membres **lpszSubjectInfo** et **lpszIssuerInfo** avec [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span><span class="sxs-lookup"><span data-stu-id="7ee00-443">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-444"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**indicateurs de sécurité de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-444"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-445">Définit ou récupère une valeur d’entier long non signé qui contient les indicateurs de sécurité d’un handle.</span><span class="sxs-lookup"><span data-stu-id="7ee00-445">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="7ee00-446">Il peut s’agir d’une combinaison de ces valeurs :</span><span class="sxs-lookup"><span data-stu-id="7ee00-446">It can be a combination of these values:</span></span>

| <span data-ttu-id="7ee00-447">Terme</span><span class="sxs-lookup"><span data-stu-id="7ee00-447">Term</span></span> | <span data-ttu-id="7ee00-448">Description</span><span class="sxs-lookup"><span data-stu-id="7ee00-448">Description</span></span> |
|-|-|
| <span data-ttu-id="7ee00-449"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>indicateur de sécurité ignorer le nom \_ \_ commun du \_ certificat \_ \_ non valide</span><span class="sxs-lookup"><span data-stu-id="7ee00-449"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="7ee00-450">Autorise un nom commun non valide dans un certificat ; autrement dit, le nom du serveur spécifié par l’application ne correspond pas au nom commun dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="7ee00-450">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="7ee00-451">Si cet indicateur est défini, l’application ne reçoit pas d' **indicateur d’état de rappel WinHTTP certificat de rappel \_ \_ \_ \_ \_ \_ non valide** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-451">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="7ee00-452"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>indicateur de sécurité \_ \_ ignore la \_ Date de certificat \_ \_ non valide</span><span class="sxs-lookup"><span data-stu-id="7ee00-452"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="7ee00-453">Autorise une date de certificat non valide, c’est-à-dire un certificat arrivé à expiration ou qui n’est pas encore efficace.</span><span class="sxs-lookup"><span data-stu-id="7ee00-453">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="7ee00-454">Si cet indicateur est défini, l’application ne reçoit pas d' **indicateur d’état de rappel WinHTTP signaler la date de rappel de \_ \_ \_ \_ certificat \_ \_ non valide** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-454">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="7ee00-455"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>indicateur de sécurité \_ \_ ignorer l’autorité de \_ \_ certification inconnue</span><span class="sxs-lookup"><span data-stu-id="7ee00-455"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="7ee00-456">Autorise une autorité de certification non valide.</span><span class="sxs-lookup"><span data-stu-id="7ee00-456">Allows an invalid certificate authority.</span></span> <span data-ttu-id="7ee00-457">Si cet indicateur est défini, l’application ne reçoit pas d' **indicateur d’état de rappel WinHTTP un rappel d' \_ autorité de \_ \_ \_ \_ certification non valide** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-457">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="7ee00-458"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>indicateur de sécurité \_ \_ Ignorer \_ \_ \_ l’utilisation incorrecte du certificat</span><span class="sxs-lookup"><span data-stu-id="7ee00-458"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="7ee00-459">Autorise l’établissement de l’identité d’un serveur à l’aide d’un certificat non-serveur (par exemple, un certificat client).</span><span class="sxs-lookup"><span data-stu-id="7ee00-459">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="7ee00-460"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>indicateur de sécurité \_ \_ ignorer la \_ \_ signature faible</span><span class="sxs-lookup"><span data-stu-id="7ee00-460"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="7ee00-461">Permet d’ignorer une signature faible.</span><span class="sxs-lookup"><span data-stu-id="7ee00-461">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="7ee00-462">Cet indicateur est disponible dans la mise à jour cumulative pour chaque système d’exploitation à partir de Windows 7 et de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="7ee00-462">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="7ee00-463"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>indicateur de sécurité \_ \_ sécurisé</span><span class="sxs-lookup"><span data-stu-id="7ee00-463"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="7ee00-464">Utilise des transferts sécurisés.</span><span class="sxs-lookup"><span data-stu-id="7ee00-464">Uses secure transfers.</span></span> <span data-ttu-id="7ee00-465">Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="7ee00-465">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="7ee00-466"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>niveau de force de l’indicateur de sécurité \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-466"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="7ee00-467">Utilise le chiffrement moyen (56 bits).</span><span class="sxs-lookup"><span data-stu-id="7ee00-467">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="7ee00-468">Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="7ee00-468">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="7ee00-469"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>force de l’indicateur de sécurité \_ \_ \_ Strong</span><span class="sxs-lookup"><span data-stu-id="7ee00-469"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="7ee00-470">Utilise le chiffrement fort (128 bits).</span><span class="sxs-lookup"><span data-stu-id="7ee00-470">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="7ee00-471">Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="7ee00-471">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="7ee00-472"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>force de l’indicateur de sécurité \_ \_ \_ faible</span><span class="sxs-lookup"><span data-stu-id="7ee00-472"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="7ee00-473">Utilise un chiffrement faible (40 bits).</span><span class="sxs-lookup"><span data-stu-id="7ee00-473">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="7ee00-474">Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="7ee00-474">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7ee00-475"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**informations de sécurité de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-475"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-476">Extrait les informations de chiffrement et de connexion SChannel pour une demande.</span><span class="sxs-lookup"><span data-stu-id="7ee00-476">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-477"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**nombre de bits de la clé de sécurité de l' \_ option WinHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-477"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-478">Récupère une valeur d’entier long non signé qui contient la force de chiffrement de la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="7ee00-478">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="7ee00-479">Un nombre plus élevé indique un chiffrement de niveau de chiffrement renforcé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-479">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-480"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**\_ \_ \_ délai d’attente d’envoi des options WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-480"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-481">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour envoyer une demande ou écrire des données.</span><span class="sxs-lookup"><span data-stu-id="7ee00-481">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="7ee00-482">Si l’envoi de la demande prend plus de temps que le délai d’attente, l’opération d’envoi est annulée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-482">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="7ee00-483">Le délai d’attente par défaut est de 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-483">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-484"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**\_serveur d’option WinHTTP \_ \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="7ee00-484"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-485">Obtient un pointeur vers une structure de [**\_ liaisons SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) qui spécifie un jeton de liaison de canal (CBT).</span><span class="sxs-lookup"><span data-stu-id="7ee00-485">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="7ee00-486">Un jeton de liaison de canal est une propriété d’un canal de transport sécurisé et est utilisé pour lier un canal d’authentification au canal de transport sécurisé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-486">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="7ee00-487">Ce jeton ne peut être obtenu que par cette option après l’établissement d’une connexion SSL.</span><span class="sxs-lookup"><span data-stu-id="7ee00-487">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="7ee00-488">Le passage de cette option et d’une valeur **null** pour *lpBuffer* à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) renvoie une erreur \_ mémoire tampon insuffisante \_ et la taille d’octet requise pour la mémoire tampon dans le paramètre *lpdwBufferLength* .</span><span class="sxs-lookup"><span data-stu-id="7ee00-488">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="7ee00-489">La valeur de la taille de la mémoire tampon retournée peut être passée dans un appel ultérieur à Query pour le jeton de liaison de canal.</span><span class="sxs-lookup"><span data-stu-id="7ee00-489">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="7ee00-490">Ces étapes sont nécessaires lors \_ \_ de la gestion de \_ la demande d’état de rappel WinHTTP si vous souhaitez modifier les en-têtes de requête en fonction du jeton de liaison de canal.</span><span class="sxs-lookup"><span data-stu-id="7ee00-490">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="7ee00-491">Notez que Windows XP et Vista ne prennent pas en charge la modification des en-têtes de demande pendant ce rappel.</span><span class="sxs-lookup"><span data-stu-id="7ee00-491">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-492"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**\_contexte de \_ chaîne du certificat de serveur d’option WinHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-492"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-493">Récupère le contexte de la chaîne de certification du serveur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-493">Retrieves the server certification chain context.</span></span> <span data-ttu-id="7ee00-494">**WinHTTP \_ L' \_ option \_ \_ \_ contexte de chaîne de certificat serveur** peut être passée pour obtenir un pointeur dupliqué vers le **\_ \_ contexte de chaîne** de certificat pour une chaîne de certificats de serveur reçue pendant une connexion SSL négociée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-494">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="7ee00-495">Le client doit appeler [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) sur le pointeur de \_ contexte PCCERT retourné qui est rempli dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7ee00-495">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-496"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**\_contexte de \_ certificat de serveur d’option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-496"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-497">Récupère le contexte de certification du serveur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-497">Retrieves the server certification context.</span></span> <span data-ttu-id="7ee00-498">**WinHTTP \_ Le \_ \_ \_ contexte** du certificat de serveur d’option peut être passé pour obtenir un pointeur dupliqué vers le [**contexte**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificat pour un certificat de serveur reçu pendant une connexion SSL négociée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-498">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="7ee00-499">Le client doit appeler [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) sur le pointeur de \_ contexte PCCERT retourné qui est rempli dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7ee00-499">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-500"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**nom principal de service du \_ serveur option WinHTTP \_ \_ \_ utilisé**</span><span class="sxs-lookup"><span data-stu-id="7ee00-500"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-501">Obtient le nom principal du serveur serveur que WinHTTP a fourni à SSPI pendant l’authentification.</span><span class="sxs-lookup"><span data-stu-id="7ee00-501">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="7ee00-502">Cette valeur de chaîne peut être passée à [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) après un échec d’authentification.</span><span class="sxs-lookup"><span data-stu-id="7ee00-502">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-503"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**SPN de l' \_ option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-503"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-504">Permet d’inclure ou de supprimer le numéro de port du serveur lorsque le SPN (nom de principal du service) est créé pour l’authentification Kerberos ou Negotiate Kerberos.</span><span class="sxs-lookup"><span data-stu-id="7ee00-504">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="7ee00-505">Cet indicateur est l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ee00-505">This flag is one of the following values:</span></span>

| <span data-ttu-id="7ee00-506">Terme</span><span class="sxs-lookup"><span data-stu-id="7ee00-506">Term</span></span> | <span data-ttu-id="7ee00-507">Description</span><span class="sxs-lookup"><span data-stu-id="7ee00-507">Description</span></span> |
|-|-|
| <span data-ttu-id="7ee00-508"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>\_port du \_ serveur de nom principal de service WinHTTP désactivé \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-508"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="7ee00-509">Supprime le numéro de port du serveur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-509">Removes the server port number.</span></span> |
| <span data-ttu-id="7ee00-510"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>\_port du \_ serveur de nom principal de service WinHTTP activé \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-510"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="7ee00-511">Comprend le numéro de port du serveur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-511">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7ee00-512"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**\_code d' \_ erreur de flux d’options WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-512"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP\_OPTION\_STREAM\_ERROR\_CODE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7ee00-513">Cette option peut être interrogée sur un handle de demande WinHttp et retourne le code d’erreur indiqué par une RST_STREAM Frame reçue sur un flux HTTP.</span><span class="sxs-lookup"><span data-stu-id="7ee00-513">This option can be queried on a WinHttp request handle, and will return the error code indicated by a RST_STREAM frame received on an HTTP stream.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-514"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**\_option WinHTTP \_ TCP \_ Fast \_ Open**</span><span class="sxs-lookup"><span data-stu-id="7ee00-514"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-515">Active TCP Fast Open pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="7ee00-515">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-516"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_option WinHTTP \_ TCP \_ KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="7ee00-516"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-517">Cette option peut être définie sur un handle de session WinHttp pour activer le comportement TCP Keep-Alive sur le Socket sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="7ee00-517">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="7ee00-518">Prend un struct [**TCP \_ KeepAlive**](/windows/win32/winsock/sio-keepalive-vals) .</span><span class="sxs-lookup"><span data-stu-id="7ee00-518">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-519"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**OPTION WINHTTP-début de la \_ \_ \_ valeur TLS false \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-519"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-520">Active le démarrage TLS false pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="7ee00-520">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-521"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**\_option WinHTTP \_ \_ protocole TLS \_ non sécurisé de \_ secours**</span><span class="sxs-lookup"><span data-stu-id="7ee00-521"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-522">Cette option peut être définie sur un handle de session WinHttp pour contrôler si le recours à TLS 1,0 est autorisé en cas d’échec de la liaison TLS avec une version de protocole plus récente.</span><span class="sxs-lookup"><span data-stu-id="7ee00-522">This option can be set on a WinHttp session handle to control whether fallback to TLS 1.0 is allowed if there is a TLS handshake failure with a newer protocol version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-523"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**\_événement de \_ notification de déchargement d’option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-523"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-524">Prend un événement qui sera défini lorsque le dernier rappel est terminé pour une session particulière.</span><span class="sxs-lookup"><span data-stu-id="7ee00-524">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="7ee00-525">Cet indicateur doit être utilisé sur un handle de session.</span><span class="sxs-lookup"><span data-stu-id="7ee00-525">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="7ee00-526">L’événement ne peut pas être fermé tant qu’il n’a pas été défini par WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7ee00-526">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-527"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**\_option WinHTTP \_ \_ -analyse d’en-tête non sécurisé \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-527"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-528">Cette option est réservée à un usage interne et ne doit pas être appelée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-528">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-529"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**\_option WinHTTP \_ mettre à niveau \_ vers \_ Web \_ Socket**</span><span class="sxs-lookup"><span data-stu-id="7ee00-529"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-530">Demande à la pile de démarrer un processus d’établissement de liaison WebSocket avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="7ee00-530">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="7ee00-531">Cette option n’accepte aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7ee00-531">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-532"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**URL de l' \_ option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-532"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-533">Récupère une valeur de chaîne qui contient l’URL complète d’une ressource téléchargée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-533">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="7ee00-534">Si l’URL d’origine contenait des données supplémentaires, telles que des chaînes ou des ancres de recherche, ou si l’appel a été redirigé, l’URL retournée est différente de l’original.</span><span class="sxs-lookup"><span data-stu-id="7ee00-534">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="7ee00-535">L’application doit passer une mémoire tampon, dimensionnée en octets, qui est suffisamment grande pour contenir l’URL retournée en caractères larges.</span><span class="sxs-lookup"><span data-stu-id="7ee00-535">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-536"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_option WinHTTP \_ utiliser \_ les \_ \_ informations d’identification du serveur global**</span><span class="sxs-lookup"><span data-stu-id="7ee00-536"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-537">Prend un **bool** et ne peut être défini qu’avec un handle de session.</span><span class="sxs-lookup"><span data-stu-id="7ee00-537">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="7ee00-538">Il se propage uniquement aux descripteurs créés à partir du descripteur de session après que l’option a été définie.</span><span class="sxs-lookup"><span data-stu-id="7ee00-538">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="7ee00-539">Si la **valeur est true**, cette option entraîne, en dernier recours, l’utilisation d’informations d’identification de serveur globales qui ont été transférées depuis wininet.</span><span class="sxs-lookup"><span data-stu-id="7ee00-539">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="7ee00-540">La valeur par défaut de cette option est **false**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-540">The default for this option is **FALSE**.</span></span> <span data-ttu-id="7ee00-541">Cette option requiert la clé de Registre **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings ! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-541">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="7ee00-542">Cette clé de Registre n’est pas présente par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ee00-542">This registry key is not present by default.</span></span> <span data-ttu-id="7ee00-543">Lorsqu’il est défini, WinINet envoie les informations d’identification vers WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7ee00-543">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="7ee00-544">Chaque fois que WinHttp reçoit une demande d’authentification et si aucune information d’identification n’est définie sur le handle actuel, il utilise les informations d’identification fournies par WinINet.</span><span class="sxs-lookup"><span data-stu-id="7ee00-544">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-545"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_ \_ agent utilisateur de \_ l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-545"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-546">Définit ou récupère la chaîne de l' [*agent utilisateur*](glossary.md) sur les handles fournis par [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) et utilisés dans les fonctions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) suivantes, à condition qu’elles ne soient pas remplacées par un en-tête ajouté par [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) ou **WinHttpSendRequest**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-546">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="7ee00-547">Lors de la récupération d’un agent utilisateur, l’application doit passer une mémoire tampon, dimensionnée en octets, qui est suffisamment grande pour contenir l’URL retournée en caractères larges.</span><span class="sxs-lookup"><span data-stu-id="7ee00-547">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="7ee00-548">Lors de la définition de l’agent utilisateur, la taille de la mémoire tampon correspond à la longueur de la chaîne, en caractères, plus la marque de fin **null** .</span><span class="sxs-lookup"><span data-stu-id="7ee00-548">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-549"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**\_option WinHTTP \_ nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="7ee00-549"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-550">Définit ou récupère une chaîne qui contient le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ee00-550">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-551"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_ \_ \_ \_ \_ délai d’attente de fermeture du socket Web de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-551"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-552">Définit le délai, en millisecondes, pendant lequel [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) doit attendre pour terminer le protocole de transfert de fermeture.</span><span class="sxs-lookup"><span data-stu-id="7ee00-552">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="7ee00-553">La valeur par défaut est 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-553">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-554"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**\_intervalle de \_ conservation \_ de \_ conservation de socket Web \_ d’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-554"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-555">Définit l’intervalle, en millisecondes, pour envoyer un paquet Keep-Alive sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="7ee00-555">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="7ee00-556">L’intervalle par défaut est de 30000 (30 secondes).</span><span class="sxs-lookup"><span data-stu-id="7ee00-556">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="7ee00-557">L’intervalle minimal est 15000 (15 secondes).</span><span class="sxs-lookup"><span data-stu-id="7ee00-557">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="7ee00-558">L’utilisation de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) pour définir une valeur inférieure à 15000 retourne **le \_ \_ paramètre error non valide**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-558">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="7ee00-559">La valeur par défaut de l' **option WinHTTP de l’intervalle de \_ \_ \_ conservation de socket \_ \_ Web** est lue à partir de **HKLM : \\ Software \\ Microsoft \\ WebSocket \\ KeepaliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="7ee00-559">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="7ee00-560">Si aucune valeur n’est définie, la valeur par défaut 30000 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-560">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="7ee00-561">Il n’est pas possible d’avoir un intervalle KeepAlive inférieur à 15000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="7ee00-561">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-562"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon de réception du socket Web \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-562"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-563">Définit ou récupère une valeur DWORD qui spécifie la taille de la mémoire tampon de réception à utiliser sur les connexions WebSocket.</span><span class="sxs-lookup"><span data-stu-id="7ee00-563">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-564"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon d’envoi du socket Web \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-564"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-565">Définit ou récupère une valeur DWORD qui spécifie la taille de la mémoire tampon d’envoi à utiliser sur les connexions WebSocket.</span><span class="sxs-lookup"><span data-stu-id="7ee00-565">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-566"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**\_nombre de \_ \_ threads de travail option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-566"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-567">Définit une valeur d’entier long non signé qui spécifie le nombre de threads de travail que le pool de threads doit utiliser pour les saisies semi-automatiques asynchrones.</span><span class="sxs-lookup"><span data-stu-id="7ee00-567">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="7ee00-568">La valeur par défaut de cette option est zéro, ce qui indique que le nombre de threads de travail est égal au nombre de processeurs sur le système.</span><span class="sxs-lookup"><span data-stu-id="7ee00-568">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="7ee00-569">Cette option ne peut être définie que sur un handle [HINTERNET](hinternet-handles-in-winhttp.md) **null** avant qu’une opération asynchrone se produise.  </span><span class="sxs-lookup"><span data-stu-id="7ee00-569">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="7ee00-570">Cette option ne peut être définie qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="7ee00-570">This option can only be set once.</span></span>

<span data-ttu-id="7ee00-571">**Windows Server 2008 R2 et Windows 7 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="7ee00-571">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ee00-572"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_taille de \_ la \_ mémoire tampon d’écriture de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-572"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ee00-573">Cette option est dépréciée ; elle n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="7ee00-573">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ee00-574">Remarques</span><span class="sxs-lookup"><span data-stu-id="7ee00-574">Remarks</span></span>

<span data-ttu-id="7ee00-575">Le tableau suivant répertorie les indicateurs d’option en spécifiant les descripteurs sur lesquels ils peuvent agir, s’ils peuvent être interrogés et définis, ainsi que le type de données utilisé.</span><span class="sxs-lookup"><span data-stu-id="7ee00-575">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="7ee00-576">Un « X » indique que l’indicateur d’option est valide pour une utilisation avec la fonction ou le handle, alors que « - » spécifie que l’indicateur d’option n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7ee00-576">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="7ee00-577">Si vous tentez de définir ou d’interroger un indicateur d’option sur une version de Windows où il n’est pas pris en charge, l' **\_ \_ \_ option WinHTTP non valide** est générée.</span><span class="sxs-lookup"><span data-stu-id="7ee00-577">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="7ee00-578">Indicateur d’option et type de données</span><span class="sxs-lookup"><span data-stu-id="7ee00-578">Option flag, and data type</span></span> | <span data-ttu-id="7ee00-579">Handle de session</span><span class="sxs-lookup"><span data-stu-id="7ee00-579">Session handle</span></span> | <span data-ttu-id="7ee00-580">Handle de demande</span><span class="sxs-lookup"><span data-stu-id="7ee00-580">Request handle</span></span> | <span data-ttu-id="7ee00-581">Option de requête</span><span class="sxs-lookup"><span data-stu-id="7ee00-581">Query option</span></span> | <span data-ttu-id="7ee00-582">Option Set</span><span class="sxs-lookup"><span data-stu-id="7ee00-582">Set option</span></span> | <span data-ttu-id="7ee00-583">Version minimale de Windows</span><span class="sxs-lookup"><span data-stu-id="7ee00-583">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="7ee00-584">OPTION WINHTTP assurée par les \_ \_ \_ \_ rappels non bloquants \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-584">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="7ee00-585">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-585">**BOOL**</span></span> | <span data-ttu-id="7ee00-586">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-586">X</span></span> | \- | \- | <span data-ttu-id="7ee00-587">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-587">X</span></span> | \- |
| <span data-ttu-id="7ee00-588">stratégie d’accès automatique aux \_ options WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-588">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="7ee00-589">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-589">**DWORD**</span></span> | \- | <span data-ttu-id="7ee00-590">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-590">X</span></span> | \- | <span data-ttu-id="7ee00-591">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-591">X</span></span> | \- |
| <span data-ttu-id="7ee00-592">\_rappel d’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-592">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="7ee00-593">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="7ee00-593">**LPVOID**</span></span> | <span data-ttu-id="7ee00-594">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-594">X</span></span> | <span data-ttu-id="7ee00-595">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-595">X</span></span> | <span data-ttu-id="7ee00-596">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-596">X</span></span> | <span data-ttu-id="7ee00-597">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-597">X</span></span> | \- |
| <span data-ttu-id="7ee00-598">\_contexte de \_ \_ certificat client \_ de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-598">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="7ee00-599">**contexte du certificat \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-599">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="7ee00-600">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-600">X</span></span> | \- | <span data-ttu-id="7ee00-601">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-601">X</span></span> | <span data-ttu-id="7ee00-602">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ee00-602">Windows Vista</span></span> |
| <span data-ttu-id="7ee00-603">\_option WinHTTP \_ \_ liste d’émetteurs de certificats client \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-603">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="7ee00-604">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="7ee00-604">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="7ee00-605">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-605">X</span></span> | <span data-ttu-id="7ee00-606">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-606">X</span></span> | \- | <span data-ttu-id="7ee00-607">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ee00-607">Windows Vista</span></span> |
| <span data-ttu-id="7ee00-608">page de codes de l' \_ option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-608">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="7ee00-609">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-609">**DWORD**</span></span> | <span data-ttu-id="7ee00-610">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-610">X</span></span> | \- | \- | <span data-ttu-id="7ee00-611">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-611">X</span></span> | \- |
| <span data-ttu-id="7ee00-612">\_option WinHTTP \_ configurer \_ l' \_ authentification Passport</span><span class="sxs-lookup"><span data-stu-id="7ee00-612">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="7ee00-613">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-613">**DWORD**</span></span> | <span data-ttu-id="7ee00-614">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-614">X</span></span> | \- | \- | <span data-ttu-id="7ee00-615">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-615">X</span></span> | \- |
| <span data-ttu-id="7ee00-616">\_ \_ nouvelles tentatives de connexion de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-616">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="7ee00-617">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-617">**DWORD**</span></span> | <span data-ttu-id="7ee00-618">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-618">X</span></span> | <span data-ttu-id="7ee00-619">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-619">X</span></span> | <span data-ttu-id="7ee00-620">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-620">X</span></span> | <span data-ttu-id="7ee00-621">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-621">X</span></span> | \- |
| <span data-ttu-id="7ee00-622">délai de connexion de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-622">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="7ee00-623">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-623">**DWORD**</span></span> | <span data-ttu-id="7ee00-624">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-624">X</span></span> | <span data-ttu-id="7ee00-625">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-625">X</span></span> | <span data-ttu-id="7ee00-626">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-626">X</span></span> | <span data-ttu-id="7ee00-627">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-627">X</span></span> | \- |
| <span data-ttu-id="7ee00-628">informations de connexion de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-628">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="7ee00-629">**\_informations de connexion WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-629">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="7ee00-630">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-630">X</span></span> | <span data-ttu-id="7ee00-631">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-631">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-632">\_Statistiques de connexion des options WinHTTP \_ \_ \_ v0</span><span class="sxs-lookup"><span data-stu-id="7ee00-632">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="7ee00-633">**\_Informations TCP \_ v0**</span><span class="sxs-lookup"><span data-stu-id="7ee00-633">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="7ee00-634">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-634">X</span></span> | <span data-ttu-id="7ee00-635">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-635">X</span></span> | \- | <span data-ttu-id="7ee00-636">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="7ee00-636">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7ee00-637">\_Statistiques de connexion des options WinHTTP \_ \_ \_ v1</span><span class="sxs-lookup"><span data-stu-id="7ee00-637">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="7ee00-638">**\_Informations TCP \_ v1**</span><span class="sxs-lookup"><span data-stu-id="7ee00-638">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="7ee00-639">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-639">X</span></span> | <span data-ttu-id="7ee00-640">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-640">X</span></span> | \- | <span data-ttu-id="7ee00-641">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="7ee00-641">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7ee00-642">valeur de contexte de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-642">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="7ee00-643">**\_ptr DWORD**</span><span class="sxs-lookup"><span data-stu-id="7ee00-643">**DWORD\_PTR**</span></span> | <span data-ttu-id="7ee00-644">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-644">X</span></span> | <span data-ttu-id="7ee00-645">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-645">X</span></span> | <span data-ttu-id="7ee00-646">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-646">X</span></span> | <span data-ttu-id="7ee00-647">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-647">X</span></span> | \- |
| <span data-ttu-id="7ee00-648">décompression des \_ options WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-648">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="7ee00-649">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-649">**DWORD**</span></span> | <span data-ttu-id="7ee00-650">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-650">X</span></span> | <span data-ttu-id="7ee00-651">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-651">X</span></span> | \- | <span data-ttu-id="7ee00-652">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-652">X</span></span> | <span data-ttu-id="7ee00-653">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7ee00-653">Windows 8.1</span></span> |
| <span data-ttu-id="7ee00-654">\_fonctionnalité de \_ désactivation de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-654">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="7ee00-655">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-655">**DWORD**</span></span> | \- | <span data-ttu-id="7ee00-656">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-656">X</span></span> | \- | <span data-ttu-id="7ee00-657">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-657">X</span></span> | \- |
| <span data-ttu-id="7ee00-658">\_option WinHTTP \_ désactiver \_ le \_ protocole sécurisé de \_ secours</span><span class="sxs-lookup"><span data-stu-id="7ee00-658">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="7ee00-659">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-659">**BOOL**</span></span> | <span data-ttu-id="7ee00-660">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-660">X</span></span> | \- | \- | <span data-ttu-id="7ee00-661">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-661">X</span></span> | <span data-ttu-id="7ee00-662">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="7ee00-662">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7ee00-663">OPTION WINHTTP- \_ \_ désactiver la \_ \_ file d’attente de flux</span><span class="sxs-lookup"><span data-stu-id="7ee00-663">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="7ee00-664">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-664">**BOOL**</span></span> | <span data-ttu-id="7ee00-665">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-665">X</span></span> | <span data-ttu-id="7ee00-666">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-666">X</span></span> | \- | <span data-ttu-id="7ee00-667">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-667">X</span></span> | <span data-ttu-id="7ee00-668">Windows 10 version 1809</span><span class="sxs-lookup"><span data-stu-id="7ee00-668">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="7ee00-669">\_option WinHTTP \_ activer la \_ fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="7ee00-669">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="7ee00-670">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-670">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="7ee00-671">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-671">X</span></span> | \- |
| <span data-ttu-id="7ee00-672">\_option WinHTTP \_ activer \_ le \_ protocole http</span><span class="sxs-lookup"><span data-stu-id="7ee00-672">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="7ee00-673">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-673">**DWORD**</span></span> | <span data-ttu-id="7ee00-674">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-674">X</span></span> | <span data-ttu-id="7ee00-675">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-675">X</span></span> | \- | <span data-ttu-id="7ee00-676">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-676">X</span></span> | <span data-ttu-id="7ee00-677">Windows 10 version 1607</span><span class="sxs-lookup"><span data-stu-id="7ee00-677">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="7ee00-678">\_Option WinHTTP \_ activer \_ le \_ \_ contexte de \_ certificat client http2 plus \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-678">WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT\_CONTEXT</span></span><br/><span data-ttu-id="7ee00-679">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-679">**BOOL**</span></span> | <span data-ttu-id="7ee00-680">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-680">X</span></span> | \- | \- | <span data-ttu-id="7ee00-681">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-681">X</span></span> | <span data-ttu-id="7ee00-682">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="7ee00-682">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7ee00-683">\_option WinHTTP \_ EnableTracing,</span><span class="sxs-lookup"><span data-stu-id="7ee00-683">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="7ee00-684">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-684">**DWORD**</span></span> | \- | \- | <span data-ttu-id="7ee00-685">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-685">X</span></span> | <span data-ttu-id="7ee00-686">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-686">X</span></span> | \- |
| <span data-ttu-id="7ee00-687">\_option WinHTTP \_ coder \_ extra</span><span class="sxs-lookup"><span data-stu-id="7ee00-687">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="7ee00-688">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-688">**BOOL**</span></span> | <span data-ttu-id="7ee00-689">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-689">X</span></span> | <span data-ttu-id="7ee00-690">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-690">X</span></span> | \- | <span data-ttu-id="7ee00-691">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-691">X</span></span> | <span data-ttu-id="7ee00-692">Windows 10 version 1803</span><span class="sxs-lookup"><span data-stu-id="7ee00-692">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="7ee00-693">expiration de la connexion de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-693">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="7ee00-694">N/A</span><span class="sxs-lookup"><span data-stu-id="7ee00-694">N/A</span></span> | \- | <span data-ttu-id="7ee00-695">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-695">X</span></span> | \- | <span data-ttu-id="7ee00-696">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-696">X</span></span> | <span data-ttu-id="7ee00-697">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="7ee00-697">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7ee00-698">\_ \_ erreur étendue de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-698">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="7ee00-699">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-699">**DWORD**</span></span> | <span data-ttu-id="7ee00-700">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-700">X</span></span> | <span data-ttu-id="7ee00-701">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-701">X</span></span> | <span data-ttu-id="7ee00-702">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-702">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-703">identification \_ du \_ proxy global des options \_ WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-703">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="7ee00-704">**\_références WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-704">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="7ee00-705">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-705">X</span></span> | <span data-ttu-id="7ee00-706">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-706">X</span></span> | \- | <span data-ttu-id="7ee00-707">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-707">X</span></span> | \- |
| <span data-ttu-id="7ee00-708">\_options WinHTTP \_ - \_ CREDS de serveur global \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-708">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="7ee00-709">**\_références WinHTTP \_ ex**</span><span class="sxs-lookup"><span data-stu-id="7ee00-709">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="7ee00-710">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-710">X</span></span> | <span data-ttu-id="7ee00-711">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-711">X</span></span> | \- | <span data-ttu-id="7ee00-712">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-712">X</span></span> | \- |
| <span data-ttu-id="7ee00-713">TYPE de handle de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-713">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="7ee00-714">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-714">**DWORD**</span></span> | <span data-ttu-id="7ee00-715">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-715">X</span></span> | <span data-ttu-id="7ee00-716">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-716">X</span></span> | <span data-ttu-id="7ee00-717">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-717">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-718">\_option WinHTTP \_ \_ protocole http \_ requis</span><span class="sxs-lookup"><span data-stu-id="7ee00-718">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="7ee00-719">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-719">**BOOL**</span></span> | <span data-ttu-id="7ee00-720">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-720">X</span></span> | <span data-ttu-id="7ee00-721">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-721">X</span></span> | \- | <span data-ttu-id="7ee00-722">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-722">X</span></span> | <span data-ttu-id="7ee00-723">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="7ee00-723">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7ee00-724">\_option WinHTTP \_ \_ protocole http \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="7ee00-724">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="7ee00-725">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-725">**DWORD**</span></span> | \- | <span data-ttu-id="7ee00-726">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-726">X</span></span> | <span data-ttu-id="7ee00-727">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-727">X</span></span> | \- | <span data-ttu-id="7ee00-728">Windows 10 version 1607</span><span class="sxs-lookup"><span data-stu-id="7ee00-728">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="7ee00-729">\_ \_ version http de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-729">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="7ee00-730">**\_informations sur la version http \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-730">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="7ee00-731">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-731">X</span></span> | <span data-ttu-id="7ee00-732">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-732">X</span></span> | <span data-ttu-id="7ee00-733">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-733">X</span></span> | <span data-ttu-id="7ee00-734">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-734">X</span></span> | \- |
| <span data-ttu-id="7ee00-735">\_Option WinHTTP \_ http2 \_ KeepAlive</span><span class="sxs-lookup"><span data-stu-id="7ee00-735">WINHTTP\_OPTION\_HTTP2\_KEEPALIVE</span></span><br/><span data-ttu-id="7ee00-736">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-736">**DWORD**</span></span> | <span data-ttu-id="7ee00-737">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-737">X</span></span> | \- | \- | <span data-ttu-id="7ee00-738">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-738">X</span></span> | <span data-ttu-id="7ee00-739">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="7ee00-739">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7ee00-740">\_Option WinHTTP \_ http2 \_ plus \_ \_ encodage de transfert</span><span class="sxs-lookup"><span data-stu-id="7ee00-740">WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING</span></span><br/><span data-ttu-id="7ee00-741">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-741">**BOOL**</span></span> | <span data-ttu-id="7ee00-742">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-742">X</span></span> | <span data-ttu-id="7ee00-743">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-743">X</span></span> | \- | <span data-ttu-id="7ee00-744">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-744">X</span></span> | <span data-ttu-id="7ee00-745">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="7ee00-745">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7ee00-746">\_option WinHTTP \_ Ignorer \_ la \_ révocation de certificat \_ hors connexion</span><span class="sxs-lookup"><span data-stu-id="7ee00-746">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="7ee00-747">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-747">**BOOL**</span></span> | \- | <span data-ttu-id="7ee00-748">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-748">X</span></span> | \- | <span data-ttu-id="7ee00-749">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-749">X</span></span> | <span data-ttu-id="7ee00-750">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="7ee00-750">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7ee00-751">\_Option WinHTTP \_ \_ Fast \_ Fallback IPv6</span><span class="sxs-lookup"><span data-stu-id="7ee00-751">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="7ee00-752">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-752">**BOOL**</span></span> | <span data-ttu-id="7ee00-753">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-753">X</span></span> | \- | \- | <span data-ttu-id="7ee00-754">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-754">X</span></span> | <span data-ttu-id="7ee00-755">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="7ee00-755">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7ee00-756">l' \_ option WinHTTP \_ est une \_ \_ réponse de connexion proxy \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-756">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="7ee00-757">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-757">**BOOL**</span></span> | <span data-ttu-id="7ee00-758">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-758">X</span></span> | <span data-ttu-id="7ee00-759">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-759">X</span></span> | <span data-ttu-id="7ee00-760">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-760">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-761">\_Option WinHTTP \_ nombre de Conn. \_ \_ par \_ \_ serveur 1 0 \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-761">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="7ee00-762">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-762">**DWORD**</span></span> | <span data-ttu-id="7ee00-763">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-763">X</span></span> | \- | <span data-ttu-id="7ee00-764">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-764">X</span></span> | <span data-ttu-id="7ee00-765">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-765">X</span></span> | \- |
| <span data-ttu-id="7ee00-766">\_option WinHTTP \_ nombre maximal de \_ conn. \_ par \_ serveur</span><span class="sxs-lookup"><span data-stu-id="7ee00-766">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="7ee00-767">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-767">**DWORD**</span></span> | <span data-ttu-id="7ee00-768">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-768">X</span></span> | \- | <span data-ttu-id="7ee00-769">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-769">X</span></span> | <span data-ttu-id="7ee00-770">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-770">X</span></span> | \- |
| <span data-ttu-id="7ee00-771">\_option WinHTTP \_ nombre maximal de \_ \_ \_ redirections http automatiques</span><span class="sxs-lookup"><span data-stu-id="7ee00-771">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="7ee00-772">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-772">**DWORD**</span></span> | <span data-ttu-id="7ee00-773">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-773">X</span></span> | <span data-ttu-id="7ee00-774">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-774">X</span></span> | <span data-ttu-id="7ee00-775">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-775">X</span></span> | <span data-ttu-id="7ee00-776">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-776">X</span></span> | \- |
| <span data-ttu-id="7ee00-777">\_ \_ État http max de l’option WinHTTP \_ \_ \_ continue</span><span class="sxs-lookup"><span data-stu-id="7ee00-777">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="7ee00-778">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-778">**DWORD**</span></span> | <span data-ttu-id="7ee00-779">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-779">X</span></span> | <span data-ttu-id="7ee00-780">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-780">X</span></span> | <span data-ttu-id="7ee00-781">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-781">X</span></span> | <span data-ttu-id="7ee00-782">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-782">X</span></span> | \- |
| <span data-ttu-id="7ee00-783">\_option WinHTTP \_ taille maximale de \_ \_ drainage \_ de la réponse</span><span class="sxs-lookup"><span data-stu-id="7ee00-783">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="7ee00-784">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-784">**DWORD**</span></span> | <span data-ttu-id="7ee00-785">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-785">X</span></span> | <span data-ttu-id="7ee00-786">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-786">X</span></span> | <span data-ttu-id="7ee00-787">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-787">X</span></span> | <span data-ttu-id="7ee00-788">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-788">X</span></span> | \- |
| <span data-ttu-id="7ee00-789">\_ \_ taille maximale d' \_ \_ en-tête de réponse \_ de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-789">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="7ee00-790">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-790">**DWORD**</span></span> | <span data-ttu-id="7ee00-791">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-791">X</span></span> | <span data-ttu-id="7ee00-792">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-792">X</span></span> | <span data-ttu-id="7ee00-793">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-793">X</span></span> | <span data-ttu-id="7ee00-794">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-794">X</span></span> | \- |
| <span data-ttu-id="7ee00-795">\_ \_ handle parent de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-795">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="7ee00-796">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="7ee00-796">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="7ee00-797">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-797">X</span></span> | <span data-ttu-id="7ee00-798">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-798">X</span></span> | <span data-ttu-id="7ee00-799">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-799">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-800">OPTION WINHTTP du texte de la \_ \_ \_ comarketingisation Passport \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-800">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="7ee00-801">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ee00-801">**LPWSTR**</span></span> | \- | <span data-ttu-id="7ee00-802">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-802">X</span></span> | <span data-ttu-id="7ee00-803">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-803">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-804">\_URL de \_ la \_ comarketing de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-804">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="7ee00-805">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ee00-805">**LPWSTR**</span></span> | \- | <span data-ttu-id="7ee00-806">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-806">X</span></span> | <span data-ttu-id="7ee00-807">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-807">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-808">\_URL de \_ \_ retour Passport \_ de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-808">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="7ee00-809">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="7ee00-809">**LPVOID**</span></span> | \- | <span data-ttu-id="7ee00-810">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-810">X</span></span> | <span data-ttu-id="7ee00-811">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-811">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-812">déconnexion de l’option WINHTTP de \_ \_ Passport \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-812">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="7ee00-813">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="7ee00-813">**LPVOID**</span></span> | <span data-ttu-id="7ee00-814">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-814">X</span></span> | \- | \- | <span data-ttu-id="7ee00-815">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-815">X</span></span> | \- |
| <span data-ttu-id="7ee00-816">\_ \_ mot de passe de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-816">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="7ee00-817">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ee00-817">**LPWSTR**</span></span> | \- | <span data-ttu-id="7ee00-818">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-818">X</span></span> | <span data-ttu-id="7ee00-819">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-819">X</span></span> | <span data-ttu-id="7ee00-820">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-820">X</span></span> | \- |
| <span data-ttu-id="7ee00-821">\_proxy d’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-821">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="7ee00-822">**\_informations sur le proxy WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-822">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="7ee00-823">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-823">X</span></span> | <span data-ttu-id="7ee00-824">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-824">X</span></span> | <span data-ttu-id="7ee00-825">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-825">X</span></span> | <span data-ttu-id="7ee00-826">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-826">X</span></span> | \- |
| <span data-ttu-id="7ee00-827">\_ \_ \_ mot de passe proxy de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-827">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="7ee00-828">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ee00-828">**LPWSTR**</span></span> | \- | <span data-ttu-id="7ee00-829">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-829">X</span></span> | <span data-ttu-id="7ee00-830">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-830">X</span></span> | <span data-ttu-id="7ee00-831">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-831">X</span></span> | \- |
| <span data-ttu-id="7ee00-832">nom de principal du proxy de l' \_ option WinHTTP \_ \_ \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="7ee00-832">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="7ee00-833">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ee00-833">**LPWSTR**</span></span> | \- | <span data-ttu-id="7ee00-834">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-834">X</span></span> | <span data-ttu-id="7ee00-835">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-835">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-836">\_ \_ \_ nom d’utilisateur proxy de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-836">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="7ee00-837">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ee00-837">**LPWSTR**</span></span> | \- | <span data-ttu-id="7ee00-838">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-838">X</span></span> | <span data-ttu-id="7ee00-839">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-839">X</span></span> | <span data-ttu-id="7ee00-840">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-840">X</span></span> | \- |
| <span data-ttu-id="7ee00-841">\_taille de \_ la \_ mémoire tampon de lecture de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-841">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="7ee00-842">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-842">**DWORD**</span></span> | \- | <span data-ttu-id="7ee00-843">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-843">X</span></span> | <span data-ttu-id="7ee00-844">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-844">X</span></span> | <span data-ttu-id="7ee00-845">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-845">X</span></span> | \- |
| <span data-ttu-id="7ee00-846">réponse de la connexion du proxy de réception de l' \_ option WinHTTP \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-846">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="7ee00-847">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-847">**BOOL**</span></span> | <span data-ttu-id="7ee00-848">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-848">X</span></span> | <span data-ttu-id="7ee00-849">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-849">X</span></span> | \- | <span data-ttu-id="7ee00-850">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-850">X</span></span> | \- |
| <span data-ttu-id="7ee00-851">\_délai de \_ réponse de réception \_ \_ de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-851">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="7ee00-852">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-852">**DWORD**</span></span> | <span data-ttu-id="7ee00-853">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-853">X</span></span> | <span data-ttu-id="7ee00-854">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-854">X</span></span> | <span data-ttu-id="7ee00-855">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-855">X</span></span> | <span data-ttu-id="7ee00-856">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-856">X</span></span> | \- |
| <span data-ttu-id="7ee00-857">\_délai de \_ réception des options WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-857">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="7ee00-858">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-858">**DWORD**</span></span> | <span data-ttu-id="7ee00-859">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-859">X</span></span> | <span data-ttu-id="7ee00-860">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-860">X</span></span> | <span data-ttu-id="7ee00-861">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-861">X</span></span> | <span data-ttu-id="7ee00-862">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-862">X</span></span> | \- |
| <span data-ttu-id="7ee00-863">\_stratégie de \_ redirection des options WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-863">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="7ee00-864">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-864">**DWORD**</span></span> | <span data-ttu-id="7ee00-865">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-865">X</span></span> | <span data-ttu-id="7ee00-866">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-866">X</span></span> | <span data-ttu-id="7ee00-867">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-867">X</span></span> | <span data-ttu-id="7ee00-868">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-868">X</span></span> | \- |
| <span data-ttu-id="7ee00-869">\_option WinHTTP \_ Reject \_ USERPWD \_ dans l' \_ URL</span><span class="sxs-lookup"><span data-stu-id="7ee00-869">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="7ee00-870">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-870">**BOOL**</span></span> | \- | <span data-ttu-id="7ee00-871">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-871">X</span></span> | \- | <span data-ttu-id="7ee00-872">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-872">X</span></span> | \- |
| <span data-ttu-id="7ee00-873">priorité des demandes de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-873">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="7ee00-874">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-874">**DWORD**</span></span> | \- | <span data-ttu-id="7ee00-875">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-875">X</span></span> | <span data-ttu-id="7ee00-876">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-876">X</span></span> | <span data-ttu-id="7ee00-877">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-877">X</span></span> | \- |
| <span data-ttu-id="7ee00-878">\_statistiques des \_ demandes d’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-878">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="7ee00-879">**\_statistiques des demandes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-879">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="7ee00-880">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-880">X</span></span> | <span data-ttu-id="7ee00-881">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-881">X</span></span> | \- | <span data-ttu-id="7ee00-882">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="7ee00-882">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7ee00-883">\_ \_ durées de demande de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-883">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="7ee00-884">**\_durées des requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-884">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="7ee00-885">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-885">X</span></span> | <span data-ttu-id="7ee00-886">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-886">X</span></span> | \- | <span data-ttu-id="7ee00-887">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="7ee00-887">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7ee00-888">l' \_ option WinHTTP \_ nécessite une \_ fin de flux \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-888">WINHTTP\_OPTION\_REQUIRE\_STREAM\_END</span></span><br/><span data-ttu-id="7ee00-889">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-889">**BOOL**</span></span> | <span data-ttu-id="7ee00-890">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-890">X</span></span> | <span data-ttu-id="7ee00-891">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-891">X</span></span> | \- | <span data-ttu-id="7ee00-892">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-892">X</span></span> | <span data-ttu-id="7ee00-893">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="7ee00-893">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7ee00-894">\_nom d' \_ hôte de résolution de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-894">WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME</span></span><br/><span data-ttu-id="7ee00-895">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ee00-895">**LPWSTR**</span></span> | \- | <span data-ttu-id="7ee00-896">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-896">X</span></span> | \- | <span data-ttu-id="7ee00-897">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-897">X</span></span> | <span data-ttu-id="7ee00-898">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="7ee00-898">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7ee00-899">délai de résolution de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-899">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="7ee00-900">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-900">**DWORD**</span></span> | <span data-ttu-id="7ee00-901">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-901">X</span></span> | <span data-ttu-id="7ee00-902">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-902">X</span></span> | <span data-ttu-id="7ee00-903">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-903">X</span></span> | <span data-ttu-id="7ee00-904">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-904">X</span></span> | \- |
| <span data-ttu-id="7ee00-905">\_ \_ protocoles sécurisés option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-905">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="7ee00-906">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-906">**DWORD**</span></span> | <span data-ttu-id="7ee00-907">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-907">X</span></span> | \- | \- | <span data-ttu-id="7ee00-908">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-908">X</span></span> | \- |
| <span data-ttu-id="7ee00-909">\_structure de \_ certificat de sécurité option \_ WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-909">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="7ee00-910">**\_informations de certificat WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7ee00-910">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="7ee00-911">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-911">X</span></span> | <span data-ttu-id="7ee00-912">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-912">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-913">indicateurs de sécurité de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-913">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="7ee00-914">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-914">**DWORD**</span></span> | \- | <span data-ttu-id="7ee00-915">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-915">X</span></span> | <span data-ttu-id="7ee00-916">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-916">X</span></span> | <span data-ttu-id="7ee00-917">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-917">X</span></span> | \- |
| <span data-ttu-id="7ee00-918">informations de sécurité de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-918">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="7ee00-919">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="7ee00-919">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="7ee00-920">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-920">X</span></span> | <span data-ttu-id="7ee00-921">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-921">X</span></span> | \- | <span data-ttu-id="7ee00-922">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="7ee00-922">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7ee00-923">nombre de bits de la clé de sécurité de l' \_ option WinHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-923">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="7ee00-924">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-924">**DWORD**</span></span> | \- | <span data-ttu-id="7ee00-925">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-925">X</span></span> | <span data-ttu-id="7ee00-926">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-926">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-927">\_ \_ \_ délai d’attente d’envoi des options WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-927">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="7ee00-928">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-928">**DWORD**</span></span> | <span data-ttu-id="7ee00-929">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-929">X</span></span> | <span data-ttu-id="7ee00-930">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-930">X</span></span> | <span data-ttu-id="7ee00-931">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-931">X</span></span> | <span data-ttu-id="7ee00-932">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-932">X</span></span> | \- |
| <span data-ttu-id="7ee00-933">\_serveur d’option WinHTTP \_ \_ CBT</span><span class="sxs-lookup"><span data-stu-id="7ee00-933">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="7ee00-934">[**\_Liaisons SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="7ee00-934">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="7ee00-935">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-935">X</span></span> | <span data-ttu-id="7ee00-936">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-936">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-937">\_contexte de \_ chaîne du certificat de serveur d’option WinHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-937">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="7ee00-938">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="7ee00-938">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="7ee00-939">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-939">X</span></span> | <span data-ttu-id="7ee00-940">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-940">X</span></span> | \- | <span data-ttu-id="7ee00-941">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="7ee00-941">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7ee00-942">\_contexte de \_ certificat de serveur d’option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-942">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="7ee00-943">**CONTEXTE DU CERTIFICAT**</span><span class="sxs-lookup"><span data-stu-id="7ee00-943">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="7ee00-944">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-944">X</span></span> | <span data-ttu-id="7ee00-945">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-945">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-946">nom principal de service du \_ serveur option WinHTTP \_ \_ \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="7ee00-946">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="7ee00-947">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ee00-947">**LPWSTR**</span></span> | \- | <span data-ttu-id="7ee00-948">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-948">X</span></span> | <span data-ttu-id="7ee00-949">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-949">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-950">SPN de l' \_ option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-950">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="7ee00-951">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-951">**DWORD**</span></span> | \- | <span data-ttu-id="7ee00-952">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-952">X</span></span> | \- | <span data-ttu-id="7ee00-953">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-953">X</span></span> | \- |
| <span data-ttu-id="7ee00-954">\_code d' \_ erreur de flux d’options WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-954">WINHTTP\_OPTION\_STREAM\_ERROR\_CODE</span></span><br/><span data-ttu-id="7ee00-955">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-955">**DWORD**</span></span> | \- | <span data-ttu-id="7ee00-956">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-956">X</span></span> | <span data-ttu-id="7ee00-957">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-957">X</span></span> | \- | <span data-ttu-id="7ee00-958">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="7ee00-958">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7ee00-959">\_option WinHTTP \_ TCP \_ Fast \_ Open</span><span class="sxs-lookup"><span data-stu-id="7ee00-959">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="7ee00-960">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-960">**BOOL**</span></span> | <span data-ttu-id="7ee00-961">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-961">X</span></span> | \- | \- | <span data-ttu-id="7ee00-962">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-962">X</span></span> | <span data-ttu-id="7ee00-963">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="7ee00-963">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7ee00-964">\_option WinHTTP \_ TCP \_ KeepAlive</span><span class="sxs-lookup"><span data-stu-id="7ee00-964">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="7ee00-965">**\_KeepAlive TCP**</span><span class="sxs-lookup"><span data-stu-id="7ee00-965">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="7ee00-966">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-966">X</span></span> | \- | \- | <span data-ttu-id="7ee00-967">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-967">X</span></span> | <span data-ttu-id="7ee00-968">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="7ee00-968">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7ee00-969">OPTION WINHTTP-début de la \_ \_ \_ valeur TLS false \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-969">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="7ee00-970">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-970">**BOOL**</span></span> | <span data-ttu-id="7ee00-971">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-971">X</span></span> | \- | \- | <span data-ttu-id="7ee00-972">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-972">X</span></span> | <span data-ttu-id="7ee00-973">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="7ee00-973">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7ee00-974">\_option WinHTTP \_ \_ protocole TLS \_ non sécurisé de \_ secours</span><span class="sxs-lookup"><span data-stu-id="7ee00-974">WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK</span></span><br/><span data-ttu-id="7ee00-975">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-975">**BOOL**</span></span> | <span data-ttu-id="7ee00-976">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-976">X</span></span> | \- | \- | <span data-ttu-id="7ee00-977">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-977">X</span></span> | <span data-ttu-id="7ee00-978">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="7ee00-978">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7ee00-979">\_événement de \_ notification de déchargement d’option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-979">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="7ee00-980">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="7ee00-980">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="7ee00-981">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-981">X</span></span> | \- | \- | <span data-ttu-id="7ee00-982">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-982">X</span></span> | \- |
| <span data-ttu-id="7ee00-983">\_option WinHTTP \_ \_ -analyse d’en-tête non sécurisé \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-983">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="7ee00-984">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-984">**DWORD**</span></span> | \- | <span data-ttu-id="7ee00-985">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-985">X</span></span> | \- | <span data-ttu-id="7ee00-986">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-986">X</span></span> | \- |
| <span data-ttu-id="7ee00-987">\_option WinHTTP \_ mettre à niveau \_ vers \_ Web \_ Socket</span><span class="sxs-lookup"><span data-stu-id="7ee00-987">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="7ee00-988">N/A</span><span class="sxs-lookup"><span data-stu-id="7ee00-988">N/A</span></span> | \- | <span data-ttu-id="7ee00-989">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-989">X</span></span> | \- | <span data-ttu-id="7ee00-990">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-990">X</span></span> | \- |
| <span data-ttu-id="7ee00-991">URL de l' \_ option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-991">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="7ee00-992">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ee00-992">**LPWSTR**</span></span> | \- | <span data-ttu-id="7ee00-993">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-993">X</span></span> | <span data-ttu-id="7ee00-994">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-994">X</span></span> | \- | \- |
| <span data-ttu-id="7ee00-995">\_option WinHTTP \_ utiliser \_ les \_ \_ informations d’identification du serveur global</span><span class="sxs-lookup"><span data-stu-id="7ee00-995">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="7ee00-996">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7ee00-996">**BOOL**</span></span> | <span data-ttu-id="7ee00-997">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-997">X</span></span> | <span data-ttu-id="7ee00-998">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-998">X</span></span> | \- | <span data-ttu-id="7ee00-999">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-999">X</span></span> | \- |
| <span data-ttu-id="7ee00-1000">\_ \_ agent utilisateur de \_ l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-1000">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="7ee00-1001">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ee00-1001">**LPWSTR**</span></span> | <span data-ttu-id="7ee00-1002">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1002">X</span></span> | \- | <span data-ttu-id="7ee00-1003">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1003">X</span></span> | <span data-ttu-id="7ee00-1004">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1004">X</span></span> | \- |
| <span data-ttu-id="7ee00-1005">\_option WinHTTP \_ nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7ee00-1005">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="7ee00-1006">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7ee00-1006">**LPWSTR**</span></span> | \- | <span data-ttu-id="7ee00-1007">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1007">X</span></span> | <span data-ttu-id="7ee00-1008">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1008">X</span></span> | <span data-ttu-id="7ee00-1009">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1009">X</span></span> | \- |
| <span data-ttu-id="7ee00-1010">\_ \_ \_ \_ \_ délai d’attente de fermeture du socket Web de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-1010">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="7ee00-1011">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-1011">**DWORD**</span></span> | \- | \- | <span data-ttu-id="7ee00-1012">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1012">X</span></span> | <span data-ttu-id="7ee00-1013">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1013">X</span></span> | \- |
| <span data-ttu-id="7ee00-1014">\_intervalle de \_ conservation \_ de \_ conservation de socket Web \_ d’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-1014">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="7ee00-1015">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-1015">**DWORD**</span></span> | \- | \- | <span data-ttu-id="7ee00-1016">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1016">X</span></span> | <span data-ttu-id="7ee00-1017">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1017">X</span></span> | \- |
| <span data-ttu-id="7ee00-1018">OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon de réception du socket Web \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-1018">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="7ee00-1019">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-1019">**DWORD**</span></span> | <span data-ttu-id="7ee00-1020">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1020">X</span></span> | <span data-ttu-id="7ee00-1021">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1021">X</span></span> | <span data-ttu-id="7ee00-1022">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1022">X</span></span> | <span data-ttu-id="7ee00-1023">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1023">X</span></span> | <span data-ttu-id="7ee00-1024">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7ee00-1024">Windows 8.1</span></span> |
| <span data-ttu-id="7ee00-1025">OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon d’envoi du socket Web \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-1025">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="7ee00-1026">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-1026">**DWORD**</span></span> | <span data-ttu-id="7ee00-1027">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1027">X</span></span> | <span data-ttu-id="7ee00-1028">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1028">X</span></span> | <span data-ttu-id="7ee00-1029">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1029">X</span></span> | <span data-ttu-id="7ee00-1030">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1030">X</span></span> | <span data-ttu-id="7ee00-1031">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7ee00-1031">Windows 8.1</span></span> |
| <span data-ttu-id="7ee00-1032">\_nombre de \_ \_ threads de travail option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-1032">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="7ee00-1033">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-1033">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="7ee00-1034">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1034">X</span></span> | \- |
| <span data-ttu-id="7ee00-1035">\_taille de \_ la \_ mémoire tampon d’écriture de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="7ee00-1035">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="7ee00-1036">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="7ee00-1036">**DWORD**</span></span> | \- | <span data-ttu-id="7ee00-1037">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1037">X</span></span> | <span data-ttu-id="7ee00-1038">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1038">X</span></span> | <span data-ttu-id="7ee00-1039">X</span><span class="sxs-lookup"><span data-stu-id="7ee00-1039">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="7ee00-1040">Pour Windows XP et Windows 2000, consultez [Configuration requise](winhttp-start-page.md)pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7ee00-1040">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ee00-1041">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7ee00-1041">Requirements</span></span>

| <span data-ttu-id="7ee00-1042">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ee00-1042">Requirement</span></span> | <span data-ttu-id="7ee00-1043">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ee00-1043">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="7ee00-1044">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ee00-1044">Minimum supported client</span></span> | <span data-ttu-id="7ee00-1045">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ee00-1045">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="7ee00-1046">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ee00-1046">Minimum supported server</span></span> | <span data-ttu-id="7ee00-1047">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ee00-1047">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="7ee00-1048">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7ee00-1048">Redistributable</span></span>          | <span data-ttu-id="7ee00-1049">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7ee00-1049">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="7ee00-1050">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ee00-1050">Header</span></span>                   | <span data-ttu-id="7ee00-1051">WinHTTP. h</span><span class="sxs-lookup"><span data-stu-id="7ee00-1051">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="7ee00-1052">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ee00-1052">See also</span></span>

[<span data-ttu-id="7ee00-1053">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ee00-1053">WinHTTP Versions</span></span>](winhttp-versions.md)
