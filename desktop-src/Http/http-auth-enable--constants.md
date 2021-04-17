---
title: Constantes HTTP_AUTH_ENABLE_ (http. h)
description: Définir les schémas d’authentification qui peuvent être activés sur un groupe d’URL.
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466790"
---
# <a name="http_auth_enable_-constants"></a><span data-ttu-id="e48f5-103">\_ \_ Constantes d’activation de l’authentification http \_</span><span class="sxs-lookup"><span data-stu-id="e48f5-103">HTTP\_AUTH\_ENABLE\_ Constants</span></span>

<span data-ttu-id="e48f5-104">Les constantes d' **\_ \_ activation** de l’authentification http définissent les schémas d’authentification qui peuvent être activés sur un groupe d’URL.</span><span class="sxs-lookup"><span data-stu-id="e48f5-104">The **HTTP\_AUTH\_ENABLE** constants define authentication schemes that can be enabled on a URL Group.</span></span>

<span data-ttu-id="e48f5-105">Ces constantes sont utilisées dans la structure des [**\_ \_ \_ informations d’authentification du serveur http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) .</span><span class="sxs-lookup"><span data-stu-id="e48f5-105">These constants are used in the [**HTTP\_SERVER\_AUTHENTICATION\_INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="e48f5-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**\_authentification http \_ activée de \_ base**</span><span class="sxs-lookup"><span data-stu-id="e48f5-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP\_AUTH\_ENABLE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e48f5-107">Le schéma d’authentification de base est activé.</span><span class="sxs-lookup"><span data-stu-id="e48f5-107">The Basic authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e48f5-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**Digest d’activation de l' \_ authentification http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e48f5-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP\_AUTH\_ENABLE\_DIGEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e48f5-109">Le schéma d’authentification Digest est activé.</span><span class="sxs-lookup"><span data-stu-id="e48f5-109">The Digest authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e48f5-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**\_authentification http \_ Enable \_ Kerberos**</span><span class="sxs-lookup"><span data-stu-id="e48f5-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP\_AUTH\_ENABLE\_KERBEROS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e48f5-111">Le schéma d’authentification Kerberos est activé.</span><span class="sxs-lookup"><span data-stu-id="e48f5-111">The Kerberos authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e48f5-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP \_ auth \_ ex \_ Flag \_ activer \_ \_ \_ la mise en cache des informations d’identification Kerberos**</span><span class="sxs-lookup"><span data-stu-id="e48f5-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP\_AUTH\_EX\_FLAG\_ENABLE\_KERBEROS\_CREDENTIAL\_CACHING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e48f5-113">La mise en cache des informations d’identification Kerberos est activée.</span><span class="sxs-lookup"><span data-stu-id="e48f5-113">Kerberos credential caching is enabled.</span></span>

<span data-ttu-id="e48f5-114">**Windows Server 2003 et antérieur :** Non disponible.</span><span class="sxs-lookup"><span data-stu-id="e48f5-114">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e48f5-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**\_ \_ \_ \_ \_ informations d’identification de capture d’indicateur http auth ex**</span><span class="sxs-lookup"><span data-stu-id="e48f5-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**HTTP\_AUTH\_EX\_FLAG\_CAPTURE\_CREDENTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e48f5-116">L’API du serveur HTTP capture l’identité de l’appelant et l’utilise pour l’authentification uniquement pour les schémas Negotiate et Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e48f5-116">The HTTP Server API captures the caller identity and uses it for authentication for Negotiate and Kerberos schemes only.</span></span>

<span data-ttu-id="e48f5-117">**Windows Server 2003 et antérieur :** Non disponible.</span><span class="sxs-lookup"><span data-stu-id="e48f5-117">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e48f5-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**\_authentification http \_ activer \_ NTLM**</span><span class="sxs-lookup"><span data-stu-id="e48f5-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP\_AUTH\_ENABLE\_NTLM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e48f5-119">Le schéma d’authentification NTLM est activé.</span><span class="sxs-lookup"><span data-stu-id="e48f5-119">The NTLM authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e48f5-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP \_ auth \_ activer \_ Negotiate**</span><span class="sxs-lookup"><span data-stu-id="e48f5-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP\_AUTH\_ENABLE\_NEGOTIATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e48f5-121">Le schéma d’authentification Negotiate est activé.</span><span class="sxs-lookup"><span data-stu-id="e48f5-121">The Negotiate authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e48f5-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP \_ auth \_ activer \_ tout**</span><span class="sxs-lookup"><span data-stu-id="e48f5-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP\_AUTH\_ENABLE\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e48f5-123">Tous les schémas d’authentification sont activés.</span><span class="sxs-lookup"><span data-stu-id="e48f5-123">All authentication schemes are enabled.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e48f5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e48f5-124">Requirements</span></span>



| <span data-ttu-id="e48f5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e48f5-125">Requirement</span></span> | <span data-ttu-id="e48f5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e48f5-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e48f5-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e48f5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e48f5-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e48f5-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e48f5-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e48f5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e48f5-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e48f5-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e48f5-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="e48f5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e48f5-132"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="e48f5-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e48f5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e48f5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e48f5-134">Constantes de la version 2,0 de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="e48f5-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="e48f5-135">**\_ \_ informations d’authentification du serveur http \_**</span><span class="sxs-lookup"><span data-stu-id="e48f5-135">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[<span data-ttu-id="e48f5-136">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="e48f5-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="e48f5-137">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="e48f5-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="e48f5-138">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="e48f5-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="e48f5-139">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="e48f5-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





