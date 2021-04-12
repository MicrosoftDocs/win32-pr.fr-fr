---
title: Structures de la version 1,0 de l’API du serveur HTTP
description: Structures de la version 1,0 de l’API du serveur HTTP
ms.assetid: e38f7a05-f966-4853-be3b-5cdbf224719e
keywords:
- Structures de l’API du serveur HTTP
- Structures HTTP, API serveur HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67cdd426bbe9329e089352999acf5c0f79b6f94f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381913"
---
# <a name="http-server-api-version-10-structures"></a><span data-ttu-id="db86f-105">Structures de la version 1,0 de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="db86f-105">HTTP Server API Version 1.0 Structures</span></span>

<span data-ttu-id="db86f-106">L’API du serveur HTTP fournit les structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="db86f-106">The HTTP Server API provides the following structures:</span></span>

-   [<span data-ttu-id="db86f-107">**VERSION de HTTPAPI \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-107">**HTTPAPI\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-httpapi_version)
-   [<span data-ttu-id="db86f-108">**\_plage d’octets http \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-108">**HTTP\_BYTE\_RANGE**</span></span>](/windows/desktop/api/Http/ns-http-http_byte_range)
-   [<span data-ttu-id="db86f-109">**\_stratégie de cache http \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-109">**HTTP\_CACHE\_POLICY**</span></span>](/windows/desktop/api/Http/ns-http-http_cache_policy)
-   [<span data-ttu-id="db86f-110">**\_URL cuite http \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-110">**HTTP\_COOKED\_URL**</span></span>](/windows/desktop/api/Http/ns-http-http_cooked_url)
-   [<span data-ttu-id="db86f-111">**\_segment de données http \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-111">**HTTP\_DATA\_CHUNK**</span></span>](/windows/desktop/api/Http/ns-http-http_data_chunk)
-   [<span data-ttu-id="db86f-112">**\_ \_ en-tête connu http**</span><span class="sxs-lookup"><span data-stu-id="db86f-112">**HTTP\_KNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_known_header)
-   <span data-ttu-id="db86f-113">[**\_requête http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db86f-113">[**HTTP\_REQUEST**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span></span>
-   [<span data-ttu-id="db86f-114">**\_ \_ en-têtes de requête http**</span><span class="sxs-lookup"><span data-stu-id="db86f-114">**HTTP\_REQUEST\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_request_headers)
-   [<span data-ttu-id="db86f-115">**\_réponse http**</span><span class="sxs-lookup"><span data-stu-id="db86f-115">**HTTP\_RESPONSE**</span></span>](http-response.md)
-   [<span data-ttu-id="db86f-116">**\_ \_ en-têtes de réponse http**</span><span class="sxs-lookup"><span data-stu-id="db86f-116">**HTTP\_RESPONSE\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_response_headers)
-   [<span data-ttu-id="db86f-117">**\_paramètre d' \_ \_ écoute IP \_ \_ de la configuration du service http**</span><span class="sxs-lookup"><span data-stu-id="db86f-117">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_param)
-   [<span data-ttu-id="db86f-118">**\_requête d' \_ \_ écoute IP \_ \_ de la configuration du service http**</span><span class="sxs-lookup"><span data-stu-id="db86f-118">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_query)
-   [<span data-ttu-id="db86f-119">**\_ \_ \_ clé SSL de la configuration du service http \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-119">**HTTP\_SERVICE\_CONFIG\_SSL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_key)
-   [<span data-ttu-id="db86f-120">**\_ \_ \_ param SSL de la configuration du service http \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-120">**HTTP\_SERVICE\_CONFIG\_SSL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_param)
-   [<span data-ttu-id="db86f-121">**\_ \_ \_ requête SSL de la configuration du service http \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-121">**HTTP\_SERVICE\_CONFIG\_SSL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_query)
-   [<span data-ttu-id="db86f-122">**\_configuration SSL du service http \_ \_ \_ définie**</span><span class="sxs-lookup"><span data-stu-id="db86f-122">**HTTP\_SERVICE\_CONFIG\_SSL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set)
-   [<span data-ttu-id="db86f-123">**\_ \_ \_ \_ clé SSL SNI \_ de la configuration du service http**</span><span class="sxs-lookup"><span data-stu-id="db86f-123">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_key)
-   [<span data-ttu-id="db86f-124">**\_requête SSL de configuration du service http \_ \_ \_ SNI \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-124">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_query)
-   [<span data-ttu-id="db86f-125">**\_configuration du service http \_ \_ \_ SNI \_ SSL**</span><span class="sxs-lookup"><span data-stu-id="db86f-125">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_set)
-   [<span data-ttu-id="db86f-126">**\_ \_ \_ clé URLACL de la configuration du service http \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-126">**HTTP\_SERVICE\_CONFIG\_URLACL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_key)
-   [<span data-ttu-id="db86f-127">**\_ \_ \_ paramètre URLACL de la configuration du service http \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-127">**HTTP\_SERVICE\_CONFIG\_URLACL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_param)
-   [<span data-ttu-id="db86f-128">**\_ \_ requête URLACL de configuration du service http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-128">**HTTP\_SERVICE\_CONFIG\_URLACL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_query)
-   [<span data-ttu-id="db86f-129">**\_configuration du service http \_ \_ URLACL \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-129">**HTTP\_SERVICE\_CONFIG\_URLACL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set)
-   [<span data-ttu-id="db86f-130">**\_informations de \_ \_ certificat client HTTP SSL \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-130">**HTTP\_SSL\_CLIENT\_CERT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_client_cert_info)
-   [<span data-ttu-id="db86f-131">**\_informations http SSL \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-131">**HTTP\_SSL\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_info)
-   [<span data-ttu-id="db86f-132">**\_adresse de transport http \_**</span><span class="sxs-lookup"><span data-stu-id="db86f-132">**HTTP\_TRANSPORT\_ADDRESS**</span></span>](/windows/desktop/api/Http/ns-http-http_transport_address)
-   [<span data-ttu-id="db86f-133">**\_ \_ en-tête http inconnu**</span><span class="sxs-lookup"><span data-stu-id="db86f-133">**HTTP\_UNKNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_unknown_header)
-   [<span data-ttu-id="db86f-134">**\_version http**</span><span class="sxs-lookup"><span data-stu-id="db86f-134">**HTTP\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-http_version)

## <a name="related-topics"></a><span data-ttu-id="db86f-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db86f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db86f-136">API serveur HTTP version 1,0, fonctions</span><span class="sxs-lookup"><span data-stu-id="db86f-136">HTTP Server API Version 1.0 Functions</span></span>](http-server-api-version-1-0-functions.md)
</dt> </dl>

 

 