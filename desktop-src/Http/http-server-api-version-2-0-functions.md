---
title: API serveur HTTP version 2,0, fonctions
description: La version 2,0 de l’API du serveur HTTP fournit les fonctions suivantes.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- API serveur HTTP version 2,0, fonctions
- Fonctions HTTP, API serveur HTTP version 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ab885d7fe45ed45d2233bd216b884d1cf9852
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379970"
---
# <a name="http-server-api-version-20-functions"></a><span data-ttu-id="5ae45-105">API serveur HTTP version 2,0, fonctions</span><span class="sxs-lookup"><span data-stu-id="5ae45-105">HTTP Server API Version 2.0 Functions</span></span>

<span data-ttu-id="5ae45-106">La version 2,0 de l’API du serveur HTTP fournit les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ae45-106">The HTTP Server API version 2.0 provides the following functions.</span></span>

## <a name="server-session"></a><span data-ttu-id="5ae45-107">Session serveur</span><span class="sxs-lookup"><span data-stu-id="5ae45-107">Server Session</span></span>



| <span data-ttu-id="5ae45-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="5ae45-108">Function</span></span>                                                                 | <span data-ttu-id="5ae45-109">Description</span><span class="sxs-lookup"><span data-stu-id="5ae45-109">Description</span></span> |
|--------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="5ae45-110">**HttpCloseServerSession**</span><span class="sxs-lookup"><span data-stu-id="5ae45-110">**HttpCloseServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseserversession)                 |             |
| [<span data-ttu-id="5ae45-111">**HttpCreateServerSession**</span><span class="sxs-lookup"><span data-stu-id="5ae45-111">**HttpCreateServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateserversession)               |             |
| [<span data-ttu-id="5ae45-112">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="5ae45-112">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) |             |
| [<span data-ttu-id="5ae45-113">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="5ae45-113">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)     |             |



 

## <a name="url-groups"></a><span data-ttu-id="5ae45-114">Groupes d’URL</span><span class="sxs-lookup"><span data-stu-id="5ae45-114">URL Groups</span></span>



| <span data-ttu-id="5ae45-115">Fonction</span><span class="sxs-lookup"><span data-stu-id="5ae45-115">Function</span></span>                                                       | <span data-ttu-id="5ae45-116">Description</span><span class="sxs-lookup"><span data-stu-id="5ae45-116">Description</span></span> |
|----------------------------------------------------------------|-------------|
| [<span data-ttu-id="5ae45-117">**HttpAddUrlToUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5ae45-117">**HttpAddUrlToUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)           |             |
| [<span data-ttu-id="5ae45-118">**HttpCreateUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5ae45-118">**HttpCreateUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateurlgroup)               |             |
| [<span data-ttu-id="5ae45-119">**HttpCloseUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5ae45-119">**HttpCloseUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseurlgroup)                 |             |
| [<span data-ttu-id="5ae45-120">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="5ae45-120">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) |             |
| [<span data-ttu-id="5ae45-121">**HttpRemoveUrlFromUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5ae45-121">**HttpRemoveUrlFromUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) |             |
| [<span data-ttu-id="5ae45-122">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="5ae45-122">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)     |             |



 

## <a name="request-queue"></a><span data-ttu-id="5ae45-123">File d'attente de requêtes</span><span class="sxs-lookup"><span data-stu-id="5ae45-123">Request Queue</span></span>



| <span data-ttu-id="5ae45-124">Fonction</span><span class="sxs-lookup"><span data-stu-id="5ae45-124">Function</span></span>                                                               | <span data-ttu-id="5ae45-125">Description</span><span class="sxs-lookup"><span data-stu-id="5ae45-125">Description</span></span> |
|------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="5ae45-126">**HttpCloseRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="5ae45-126">**HttpCloseRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcloserequestqueue)                 |             |
| [<span data-ttu-id="5ae45-127">**HttpCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="5ae45-127">**HttpCreateRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue)               |             |
| [<span data-ttu-id="5ae45-128">**HttpQueryRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="5ae45-128">**HttpQueryRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) |             |
| [<span data-ttu-id="5ae45-129">**HttpSetRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="5ae45-129">**HttpSetRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty)     |             |
| [<span data-ttu-id="5ae45-130">**HttpShutdownRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="5ae45-130">**HttpShutdownRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue)           |             |
| [<span data-ttu-id="5ae45-131">**HttpWaitForDemandStart**</span><span class="sxs-lookup"><span data-stu-id="5ae45-131">**HttpWaitForDemandStart**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart)               |             |



 

## <a name="related-topics"></a><span data-ttu-id="5ae45-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ae45-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ae45-133">Structures de la version 2,0 de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="5ae45-133">HTTP Server API Version 2.0 Structures</span></span>](http-server-api-version-2-0-structures.md)
</dt> </dl>

 

 




