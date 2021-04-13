---
title: Structures de la version 2,0 de l’API du serveur HTTP
description: La version 2,0 de l’API du serveur HTTP fournit les structures suivantes pour l’écriture d’applications
ms.assetid: 5a8e28e9-f85b-4550-929e-53f38eca6a8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5e41016592e16fcf159188cc1ebc760568f807
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379969"
---
# <a name="http-server-api-version-20-structures"></a><span data-ttu-id="57253-103">Structures de la version 2,0 de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="57253-103">HTTP Server API Version 2.0 Structures</span></span>

<span data-ttu-id="57253-104">La version 2,0 de l’API du serveur HTTP fournit les structures suivantes pour l’écriture des applications :</span><span class="sxs-lookup"><span data-stu-id="57253-104">The HTTP Server API version 2.0 provides the following structures for writing applications:</span></span>

-   [<span data-ttu-id="57253-105">**\_ \_ informations sur la limite de bande PASSANTe http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-105">**HTTP\_BANDWIDTH\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)
-   [<span data-ttu-id="57253-106">**\_informations de liaison http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-106">**HTTP\_BINDING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_binding_info)
-   [<span data-ttu-id="57253-107">**\_informations de \_ liaison de canal http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-107">**HTTP\_CHANNEL\_BIND\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_channel_bind_info)
-   [<span data-ttu-id="57253-108">**\_informations de \_ limite de connexion http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-108">**HTTP\_CONNECTION\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_connection_limit_info)
-   [<span data-ttu-id="57253-109">**\_informations de débit http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-109">**HTTP\_FLOWRATE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_flowrate_info)
-   [<span data-ttu-id="57253-110">**\_ \_ informations sur le point de terminaison d’écoute http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-110">**HTTP\_LISTEN\_ENDPOINT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_listen_endpoint_info)
-   [<span data-ttu-id="57253-111">**\_données du journal http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-111">**HTTP\_LOG\_DATA**</span></span>](/windows/desktop/api/Http/ns-http-http_log_data)
-   [<span data-ttu-id="57253-112">**\_données des \_ champs du journal http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-112">**HTTP\_LOG\_FIELDS\_DATA**</span></span>](/windows/desktop/api/Http/ns-http-http_log_fields_data)
-   [<span data-ttu-id="57253-113">**\_informations de journalisation http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-113">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
-   [<span data-ttu-id="57253-114">**HTTP \_ plusieurs \_ \_ en-têtes connus**</span><span class="sxs-lookup"><span data-stu-id="57253-114">**HTTP\_MULTIPLE\_KNOWN\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_multiple_known_headers)
-   [<span data-ttu-id="57253-115">**\_indicateurs de propriété http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-115">**HTTP\_PROPERTY\_FLAGS**</span></span>](/windows/desktop/api/Http/ns-http-http_property_flags)
-   [<span data-ttu-id="57253-116">**\_informations de \_ paramètre \_ QoS http**</span><span class="sxs-lookup"><span data-stu-id="57253-116">**HTTP\_QOS\_SETTING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_qos_setting_info)
-   [<span data-ttu-id="57253-117">**informations d’authentification de la \_ requête HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57253-117">**HTTP\_REQUEST\_AUTH\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_request_auth_info)
-   [<span data-ttu-id="57253-118">**\_État de \_ liaison du canal \_ \_ de la requête http**</span><span class="sxs-lookup"><span data-stu-id="57253-118">**HTTP\_REQUEST\_CHANNEL\_BIND\_STATUS**</span></span>](/windows/desktop/api/Http/ns-http-http_request_channel_bind_status)
-   [<span data-ttu-id="57253-119">**\_informations sur la requête HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="57253-119">**HTTP\_REQUEST\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_request_info)
-   [<span data-ttu-id="57253-120">**\_Requête HTTP \_ v1**</span><span class="sxs-lookup"><span data-stu-id="57253-120">**HTTP\_REQUEST\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_request_v1)
-   [<span data-ttu-id="57253-121">**\_Requête HTTP \_ v2**</span><span class="sxs-lookup"><span data-stu-id="57253-121">**HTTP\_REQUEST\_V2**</span></span>](/windows/desktop/api/Http/ns-http-http_request_v2)
-   [<span data-ttu-id="57253-122">**\_informations de réponse http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-122">**HTTP\_RESPONSE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_response_info)
-   [<span data-ttu-id="57253-123">**\_Réponse http \_ v1**</span><span class="sxs-lookup"><span data-stu-id="57253-123">**HTTP\_RESPONSE\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v1)
-   [<span data-ttu-id="57253-124">**\_Réponse http \_ v2**</span><span class="sxs-lookup"><span data-stu-id="57253-124">**HTTP\_RESPONSE\_V2**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v2)
-   [<span data-ttu-id="57253-125">**\_paramètres de \_ base de l’authentification du serveur http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57253-125">**HTTP\_SERVER\_AUTHENTICATION\_BASIC\_PARAMS**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_basic_params)
-   [<span data-ttu-id="57253-126">**\_paramètres de \_ Résumé de l’authentification du serveur http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57253-126">**HTTP\_SERVER\_AUTHENTICATION\_DIGEST\_PARAMS**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_digest_params)
-   [<span data-ttu-id="57253-127">**\_ \_ informations d’authentification du serveur http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-127">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
-   [<span data-ttu-id="57253-128">**\_ \_ liaison de service http \_ A**</span><span class="sxs-lookup"><span data-stu-id="57253-128">**HTTP\_SERVICE\_BINDING\_A**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_a)
-   [<span data-ttu-id="57253-129">**\_liaison de service http \_ \_ avec**</span><span class="sxs-lookup"><span data-stu-id="57253-129">**HTTP\_SERVICE\_BINDING\_W**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_w)
-   [<span data-ttu-id="57253-130">**\_base de \_ liaison de service http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-130">**HTTP\_SERVICE\_BINDING\_BASE**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_base)
-   [<span data-ttu-id="57253-131">**\_type de \_ liaison de service http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-131">**HTTP\_SERVICE\_BINDING\_TYPE**</span></span>](/windows/desktop/api/Http/ne-http-http_service_binding_type)
-   [<span data-ttu-id="57253-132">**CACHE de la \_ \_ configuration du service http \_ \_ défini**</span><span class="sxs-lookup"><span data-stu-id="57253-132">**HTTP\_SERVICE\_CONFIG\_CACHE\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_cache_set)
-   [<span data-ttu-id="57253-133">**\_ \_ délai d’attente de la configuration du service http \_ \_ défini**</span><span class="sxs-lookup"><span data-stu-id="57253-133">**HTTP\_SERVICE\_CONFIG\_TIMEOUT\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set)
-   [<span data-ttu-id="57253-134">**\_informations d’État http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-134">**HTTP\_STATE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_state_info)
-   [<span data-ttu-id="57253-135">**\_ \_ informations sur la limite du délai d’expiration http \_**</span><span class="sxs-lookup"><span data-stu-id="57253-135">**HTTP\_TIMEOUT\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)

 

 




