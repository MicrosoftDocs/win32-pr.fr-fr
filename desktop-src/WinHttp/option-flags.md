---
Description: Les indicateurs d’option suivants sont pris en charge par WinHttpQueryOption et WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Indicateurs d’option (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 25049ee11c59c6b320b794c07bd65e5ec9b930c9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395414"
---
# <a name="option-flags"></a><span data-ttu-id="00a69-103">Indicateurs d’option</span><span class="sxs-lookup"><span data-stu-id="00a69-103">Option Flags</span></span>

<span data-ttu-id="00a69-104">Les indicateurs d’option suivants sont pris en charge par [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) et [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="00a69-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="00a69-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**OPTION WINHTTP assurée par les \_ \_ \_ \_ rappels non bloquants \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-106">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="00a69-106">The default is FALSE.</span></span> <span data-ttu-id="00a69-107">Si la valeur est TRUE, WinHTTP ne garantit pas la progression si les rappels d’État sont bloqués par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="00a69-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="00a69-108">L’application cliente doit être particulièrement prudente pour effectuer des opérations minimales dans le rappel sans blocage, ce qui revient le plus rapidement possible et, en particulier, ne doit pas attendre d’appels WinHTTP ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="00a69-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="00a69-109">S’il ne suit pas ces instructions, il est probable qu’il y ait un impact négatif sur les performances ou qu’une application potentielle se bloque.</span><span class="sxs-lookup"><span data-stu-id="00a69-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="00a69-110">Si elle est utilisée de la manière prescrite, cette option peut améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="00a69-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**stratégie d’accès automatique aux \_ options WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-112">Définit une valeur d’entier long non signé qui spécifie la [stratégie d’ouverture de session automatique](authentication-in-winhttp.md) avec l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="00a69-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="00a69-113">Terme</span><span class="sxs-lookup"><span data-stu-id="00a69-113">Term</span></span> | <span data-ttu-id="00a69-114">Description</span><span class="sxs-lookup"><span data-stu-id="00a69-114">Description</span></span> |
|-|-|
| <span data-ttu-id="00a69-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>niveau de sécurité de l' \_ AUTOLOGO WINHTTP WinHTTP \_ \_ \_ élevé</span><span class="sxs-lookup"><span data-stu-id="00a69-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="00a69-116">Les informations d’identification par défaut ne sont pas utilisées.</span><span class="sxs-lookup"><span data-stu-id="00a69-116">Default credentials are not used.</span></span> <span data-ttu-id="00a69-117">Notez que cet indicateur prend effet uniquement si vous spécifiez le serveur par le nom de l’ordinateur réel.</span><span class="sxs-lookup"><span data-stu-id="00a69-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="00a69-118">Elle ne prend pas effet si vous spécifiez le serveur par « localhost » ou par adresse IP.</span><span class="sxs-lookup"><span data-stu-id="00a69-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="00a69-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>niveau de sécurité de l’ouverture de certification WINHTTP \_ \_ \_ \_ bas</span><span class="sxs-lookup"><span data-stu-id="00a69-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="00a69-120">Une ouverture de session authentifiée à l’aide des informations d’identification par défaut est effectuée pour toutes les demandes.</span><span class="sxs-lookup"><span data-stu-id="00a69-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="00a69-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>niveau de sécurité de la \_ protection d’accès réseau WinHTTP \_ \_ \_ moyen</span><span class="sxs-lookup"><span data-stu-id="00a69-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="00a69-122">Une connexion authentifiée à l’aide des informations d’identification par défaut est exécutée uniquement pour les demandes sur l’intranet local.</span><span class="sxs-lookup"><span data-stu-id="00a69-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="00a69-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**\_connexions en \_ arrière-plan des options WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00a69-124">Lorsque vous définissez cette option sur un handle de session, vous devez transmettre le nombre de connexions que vous souhaitez ouvrir.</span><span class="sxs-lookup"><span data-stu-id="00a69-124">When you set this option on a session handle, you must pass the number of connections you wish to open.</span></span> <span data-ttu-id="00a69-125">Ensuite, lors de la première envoi d’une demande, au lieu d’ouvrir une seule connexion, WinHttp ouvre plusieurs connexions en parallèle.</span><span class="sxs-lookup"><span data-stu-id="00a69-125">Then, upon first sending a request, rather than opening only a single connection, WinHttp opens a number of connections in parallel.</span></span> <span data-ttu-id="00a69-126">Cela peut améliorer les performances des demandes suivantes adressées à la même destination, ce qui n’entraîne pas la surcharge liée à l’établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="00a69-126">This can improve the performance of subsequent requests to the same destination, which won't have the overhead of connection establishment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_rappel d’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-128">Récupère le pointeur vers la fonction de rappel définie avec [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="00a69-128">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_contexte de \_ \_ certificat client \_ de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-130">Définit le contexte du certificat client.</span><span class="sxs-lookup"><span data-stu-id="00a69-130">Sets the client certificate context.</span></span> <span data-ttu-id="00a69-131">Si une application reçoit un certificat d' [**\_ authentification de \_ client WinHTTP \_ \_ \_ nécessaire**](error-messages.md), elle doit appeler [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) pour fournir un certificat avant de retenter la demande.</span><span class="sxs-lookup"><span data-stu-id="00a69-131">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="00a69-132">Dans le cadre du traitement de cette option, WinHttp appelle [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) sur le contexte de certificat fourni par l’appelant afin que le contexte de certificat puisse être libéré indépendamment par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="00a69-132">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="00a69-133">L’application ne doit pas tenter de fermer le magasin de certificats avec l’indicateur de fermeture de l' \_ \_ indicateur de fin de magasin de certificats \_ de l' \_ appel à [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) sur le magasin de certificats à partir duquel le contexte de certificat a été récupéré.</span><span class="sxs-lookup"><span data-stu-id="00a69-133">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="00a69-134">Une violation d’accès peut se produire.</span><span class="sxs-lookup"><span data-stu-id="00a69-134">An access violation may occur.</span></span>

<span data-ttu-id="00a69-135">Lorsque le serveur demande un certificat client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retourne une erreur message d' [**authentification du \_ \_ client WinHTTP \_ \_ \_ requis**](error-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="00a69-135">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="00a69-136">Si le serveur demande le certificat mais n’en a pas besoin, l’application peut spécifier cette option pour indiquer qu’elle n’a pas de certificat.</span><span class="sxs-lookup"><span data-stu-id="00a69-136">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="00a69-137">Le serveur peut choisir un autre schéma d’authentification ou autoriser un accès anonyme au serveur.</span><span class="sxs-lookup"><span data-stu-id="00a69-137">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="00a69-138">L’application fournit la macro de **contexte de certificat du \_ client WinHTTP no \_ client \_ \_** dans le paramètre *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="00a69-138">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="00a69-139">Si le serveur a besoin d’un certificat client, il peut envoyer un code d’état HTTP 403 en réponse.</span><span class="sxs-lookup"><span data-stu-id="00a69-139">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="00a69-140">Pour plus d’informations, consultez l’option **WinHTTP \_ \_ liste d' \_ \_ émetteurs \_ de certificats client** .</span><span class="sxs-lookup"><span data-stu-id="00a69-140">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_option WinHTTP \_ \_ liste d’émetteurs de certificats client \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-142">Récupère une structure [**SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) lorsque l’erreur de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) est un **\_ certificat d' \_ authentification client WinHTTP \_ \_ \_ nécessaire**.</span><span class="sxs-lookup"><span data-stu-id="00a69-142">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="00a69-143">La liste d’émetteurs de la structure contient une liste d’autorités de certification (CA) acceptables du serveur.</span><span class="sxs-lookup"><span data-stu-id="00a69-143">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="00a69-144">L’application cliente peut filtrer la liste des autorités de certification pour récupérer le certificat client pour l’authentification SSL.</span><span class="sxs-lookup"><span data-stu-id="00a69-144">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="00a69-145">En revanche, si le serveur demande le certificat client, mais ne l’exige pas, l’application peut appeler [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avec l' **option \_ WinHTTP \_ \_ \_ contexte de certificat client CERT** .</span><span class="sxs-lookup"><span data-stu-id="00a69-145">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="00a69-146">Pour plus d’informations, consultez l’option de **\_ \_ \_ \_ contexte certificat du client de l’option WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="00a69-146">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**page de codes de l' \_ option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-148">Définit la [*page de codes*](glossary.md) utilisée pour traiter l’URL (c’est-à-dire, la chaîne de requête).</span><span class="sxs-lookup"><span data-stu-id="00a69-148">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="00a69-149">La valeur par défaut est UTF-8.</span><span class="sxs-lookup"><span data-stu-id="00a69-149">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_option WinHTTP \_ configurer \_ l' \_ authentification Passport**</span><span class="sxs-lookup"><span data-stu-id="00a69-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-151">Définit une valeur d’entier long non signé qui spécifie si [l’authentification Passport dans](passport-authentication-in-winhttp.md) l’authentification WinHTTP est activée.</span><span class="sxs-lookup"><span data-stu-id="00a69-151">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="00a69-152">Il peut s'agir de l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="00a69-152">The value can be one of the following:</span></span>

| <span data-ttu-id="00a69-153">Terme</span><span class="sxs-lookup"><span data-stu-id="00a69-153">Term</span></span> | <span data-ttu-id="00a69-154">Description</span><span class="sxs-lookup"><span data-stu-id="00a69-154">Description</span></span> |
|-|-|
| <span data-ttu-id="00a69-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP- \_ désactiver l' \_ \_ authentification Passport</span><span class="sxs-lookup"><span data-stu-id="00a69-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="00a69-156">L’authentification Microsoft Passport est désactivée.</span><span class="sxs-lookup"><span data-stu-id="00a69-156">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="00a69-157">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="00a69-157">This is the default.</span></span> |
| <span data-ttu-id="00a69-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP-désactiver le porte- \_ \_ \_ clés Passport</span><span class="sxs-lookup"><span data-stu-id="00a69-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="00a69-159">Le porte-clés Passport est désactivé.</span><span class="sxs-lookup"><span data-stu-id="00a69-159">The Passport keyring is disabled.</span></span> <span data-ttu-id="00a69-160">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="00a69-160">This is the default.</span></span> |
| <span data-ttu-id="00a69-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>activation de WINHTTP avec l' \_ \_ \_ authentification Passport</span><span class="sxs-lookup"><span data-stu-id="00a69-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="00a69-162">L’authentification Passport est activée.</span><span class="sxs-lookup"><span data-stu-id="00a69-162">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="00a69-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP activer le porte- \_ \_ \_ clés Passport</span><span class="sxs-lookup"><span data-stu-id="00a69-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="00a69-164">Le porte-clés Passport est activé.</span><span class="sxs-lookup"><span data-stu-id="00a69-164">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="00a69-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_ \_ nouvelles tentatives de connexion de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-166">Définit ou récupère une valeur d’entier long non signé qui contient le nombre de tentatives de connexion de timesWinHTTP à un hôte.</span><span class="sxs-lookup"><span data-stu-id="00a69-166">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="00a69-167">Les services HTTP Microsoft Windows (WinHTTP) ne tentent qu’une seule fois par adresse IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="00a69-167">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="00a69-168">Par exemple, si vous tentez de vous connecter à un hôte multirésident qui a 10 adresses IP et que les **\_ \_ \_ nouvelles tentatives de connexion de l’option WinHTTP** ont la valeur 7, WinHTTP tente uniquement de se connecter aux sept premières adresses IP.</span><span class="sxs-lookup"><span data-stu-id="00a69-168">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="00a69-169">Étant donné le même jeu de 10 adresses IP, si l' **\_ option de connexion des \_ \_ nouvelles tentatives WinHTTP** est définie sur 20, WinHTTP tente chacune des 10 une seule fois.</span><span class="sxs-lookup"><span data-stu-id="00a69-169">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="00a69-170">Si une tentative de connexion échoue encore après le nombre spécifié de tentatives, ou si le délai de connexion a expiré avant, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="00a69-170">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="00a69-171">La valeur par défaut pour les **\_ \_ \_ nouvelles tentatives de connexion de l’option WinHTTP** est de cinq tentatives.</span><span class="sxs-lookup"><span data-stu-id="00a69-171">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**délai de connexion de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-173">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="00a69-173">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="00a69-174">La définition de cette option sur Infinite (0xFFFFFFFF) désactive ce minuteur.</span><span class="sxs-lookup"><span data-stu-id="00a69-174">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="00a69-175">Si une demande de connexion TCP prend plus de temps que cette valeur de délai d’attente, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="00a69-175">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="00a69-176">Le délai d’attente par défaut est de 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="00a69-176">The default timeout is 60 seconds.</span></span> <span data-ttu-id="00a69-177">Lorsque vous tentez de vous connecter à plusieurs adresses IP pour un seul hôte (un hôte multirésident), le délai d’expiration est fixé pour chaque connexion individuelle.</span><span class="sxs-lookup"><span data-stu-id="00a69-177">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**informations de connexion de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-179">Récupère l’adresse IP source et de destination, ainsi que le port de la demande qui a généré la réponse quand [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retourne.</span><span class="sxs-lookup"><span data-stu-id="00a69-179">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="00a69-180">L’application appelle [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) avec l’option **WinHTTP \_ option \_ Connection \_ info** , et fournit la structure des [**\_ \_ informations de connexion WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) dans le paramètre *lpBuffer* .</span><span class="sxs-lookup"><span data-stu-id="00a69-180">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="00a69-181">Pour plus d’informations, **consultez \_ \_ informations de connexion WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="00a69-181">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="00a69-182">**Windows Server 2003 avec SP1 et Windows XP avec SP2 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="00a69-182">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_Statistiques de connexion des options WinHTTP \_ \_ \_ v0**</span><span class="sxs-lookup"><span data-stu-id="00a69-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-184">Extrait le struct d' [**\_ informations TCP \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) pour la connexion sous-jacente utilisée par la demande.</span><span class="sxs-lookup"><span data-stu-id="00a69-184">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="00a69-185">La structure retournée peut contenir des statistiques des requêtes précédentes envoyées sur la même connexion.</span><span class="sxs-lookup"><span data-stu-id="00a69-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="00a69-186">Cette option a été remplacée par les **statistiques de connexion de l' \_ option WinHTTP \_ \_ \_ v1**.</span><span class="sxs-lookup"><span data-stu-id="00a69-186">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Statistiques de connexion des options WinHTTP \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="00a69-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-188">Extrait le struct d' [**\_ informations TCP \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) pour la connexion sous-jacente utilisée par la demande.</span><span class="sxs-lookup"><span data-stu-id="00a69-188">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="00a69-189">La structure retournée peut contenir des statistiques des requêtes précédentes envoyées sur la même connexion.</span><span class="sxs-lookup"><span data-stu-id="00a69-189">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**valeur de contexte de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-191">Définit ou récupère un **\_ ptr DWORD** qui contient un pointeur vers la valeur de contexte associée à ce handle [HINTERNET](hinternet-handles-in-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="00a69-191">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="00a69-192">La valeur stockée dans la mémoire tampon est utilisée et la nouvelle valeur est assignée à l’indicateur d’option de la valeur de contexte de l' **\_ option \_ \_ WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="00a69-192">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**décompression des \_ options WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-194">Définit un DWORD d’indicateurs qui déterminent si WinHTTP décompresse automatiquement les corps de réponse avec les encodages de contenu compressés.</span><span class="sxs-lookup"><span data-stu-id="00a69-194">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="00a69-195">WinHTTP définira également un en-tête de Accept-Encoding approprié, en remplaçant tout fourni par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="00a69-195">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="00a69-196">Les valeurs prises en charge sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="00a69-196">Supported values are:</span></span>

| <span data-ttu-id="00a69-197">Terme</span><span class="sxs-lookup"><span data-stu-id="00a69-197">Term</span></span> | <span data-ttu-id="00a69-198">Description</span><span class="sxs-lookup"><span data-stu-id="00a69-198">Description</span></span> |
|-|-|
| <span data-ttu-id="00a69-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_indicateur de décompression WinHTTP, \_ \_ gzip</span><span class="sxs-lookup"><span data-stu-id="00a69-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="00a69-200">Décompresser Content-Encoding : réponses gzip.</span><span class="sxs-lookup"><span data-stu-id="00a69-200">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="00a69-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_indicateur de décompression WinHTTP \_ \_ deflate</span><span class="sxs-lookup"><span data-stu-id="00a69-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="00a69-202">Décompresser le contenu-encodage : réponses décompressées.</span><span class="sxs-lookup"><span data-stu-id="00a69-202">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="00a69-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_indicateur de décompression WinHTTP \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="00a69-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="00a69-204">Décompressez les réponses avec tout encodage de contenu pris en charge.</span><span class="sxs-lookup"><span data-stu-id="00a69-204">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="00a69-205">Par défaut, WinHTTP remet les réponses compressées à l’appelant sans les modifier.</span><span class="sxs-lookup"><span data-stu-id="00a69-205">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**OPTION WINHTTP- \_ désactiver la génération de \_ \_ chaîne de certificats \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="00a69-207">La définition de cette option sur un handle de session WinHttp vous permet d’activer ou de désactiver la génération de la chaîne de certificats du serveur.</span><span class="sxs-lookup"><span data-stu-id="00a69-207">Setting this option on a WinHttp session handle allows you to enable/disable whether the server certificate chain is built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**\_fonctionnalité de \_ désactivation de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-209">Définit une valeur d’entier long non signé qui spécifie les fonctionnalités qui sont désactivées avec un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="00a69-209">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="00a69-210">N’oubliez pas que cette fonctionnalité doit être transmise uniquement à [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) sur les handles de requête après la création du handle de demande avec [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), et avant l’envoi de la demande avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="00a69-210">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="00a69-211">Terme</span><span class="sxs-lookup"><span data-stu-id="00a69-211">Term</span></span> | <span data-ttu-id="00a69-212">Description</span><span class="sxs-lookup"><span data-stu-id="00a69-212">Description</span></span> |
|-|-|
| <span data-ttu-id="00a69-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>\_désactiver \_ l’authentification WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="00a69-214">L’authentification automatique est désactivée.</span><span class="sxs-lookup"><span data-stu-id="00a69-214">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="00a69-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>désactivation des \_ \_ cookies WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="00a69-216">L’ajout automatique d’en-têtes de cookie aux demandes est désactivé.</span><span class="sxs-lookup"><span data-stu-id="00a69-216">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="00a69-217">En outre, les cookies retournés ne sont pas automatiquement ajoutés à la base de données de cookies.</span><span class="sxs-lookup"><span data-stu-id="00a69-217">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="00a69-218">La désactivation des cookies peut entraîner des performances médiocres pour l’authentification Passport.</span><span class="sxs-lookup"><span data-stu-id="00a69-218">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="00a69-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>\_désactiver \_ Keep \_ Alive dans WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="00a69-220">Désactive la sémantique Keep-Alive pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="00a69-220">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="00a69-221">La sémantique Keep-Alive est requise pour MSN, NTLM et d’autres types d’authentification.</span><span class="sxs-lookup"><span data-stu-id="00a69-221">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="00a69-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>désactivation des \_ \_ redirections WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="00a69-223">La redirection automatique est désactivée lors de l’envoi de demandes avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="00a69-223">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="00a69-224">Si la redirection automatique est désactivée, une application doit inscrire une fonction de rappel pour que l’authentification Passport aboutisse.</span><span class="sxs-lookup"><span data-stu-id="00a69-224">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="00a69-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_option WinHTTP \_ désactiver \_ le \_ protocole sécurisé de \_ secours**</span><span class="sxs-lookup"><span data-stu-id="00a69-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-226">Empêche WinHTTP de retenter une connexion avec une version antérieure du protocole de sécurité en cas d’échec de la négociation de protocole initiale.</span><span class="sxs-lookup"><span data-stu-id="00a69-226">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPTION WINHTTP- \_ \_ désactiver la \_ \_ file d’attente de flux**</span><span class="sxs-lookup"><span data-stu-id="00a69-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-228">Autorise les nouvelles demandes à ouvrir une connexion HTTP/2 supplémentaire lorsque la limite de flux simultané maximale est atteinte, plutôt que d’attendre le flux disponible suivant sur une connexion existante.</span><span class="sxs-lookup"><span data-stu-id="00a69-228">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**\_option WinHTTP \_ activer la \_ fonctionnalité**</span><span class="sxs-lookup"><span data-stu-id="00a69-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-230">Définit une valeur d’entier long non signé qui spécifie les fonctionnalités actuellement activées.</span><span class="sxs-lookup"><span data-stu-id="00a69-230">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="00a69-231">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="00a69-231">Can be one of the following values.</span></span>

| <span data-ttu-id="00a69-232">Terme</span><span class="sxs-lookup"><span data-stu-id="00a69-232">Term</span></span> | <span data-ttu-id="00a69-233">Description</span><span class="sxs-lookup"><span data-stu-id="00a69-233">Description</span></span> |
|-|-|
| <span data-ttu-id="00a69-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ activer \_ l' \_ emprunt d' \_ identité par le biais de SSL</span><span class="sxs-lookup"><span data-stu-id="00a69-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="00a69-235">S’il est activé, WinHTTP rétablit temporairement l’emprunt d’identité du client pendant la durée des opérations d’authentification du certificat SSL.</span><span class="sxs-lookup"><span data-stu-id="00a69-235">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="00a69-236">Cette valeur ne peut être définie que sur le descripteur de session.</span><span class="sxs-lookup"><span data-stu-id="00a69-236">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="00a69-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ activer \_ la \_ révocation SSL</span><span class="sxs-lookup"><span data-stu-id="00a69-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="00a69-238">Si cette option est activée, WinHTTP autorise la révocation SSL.</span><span class="sxs-lookup"><span data-stu-id="00a69-238">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="00a69-239">Cette valeur peut être définie uniquement sur le handle de demande.</span><span class="sxs-lookup"><span data-stu-id="00a69-239">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_option WinHTTP \_ activer \_ le \_ protocole http**</span><span class="sxs-lookup"><span data-stu-id="00a69-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-241">Définit un masque de réinitialisation DWORD des versions HTTP avancées acceptables.</span><span class="sxs-lookup"><span data-stu-id="00a69-241">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="00a69-242">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="00a69-242">Possible values are:</span></span>

| <span data-ttu-id="00a69-243">Terme</span><span class="sxs-lookup"><span data-stu-id="00a69-243">Term</span></span> | <span data-ttu-id="00a69-244">Description</span><span class="sxs-lookup"><span data-stu-id="00a69-244">Description</span></span> |
|-|-|
| <span data-ttu-id="00a69-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_ \_ Indicateur de protocole WinHTTP \_ http2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="00a69-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="00a69-246">Active HTTP/2 pour la requête.</span><span class="sxs-lookup"><span data-stu-id="00a69-246">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="00a69-247">Aucun (0x0)</span><span class="sxs-lookup"><span data-stu-id="00a69-247">None (0x0)</span></span> | <span data-ttu-id="00a69-248">Limite la demande à HTTP/1.1 et antérieur.</span><span class="sxs-lookup"><span data-stu-id="00a69-248">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="00a69-249">Les versions héritées de HTTP (1,1 et versions antérieures) ne peuvent pas être désactivées à l’aide de cette option.</span><span class="sxs-lookup"><span data-stu-id="00a69-249">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="00a69-250">La valeur par défaut est 0x0.</span><span class="sxs-lookup"><span data-stu-id="00a69-250">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**\_Option WinHTTP \_ activer \_ le \_ certificat du client http2 plus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="00a69-252">Cette option peut être définie sur un handle de session WinHttp pour permettre à WinHttp d’utiliser le contexte de certificat client fourni par l’appelant lorsque le protocole HTTP/2 est utilisé.</span><span class="sxs-lookup"><span data-stu-id="00a69-252">This option can be set on a WinHttp session handle to allow WinHttp to use the caller-provided client certificate context when HTTP/2 is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_option WinHTTP \_ EnableTracing,**</span><span class="sxs-lookup"><span data-stu-id="00a69-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-254">Définit une valeur **bool** qui spécifie si le traçage est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="00a69-254">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="00a69-255">Pour plus d’informations sur la fonctionnalité de trace dans WinHTTP, consultez [WinHTTP trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="00a69-255">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="00a69-256">Cette option ne peut être définie que sur un handle **HINTERNET** **null** .</span><span class="sxs-lookup"><span data-stu-id="00a69-256">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="00a69-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**\_option WinHTTP \_ coder \_ extra**</span><span class="sxs-lookup"><span data-stu-id="00a69-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-258">Active l’encodage de pourcentage d’URL pour le chemin d’accès et la chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="00a69-258">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="00a69-259">Vous pouvez également encoder en pourcentage avant d’appeler WinHttp.</span><span class="sxs-lookup"><span data-stu-id="00a69-259">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="00a69-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**expiration de la connexion de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-261">Cette option ne peut être définie que sur un handle de demande qui est toujours actif (envoi ou réception).</span><span class="sxs-lookup"><span data-stu-id="00a69-261">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="00a69-262">La définition de cette option indique à WinHttp d’arrêter de servir les demandes sur la connexion associée au handle de demande passé.</span><span class="sxs-lookup"><span data-stu-id="00a69-262">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="00a69-263">La connexion sera fermée après le handle de requête. cette option est appelée avec est terminée.</span><span class="sxs-lookup"><span data-stu-id="00a69-263">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="00a69-264">Cette option ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="00a69-264">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ erreur étendue de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-266">Récupère une valeur d’entier long non signé qui contient un code d’erreur Microsoft Windows Sockets qui a été mappé à l’erreur \_ WinHTTP \_ \* messages d’erreur retournés dans ce contexte de thread.</span><span class="sxs-lookup"><span data-stu-id="00a69-266">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="00a69-267">Vous pouvez passer **null** comme valeur de handle.</span><span class="sxs-lookup"><span data-stu-id="00a69-267">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**\_option WinHTTP \_ première \_ \_ connexion disponible**</span><span class="sxs-lookup"><span data-stu-id="00a69-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="00a69-269">Par défaut, lorsque WinHttp envoie une demande, si aucune connexion n’est disponible pour répondre à la demande, WinHttp tente d’établir une nouvelle connexion et la demande est liée à cette nouvelle connexion.</span><span class="sxs-lookup"><span data-stu-id="00a69-269">By default, when WinHttp sends a request, if there are no available connections to serve the request, WinHttp will attempt to establish a new connection, and the request will be bound to this new connection.</span></span> <span data-ttu-id="00a69-270">Lorsque vous définissez cette option, une telle demande est traitée à la première connexion qui devient disponible, et pas nécessairement celle qui est établie.</span><span class="sxs-lookup"><span data-stu-id="00a69-270">When you set this option, such a request will instead be served on the first connection that becomes available, and not necessarily the one being established.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**identification \_ du \_ proxy global des options \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-272">Prend un pointeur vers une structure d' [**\_ CREDS \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) d’identification WinHTTP avec le paramètre de fonction *hInternet* ayant la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="00a69-272">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="00a69-273">Cette option requiert la clé de Registre **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings ! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="00a69-273">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="00a69-274">Si cette clé de Registre n’est pas définie, WinHTTP retourne l' **\_ option erreur WinHTTP \_ non valide \_**.</span><span class="sxs-lookup"><span data-stu-id="00a69-274">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="00a69-275">Cette clé de Registre n’est pas présente par défaut.</span><span class="sxs-lookup"><span data-stu-id="00a69-275">This registry key is not present by default.</span></span> <span data-ttu-id="00a69-276">Lorsqu’il est défini, WinINet envoie les informations d’identification vers WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="00a69-276">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="00a69-277">Chaque fois que WinHttp reçoit une demande d’authentification et si aucune information d’identification n’est définie sur le handle actuel, il utilise les informations d’identification fournies par WinINet.</span><span class="sxs-lookup"><span data-stu-id="00a69-277">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="00a69-278">Pour partager des informations d’identification de serveur en plus des informations d’identification de proxy, les utilisateurs doivent définir l' **\_ option WinHTTP utiliser les \_ \_ \_ \_ informations d’identification du serveur global** .</span><span class="sxs-lookup"><span data-stu-id="00a69-278">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_options WinHTTP \_ - \_ CREDS de serveur global \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-280">Prend un pointeur vers une structure d' [**\_ CREDS \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) d’identification WinHTTP avec le paramètre de fonction *hInternet* ayant la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="00a69-280">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="00a69-281">Cette option requiert la clé de Registre **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings ! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="00a69-281">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="00a69-282">Si cette clé de Registre n’est pas définie, WinHTTP retourne l' **\_ option erreur WinHTTP \_ non valide \_**.</span><span class="sxs-lookup"><span data-stu-id="00a69-282">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="00a69-283">Cette clé de Registre n’est pas présente par défaut.</span><span class="sxs-lookup"><span data-stu-id="00a69-283">This registry key is not present by default.</span></span> <span data-ttu-id="00a69-284">Lorsqu’il est défini, WinINet envoie les informations d’identification vers WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="00a69-284">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="00a69-285">Chaque fois que WinHttp reçoit une demande d’authentification et si aucune information d’identification n’est définie sur le handle actuel, il utilise les informations d’identification fournies par WinINet.</span><span class="sxs-lookup"><span data-stu-id="00a69-285">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="00a69-286">Pour partager des informations d’identification de serveur en plus des informations d’identification de proxy, les utilisateurs doivent définir l' **\_ option WinHTTP utiliser les \_ \_ \_ \_ informations d’identification du serveur global** .</span><span class="sxs-lookup"><span data-stu-id="00a69-286">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TYPE de handle de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-288">Récupère une valeur d’entier long non signé qui contient le type du handle [HINTERNET](hinternet-handles-in-winhttp.md) passé.</span><span class="sxs-lookup"><span data-stu-id="00a69-288">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="00a69-289">La valeur de retour peut être une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="00a69-289">The return value can be one of the following:</span></span>

| <span data-ttu-id="00a69-290">Terme</span><span class="sxs-lookup"><span data-stu-id="00a69-290">Term</span></span> | <span data-ttu-id="00a69-291">Description</span><span class="sxs-lookup"><span data-stu-id="00a69-291">Description</span></span> |
|-|-|
| <span data-ttu-id="00a69-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>\_connexion au \_ type de handle WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="00a69-293">Le descripteur est un handle de connexion.</span><span class="sxs-lookup"><span data-stu-id="00a69-293">The handle is a connection handle.</span></span> |
| <span data-ttu-id="00a69-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_demande de \_ type de handle WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="00a69-295">Le descripteur est un handle de demande.</span><span class="sxs-lookup"><span data-stu-id="00a69-295">The handle is a request handle.</span></span> |
| <span data-ttu-id="00a69-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_session de \_ type de handle WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="00a69-297">Le descripteur est un handle de session.</span><span class="sxs-lookup"><span data-stu-id="00a69-297">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="00a69-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_option WinHTTP \_ \_ protocole http \_ requis**</span><span class="sxs-lookup"><span data-stu-id="00a69-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-299">Empêche l’utilisation de versions de protocole autres que celles activées par l' **\_ option WinHTTP activer le \_ \_ \_ protocole http** pour la demande.</span><span class="sxs-lookup"><span data-stu-id="00a69-299">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**\_option WinHTTP \_ \_ protocole http \_ utilisé**</span><span class="sxs-lookup"><span data-stu-id="00a69-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-301">Obtient une valeur DWORD qui indique quelle version HTTP avancée a été utilisée sur une demande donnée.</span><span class="sxs-lookup"><span data-stu-id="00a69-301">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="00a69-302">Pour obtenir la liste des valeurs possibles, **consultez \_ option WinHTTP \_ activer le \_ \_ protocole http**.</span><span class="sxs-lookup"><span data-stu-id="00a69-302">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_ \_ version http de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-304">Définit ou récupère une structure [**d' \_ \_ informations de version http**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) qui contient la version http prise en charge.</span><span class="sxs-lookup"><span data-stu-id="00a69-304">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="00a69-305">Il s’agit d’une option à l’ensemble du processus ; Utilisez la **valeur null** pour le descripteur.</span><span class="sxs-lookup"><span data-stu-id="00a69-305">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**\_Option WinHTTP \_ http2 \_ KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="00a69-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP\_OPTION\_HTTP2\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="00a69-307">Cette option peut être définie sur un handle de session pour que WinHttp utilise des trames PING HTTP/2 comme mécanisme KeepAlive.</span><span class="sxs-lookup"><span data-stu-id="00a69-307">This option can be set on a session handle to have WinHttp use HTTP/2 PING frames as a keepalive mechanism.</span></span> <span data-ttu-id="00a69-308">Les appelants spécifient un délai d’expiration en millisecondes et, après l’absence d’activité sur une connexion pour ce délai, WinHttp commence à envoyer des trames PING HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="00a69-308">Callers specify a timeout in milliseconds, and after there is no activity on a connection for that timeout period, WinHttp will begin to send HTTP/2 PING frames.</span></span> <span data-ttu-id="00a69-309">Les appelants ne peuvent pas définir une valeur de délai d’expiration inférieure à 5000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="00a69-309">Callers cannot set a timeout value less than 5000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**\_Option WinHTTP \_ http2 \_ plus \_ \_ encodage de transfert**</span><span class="sxs-lookup"><span data-stu-id="00a69-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="00a69-311">Cette option peut être définie sur un handle de demande WinHttp pour contrôler la façon dont WinHttp se comporte lorsqu’une réponse HTTP/2 contient un en-tête « Transfer-Encoding ».</span><span class="sxs-lookup"><span data-stu-id="00a69-311">This option can be set on a WinHttp request handle to control how WinHttp behaves when an HTTP/2 response contains a "Transfer-Encoding" header.</span></span> <span data-ttu-id="00a69-312">Dans ce cas, WinHttp retourne une erreur si cette option a la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="00a69-312">In such a case, WinHttp will return an error if this option is set to **FALSE**.</span></span>


</dt> </dl> </dd> <dt>


<span data-ttu-id="00a69-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_option WinHTTP \_ Ignorer \_ la \_ révocation de certificat \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="00a69-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-314">Autorise les connexions sécurisées à utiliser des certificats de sécurité pour lesquels la liste de révocation de certificats n’a pas pu être téléchargée.</span><span class="sxs-lookup"><span data-stu-id="00a69-314">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_Option WinHTTP \_ \_ Fast \_ Fallback IPv6**</span><span class="sxs-lookup"><span data-stu-id="00a69-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-316">Active la connexion Fast de secours IPv6 (les yeux plus heureux) pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="00a69-316">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="00a69-317">Ce comportement est similaire au comportement de l’œil heureux décrit dans le [document RFC 6555](https://tools.ietf.org/html/rfc6555) pour améliorer les temps de connexion sur les réseaux où IPv6 n’est pas fiable.</span><span class="sxs-lookup"><span data-stu-id="00a69-317">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="00a69-318">Si les adresses IPv6 et IPv4 sont résolues pour un hôte donné, WinHttp commence par se connecter à la première adresse IPv6 résolue avec un délai d’expiration court (300 mètres).</span><span class="sxs-lookup"><span data-stu-id="00a69-318">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="00a69-319">En cas d’échec de cette connexion, WinHttp tente de se connecter à la première adresse IPv4 résolue avec le délai d’attente standard.</span><span class="sxs-lookup"><span data-stu-id="00a69-319">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="00a69-320">En cas d’échec de la deuxième connexion, WinHttp réessaiera la première adresse IPv6 résolue avec le délai d’expiration standard.</span><span class="sxs-lookup"><span data-stu-id="00a69-320">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="00a69-321">En cas d’échec de la troisième connexion, WinHttp rétablit le comportement par défaut pour toutes les adresses restantes, en tentant une connexion avec le délai d’expiration standard jusqu’à ce qu’une connexion soit établie ou qu’aucune adresse ne soit conservée.</span><span class="sxs-lookup"><span data-stu-id="00a69-321">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**l' \_ option WinHTTP \_ est une \_ \_ réponse de connexion proxy \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-323">Obtient une valeur indiquant si une réponse de connexion de retour de proxy peut être récupérée.</span><span class="sxs-lookup"><span data-stu-id="00a69-323">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_Option WinHTTP \_ nombre de Conn. \_ \_ par \_ \_ serveur 1 0 \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-325">Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par serveur HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="00a69-325">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="00a69-326">La valeur par défaut est **infinite**.</span><span class="sxs-lookup"><span data-stu-id="00a69-326">The default value is **INFINITE**.</span></span>

<span data-ttu-id="00a69-327">**Windows Vista avec SP1 et Windows Server 2008 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="00a69-327">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_option WinHTTP \_ nombre maximal de \_ conn. \_ par \_ serveur**</span><span class="sxs-lookup"><span data-stu-id="00a69-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-329">Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par serveur.</span><span class="sxs-lookup"><span data-stu-id="00a69-329">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="00a69-330">La valeur par défaut est **infinite**.</span><span class="sxs-lookup"><span data-stu-id="00a69-330">The default value is **INFINITE**.</span></span>

<span data-ttu-id="00a69-331">Lorsque cette option a la valeur zéro, WinHTTP définit la limite du nombre de connexions à 2.</span><span class="sxs-lookup"><span data-stu-id="00a69-331">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**\_option WinHTTP \_ nombre maximal de \_ \_ \_ redirections http automatiques**</span><span class="sxs-lookup"><span data-stu-id="00a69-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-333">Définit le nombre maximal de redirections que WinHTTP suit ; la valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="00a69-333">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="00a69-334">Cette limite empêche les sites non autorisés de suspendre le client WinHTTP après un grand nombre de redirections.</span><span class="sxs-lookup"><span data-stu-id="00a69-334">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="00a69-335">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="00a69-335">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_ \_ État http max de l’option WinHTTP \_ \_ \_ continue**</span><span class="sxs-lookup"><span data-stu-id="00a69-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-337">Le nombre maximal de réponses du code d’État 100-199 est ignoré avant de renvoyer le code d’état final au client WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="00a69-337">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="00a69-338">Les codes d’État informations 100-199 peuvent être envoyés par le serveur avant le code d’état final et sont décrits dans la spécification pour HTTP/1.1 (pour plus d’informations, consultez [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="00a69-338">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="00a69-339">La valeur par défaut est de 10.</span><span class="sxs-lookup"><span data-stu-id="00a69-339">The default is 10.</span></span>

<span data-ttu-id="00a69-340">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="00a69-340">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**\_option WinHTTP \_ taille maximale de \_ \_ drainage \_ de la réponse**</span><span class="sxs-lookup"><span data-stu-id="00a69-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-342">Lié sur la quantité de données vidées des réponses afin de réutiliser une connexion, spécifiée en octets.</span><span class="sxs-lookup"><span data-stu-id="00a69-342">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="00a69-343">La valeur par défaut est 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="00a69-343">The default is 1MB.</span></span>

<span data-ttu-id="00a69-344">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="00a69-344">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_ \_ taille maximale d' \_ \_ en-tête de réponse \_ de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-346">Une limite définie sur la taille maximale de la partie en-tête de la réponse du serveur, spécifiée en octets.</span><span class="sxs-lookup"><span data-stu-id="00a69-346">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="00a69-347">Cette liaison protège le client contre les tentatives de blocage du client par un serveur non autorisé en envoyant une réponse avec une quantité infinie de données d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="00a69-347">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="00a69-348">La valeur par défaut est 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="00a69-348">The default value is 64KB.</span></span>

<span data-ttu-id="00a69-349">**Windows XP avec SP1 et windows 2000 avec SP3 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="00a69-349">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ handle parent de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-351">Récupère le handle parent de ce handle.</span><span class="sxs-lookup"><span data-stu-id="00a69-351">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**OPTION WINHTTP du texte de la \_ \_ \_ comarketingisation Passport \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-353">Récupère une chaîne qui contient le texte de [*copersonnalisation*](glossary.md) fourni par le serveur d’ouverture de session Passport.</span><span class="sxs-lookup"><span data-stu-id="00a69-353">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="00a69-354">Cette option doit être récupérée immédiatement après que le serveur d’ouverture de session a répondu avec un code d’état 401.</span><span class="sxs-lookup"><span data-stu-id="00a69-354">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="00a69-355">Une application doit passer une taille de mémoire tampon, en octets, qui est suffisamment grande pour contenir la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="00a69-355">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_URL de \_ la \_ comarketing de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-357">Récupère une chaîne qui contient une URL pour un graphique de [*copersonnalisation*](glossary.md) fourni par le serveur d’ouverture de session Passport.</span><span class="sxs-lookup"><span data-stu-id="00a69-357">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="00a69-358">Cette option doit être récupérée immédiatement après que le serveur d’ouverture de session a répondu avec un code d’état 401.</span><span class="sxs-lookup"><span data-stu-id="00a69-358">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="00a69-359">Une application doit passer une taille de mémoire tampon, en octets, qui est suffisamment grande pour contenir la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="00a69-359">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_URL de \_ \_ retour Passport \_ de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-361">Définit une option en lecture seule sur un handle de demande qui récupère l’URL de retour Passport.</span><span class="sxs-lookup"><span data-stu-id="00a69-361">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**déconnexion de l’option WINHTTP de \_ \_ Passport \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-363">Définit l’option sur un handle de session pour se déconnecter de toutes les connexions Passport.</span><span class="sxs-lookup"><span data-stu-id="00a69-363">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="00a69-364">Une application doit transmettre l’URL de retour Passport qui a été récupérée avec l' **\_ option WinHTTP \_ \_ \_ URL de renvoi Passport**.</span><span class="sxs-lookup"><span data-stu-id="00a69-364">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="00a69-365">Tous les cookies associés à l’URL de renvoi sont effacés.</span><span class="sxs-lookup"><span data-stu-id="00a69-365">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_ \_ mot de passe de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-367">Définit ou récupère une valeur de chaîne qui contient le mot de passe associé à un handle de demande.</span><span class="sxs-lookup"><span data-stu-id="00a69-367">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_proxy d’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-369">Définit ou récupère une structure [**d' \_ \_ informations de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) qui contient les données de proxy sur un handle de session ou un handle de demande existant.</span><span class="sxs-lookup"><span data-stu-id="00a69-369">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="00a69-370">Lors de la récupération de données de proxy, une application doit libérer les chaînes **lpszProxy** et **lpszProxyBypass** contenues dans cette structure (si elles n’ont pas la **valeur null**) à l’aide de la fonction [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="00a69-370">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="00a69-371">Une application peut interroger les données de proxy globales (le proxy par défaut) en passant un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="00a69-371">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_ \_ \_ mot de passe proxy de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-373">Définit ou récupère une valeur de chaîne qui contient le mot de passe utilisé pour accéder au proxy.</span><span class="sxs-lookup"><span data-stu-id="00a69-373">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**nom de principal du proxy de l' \_ option WinHTTP \_ \_ \_ utilisé**</span><span class="sxs-lookup"><span data-stu-id="00a69-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-375">Obtient le nom principal du serveur proxy que WinHTTP a fourni à SSPI pendant l’authentification.</span><span class="sxs-lookup"><span data-stu-id="00a69-375">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="00a69-376">Cette valeur de chaîne est usefor transmettant à [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) après un échec d’authentification.</span><span class="sxs-lookup"><span data-stu-id="00a69-376">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_ \_ \_ nom d’utilisateur proxy de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-378">Définit ou récupère une valeur de chaîne qui contient le nom d’utilisateur utilisé pour accéder au proxy.</span><span class="sxs-lookup"><span data-stu-id="00a69-378">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_taille de \_ la \_ mémoire tampon de lecture de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-380">Cette option est dépréciée ; elle n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="00a69-380">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**réponse de la connexion du proxy de réception de l' \_ option WinHTTP \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-382">Définit si l’entité de réponse du proxy peut être récupérée.</span><span class="sxs-lookup"><span data-stu-id="00a69-382">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="00a69-383">Cette option est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="00a69-383">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**\_délai de \_ réponse de réception \_ \_ de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-385">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, à attendre pour recevoir tous les en-têtes de réponse d’une demande.</span><span class="sxs-lookup"><span data-stu-id="00a69-385">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="00a69-386">Si WinHTTP ne parvient pas à recevoir tous les en-têtes dans ce délai, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="00a69-386">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="00a69-387">La valeur du délai d’attente par défaut est de 90 secondes.</span><span class="sxs-lookup"><span data-stu-id="00a69-387">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="00a69-388">Ce délai d’expiration est vérifié uniquement lorsque des données sont reçues du Socket.</span><span class="sxs-lookup"><span data-stu-id="00a69-388">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="00a69-389">Par conséquent, lorsque le délai d’attente expire, l’application cliente n’est pas notifiée tant que davantage de données n’arrivent pas sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="00a69-389">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="00a69-390">Si aucune donnée n’arrive à partir du serveur, le délai entre l’expiration du délai d’attente et la notification de l’application cliente peut être aussi important que celui défini à l’aide du paramètre *dwReceiveTimeout* de la fonction [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .</span><span class="sxs-lookup"><span data-stu-id="00a69-390">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_délai de \_ réception des options WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-392">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour recevoir une réponse partielle à une demande ou lire des données.</span><span class="sxs-lookup"><span data-stu-id="00a69-392">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="00a69-393">Si la réponse prend plus de temps que cette valeur de délai d’attente, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="00a69-393">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="00a69-394">La valeur de délai d'attente par défaut est de 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="00a69-394">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_stratégie de \_ redirection des options WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-396">Définit le comportement de WinHTTP en ce qui concerne la gestion d’un code d’état de redirection HTTP 30.</span><span class="sxs-lookup"><span data-stu-id="00a69-396">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="00a69-397">Cette option peut être définie sur une session ou un handle de demande sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="00a69-397">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="00a69-398">Terme</span><span class="sxs-lookup"><span data-stu-id="00a69-398">Term</span></span> | <span data-ttu-id="00a69-399">Description</span><span class="sxs-lookup"><span data-stu-id="00a69-399">Description</span></span> |
|-|-|
| <span data-ttu-id="00a69-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_la stratégie de REdirection de l’option WinHTTP est \_ \_ \_ toujours</span><span class="sxs-lookup"><span data-stu-id="00a69-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="00a69-401">Toutes les redirections sont suivies automatiquement.</span><span class="sxs-lookup"><span data-stu-id="00a69-401">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="00a69-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_ \_ la stratégie de redirection des options WinHTTP \_ \_ interdit \_ https \_ à \_ http</span><span class="sxs-lookup"><span data-stu-id="00a69-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="00a69-403">Toutes les redirections sont suivies, à l’exception de celles qui proviennent d’une URL sécurisée (https) vers une URL non sécurisée (http).</span><span class="sxs-lookup"><span data-stu-id="00a69-403">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="00a69-404">Il s'agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="00a69-404">This is the default setting.</span></span> |
| <span data-ttu-id="00a69-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>\_stratégie de \_ redirection des options WinHTTP \_ \_ jamais</span><span class="sxs-lookup"><span data-stu-id="00a69-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="00a69-406">Les redirections ne sont jamais suivies.</span><span class="sxs-lookup"><span data-stu-id="00a69-406">Redirects are never followed.</span></span> <span data-ttu-id="00a69-407">L’état de 30 est renvoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="00a69-407">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_option WinHTTP \_ Reject \_ USERPWD \_ dans l' \_ URL**</span><span class="sxs-lookup"><span data-stu-id="00a69-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-409">Rejette les URL qui contiennent un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="00a69-409">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="00a69-410">Cette option rejette également les URL qui contiennent la sémantique *username : password* , même si aucun nom d’utilisateur ou mot de passe n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="00a69-410">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="00a69-411">Par exemple, « u:p@hostname », « :@hostname », « u:@hostname » et « :p@hostname » sont tous marqués comme étant non valides.</span><span class="sxs-lookup"><span data-stu-id="00a69-411">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="00a69-412">Si une URL non valide est transmise à la fonction, elle retourne l' [erreur \_ WinHTTP \_ \_ URL non valide](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="00a69-412">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="00a69-413">Cette option est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="00a69-413">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**priorité des demandes de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-415">Cette option est dépréciée ; elle n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="00a69-415">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_statistiques des \_ demandes d’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-417">Extrait les statistiques de la demande.</span><span class="sxs-lookup"><span data-stu-id="00a69-417">Retreives statistics for the request.</span></span>  <span data-ttu-id="00a69-418">Pour obtenir la liste des statistiques disponibles, consultez [**\_ \_ statistiques des demandes WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="00a69-418">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**\_ \_ durées de demande de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-420">Informations de minutage extrait pour la requête.</span><span class="sxs-lookup"><span data-stu-id="00a69-420">Retreives timing information for the request.</span></span> <span data-ttu-id="00a69-421">Pour obtenir la liste des minutages disponibles, consultez [**\_ \_ durée des requêtes WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="00a69-421">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**l' \_ option WinHTTP \_ nécessite une \_ fin de flux \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP\_OPTION\_REQUIRE\_STREAM\_END**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="00a69-423">Cette option indique à WinHttp d’ignorer les en-têtes de réponse « Content-Length » et de continuer à recevoir sur un flux jusqu’à ce que l’indicateur END_STREAM soit reçu.</span><span class="sxs-lookup"><span data-stu-id="00a69-423">This option tells WinHttp to ignore "Content-Length" response headers, and continue receiving on a stream until the END_STREAM flag is received.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**\_nom d' \_ hôte de résolution de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="00a69-425">Cette option peut être définie sur un handle de demande WinHttp avant son envoi.</span><span class="sxs-lookup"><span data-stu-id="00a69-425">This option can be set on a WinHttp request handle before it has been sent.</span></span> <span data-ttu-id="00a69-426">Si cette valeur est définie, WinHttp utilise la chaîne fournie par l’appelant comme nom d’hôte pour la résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="00a69-426">If set, WinHttp will use the caller-provided string as the hostname for DNS resolution.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**délai de résolution de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-428">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour résoudre un nom d’hôte.</span><span class="sxs-lookup"><span data-stu-id="00a69-428">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="00a69-429">La valeur par défaut du délai d’attente est **infinie**.</span><span class="sxs-lookup"><span data-stu-id="00a69-429">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="00a69-430">Si une valeur non définie par défaut est spécifiée, il existe une surcharge liée à la création d’un thread par la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="00a69-430">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**\_ \_ protocoles sécurisés option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-432">Définit une valeur d’entier long non signé qui spécifie les protocoles sécurisés qui sont acceptables.</span><span class="sxs-lookup"><span data-stu-id="00a69-432">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="00a69-433">Par défaut, les paramètres SSL3 et TLS1 sont activés uniquement dans Windows 7 et Windows 8.</span><span class="sxs-lookup"><span data-stu-id="00a69-433">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="00a69-434">Par défaut, les protocoles SSL3, TLS 1.0, TLS 1.1 et TLS 1.2 sont activés dans Windows 8.1 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="00a69-434">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="00a69-435">La valeur peut être une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="00a69-435">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="00a69-436">Terme</span><span class="sxs-lookup"><span data-stu-id="00a69-436">Term</span></span> | <span data-ttu-id="00a69-437">Description</span><span class="sxs-lookup"><span data-stu-id="00a69-437">Description</span></span> |
|-|-|
| <span data-ttu-id="00a69-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>\_indicateur WinHTTP \_ \_ tout protocole \_ sécurisé</span><span class="sxs-lookup"><span data-stu-id="00a69-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="00a69-439">Les protocoles SSL (Secure Sockets Layer) (SSL) 2,0, SSL 3,0 et TLS (Transport Layer Security) 1,0 peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="00a69-439">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="00a69-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>\_SSL2 de \_ \_ protocole sécurisé d’indicateur \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="00a69-441">Le protocole SSL 2,0 peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="00a69-441">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="00a69-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>\_Indicateur WinHTTP \_ \_ protocole sécurisé \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="00a69-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="00a69-443">Le protocole SSL 3,0 peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="00a69-443">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="00a69-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>\_TLS1 de \_ \_ protocole sécurisé d’indicateur \_ WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="00a69-445">Le protocole TLS 1,0 peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="00a69-445">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="00a69-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>\_Protocole sécurisé d’indicateur WinHTTP \_ \_ \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="00a69-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="00a69-447">Le protocole TLS 1,1 peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="00a69-447">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="00a69-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>\_Indicateur WinHTTP \_ \_ protocole sécurisé \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="00a69-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="00a69-449">Le protocole TLS 1,2 peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="00a69-449">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="00a69-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_structure de \_ certificat de sécurité option \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-451">Récupère le certificat pour un serveur SSL/TLS dans la structure [**des \_ \_ informations de certificat WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) .</span><span class="sxs-lookup"><span data-stu-id="00a69-451">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="00a69-452">L’application doit libérer les membres **lpszSubjectInfo** et **lpszIssuerInfo** avec [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span><span class="sxs-lookup"><span data-stu-id="00a69-452">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**indicateurs de sécurité de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-454">Définit ou récupère une valeur d’entier long non signé qui contient les indicateurs de sécurité d’un handle.</span><span class="sxs-lookup"><span data-stu-id="00a69-454">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="00a69-455">Il peut s’agir d’une combinaison de ces valeurs :</span><span class="sxs-lookup"><span data-stu-id="00a69-455">It can be a combination of these values:</span></span>

| <span data-ttu-id="00a69-456">Terme</span><span class="sxs-lookup"><span data-stu-id="00a69-456">Term</span></span> | <span data-ttu-id="00a69-457">Description</span><span class="sxs-lookup"><span data-stu-id="00a69-457">Description</span></span> |
|-|-|
| <span data-ttu-id="00a69-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>indicateur de sécurité ignorer le nom \_ \_ commun du \_ certificat \_ \_ non valide</span><span class="sxs-lookup"><span data-stu-id="00a69-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="00a69-459">Autorise un nom commun non valide dans un certificat ; autrement dit, le nom du serveur spécifié par l’application ne correspond pas au nom commun dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="00a69-459">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="00a69-460">Si cet indicateur est défini, l’application ne reçoit pas d' **indicateur d’état de rappel WinHTTP certificat de rappel \_ \_ \_ \_ \_ \_ non valide** .</span><span class="sxs-lookup"><span data-stu-id="00a69-460">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="00a69-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>indicateur de sécurité \_ \_ ignore la \_ Date de certificat \_ \_ non valide</span><span class="sxs-lookup"><span data-stu-id="00a69-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="00a69-462">Autorise une date de certificat non valide, c’est-à-dire un certificat arrivé à expiration ou qui n’est pas encore efficace.</span><span class="sxs-lookup"><span data-stu-id="00a69-462">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="00a69-463">Si cet indicateur est défini, l’application ne reçoit pas d' **indicateur d’état de rappel WinHTTP signaler la date de rappel de \_ \_ \_ \_ certificat \_ \_ non valide** .</span><span class="sxs-lookup"><span data-stu-id="00a69-463">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="00a69-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>indicateur de sécurité \_ \_ ignorer l’autorité de \_ \_ certification inconnue</span><span class="sxs-lookup"><span data-stu-id="00a69-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="00a69-465">Autorise une autorité de certification non valide.</span><span class="sxs-lookup"><span data-stu-id="00a69-465">Allows an invalid certificate authority.</span></span> <span data-ttu-id="00a69-466">Si cet indicateur est défini, l’application ne reçoit pas d' **indicateur d’état de rappel WinHTTP un rappel d' \_ autorité de \_ \_ \_ \_ certification non valide** .</span><span class="sxs-lookup"><span data-stu-id="00a69-466">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="00a69-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>indicateur de sécurité \_ \_ Ignorer \_ \_ \_ l’utilisation incorrecte du certificat</span><span class="sxs-lookup"><span data-stu-id="00a69-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="00a69-468">Autorise l’établissement de l’identité d’un serveur à l’aide d’un certificat non-serveur (par exemple, un certificat client).</span><span class="sxs-lookup"><span data-stu-id="00a69-468">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="00a69-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>indicateur de sécurité \_ \_ ignorer la \_ \_ signature faible</span><span class="sxs-lookup"><span data-stu-id="00a69-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="00a69-470">Permet d’ignorer une signature faible.</span><span class="sxs-lookup"><span data-stu-id="00a69-470">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="00a69-471">Cet indicateur est disponible dans la mise à jour cumulative pour chaque système d’exploitation à partir de Windows 7 et de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="00a69-471">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="00a69-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>indicateur de sécurité \_ \_ sécurisé</span><span class="sxs-lookup"><span data-stu-id="00a69-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="00a69-473">Utilise des transferts sécurisés.</span><span class="sxs-lookup"><span data-stu-id="00a69-473">Uses secure transfers.</span></span> <span data-ttu-id="00a69-474">Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="00a69-474">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="00a69-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>niveau de force de l’indicateur de sécurité \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="00a69-476">Utilise le chiffrement moyen (56 bits).</span><span class="sxs-lookup"><span data-stu-id="00a69-476">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="00a69-477">Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="00a69-477">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="00a69-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>force de l’indicateur de sécurité \_ \_ \_ Strong</span><span class="sxs-lookup"><span data-stu-id="00a69-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="00a69-479">Utilise le chiffrement fort (128 bits).</span><span class="sxs-lookup"><span data-stu-id="00a69-479">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="00a69-480">Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="00a69-480">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="00a69-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>force de l’indicateur de sécurité \_ \_ \_ faible</span><span class="sxs-lookup"><span data-stu-id="00a69-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="00a69-482">Utilise un chiffrement faible (40 bits).</span><span class="sxs-lookup"><span data-stu-id="00a69-482">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="00a69-483">Cela est retourné uniquement dans un appel à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="00a69-483">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="00a69-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**informations de sécurité de l' \_ option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-485">Extrait les informations de chiffrement et de connexion SChannel pour une demande.</span><span class="sxs-lookup"><span data-stu-id="00a69-485">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**nombre de bits de la clé de sécurité de l' \_ option WinHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-487">Récupère une valeur d’entier long non signé qui contient la force de chiffrement de la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="00a69-487">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="00a69-488">Un nombre plus élevé indique un chiffrement de niveau de chiffrement renforcé.</span><span class="sxs-lookup"><span data-stu-id="00a69-488">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**\_ \_ \_ délai d’attente d’envoi des options WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-490">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour envoyer une demande ou écrire des données.</span><span class="sxs-lookup"><span data-stu-id="00a69-490">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="00a69-491">Si l’envoi de la demande prend plus de temps que le délai d’attente, l’opération d’envoi est annulée.</span><span class="sxs-lookup"><span data-stu-id="00a69-491">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="00a69-492">Le délai d’attente par défaut est de 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="00a69-492">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**\_serveur d’option WinHTTP \_ \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="00a69-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-494">Obtient un pointeur vers une structure de [**\_ liaisons SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) qui spécifie un jeton de liaison de canal (CBT).</span><span class="sxs-lookup"><span data-stu-id="00a69-494">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="00a69-495">Un jeton de liaison de canal est une propriété d’un canal de transport sécurisé et est utilisé pour lier un canal d’authentification au canal de transport sécurisé.</span><span class="sxs-lookup"><span data-stu-id="00a69-495">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="00a69-496">Ce jeton ne peut être obtenu que par cette option après l’établissement d’une connexion SSL.</span><span class="sxs-lookup"><span data-stu-id="00a69-496">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="00a69-497">Le passage de cette option et d’une valeur **null** pour *lpBuffer* à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) renvoie une erreur \_ mémoire tampon insuffisante \_ et la taille d’octet requise pour la mémoire tampon dans le paramètre *lpdwBufferLength* .</span><span class="sxs-lookup"><span data-stu-id="00a69-497">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="00a69-498">La valeur de la taille de la mémoire tampon retournée peut être passée dans un appel ultérieur à Query pour le jeton de liaison de canal.</span><span class="sxs-lookup"><span data-stu-id="00a69-498">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="00a69-499">Ces étapes sont nécessaires lors \_ \_ de la gestion de \_ la demande d’état de rappel WinHTTP si vous souhaitez modifier les en-têtes de requête en fonction du jeton de liaison de canal.</span><span class="sxs-lookup"><span data-stu-id="00a69-499">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="00a69-500">Notez que Windows XP et Vista ne prennent pas en charge la modification des en-têtes de demande pendant ce rappel.</span><span class="sxs-lookup"><span data-stu-id="00a69-500">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**\_contexte de \_ chaîne du certificat de serveur d’option WinHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-502">Récupère le contexte de la chaîne de certification du serveur.</span><span class="sxs-lookup"><span data-stu-id="00a69-502">Retrieves the server certification chain context.</span></span> <span data-ttu-id="00a69-503">**WinHTTP \_ L' \_ option \_ \_ \_ contexte de chaîne de certificat serveur** peut être passée pour obtenir un pointeur dupliqué vers le **\_ \_ contexte de chaîne** de certificat pour une chaîne de certificats de serveur reçue pendant une connexion SSL négociée.</span><span class="sxs-lookup"><span data-stu-id="00a69-503">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="00a69-504">Le client doit appeler [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) sur le pointeur de \_ contexte PCCERT retourné qui est rempli dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="00a69-504">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**\_contexte de \_ certificat de serveur d’option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-506">Récupère le contexte de certification du serveur.</span><span class="sxs-lookup"><span data-stu-id="00a69-506">Retrieves the server certification context.</span></span> <span data-ttu-id="00a69-507">**WinHTTP \_ Le \_ \_ \_ contexte** du certificat de serveur d’option peut être passé pour obtenir un pointeur dupliqué vers le [**contexte**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificat pour un certificat de serveur reçu pendant une connexion SSL négociée.</span><span class="sxs-lookup"><span data-stu-id="00a69-507">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="00a69-508">Le client doit appeler [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) sur le pointeur de \_ contexte PCCERT retourné qui est rempli dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="00a69-508">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**nom principal de service du \_ serveur option WinHTTP \_ \_ \_ utilisé**</span><span class="sxs-lookup"><span data-stu-id="00a69-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-510">Obtient le nom principal du serveur serveur que WinHTTP a fourni à SSPI pendant l’authentification.</span><span class="sxs-lookup"><span data-stu-id="00a69-510">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="00a69-511">Cette valeur de chaîne peut être passée à [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) après un échec d’authentification.</span><span class="sxs-lookup"><span data-stu-id="00a69-511">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**SPN de l' \_ option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-513">Permet d’inclure ou de supprimer le numéro de port du serveur lorsque le SPN (nom de principal du service) est créé pour l’authentification Kerberos ou Negotiate Kerberos.</span><span class="sxs-lookup"><span data-stu-id="00a69-513">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="00a69-514">Cet indicateur est l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="00a69-514">This flag is one of the following values:</span></span>

| <span data-ttu-id="00a69-515">Terme</span><span class="sxs-lookup"><span data-stu-id="00a69-515">Term</span></span> | <span data-ttu-id="00a69-516">Description</span><span class="sxs-lookup"><span data-stu-id="00a69-516">Description</span></span> |
|-|-|
| <span data-ttu-id="00a69-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>\_port du \_ serveur de nom principal de service WinHTTP désactivé \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="00a69-518">Supprime le numéro de port du serveur.</span><span class="sxs-lookup"><span data-stu-id="00a69-518">Removes the server port number.</span></span> |
| <span data-ttu-id="00a69-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>\_port du \_ serveur de nom principal de service WinHTTP activé \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="00a69-520">Comprend le numéro de port du serveur.</span><span class="sxs-lookup"><span data-stu-id="00a69-520">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="00a69-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**\_code d' \_ erreur de flux d’options WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP\_OPTION\_STREAM\_ERROR\_CODE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="00a69-522">Cette option peut être interrogée sur un handle de demande WinHttp et retourne le code d’erreur indiqué par une RST_STREAM Frame reçue sur un flux HTTP.</span><span class="sxs-lookup"><span data-stu-id="00a69-522">This option can be queried on a WinHttp request handle, and will return the error code indicated by a RST_STREAM frame received on an HTTP stream.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**\_option WinHTTP \_ TCP \_ Fast \_ Open**</span><span class="sxs-lookup"><span data-stu-id="00a69-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-524">Active TCP Fast Open pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="00a69-524">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_option WinHTTP \_ TCP \_ KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="00a69-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-526">Cette option peut être définie sur un handle de session WinHttp pour activer le comportement TCP Keep-Alive sur le Socket sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="00a69-526">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="00a69-527">Prend un struct [**TCP \_ KeepAlive**](/windows/win32/winsock/sio-keepalive-vals) .</span><span class="sxs-lookup"><span data-stu-id="00a69-527">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**OPTION WINHTTP-début de la \_ \_ \_ valeur TLS false \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-529">Active le démarrage TLS false pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="00a69-529">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**\_option WinHTTP \_ \_ protocole TLS \_ non sécurisé de \_ secours**</span><span class="sxs-lookup"><span data-stu-id="00a69-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-531">Cette option peut être définie sur un handle de session WinHttp pour contrôler si le recours à TLS 1,0 est autorisé en cas d’échec de la liaison TLS avec une version de protocole plus récente.</span><span class="sxs-lookup"><span data-stu-id="00a69-531">This option can be set on a WinHttp session handle to control whether fallback to TLS 1.0 is allowed if there is a TLS handshake failure with a newer protocol version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**\_événement de \_ notification de déchargement d’option WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-533">Prend un événement qui sera défini lorsque le dernier rappel est terminé pour une session particulière.</span><span class="sxs-lookup"><span data-stu-id="00a69-533">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="00a69-534">Cet indicateur doit être utilisé sur un handle de session.</span><span class="sxs-lookup"><span data-stu-id="00a69-534">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="00a69-535">L’événement ne peut pas être fermé tant qu’il n’a pas été défini par WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="00a69-535">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**\_option WinHTTP \_ \_ -analyse d’en-tête non sécurisé \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-537">Cette option est réservée à un usage interne et ne doit pas être appelée.</span><span class="sxs-lookup"><span data-stu-id="00a69-537">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**\_option WinHTTP \_ mettre à niveau \_ vers \_ Web \_ Socket**</span><span class="sxs-lookup"><span data-stu-id="00a69-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-539">Demande à la pile de démarrer un processus d’établissement de liaison WebSocket avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="00a69-539">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="00a69-540">Cette option n’accepte aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="00a69-540">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**URL de l' \_ option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-542">Récupère une valeur de chaîne qui contient l’URL complète d’une ressource téléchargée.</span><span class="sxs-lookup"><span data-stu-id="00a69-542">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="00a69-543">Si l’URL d’origine contenait des données supplémentaires, telles que des chaînes ou des ancres de recherche, ou si l’appel a été redirigé, l’URL retournée est différente de l’original.</span><span class="sxs-lookup"><span data-stu-id="00a69-543">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="00a69-544">L’application doit passer une mémoire tampon, dimensionnée en octets, qui est suffisamment grande pour contenir l’URL retournée en caractères larges.</span><span class="sxs-lookup"><span data-stu-id="00a69-544">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_option WinHTTP \_ utiliser \_ les \_ \_ informations d’identification du serveur global**</span><span class="sxs-lookup"><span data-stu-id="00a69-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-546">Prend un **bool** et ne peut être défini qu’avec un handle de session.</span><span class="sxs-lookup"><span data-stu-id="00a69-546">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="00a69-547">Il se propage uniquement aux descripteurs créés à partir du descripteur de session après que l’option a été définie.</span><span class="sxs-lookup"><span data-stu-id="00a69-547">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="00a69-548">Si la **valeur est true**, cette option entraîne, en dernier recours, l’utilisation d’informations d’identification de serveur globales qui ont été transférées depuis wininet.</span><span class="sxs-lookup"><span data-stu-id="00a69-548">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="00a69-549">La valeur par défaut de cette option est **false**.</span><span class="sxs-lookup"><span data-stu-id="00a69-549">The default for this option is **FALSE**.</span></span> <span data-ttu-id="00a69-550">Cette option requiert la clé de Registre **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings ! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="00a69-550">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="00a69-551">Cette clé de Registre n’est pas présente par défaut.</span><span class="sxs-lookup"><span data-stu-id="00a69-551">This registry key is not present by default.</span></span> <span data-ttu-id="00a69-552">Lorsqu’il est défini, WinINet envoie les informations d’identification vers WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="00a69-552">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="00a69-553">Chaque fois que WinHttp reçoit une demande d’authentification et si aucune information d’identification n’est définie sur le handle actuel, il utilise les informations d’identification fournies par WinINet.</span><span class="sxs-lookup"><span data-stu-id="00a69-553">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_ \_ agent utilisateur de \_ l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-555">Définit ou récupère la chaîne de l' [*agent utilisateur*](glossary.md) sur les handles fournis par [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) et utilisés dans les fonctions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) suivantes, à condition qu’elles ne soient pas remplacées par un en-tête ajouté par [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) ou **WinHttpSendRequest**.</span><span class="sxs-lookup"><span data-stu-id="00a69-555">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="00a69-556">Lors de la récupération d’un agent utilisateur, l’application doit passer une mémoire tampon, dimensionnée en octets, qui est suffisamment grande pour contenir l’URL retournée en caractères larges.</span><span class="sxs-lookup"><span data-stu-id="00a69-556">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="00a69-557">Lors de la définition de l’agent utilisateur, la taille de la mémoire tampon correspond à la longueur de la chaîne, en caractères, plus la marque de fin **null** .</span><span class="sxs-lookup"><span data-stu-id="00a69-557">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**\_option WinHTTP \_ nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="00a69-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-559">Définit ou récupère une chaîne qui contient le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="00a69-559">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_ \_ \_ \_ \_ délai d’attente de fermeture du socket Web de l’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-561">Définit le délai, en millisecondes, pendant lequel [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) doit attendre pour terminer le protocole de transfert de fermeture.</span><span class="sxs-lookup"><span data-stu-id="00a69-561">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="00a69-562">La valeur par défaut est 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="00a69-562">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**\_intervalle de \_ conservation \_ de \_ conservation de socket Web \_ d’option WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-564">Définit l’intervalle, en millisecondes, pour envoyer un paquet Keep-Alive sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="00a69-564">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="00a69-565">L’intervalle par défaut est de 30000 (30 secondes).</span><span class="sxs-lookup"><span data-stu-id="00a69-565">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="00a69-566">L’intervalle minimal est 15000 (15 secondes).</span><span class="sxs-lookup"><span data-stu-id="00a69-566">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="00a69-567">L’utilisation de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) pour définir une valeur inférieure à 15000 retourne **le \_ \_ paramètre error non valide**.</span><span class="sxs-lookup"><span data-stu-id="00a69-567">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="00a69-568">La valeur par défaut de l' **option WinHTTP de l’intervalle de \_ \_ \_ conservation de socket \_ \_ Web** est lue à partir de **HKLM : \\ Software \\ Microsoft \\ WebSocket \\ KeepaliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="00a69-568">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="00a69-569">Si aucune valeur n’est définie, la valeur par défaut 30000 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="00a69-569">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="00a69-570">Il n’est pas possible d’avoir un intervalle KeepAlive inférieur à 15000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="00a69-570">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon de réception du socket Web \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-572">Définit ou récupère une valeur DWORD qui spécifie la taille de la mémoire tampon de réception à utiliser sur les connexions WebSocket.</span><span class="sxs-lookup"><span data-stu-id="00a69-572">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon d’envoi du socket Web \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-574">Définit ou récupère une valeur DWORD qui spécifie la taille de la mémoire tampon d’envoi à utiliser sur les connexions WebSocket.</span><span class="sxs-lookup"><span data-stu-id="00a69-574">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**\_nombre de \_ \_ threads de travail option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-576">Définit une valeur d’entier long non signé qui spécifie le nombre de threads de travail que le pool de threads doit utiliser pour les saisies semi-automatiques asynchrones.</span><span class="sxs-lookup"><span data-stu-id="00a69-576">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="00a69-577">La valeur par défaut de cette option est zéro, ce qui indique que le nombre de threads de travail est égal au nombre de processeurs sur le système.</span><span class="sxs-lookup"><span data-stu-id="00a69-577">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="00a69-578">Cette option ne peut être définie que sur un handle [HINTERNET](hinternet-handles-in-winhttp.md) **null** avant qu’une opération asynchrone se produise.  </span><span class="sxs-lookup"><span data-stu-id="00a69-578">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="00a69-579">Cette option ne peut être définie qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="00a69-579">This option can only be set once.</span></span>

<span data-ttu-id="00a69-580">**Windows Server 2008 R2 et Windows 7 :** Cet indicateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="00a69-580">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="00a69-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_taille de \_ la \_ mémoire tampon d’écriture de l’option WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="00a69-582">Cette option est dépréciée ; elle n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="00a69-582">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00a69-583">Remarques</span><span class="sxs-lookup"><span data-stu-id="00a69-583">Remarks</span></span>

<span data-ttu-id="00a69-584">Le tableau suivant répertorie les indicateurs d’option en spécifiant les descripteurs sur lesquels ils peuvent agir, s’ils peuvent être interrogés et définis, ainsi que le type de données utilisé.</span><span class="sxs-lookup"><span data-stu-id="00a69-584">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="00a69-585">Un « X » indique que l’indicateur d’option est valide pour une utilisation avec la fonction ou le handle, alors que « - » spécifie que l’indicateur d’option n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="00a69-585">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="00a69-586">Si vous tentez de définir ou d’interroger un indicateur d’option sur une version de Windows où il n’est pas pris en charge, l' **\_ \_ \_ option WinHTTP non valide** est générée.</span><span class="sxs-lookup"><span data-stu-id="00a69-586">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="00a69-587">Indicateur d’option et type de données</span><span class="sxs-lookup"><span data-stu-id="00a69-587">Option flag, and data type</span></span> | <span data-ttu-id="00a69-588">Handle de session</span><span class="sxs-lookup"><span data-stu-id="00a69-588">Session handle</span></span> | <span data-ttu-id="00a69-589">Handle de demande</span><span class="sxs-lookup"><span data-stu-id="00a69-589">Request handle</span></span> | <span data-ttu-id="00a69-590">Option de requête</span><span class="sxs-lookup"><span data-stu-id="00a69-590">Query option</span></span> | <span data-ttu-id="00a69-591">Option Set</span><span class="sxs-lookup"><span data-stu-id="00a69-591">Set option</span></span> | <span data-ttu-id="00a69-592">Version minimale de Windows</span><span class="sxs-lookup"><span data-stu-id="00a69-592">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="00a69-593">OPTION WINHTTP assurée par les \_ \_ \_ \_ rappels non bloquants \_</span><span class="sxs-lookup"><span data-stu-id="00a69-593">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="00a69-594">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-594">**BOOL**</span></span> | <span data-ttu-id="00a69-595">X</span><span class="sxs-lookup"><span data-stu-id="00a69-595">X</span></span> | \- | \- | <span data-ttu-id="00a69-596">X</span><span class="sxs-lookup"><span data-stu-id="00a69-596">X</span></span> | \- |
| <span data-ttu-id="00a69-597">stratégie d’accès automatique aux \_ options WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-597">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="00a69-598">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-598">**DWORD**</span></span> | \- | <span data-ttu-id="00a69-599">X</span><span class="sxs-lookup"><span data-stu-id="00a69-599">X</span></span> | \- | <span data-ttu-id="00a69-600">X</span><span class="sxs-lookup"><span data-stu-id="00a69-600">X</span></span> | \- |
| <span data-ttu-id="00a69-601">\_connexions en \_ arrière-plan des options WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-601">WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS</span></span><br/><span data-ttu-id="00a69-602">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-602">**DWORD**</span></span> | <span data-ttu-id="00a69-603">X</span><span class="sxs-lookup"><span data-stu-id="00a69-603">X</span></span> | \- | \- | <span data-ttu-id="00a69-604">X</span><span class="sxs-lookup"><span data-stu-id="00a69-604">X</span></span> | <span data-ttu-id="00a69-605">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="00a69-605">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="00a69-606">\_rappel d’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-606">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="00a69-607">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="00a69-607">**LPVOID**</span></span> | <span data-ttu-id="00a69-608">X</span><span class="sxs-lookup"><span data-stu-id="00a69-608">X</span></span> | <span data-ttu-id="00a69-609">X</span><span class="sxs-lookup"><span data-stu-id="00a69-609">X</span></span> | <span data-ttu-id="00a69-610">X</span><span class="sxs-lookup"><span data-stu-id="00a69-610">X</span></span> | <span data-ttu-id="00a69-611">X</span><span class="sxs-lookup"><span data-stu-id="00a69-611">X</span></span> | \- |
| <span data-ttu-id="00a69-612">\_contexte de \_ \_ certificat client \_ de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-612">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="00a69-613">**contexte du certificat \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-613">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="00a69-614">X</span><span class="sxs-lookup"><span data-stu-id="00a69-614">X</span></span> | \- | <span data-ttu-id="00a69-615">X</span><span class="sxs-lookup"><span data-stu-id="00a69-615">X</span></span> | <span data-ttu-id="00a69-616">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00a69-616">Windows Vista</span></span> |
| <span data-ttu-id="00a69-617">\_option WinHTTP \_ \_ liste d’émetteurs de certificats client \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-617">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="00a69-618">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="00a69-618">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="00a69-619">X</span><span class="sxs-lookup"><span data-stu-id="00a69-619">X</span></span> | <span data-ttu-id="00a69-620">X</span><span class="sxs-lookup"><span data-stu-id="00a69-620">X</span></span> | \- | <span data-ttu-id="00a69-621">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00a69-621">Windows Vista</span></span> |
| <span data-ttu-id="00a69-622">page de codes de l' \_ option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-622">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="00a69-623">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-623">**DWORD**</span></span> | <span data-ttu-id="00a69-624">X</span><span class="sxs-lookup"><span data-stu-id="00a69-624">X</span></span> | \- | \- | <span data-ttu-id="00a69-625">X</span><span class="sxs-lookup"><span data-stu-id="00a69-625">X</span></span> | \- |
| <span data-ttu-id="00a69-626">\_option WinHTTP \_ configurer \_ l' \_ authentification Passport</span><span class="sxs-lookup"><span data-stu-id="00a69-626">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="00a69-627">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-627">**DWORD**</span></span> | <span data-ttu-id="00a69-628">X</span><span class="sxs-lookup"><span data-stu-id="00a69-628">X</span></span> | \- | \- | <span data-ttu-id="00a69-629">X</span><span class="sxs-lookup"><span data-stu-id="00a69-629">X</span></span> | \- |
| <span data-ttu-id="00a69-630">\_ \_ nouvelles tentatives de connexion de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-630">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="00a69-631">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-631">**DWORD**</span></span> | <span data-ttu-id="00a69-632">X</span><span class="sxs-lookup"><span data-stu-id="00a69-632">X</span></span> | <span data-ttu-id="00a69-633">X</span><span class="sxs-lookup"><span data-stu-id="00a69-633">X</span></span> | <span data-ttu-id="00a69-634">X</span><span class="sxs-lookup"><span data-stu-id="00a69-634">X</span></span> | <span data-ttu-id="00a69-635">X</span><span class="sxs-lookup"><span data-stu-id="00a69-635">X</span></span> | \- |
| <span data-ttu-id="00a69-636">délai de connexion de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-636">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="00a69-637">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-637">**DWORD**</span></span> | <span data-ttu-id="00a69-638">X</span><span class="sxs-lookup"><span data-stu-id="00a69-638">X</span></span> | <span data-ttu-id="00a69-639">X</span><span class="sxs-lookup"><span data-stu-id="00a69-639">X</span></span> | <span data-ttu-id="00a69-640">X</span><span class="sxs-lookup"><span data-stu-id="00a69-640">X</span></span> | <span data-ttu-id="00a69-641">X</span><span class="sxs-lookup"><span data-stu-id="00a69-641">X</span></span> | \- |
| <span data-ttu-id="00a69-642">informations de connexion de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-642">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="00a69-643">**\_informations de connexion WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-643">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="00a69-644">X</span><span class="sxs-lookup"><span data-stu-id="00a69-644">X</span></span> | <span data-ttu-id="00a69-645">X</span><span class="sxs-lookup"><span data-stu-id="00a69-645">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-646">\_Statistiques de connexion des options WinHTTP \_ \_ \_ v0</span><span class="sxs-lookup"><span data-stu-id="00a69-646">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="00a69-647">**\_Informations TCP \_ v0**</span><span class="sxs-lookup"><span data-stu-id="00a69-647">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="00a69-648">X</span><span class="sxs-lookup"><span data-stu-id="00a69-648">X</span></span> | <span data-ttu-id="00a69-649">X</span><span class="sxs-lookup"><span data-stu-id="00a69-649">X</span></span> | \- | <span data-ttu-id="00a69-650">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="00a69-650">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="00a69-651">\_Statistiques de connexion des options WinHTTP \_ \_ \_ v1</span><span class="sxs-lookup"><span data-stu-id="00a69-651">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="00a69-652">**\_Informations TCP \_ v1**</span><span class="sxs-lookup"><span data-stu-id="00a69-652">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="00a69-653">X</span><span class="sxs-lookup"><span data-stu-id="00a69-653">X</span></span> | <span data-ttu-id="00a69-654">X</span><span class="sxs-lookup"><span data-stu-id="00a69-654">X</span></span> | \- | <span data-ttu-id="00a69-655">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="00a69-655">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="00a69-656">valeur de contexte de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-656">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="00a69-657">**\_ptr DWORD**</span><span class="sxs-lookup"><span data-stu-id="00a69-657">**DWORD\_PTR**</span></span> | <span data-ttu-id="00a69-658">X</span><span class="sxs-lookup"><span data-stu-id="00a69-658">X</span></span> | <span data-ttu-id="00a69-659">X</span><span class="sxs-lookup"><span data-stu-id="00a69-659">X</span></span> | <span data-ttu-id="00a69-660">X</span><span class="sxs-lookup"><span data-stu-id="00a69-660">X</span></span> | <span data-ttu-id="00a69-661">X</span><span class="sxs-lookup"><span data-stu-id="00a69-661">X</span></span> | \- |
| <span data-ttu-id="00a69-662">décompression des \_ options WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-662">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="00a69-663">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-663">**DWORD**</span></span> | <span data-ttu-id="00a69-664">X</span><span class="sxs-lookup"><span data-stu-id="00a69-664">X</span></span> | <span data-ttu-id="00a69-665">X</span><span class="sxs-lookup"><span data-stu-id="00a69-665">X</span></span> | \- | <span data-ttu-id="00a69-666">X</span><span class="sxs-lookup"><span data-stu-id="00a69-666">X</span></span> | <span data-ttu-id="00a69-667">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="00a69-667">Windows 8.1</span></span> |
| <span data-ttu-id="00a69-668">OPTION WINHTTP- \_ désactiver la génération de \_ \_ chaîne de certificats \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-668">WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING</span></span><br/><span data-ttu-id="00a69-669">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-669">**BOOL**</span></span> | <span data-ttu-id="00a69-670">X</span><span class="sxs-lookup"><span data-stu-id="00a69-670">X</span></span> | \- | \- | <span data-ttu-id="00a69-671">X</span><span class="sxs-lookup"><span data-stu-id="00a69-671">X</span></span> | <span data-ttu-id="00a69-672">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="00a69-672">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="00a69-673">\_fonctionnalité de \_ désactivation de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-673">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="00a69-674">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-674">**DWORD**</span></span> | \- | <span data-ttu-id="00a69-675">X</span><span class="sxs-lookup"><span data-stu-id="00a69-675">X</span></span> | \- | <span data-ttu-id="00a69-676">X</span><span class="sxs-lookup"><span data-stu-id="00a69-676">X</span></span> | \- |
| <span data-ttu-id="00a69-677">\_option WinHTTP \_ désactiver \_ le \_ protocole sécurisé de \_ secours</span><span class="sxs-lookup"><span data-stu-id="00a69-677">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="00a69-678">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-678">**BOOL**</span></span> | <span data-ttu-id="00a69-679">X</span><span class="sxs-lookup"><span data-stu-id="00a69-679">X</span></span> | \- | \- | <span data-ttu-id="00a69-680">X</span><span class="sxs-lookup"><span data-stu-id="00a69-680">X</span></span> | <span data-ttu-id="00a69-681">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="00a69-681">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="00a69-682">OPTION WINHTTP- \_ \_ désactiver la \_ \_ file d’attente de flux</span><span class="sxs-lookup"><span data-stu-id="00a69-682">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="00a69-683">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-683">**BOOL**</span></span> | <span data-ttu-id="00a69-684">X</span><span class="sxs-lookup"><span data-stu-id="00a69-684">X</span></span> | <span data-ttu-id="00a69-685">X</span><span class="sxs-lookup"><span data-stu-id="00a69-685">X</span></span> | \- | <span data-ttu-id="00a69-686">X</span><span class="sxs-lookup"><span data-stu-id="00a69-686">X</span></span> | <span data-ttu-id="00a69-687">Windows 10 version 1809</span><span class="sxs-lookup"><span data-stu-id="00a69-687">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="00a69-688">\_option WinHTTP \_ activer la \_ fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="00a69-688">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="00a69-689">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-689">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="00a69-690">X</span><span class="sxs-lookup"><span data-stu-id="00a69-690">X</span></span> | \- |
| <span data-ttu-id="00a69-691">\_option WinHTTP \_ activer \_ le \_ protocole http</span><span class="sxs-lookup"><span data-stu-id="00a69-691">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="00a69-692">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-692">**DWORD**</span></span> | <span data-ttu-id="00a69-693">X</span><span class="sxs-lookup"><span data-stu-id="00a69-693">X</span></span> | <span data-ttu-id="00a69-694">X</span><span class="sxs-lookup"><span data-stu-id="00a69-694">X</span></span> | \- | <span data-ttu-id="00a69-695">X</span><span class="sxs-lookup"><span data-stu-id="00a69-695">X</span></span> | <span data-ttu-id="00a69-696">Windows 10 version 1607</span><span class="sxs-lookup"><span data-stu-id="00a69-696">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="00a69-697">\_Option WinHTTP \_ activer \_ le \_ \_ contexte de \_ certificat client http2 plus \_</span><span class="sxs-lookup"><span data-stu-id="00a69-697">WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT\_CONTEXT</span></span><br/><span data-ttu-id="00a69-698">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-698">**BOOL**</span></span> | <span data-ttu-id="00a69-699">X</span><span class="sxs-lookup"><span data-stu-id="00a69-699">X</span></span> | \- | \- | <span data-ttu-id="00a69-700">X</span><span class="sxs-lookup"><span data-stu-id="00a69-700">X</span></span> | <span data-ttu-id="00a69-701">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="00a69-701">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="00a69-702">\_option WinHTTP \_ EnableTracing,</span><span class="sxs-lookup"><span data-stu-id="00a69-702">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="00a69-703">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-703">**DWORD**</span></span> | \- | \- | <span data-ttu-id="00a69-704">X</span><span class="sxs-lookup"><span data-stu-id="00a69-704">X</span></span> | <span data-ttu-id="00a69-705">X</span><span class="sxs-lookup"><span data-stu-id="00a69-705">X</span></span> | \- |
| <span data-ttu-id="00a69-706">\_option WinHTTP \_ coder \_ extra</span><span class="sxs-lookup"><span data-stu-id="00a69-706">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="00a69-707">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-707">**BOOL**</span></span> | <span data-ttu-id="00a69-708">X</span><span class="sxs-lookup"><span data-stu-id="00a69-708">X</span></span> | <span data-ttu-id="00a69-709">X</span><span class="sxs-lookup"><span data-stu-id="00a69-709">X</span></span> | \- | <span data-ttu-id="00a69-710">X</span><span class="sxs-lookup"><span data-stu-id="00a69-710">X</span></span> | <span data-ttu-id="00a69-711">Windows 10 version 1803</span><span class="sxs-lookup"><span data-stu-id="00a69-711">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="00a69-712">expiration de la connexion de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-712">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="00a69-713">N/A</span><span class="sxs-lookup"><span data-stu-id="00a69-713">N/A</span></span> | \- | <span data-ttu-id="00a69-714">X</span><span class="sxs-lookup"><span data-stu-id="00a69-714">X</span></span> | \- | <span data-ttu-id="00a69-715">X</span><span class="sxs-lookup"><span data-stu-id="00a69-715">X</span></span> | <span data-ttu-id="00a69-716">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="00a69-716">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="00a69-717">\_ \_ erreur étendue de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-717">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="00a69-718">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-718">**DWORD**</span></span> | <span data-ttu-id="00a69-719">X</span><span class="sxs-lookup"><span data-stu-id="00a69-719">X</span></span> | <span data-ttu-id="00a69-720">X</span><span class="sxs-lookup"><span data-stu-id="00a69-720">X</span></span> | <span data-ttu-id="00a69-721">X</span><span class="sxs-lookup"><span data-stu-id="00a69-721">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-722">\_option WinHTTP \_ première \_ \_ connexion disponible</span><span class="sxs-lookup"><span data-stu-id="00a69-722">WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION</span></span><br/><span data-ttu-id="00a69-723">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-723">**BOOL**</span></span> | <span data-ttu-id="00a69-724">X</span><span class="sxs-lookup"><span data-stu-id="00a69-724">X</span></span> | \- | \- | <span data-ttu-id="00a69-725">X</span><span class="sxs-lookup"><span data-stu-id="00a69-725">X</span></span> | <span data-ttu-id="00a69-726">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="00a69-726">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="00a69-727">identification \_ du \_ proxy global des options \_ WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-727">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="00a69-728">**\_références WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="00a69-728">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="00a69-729">X</span><span class="sxs-lookup"><span data-stu-id="00a69-729">X</span></span> | <span data-ttu-id="00a69-730">X</span><span class="sxs-lookup"><span data-stu-id="00a69-730">X</span></span> | \- | <span data-ttu-id="00a69-731">X</span><span class="sxs-lookup"><span data-stu-id="00a69-731">X</span></span> | \- |
| <span data-ttu-id="00a69-732">\_options WinHTTP \_ - \_ CREDS de serveur global \_</span><span class="sxs-lookup"><span data-stu-id="00a69-732">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="00a69-733">**\_références WinHTTP \_ ex**</span><span class="sxs-lookup"><span data-stu-id="00a69-733">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="00a69-734">X</span><span class="sxs-lookup"><span data-stu-id="00a69-734">X</span></span> | <span data-ttu-id="00a69-735">X</span><span class="sxs-lookup"><span data-stu-id="00a69-735">X</span></span> | \- | <span data-ttu-id="00a69-736">X</span><span class="sxs-lookup"><span data-stu-id="00a69-736">X</span></span> | \- |
| <span data-ttu-id="00a69-737">TYPE de handle de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-737">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="00a69-738">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-738">**DWORD**</span></span> | <span data-ttu-id="00a69-739">X</span><span class="sxs-lookup"><span data-stu-id="00a69-739">X</span></span> | <span data-ttu-id="00a69-740">X</span><span class="sxs-lookup"><span data-stu-id="00a69-740">X</span></span> | <span data-ttu-id="00a69-741">X</span><span class="sxs-lookup"><span data-stu-id="00a69-741">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-742">\_option WinHTTP \_ \_ protocole http \_ requis</span><span class="sxs-lookup"><span data-stu-id="00a69-742">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="00a69-743">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-743">**BOOL**</span></span> | <span data-ttu-id="00a69-744">X</span><span class="sxs-lookup"><span data-stu-id="00a69-744">X</span></span> | <span data-ttu-id="00a69-745">X</span><span class="sxs-lookup"><span data-stu-id="00a69-745">X</span></span> | \- | <span data-ttu-id="00a69-746">X</span><span class="sxs-lookup"><span data-stu-id="00a69-746">X</span></span> | <span data-ttu-id="00a69-747">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="00a69-747">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="00a69-748">\_option WinHTTP \_ \_ protocole http \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="00a69-748">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="00a69-749">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-749">**DWORD**</span></span> | \- | <span data-ttu-id="00a69-750">X</span><span class="sxs-lookup"><span data-stu-id="00a69-750">X</span></span> | <span data-ttu-id="00a69-751">X</span><span class="sxs-lookup"><span data-stu-id="00a69-751">X</span></span> | \- | <span data-ttu-id="00a69-752">Windows 10 version 1607</span><span class="sxs-lookup"><span data-stu-id="00a69-752">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="00a69-753">\_ \_ version http de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-753">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="00a69-754">**\_informations sur la version http \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-754">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="00a69-755">X</span><span class="sxs-lookup"><span data-stu-id="00a69-755">X</span></span> | <span data-ttu-id="00a69-756">X</span><span class="sxs-lookup"><span data-stu-id="00a69-756">X</span></span> | <span data-ttu-id="00a69-757">X</span><span class="sxs-lookup"><span data-stu-id="00a69-757">X</span></span> | <span data-ttu-id="00a69-758">X</span><span class="sxs-lookup"><span data-stu-id="00a69-758">X</span></span> | \- |
| <span data-ttu-id="00a69-759">\_Option WinHTTP \_ http2 \_ KeepAlive</span><span class="sxs-lookup"><span data-stu-id="00a69-759">WINHTTP\_OPTION\_HTTP2\_KEEPALIVE</span></span><br/><span data-ttu-id="00a69-760">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-760">**DWORD**</span></span> | <span data-ttu-id="00a69-761">X</span><span class="sxs-lookup"><span data-stu-id="00a69-761">X</span></span> | \- | \- | <span data-ttu-id="00a69-762">X</span><span class="sxs-lookup"><span data-stu-id="00a69-762">X</span></span> | <span data-ttu-id="00a69-763">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="00a69-763">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="00a69-764">\_Option WinHTTP \_ http2 \_ plus \_ \_ encodage de transfert</span><span class="sxs-lookup"><span data-stu-id="00a69-764">WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING</span></span><br/><span data-ttu-id="00a69-765">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-765">**BOOL**</span></span> | <span data-ttu-id="00a69-766">X</span><span class="sxs-lookup"><span data-stu-id="00a69-766">X</span></span> | <span data-ttu-id="00a69-767">X</span><span class="sxs-lookup"><span data-stu-id="00a69-767">X</span></span> | \- | <span data-ttu-id="00a69-768">X</span><span class="sxs-lookup"><span data-stu-id="00a69-768">X</span></span> | <span data-ttu-id="00a69-769">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="00a69-769">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="00a69-770">\_option WinHTTP \_ Ignorer \_ la \_ révocation de certificat \_ hors connexion</span><span class="sxs-lookup"><span data-stu-id="00a69-770">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="00a69-771">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-771">**BOOL**</span></span> | \- | <span data-ttu-id="00a69-772">X</span><span class="sxs-lookup"><span data-stu-id="00a69-772">X</span></span> | \- | <span data-ttu-id="00a69-773">X</span><span class="sxs-lookup"><span data-stu-id="00a69-773">X</span></span> | <span data-ttu-id="00a69-774">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="00a69-774">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="00a69-775">\_Option WinHTTP \_ \_ Fast \_ Fallback IPv6</span><span class="sxs-lookup"><span data-stu-id="00a69-775">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="00a69-776">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-776">**BOOL**</span></span> | <span data-ttu-id="00a69-777">X</span><span class="sxs-lookup"><span data-stu-id="00a69-777">X</span></span> | \- | \- | <span data-ttu-id="00a69-778">X</span><span class="sxs-lookup"><span data-stu-id="00a69-778">X</span></span> | <span data-ttu-id="00a69-779">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="00a69-779">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="00a69-780">l' \_ option WinHTTP \_ est une \_ \_ réponse de connexion proxy \_</span><span class="sxs-lookup"><span data-stu-id="00a69-780">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="00a69-781">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-781">**BOOL**</span></span> | <span data-ttu-id="00a69-782">X</span><span class="sxs-lookup"><span data-stu-id="00a69-782">X</span></span> | <span data-ttu-id="00a69-783">X</span><span class="sxs-lookup"><span data-stu-id="00a69-783">X</span></span> | <span data-ttu-id="00a69-784">X</span><span class="sxs-lookup"><span data-stu-id="00a69-784">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-785">\_Option WinHTTP \_ nombre de Conn. \_ \_ par \_ \_ serveur 1 0 \_</span><span class="sxs-lookup"><span data-stu-id="00a69-785">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="00a69-786">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-786">**DWORD**</span></span> | <span data-ttu-id="00a69-787">X</span><span class="sxs-lookup"><span data-stu-id="00a69-787">X</span></span> | \- | <span data-ttu-id="00a69-788">X</span><span class="sxs-lookup"><span data-stu-id="00a69-788">X</span></span> | <span data-ttu-id="00a69-789">X</span><span class="sxs-lookup"><span data-stu-id="00a69-789">X</span></span> | \- |
| <span data-ttu-id="00a69-790">\_option WinHTTP \_ nombre maximal de \_ conn. \_ par \_ serveur</span><span class="sxs-lookup"><span data-stu-id="00a69-790">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="00a69-791">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-791">**DWORD**</span></span> | <span data-ttu-id="00a69-792">X</span><span class="sxs-lookup"><span data-stu-id="00a69-792">X</span></span> | \- | <span data-ttu-id="00a69-793">X</span><span class="sxs-lookup"><span data-stu-id="00a69-793">X</span></span> | <span data-ttu-id="00a69-794">X</span><span class="sxs-lookup"><span data-stu-id="00a69-794">X</span></span> | \- |
| <span data-ttu-id="00a69-795">\_option WinHTTP \_ nombre maximal de \_ \_ \_ redirections http automatiques</span><span class="sxs-lookup"><span data-stu-id="00a69-795">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="00a69-796">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-796">**DWORD**</span></span> | <span data-ttu-id="00a69-797">X</span><span class="sxs-lookup"><span data-stu-id="00a69-797">X</span></span> | <span data-ttu-id="00a69-798">X</span><span class="sxs-lookup"><span data-stu-id="00a69-798">X</span></span> | <span data-ttu-id="00a69-799">X</span><span class="sxs-lookup"><span data-stu-id="00a69-799">X</span></span> | <span data-ttu-id="00a69-800">X</span><span class="sxs-lookup"><span data-stu-id="00a69-800">X</span></span> | \- |
| <span data-ttu-id="00a69-801">\_ \_ État http max de l’option WinHTTP \_ \_ \_ continue</span><span class="sxs-lookup"><span data-stu-id="00a69-801">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="00a69-802">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-802">**DWORD**</span></span> | <span data-ttu-id="00a69-803">X</span><span class="sxs-lookup"><span data-stu-id="00a69-803">X</span></span> | <span data-ttu-id="00a69-804">X</span><span class="sxs-lookup"><span data-stu-id="00a69-804">X</span></span> | <span data-ttu-id="00a69-805">X</span><span class="sxs-lookup"><span data-stu-id="00a69-805">X</span></span> | <span data-ttu-id="00a69-806">X</span><span class="sxs-lookup"><span data-stu-id="00a69-806">X</span></span> | \- |
| <span data-ttu-id="00a69-807">\_option WinHTTP \_ taille maximale de \_ \_ drainage \_ de la réponse</span><span class="sxs-lookup"><span data-stu-id="00a69-807">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="00a69-808">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-808">**DWORD**</span></span> | <span data-ttu-id="00a69-809">X</span><span class="sxs-lookup"><span data-stu-id="00a69-809">X</span></span> | <span data-ttu-id="00a69-810">X</span><span class="sxs-lookup"><span data-stu-id="00a69-810">X</span></span> | <span data-ttu-id="00a69-811">X</span><span class="sxs-lookup"><span data-stu-id="00a69-811">X</span></span> | <span data-ttu-id="00a69-812">X</span><span class="sxs-lookup"><span data-stu-id="00a69-812">X</span></span> | \- |
| <span data-ttu-id="00a69-813">\_ \_ taille maximale d' \_ \_ en-tête de réponse \_ de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-813">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="00a69-814">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-814">**DWORD**</span></span> | <span data-ttu-id="00a69-815">X</span><span class="sxs-lookup"><span data-stu-id="00a69-815">X</span></span> | <span data-ttu-id="00a69-816">X</span><span class="sxs-lookup"><span data-stu-id="00a69-816">X</span></span> | <span data-ttu-id="00a69-817">X</span><span class="sxs-lookup"><span data-stu-id="00a69-817">X</span></span> | <span data-ttu-id="00a69-818">X</span><span class="sxs-lookup"><span data-stu-id="00a69-818">X</span></span> | \- |
| <span data-ttu-id="00a69-819">\_ \_ handle parent de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-819">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="00a69-820">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="00a69-820">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="00a69-821">X</span><span class="sxs-lookup"><span data-stu-id="00a69-821">X</span></span> | <span data-ttu-id="00a69-822">X</span><span class="sxs-lookup"><span data-stu-id="00a69-822">X</span></span> | <span data-ttu-id="00a69-823">X</span><span class="sxs-lookup"><span data-stu-id="00a69-823">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-824">OPTION WINHTTP du texte de la \_ \_ \_ comarketingisation Passport \_</span><span class="sxs-lookup"><span data-stu-id="00a69-824">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="00a69-825">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="00a69-825">**LPWSTR**</span></span> | \- | <span data-ttu-id="00a69-826">X</span><span class="sxs-lookup"><span data-stu-id="00a69-826">X</span></span> | <span data-ttu-id="00a69-827">X</span><span class="sxs-lookup"><span data-stu-id="00a69-827">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-828">\_URL de \_ la \_ comarketing de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-828">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="00a69-829">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="00a69-829">**LPWSTR**</span></span> | \- | <span data-ttu-id="00a69-830">X</span><span class="sxs-lookup"><span data-stu-id="00a69-830">X</span></span> | <span data-ttu-id="00a69-831">X</span><span class="sxs-lookup"><span data-stu-id="00a69-831">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-832">\_URL de \_ \_ retour Passport \_ de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-832">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="00a69-833">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="00a69-833">**LPVOID**</span></span> | \- | <span data-ttu-id="00a69-834">X</span><span class="sxs-lookup"><span data-stu-id="00a69-834">X</span></span> | <span data-ttu-id="00a69-835">X</span><span class="sxs-lookup"><span data-stu-id="00a69-835">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-836">déconnexion de l’option WINHTTP de \_ \_ Passport \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-836">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="00a69-837">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="00a69-837">**LPVOID**</span></span> | <span data-ttu-id="00a69-838">X</span><span class="sxs-lookup"><span data-stu-id="00a69-838">X</span></span> | \- | \- | <span data-ttu-id="00a69-839">X</span><span class="sxs-lookup"><span data-stu-id="00a69-839">X</span></span> | \- |
| <span data-ttu-id="00a69-840">\_ \_ mot de passe de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-840">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="00a69-841">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="00a69-841">**LPWSTR**</span></span> | \- | <span data-ttu-id="00a69-842">X</span><span class="sxs-lookup"><span data-stu-id="00a69-842">X</span></span> | <span data-ttu-id="00a69-843">X</span><span class="sxs-lookup"><span data-stu-id="00a69-843">X</span></span> | <span data-ttu-id="00a69-844">X</span><span class="sxs-lookup"><span data-stu-id="00a69-844">X</span></span> | \- |
| <span data-ttu-id="00a69-845">\_proxy d’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-845">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="00a69-846">**\_informations sur le proxy WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-846">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="00a69-847">X</span><span class="sxs-lookup"><span data-stu-id="00a69-847">X</span></span> | <span data-ttu-id="00a69-848">X</span><span class="sxs-lookup"><span data-stu-id="00a69-848">X</span></span> | <span data-ttu-id="00a69-849">X</span><span class="sxs-lookup"><span data-stu-id="00a69-849">X</span></span> | <span data-ttu-id="00a69-850">X</span><span class="sxs-lookup"><span data-stu-id="00a69-850">X</span></span> | \- |
| <span data-ttu-id="00a69-851">\_ \_ \_ mot de passe proxy de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-851">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="00a69-852">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="00a69-852">**LPWSTR**</span></span> | \- | <span data-ttu-id="00a69-853">X</span><span class="sxs-lookup"><span data-stu-id="00a69-853">X</span></span> | <span data-ttu-id="00a69-854">X</span><span class="sxs-lookup"><span data-stu-id="00a69-854">X</span></span> | <span data-ttu-id="00a69-855">X</span><span class="sxs-lookup"><span data-stu-id="00a69-855">X</span></span> | \- |
| <span data-ttu-id="00a69-856">nom de principal du proxy de l' \_ option WinHTTP \_ \_ \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="00a69-856">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="00a69-857">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="00a69-857">**LPWSTR**</span></span> | \- | <span data-ttu-id="00a69-858">X</span><span class="sxs-lookup"><span data-stu-id="00a69-858">X</span></span> | <span data-ttu-id="00a69-859">X</span><span class="sxs-lookup"><span data-stu-id="00a69-859">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-860">\_ \_ \_ nom d’utilisateur proxy de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-860">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="00a69-861">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="00a69-861">**LPWSTR**</span></span> | \- | <span data-ttu-id="00a69-862">X</span><span class="sxs-lookup"><span data-stu-id="00a69-862">X</span></span> | <span data-ttu-id="00a69-863">X</span><span class="sxs-lookup"><span data-stu-id="00a69-863">X</span></span> | <span data-ttu-id="00a69-864">X</span><span class="sxs-lookup"><span data-stu-id="00a69-864">X</span></span> | \- |
| <span data-ttu-id="00a69-865">\_taille de \_ la \_ mémoire tampon de lecture de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-865">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="00a69-866">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-866">**DWORD**</span></span> | \- | <span data-ttu-id="00a69-867">X</span><span class="sxs-lookup"><span data-stu-id="00a69-867">X</span></span> | <span data-ttu-id="00a69-868">X</span><span class="sxs-lookup"><span data-stu-id="00a69-868">X</span></span> | <span data-ttu-id="00a69-869">X</span><span class="sxs-lookup"><span data-stu-id="00a69-869">X</span></span> | \- |
| <span data-ttu-id="00a69-870">réponse de la connexion du proxy de réception de l' \_ option WinHTTP \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-870">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="00a69-871">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-871">**BOOL**</span></span> | <span data-ttu-id="00a69-872">X</span><span class="sxs-lookup"><span data-stu-id="00a69-872">X</span></span> | <span data-ttu-id="00a69-873">X</span><span class="sxs-lookup"><span data-stu-id="00a69-873">X</span></span> | \- | <span data-ttu-id="00a69-874">X</span><span class="sxs-lookup"><span data-stu-id="00a69-874">X</span></span> | \- |
| <span data-ttu-id="00a69-875">\_délai de \_ réponse de réception \_ \_ de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-875">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="00a69-876">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-876">**DWORD**</span></span> | <span data-ttu-id="00a69-877">X</span><span class="sxs-lookup"><span data-stu-id="00a69-877">X</span></span> | <span data-ttu-id="00a69-878">X</span><span class="sxs-lookup"><span data-stu-id="00a69-878">X</span></span> | <span data-ttu-id="00a69-879">X</span><span class="sxs-lookup"><span data-stu-id="00a69-879">X</span></span> | <span data-ttu-id="00a69-880">X</span><span class="sxs-lookup"><span data-stu-id="00a69-880">X</span></span> | \- |
| <span data-ttu-id="00a69-881">\_délai de \_ réception des options WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-881">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="00a69-882">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-882">**DWORD**</span></span> | <span data-ttu-id="00a69-883">X</span><span class="sxs-lookup"><span data-stu-id="00a69-883">X</span></span> | <span data-ttu-id="00a69-884">X</span><span class="sxs-lookup"><span data-stu-id="00a69-884">X</span></span> | <span data-ttu-id="00a69-885">X</span><span class="sxs-lookup"><span data-stu-id="00a69-885">X</span></span> | <span data-ttu-id="00a69-886">X</span><span class="sxs-lookup"><span data-stu-id="00a69-886">X</span></span> | \- |
| <span data-ttu-id="00a69-887">\_stratégie de \_ redirection des options WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-887">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="00a69-888">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-888">**DWORD**</span></span> | <span data-ttu-id="00a69-889">X</span><span class="sxs-lookup"><span data-stu-id="00a69-889">X</span></span> | <span data-ttu-id="00a69-890">X</span><span class="sxs-lookup"><span data-stu-id="00a69-890">X</span></span> | <span data-ttu-id="00a69-891">X</span><span class="sxs-lookup"><span data-stu-id="00a69-891">X</span></span> | <span data-ttu-id="00a69-892">X</span><span class="sxs-lookup"><span data-stu-id="00a69-892">X</span></span> | \- |
| <span data-ttu-id="00a69-893">\_option WinHTTP \_ Reject \_ USERPWD \_ dans l' \_ URL</span><span class="sxs-lookup"><span data-stu-id="00a69-893">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="00a69-894">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-894">**BOOL**</span></span> | \- | <span data-ttu-id="00a69-895">X</span><span class="sxs-lookup"><span data-stu-id="00a69-895">X</span></span> | \- | <span data-ttu-id="00a69-896">X</span><span class="sxs-lookup"><span data-stu-id="00a69-896">X</span></span> | \- |
| <span data-ttu-id="00a69-897">priorité des demandes de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-897">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="00a69-898">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-898">**DWORD**</span></span> | \- | <span data-ttu-id="00a69-899">X</span><span class="sxs-lookup"><span data-stu-id="00a69-899">X</span></span> | <span data-ttu-id="00a69-900">X</span><span class="sxs-lookup"><span data-stu-id="00a69-900">X</span></span> | <span data-ttu-id="00a69-901">X</span><span class="sxs-lookup"><span data-stu-id="00a69-901">X</span></span> | \- |
| <span data-ttu-id="00a69-902">\_statistiques des \_ demandes d’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-902">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="00a69-903">**\_statistiques des demandes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-903">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="00a69-904">X</span><span class="sxs-lookup"><span data-stu-id="00a69-904">X</span></span> | <span data-ttu-id="00a69-905">X</span><span class="sxs-lookup"><span data-stu-id="00a69-905">X</span></span> | \- | <span data-ttu-id="00a69-906">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="00a69-906">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="00a69-907">\_ \_ durées de demande de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-907">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="00a69-908">**\_durées des requêtes WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-908">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="00a69-909">X</span><span class="sxs-lookup"><span data-stu-id="00a69-909">X</span></span> | <span data-ttu-id="00a69-910">X</span><span class="sxs-lookup"><span data-stu-id="00a69-910">X</span></span> | \- | <span data-ttu-id="00a69-911">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="00a69-911">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="00a69-912">l' \_ option WinHTTP \_ nécessite une \_ fin de flux \_</span><span class="sxs-lookup"><span data-stu-id="00a69-912">WINHTTP\_OPTION\_REQUIRE\_STREAM\_END</span></span><br/><span data-ttu-id="00a69-913">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-913">**BOOL**</span></span> | <span data-ttu-id="00a69-914">X</span><span class="sxs-lookup"><span data-stu-id="00a69-914">X</span></span> | <span data-ttu-id="00a69-915">X</span><span class="sxs-lookup"><span data-stu-id="00a69-915">X</span></span> | \- | <span data-ttu-id="00a69-916">X</span><span class="sxs-lookup"><span data-stu-id="00a69-916">X</span></span> | <span data-ttu-id="00a69-917">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="00a69-917">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="00a69-918">\_nom d' \_ hôte de résolution de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-918">WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME</span></span><br/><span data-ttu-id="00a69-919">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="00a69-919">**LPWSTR**</span></span> | \- | <span data-ttu-id="00a69-920">X</span><span class="sxs-lookup"><span data-stu-id="00a69-920">X</span></span> | \- | <span data-ttu-id="00a69-921">X</span><span class="sxs-lookup"><span data-stu-id="00a69-921">X</span></span> | <span data-ttu-id="00a69-922">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="00a69-922">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="00a69-923">délai de résolution de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-923">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="00a69-924">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-924">**DWORD**</span></span> | <span data-ttu-id="00a69-925">X</span><span class="sxs-lookup"><span data-stu-id="00a69-925">X</span></span> | <span data-ttu-id="00a69-926">X</span><span class="sxs-lookup"><span data-stu-id="00a69-926">X</span></span> | <span data-ttu-id="00a69-927">X</span><span class="sxs-lookup"><span data-stu-id="00a69-927">X</span></span> | <span data-ttu-id="00a69-928">X</span><span class="sxs-lookup"><span data-stu-id="00a69-928">X</span></span> | \- |
| <span data-ttu-id="00a69-929">\_ \_ protocoles sécurisés option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-929">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="00a69-930">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-930">**DWORD**</span></span> | <span data-ttu-id="00a69-931">X</span><span class="sxs-lookup"><span data-stu-id="00a69-931">X</span></span> | \- | \- | <span data-ttu-id="00a69-932">X</span><span class="sxs-lookup"><span data-stu-id="00a69-932">X</span></span> | \- |
| <span data-ttu-id="00a69-933">\_structure de \_ certificat de sécurité option \_ WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-933">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="00a69-934">**\_informations de certificat WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="00a69-934">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="00a69-935">X</span><span class="sxs-lookup"><span data-stu-id="00a69-935">X</span></span> | <span data-ttu-id="00a69-936">X</span><span class="sxs-lookup"><span data-stu-id="00a69-936">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-937">indicateurs de sécurité de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-937">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="00a69-938">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-938">**DWORD**</span></span> | \- | <span data-ttu-id="00a69-939">X</span><span class="sxs-lookup"><span data-stu-id="00a69-939">X</span></span> | <span data-ttu-id="00a69-940">X</span><span class="sxs-lookup"><span data-stu-id="00a69-940">X</span></span> | <span data-ttu-id="00a69-941">X</span><span class="sxs-lookup"><span data-stu-id="00a69-941">X</span></span> | \- |
| <span data-ttu-id="00a69-942">informations de sécurité de l' \_ option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-942">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="00a69-943">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="00a69-943">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="00a69-944">X</span><span class="sxs-lookup"><span data-stu-id="00a69-944">X</span></span> | <span data-ttu-id="00a69-945">X</span><span class="sxs-lookup"><span data-stu-id="00a69-945">X</span></span> | \- | <span data-ttu-id="00a69-946">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="00a69-946">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="00a69-947">nombre de bits de la clé de sécurité de l' \_ option WinHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-947">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="00a69-948">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-948">**DWORD**</span></span> | \- | <span data-ttu-id="00a69-949">X</span><span class="sxs-lookup"><span data-stu-id="00a69-949">X</span></span> | <span data-ttu-id="00a69-950">X</span><span class="sxs-lookup"><span data-stu-id="00a69-950">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-951">\_ \_ \_ délai d’attente d’envoi des options WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-951">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="00a69-952">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-952">**DWORD**</span></span> | <span data-ttu-id="00a69-953">X</span><span class="sxs-lookup"><span data-stu-id="00a69-953">X</span></span> | <span data-ttu-id="00a69-954">X</span><span class="sxs-lookup"><span data-stu-id="00a69-954">X</span></span> | <span data-ttu-id="00a69-955">X</span><span class="sxs-lookup"><span data-stu-id="00a69-955">X</span></span> | <span data-ttu-id="00a69-956">X</span><span class="sxs-lookup"><span data-stu-id="00a69-956">X</span></span> | \- |
| <span data-ttu-id="00a69-957">\_serveur d’option WinHTTP \_ \_ CBT</span><span class="sxs-lookup"><span data-stu-id="00a69-957">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="00a69-958">[**\_Liaisons SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="00a69-958">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="00a69-959">X</span><span class="sxs-lookup"><span data-stu-id="00a69-959">X</span></span> | <span data-ttu-id="00a69-960">X</span><span class="sxs-lookup"><span data-stu-id="00a69-960">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-961">\_contexte de \_ chaîne du certificat de serveur d’option WinHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-961">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="00a69-962">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="00a69-962">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="00a69-963">X</span><span class="sxs-lookup"><span data-stu-id="00a69-963">X</span></span> | <span data-ttu-id="00a69-964">X</span><span class="sxs-lookup"><span data-stu-id="00a69-964">X</span></span> | \- | <span data-ttu-id="00a69-965">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="00a69-965">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="00a69-966">\_contexte de \_ certificat de serveur d’option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-966">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="00a69-967">**CONTEXTE DU CERTIFICAT**</span><span class="sxs-lookup"><span data-stu-id="00a69-967">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="00a69-968">X</span><span class="sxs-lookup"><span data-stu-id="00a69-968">X</span></span> | <span data-ttu-id="00a69-969">X</span><span class="sxs-lookup"><span data-stu-id="00a69-969">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-970">nom principal de service du \_ serveur option WinHTTP \_ \_ \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="00a69-970">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="00a69-971">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="00a69-971">**LPWSTR**</span></span> | \- | <span data-ttu-id="00a69-972">X</span><span class="sxs-lookup"><span data-stu-id="00a69-972">X</span></span> | <span data-ttu-id="00a69-973">X</span><span class="sxs-lookup"><span data-stu-id="00a69-973">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-974">SPN de l' \_ option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-974">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="00a69-975">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-975">**DWORD**</span></span> | \- | <span data-ttu-id="00a69-976">X</span><span class="sxs-lookup"><span data-stu-id="00a69-976">X</span></span> | \- | <span data-ttu-id="00a69-977">X</span><span class="sxs-lookup"><span data-stu-id="00a69-977">X</span></span> | \- |
| <span data-ttu-id="00a69-978">\_code d' \_ erreur de flux d’options WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-978">WINHTTP\_OPTION\_STREAM\_ERROR\_CODE</span></span><br/><span data-ttu-id="00a69-979">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-979">**DWORD**</span></span> | \- | <span data-ttu-id="00a69-980">X</span><span class="sxs-lookup"><span data-stu-id="00a69-980">X</span></span> | <span data-ttu-id="00a69-981">X</span><span class="sxs-lookup"><span data-stu-id="00a69-981">X</span></span> | \- | <span data-ttu-id="00a69-982">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="00a69-982">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="00a69-983">\_option WinHTTP \_ TCP \_ Fast \_ Open</span><span class="sxs-lookup"><span data-stu-id="00a69-983">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="00a69-984">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-984">**BOOL**</span></span> | <span data-ttu-id="00a69-985">X</span><span class="sxs-lookup"><span data-stu-id="00a69-985">X</span></span> | \- | \- | <span data-ttu-id="00a69-986">X</span><span class="sxs-lookup"><span data-stu-id="00a69-986">X</span></span> | <span data-ttu-id="00a69-987">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="00a69-987">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="00a69-988">\_option WinHTTP \_ TCP \_ KeepAlive</span><span class="sxs-lookup"><span data-stu-id="00a69-988">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="00a69-989">**\_KeepAlive TCP**</span><span class="sxs-lookup"><span data-stu-id="00a69-989">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="00a69-990">X</span><span class="sxs-lookup"><span data-stu-id="00a69-990">X</span></span> | \- | \- | <span data-ttu-id="00a69-991">X</span><span class="sxs-lookup"><span data-stu-id="00a69-991">X</span></span> | <span data-ttu-id="00a69-992">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="00a69-992">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="00a69-993">OPTION WINHTTP-début de la \_ \_ \_ valeur TLS false \_</span><span class="sxs-lookup"><span data-stu-id="00a69-993">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="00a69-994">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-994">**BOOL**</span></span> | <span data-ttu-id="00a69-995">X</span><span class="sxs-lookup"><span data-stu-id="00a69-995">X</span></span> | \- | \- | <span data-ttu-id="00a69-996">X</span><span class="sxs-lookup"><span data-stu-id="00a69-996">X</span></span> | <span data-ttu-id="00a69-997">Windows 10 version 2004</span><span class="sxs-lookup"><span data-stu-id="00a69-997">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="00a69-998">\_option WinHTTP \_ \_ protocole TLS \_ non sécurisé de \_ secours</span><span class="sxs-lookup"><span data-stu-id="00a69-998">WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK</span></span><br/><span data-ttu-id="00a69-999">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-999">**BOOL**</span></span> | <span data-ttu-id="00a69-1000">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1000">X</span></span> | \- | \- | <span data-ttu-id="00a69-1001">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1001">X</span></span> | <span data-ttu-id="00a69-1002">Windows 10 version 21H1</span><span class="sxs-lookup"><span data-stu-id="00a69-1002">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="00a69-1003">\_événement de \_ notification de déchargement d’option WinHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a69-1003">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="00a69-1004">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="00a69-1004">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="00a69-1005">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1005">X</span></span> | \- | \- | <span data-ttu-id="00a69-1006">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1006">X</span></span> | \- |
| <span data-ttu-id="00a69-1007">\_option WinHTTP \_ \_ -analyse d’en-tête non sécurisé \_</span><span class="sxs-lookup"><span data-stu-id="00a69-1007">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="00a69-1008">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-1008">**DWORD**</span></span> | \- | <span data-ttu-id="00a69-1009">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1009">X</span></span> | \- | <span data-ttu-id="00a69-1010">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1010">X</span></span> | \- |
| <span data-ttu-id="00a69-1011">\_option WinHTTP \_ mettre à niveau \_ vers \_ Web \_ Socket</span><span class="sxs-lookup"><span data-stu-id="00a69-1011">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="00a69-1012">N/A</span><span class="sxs-lookup"><span data-stu-id="00a69-1012">N/A</span></span> | \- | <span data-ttu-id="00a69-1013">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1013">X</span></span> | \- | <span data-ttu-id="00a69-1014">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1014">X</span></span> | \- |
| <span data-ttu-id="00a69-1015">URL de l' \_ option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-1015">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="00a69-1016">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="00a69-1016">**LPWSTR**</span></span> | \- | <span data-ttu-id="00a69-1017">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1017">X</span></span> | <span data-ttu-id="00a69-1018">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1018">X</span></span> | \- | \- |
| <span data-ttu-id="00a69-1019">\_option WinHTTP \_ utiliser \_ les \_ \_ informations d’identification du serveur global</span><span class="sxs-lookup"><span data-stu-id="00a69-1019">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="00a69-1020">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00a69-1020">**BOOL**</span></span> | <span data-ttu-id="00a69-1021">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1021">X</span></span> | <span data-ttu-id="00a69-1022">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1022">X</span></span> | \- | <span data-ttu-id="00a69-1023">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1023">X</span></span> | \- |
| <span data-ttu-id="00a69-1024">\_ \_ agent utilisateur de \_ l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-1024">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="00a69-1025">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="00a69-1025">**LPWSTR**</span></span> | <span data-ttu-id="00a69-1026">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1026">X</span></span> | \- | <span data-ttu-id="00a69-1027">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1027">X</span></span> | <span data-ttu-id="00a69-1028">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1028">X</span></span> | \- |
| <span data-ttu-id="00a69-1029">\_option WinHTTP \_ nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="00a69-1029">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="00a69-1030">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="00a69-1030">**LPWSTR**</span></span> | \- | <span data-ttu-id="00a69-1031">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1031">X</span></span> | <span data-ttu-id="00a69-1032">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1032">X</span></span> | <span data-ttu-id="00a69-1033">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1033">X</span></span> | \- |
| <span data-ttu-id="00a69-1034">\_ \_ \_ \_ \_ délai d’attente de fermeture du socket Web de l’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-1034">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="00a69-1035">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-1035">**DWORD**</span></span> | \- | \- | <span data-ttu-id="00a69-1036">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1036">X</span></span> | <span data-ttu-id="00a69-1037">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1037">X</span></span> | \- |
| <span data-ttu-id="00a69-1038">\_intervalle de \_ conservation \_ de \_ conservation de socket Web \_ d’option WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-1038">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="00a69-1039">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-1039">**DWORD**</span></span> | \- | \- | <span data-ttu-id="00a69-1040">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1040">X</span></span> | <span data-ttu-id="00a69-1041">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1041">X</span></span> | \- |
| <span data-ttu-id="00a69-1042">OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon de réception du socket Web \_</span><span class="sxs-lookup"><span data-stu-id="00a69-1042">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="00a69-1043">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-1043">**DWORD**</span></span> | <span data-ttu-id="00a69-1044">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1044">X</span></span> | <span data-ttu-id="00a69-1045">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1045">X</span></span> | <span data-ttu-id="00a69-1046">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1046">X</span></span> | <span data-ttu-id="00a69-1047">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1047">X</span></span> | <span data-ttu-id="00a69-1048">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="00a69-1048">Windows 8.1</span></span> |
| <span data-ttu-id="00a69-1049">OPTION WINHTTP taille de la \_ \_ \_ \_ \_ mémoire tampon d’envoi du socket Web \_</span><span class="sxs-lookup"><span data-stu-id="00a69-1049">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="00a69-1050">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-1050">**DWORD**</span></span> | <span data-ttu-id="00a69-1051">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1051">X</span></span> | <span data-ttu-id="00a69-1052">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1052">X</span></span> | <span data-ttu-id="00a69-1053">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1053">X</span></span> | <span data-ttu-id="00a69-1054">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1054">X</span></span> | <span data-ttu-id="00a69-1055">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="00a69-1055">Windows 8.1</span></span> |
| <span data-ttu-id="00a69-1056">\_nombre de \_ \_ threads de travail option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-1056">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="00a69-1057">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-1057">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="00a69-1058">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1058">X</span></span> | \- |
| <span data-ttu-id="00a69-1059">\_taille de \_ la \_ mémoire tampon d’écriture de l’option WinHTTP \_</span><span class="sxs-lookup"><span data-stu-id="00a69-1059">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="00a69-1060">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="00a69-1060">**DWORD**</span></span> | \- | <span data-ttu-id="00a69-1061">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1061">X</span></span> | <span data-ttu-id="00a69-1062">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1062">X</span></span> | <span data-ttu-id="00a69-1063">X</span><span class="sxs-lookup"><span data-stu-id="00a69-1063">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="00a69-1064">Pour Windows XP et Windows 2000, consultez [Configuration requise](winhttp-start-page.md)pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="00a69-1064">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00a69-1065">Spécifications</span><span class="sxs-lookup"><span data-stu-id="00a69-1065">Requirements</span></span>

| <span data-ttu-id="00a69-1066">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00a69-1066">Requirement</span></span> | <span data-ttu-id="00a69-1067">Valeur</span><span class="sxs-lookup"><span data-stu-id="00a69-1067">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="00a69-1068">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00a69-1068">Minimum supported client</span></span> | <span data-ttu-id="00a69-1069">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00a69-1069">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="00a69-1070">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00a69-1070">Minimum supported server</span></span> | <span data-ttu-id="00a69-1071">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00a69-1071">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="00a69-1072">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="00a69-1072">Redistributable</span></span>          | <span data-ttu-id="00a69-1073">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="00a69-1073">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="00a69-1074">En-tête</span><span class="sxs-lookup"><span data-stu-id="00a69-1074">Header</span></span>                   | <span data-ttu-id="00a69-1075">WinHTTP. h</span><span class="sxs-lookup"><span data-stu-id="00a69-1075">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="00a69-1076">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00a69-1076">See also</span></span>

[<span data-ttu-id="00a69-1077">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="00a69-1077">WinHTTP Versions</span></span>](winhttp-versions.md)
