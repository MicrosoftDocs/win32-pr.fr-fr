---
title: API serveur HTTP version 2,0, fonctions
description: La version 2,0 de l’API du serveur HTTP fournit les fonctions suivantes.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- API serveur HTTP version 2,0, fonctions
- Fonctions HTTP, API serveur HTTP version 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e4d5c09c001caa58d43c1e61d800f66b39706b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549074"
---
# <a name="http-server-api-version-20-functions"></a><span data-ttu-id="fe54c-105">API serveur HTTP version 2,0, fonctions</span><span class="sxs-lookup"><span data-stu-id="fe54c-105">HTTP Server API version 2.0 functions</span></span>

<span data-ttu-id="fe54c-106">La version 2,0 de l’API du serveur HTTP fournit les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="fe54c-106">The HTTP Server API version 2.0 provides the following functions.</span></span>

| <span data-ttu-id="fe54c-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="fe54c-107">Function</span></span> | <span data-ttu-id="fe54c-108">Description</span><span class="sxs-lookup"><span data-stu-id="fe54c-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="fe54c-109">**HttpDelegateRequestEx**</span><span class="sxs-lookup"><span data-stu-id="fe54c-109">**HttpDelegateRequestEx**</span></span>](/windows/win32/api/http/nf-http-httpdelegaterequestex) | <span data-ttu-id="fe54c-110">Délègue une requête de la file d’attente de demandes source à la file d’attente de demandes cible.</span><span class="sxs-lookup"><span data-stu-id="fe54c-110">Delegates a request from the source request queue to the target request queue.</span></span> |
| [<span data-ttu-id="fe54c-111">**HttpFindUrlGroupId**</span><span class="sxs-lookup"><span data-stu-id="fe54c-111">**HttpFindUrlGroupId**</span></span>](/windows/win32/api/http/nf-http-httpfindurlgroupid) | <span data-ttu-id="fe54c-112">Récupère un ID de groupe d’URL pour une URL et une file d’attente de demandes.</span><span class="sxs-lookup"><span data-stu-id="fe54c-112">Retrieves a URL group ID for a URL and a request queue.</span></span> |
| [<span data-ttu-id="fe54c-113">**HttpIsFeatureSupported**</span><span class="sxs-lookup"><span data-stu-id="fe54c-113">**HttpIsFeatureSupported**</span></span>](/windows/win32/api/http/nf-http-httpisfeaturesupported) | <span data-ttu-id="fe54c-114">Vérifie si une fonctionnalité particulière est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fe54c-114">Checks whether a particular feature is supported.</span></span> |

## <a name="server-session"></a><span data-ttu-id="fe54c-115">Session serveur</span><span class="sxs-lookup"><span data-stu-id="fe54c-115">Server session</span></span>

| <span data-ttu-id="fe54c-116">Fonction</span><span class="sxs-lookup"><span data-stu-id="fe54c-116">Function</span></span> | <span data-ttu-id="fe54c-117">Description</span><span class="sxs-lookup"><span data-stu-id="fe54c-117">Description</span></span> |
|-|-|
| [<span data-ttu-id="fe54c-118">**HttpCloseServerSession**</span><span class="sxs-lookup"><span data-stu-id="fe54c-118">**HttpCloseServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [<span data-ttu-id="fe54c-119">**HttpCreateServerSession**</span><span class="sxs-lookup"><span data-stu-id="fe54c-119">**HttpCreateServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [<span data-ttu-id="fe54c-120">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="fe54c-120">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [<span data-ttu-id="fe54c-121">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="fe54c-121">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a><span data-ttu-id="fe54c-122">Groupes d’URL</span><span class="sxs-lookup"><span data-stu-id="fe54c-122">URL Groups</span></span>

| <span data-ttu-id="fe54c-123">Fonction</span><span class="sxs-lookup"><span data-stu-id="fe54c-123">Function</span></span> | <span data-ttu-id="fe54c-124">Description</span><span class="sxs-lookup"><span data-stu-id="fe54c-124">Description</span></span> |
|-|-|
| [<span data-ttu-id="fe54c-125">**HttpAddUrlToUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="fe54c-125">**HttpAddUrlToUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [<span data-ttu-id="fe54c-126">**HttpCreateUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="fe54c-126">**HttpCreateUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [<span data-ttu-id="fe54c-127">**HttpCloseUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="fe54c-127">**HttpCloseUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [<span data-ttu-id="fe54c-128">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="fe54c-128">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [<span data-ttu-id="fe54c-129">**HttpRemoveUrlFromUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="fe54c-129">**HttpRemoveUrlFromUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [<span data-ttu-id="fe54c-130">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="fe54c-130">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a><span data-ttu-id="fe54c-131">File d'attente de requêtes</span><span class="sxs-lookup"><span data-stu-id="fe54c-131">Request Queue</span></span>

| <span data-ttu-id="fe54c-132">Fonction</span><span class="sxs-lookup"><span data-stu-id="fe54c-132">Function</span></span> | <span data-ttu-id="fe54c-133">Description</span><span class="sxs-lookup"><span data-stu-id="fe54c-133">Description</span></span> |
|-|-|
| [<span data-ttu-id="fe54c-134">**HttpCloseRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="fe54c-134">**HttpCloseRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [<span data-ttu-id="fe54c-135">**HttpCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="fe54c-135">**HttpCreateRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [<span data-ttu-id="fe54c-136">**HttpQueryRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="fe54c-136">**HttpQueryRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [<span data-ttu-id="fe54c-137">**HttpSetRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="fe54c-137">**HttpSetRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [<span data-ttu-id="fe54c-138">**HttpShutdownRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="fe54c-138">**HttpShutdownRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [<span data-ttu-id="fe54c-139">**HttpWaitForDemandStart**</span><span class="sxs-lookup"><span data-stu-id="fe54c-139">**HttpWaitForDemandStart**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a><span data-ttu-id="fe54c-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe54c-140">Related topics</span></span>

[<span data-ttu-id="fe54c-141">Structures de la version 2,0 de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="fe54c-141">HTTP Server API version 2.0 structures</span></span>](http-server-api-version-2-0-structures.md)
