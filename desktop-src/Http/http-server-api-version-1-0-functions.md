---
title: API serveur HTTP version 1,0, fonctions
description: L’API du serveur HTTP fournit les fonctions suivantes pour l’écriture d’applications.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- API serveur HTTP version 1,0, fonctions
- Fonctions HTTP, API serveur HTTP version 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050821e40695268d6e3fa2c946d2e8859748db2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197213"
---
# <a name="http-server-api-version-10-functions"></a><span data-ttu-id="78814-105">API serveur HTTP version 1,0, fonctions</span><span class="sxs-lookup"><span data-stu-id="78814-105">HTTP Server API Version 1.0 Functions</span></span>

<span data-ttu-id="78814-106">L’API du serveur HTTP fournit les fonctions suivantes pour l’écriture d’applications.</span><span class="sxs-lookup"><span data-stu-id="78814-106">The HTTP Server API provides the following functions for writing applications.</span></span>

## <a name="general"></a><span data-ttu-id="78814-107">Général</span><span class="sxs-lookup"><span data-stu-id="78814-107">General</span></span>



| <span data-ttu-id="78814-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="78814-108">Function</span></span>                                             | <span data-ttu-id="78814-109">Description</span><span class="sxs-lookup"><span data-stu-id="78814-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78814-110">**HttpCreateHttpHandle**</span><span class="sxs-lookup"><span data-stu-id="78814-110">**HttpCreateHttpHandle**</span></span>](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | <span data-ttu-id="78814-111">Crée une file d’attente de requêtes HTTP et retourne un descripteur à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="78814-111">Creates an HTTP request queue and returns a handle to it.</span></span>                                                                         |
| [<span data-ttu-id="78814-112">**HttpInitialize**</span><span class="sxs-lookup"><span data-stu-id="78814-112">**HttpInitialize**</span></span>](/windows/desktop/api/Http/nf-http-httpinitialize)             | <span data-ttu-id="78814-113">Initialise l’API du serveur HTTP pour une utilisation par le processus appelant.</span><span class="sxs-lookup"><span data-stu-id="78814-113">Initializes the HTTP Server API for use by the calling process.</span></span>                                                                   |
| [<span data-ttu-id="78814-114">**HttpPrepareUrl**</span><span class="sxs-lookup"><span data-stu-id="78814-114">**HttpPrepareUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpprepareurl)             | <span data-ttu-id="78814-115">Analyse, analyse et normalise une URL Unicode ou Punycode non normalisée afin qu’elle soit sûre et valide à utiliser dans d’autres fonctions HTTP.</span><span class="sxs-lookup"><span data-stu-id="78814-115">Parses, analyzes, and normalizes a non-normalized Unicode or punycode URL so it is safe and valid to use in other HTTP functions.</span></span> |
| [<span data-ttu-id="78814-116">**HttpTerminate**</span><span class="sxs-lookup"><span data-stu-id="78814-116">**HttpTerminate**</span></span>](/windows/desktop/api/Http/nf-http-httpterminate)               | <span data-ttu-id="78814-117">Dirige l’API du serveur HTTP pour nettoyer toutes les ressources associées à un processus particulier.</span><span class="sxs-lookup"><span data-stu-id="78814-117">Directs the HTTP Server API to clean up any resources associated with a particular process.</span></span>                                       |



 

## <a name="cache-management"></a><span data-ttu-id="78814-118">Gestion du cache</span><span class="sxs-lookup"><span data-stu-id="78814-118">Cache Management</span></span>



| <span data-ttu-id="78814-119">Fonction</span><span class="sxs-lookup"><span data-stu-id="78814-119">Function</span></span>                                                       | <span data-ttu-id="78814-120">Description</span><span class="sxs-lookup"><span data-stu-id="78814-120">Description</span></span>                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78814-121">**HttpAddFragmentToCache**</span><span class="sxs-lookup"><span data-stu-id="78814-121">**HttpAddFragmentToCache**</span></span>](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | <span data-ttu-id="78814-122">Met en cache un fragment de données afin qu’il puisse être utilisé pour composer une réponse dynamique sans lire à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="78814-122">Caches a data fragment so that it can be used to compose a dynamic response without reading from disk.</span></span> |
| [<span data-ttu-id="78814-123">**HttpFlushResponseCache**</span><span class="sxs-lookup"><span data-stu-id="78814-123">**HttpFlushResponseCache**</span></span>](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | <span data-ttu-id="78814-124">Supprime les fragments mis en cache spécifiés du cache HTTP.</span><span class="sxs-lookup"><span data-stu-id="78814-124">Removes specified cached fragments from the HTTP cache.</span></span>                                                |
| [<span data-ttu-id="78814-125">**HttpReadFragmentFromCache**</span><span class="sxs-lookup"><span data-stu-id="78814-125">**HttpReadFragmentFromCache**</span></span>](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | <span data-ttu-id="78814-126">Récupère un fragment de réponse mis en cache spécifié.</span><span class="sxs-lookup"><span data-stu-id="78814-126">Retrieves a specified cached response fragment.</span></span>                                                        |



 

## <a name="configuration"></a><span data-ttu-id="78814-127">Configuration</span><span class="sxs-lookup"><span data-stu-id="78814-127">Configuration</span></span>



| <span data-ttu-id="78814-128">Fonction</span><span class="sxs-lookup"><span data-stu-id="78814-128">Function</span></span>                                                                 | <span data-ttu-id="78814-129">Description</span><span class="sxs-lookup"><span data-stu-id="78814-129">Description</span></span>                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="78814-130">**HttpDeleteServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="78814-130">**HttpDeleteServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | <span data-ttu-id="78814-131">Supprime les informations spécifiées du magasin de configuration HTTP.</span><span class="sxs-lookup"><span data-stu-id="78814-131">Deletes specified information from the HTTP configuration store.</span></span>  |
| [<span data-ttu-id="78814-132">**HttpQueryServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="78814-132">**HttpQueryServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | <span data-ttu-id="78814-133">Interroge le magasin de configuration HTTP pour obtenir les informations spécifiées.</span><span class="sxs-lookup"><span data-stu-id="78814-133">Queries the HTTP configuration store for specified information.</span></span>   |
| [<span data-ttu-id="78814-134">**HttpSetServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="78814-134">**HttpSetServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | <span data-ttu-id="78814-135">Définit les valeurs spécifiées dans le magasin de configuration de l’API du serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="78814-135">Sets specified values in the HTTP Server API configuration store.</span></span> |



 

## <a name="input-and-output"></a><span data-ttu-id="78814-136">Entrées et sorties</span><span class="sxs-lookup"><span data-stu-id="78814-136">Input and Output</span></span>



| <span data-ttu-id="78814-137">Fonction</span><span class="sxs-lookup"><span data-stu-id="78814-137">Function</span></span>                                                             | <span data-ttu-id="78814-138">Description</span><span class="sxs-lookup"><span data-stu-id="78814-138">Description</span></span>                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="78814-139">**HttpReceiveHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="78814-139">**HttpReceiveHttpRequest**</span></span>](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | <span data-ttu-id="78814-140">Récupère une requête HTTP à partir d’une file d’attente de demandes spécifiée.</span><span class="sxs-lookup"><span data-stu-id="78814-140">Retrieves an HTTP request from a specified request queue.</span></span>      |
| [<span data-ttu-id="78814-141">**HttpReceiveRequestEntityBody**</span><span class="sxs-lookup"><span data-stu-id="78814-141">**HttpReceiveRequestEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | <span data-ttu-id="78814-142">Récupère les données de corps d’entité d’une requête HTTP particulière.</span><span class="sxs-lookup"><span data-stu-id="78814-142">Retrieves entity-body data of a particular HTTP request.</span></span>       |
| [<span data-ttu-id="78814-143">**HttpSendHttpResponse**</span><span class="sxs-lookup"><span data-stu-id="78814-143">**HttpSendHttpResponse**</span></span>](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | <span data-ttu-id="78814-144">Envoie une réponse HTTP pour une requête HTTP particulière.</span><span class="sxs-lookup"><span data-stu-id="78814-144">Sends an HTTP response for a particular HTTP request.</span></span>          |
| [<span data-ttu-id="78814-145">**HttpSendResponseEntityBody**</span><span class="sxs-lookup"><span data-stu-id="78814-145">**HttpSendResponseEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | <span data-ttu-id="78814-146">Envoie des données de corps d’entité d’une réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="78814-146">Sends entity-body data of an HTTP response.</span></span>                    |
| [<span data-ttu-id="78814-147">**HttpWaitForDisconnect**</span><span class="sxs-lookup"><span data-stu-id="78814-147">**HttpWaitForDisconnect**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | <span data-ttu-id="78814-148">Avertit l’application lorsqu’un client HTTP est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="78814-148">Notifies the application when an HTTP client has disconnected.</span></span> |



 

## <a name="ssl"></a><span data-ttu-id="78814-149">SSL</span><span class="sxs-lookup"><span data-stu-id="78814-149">SSL</span></span>



| <span data-ttu-id="78814-150">Fonction</span><span class="sxs-lookup"><span data-stu-id="78814-150">Function</span></span>                                                             | <span data-ttu-id="78814-151">Description</span><span class="sxs-lookup"><span data-stu-id="78814-151">Description</span></span>                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="78814-152">**HttpReceiveClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="78814-152">**HttpReceiveClientCertificate**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | <span data-ttu-id="78814-153">Récupère le certificat client pour une connexion SSL.</span><span class="sxs-lookup"><span data-stu-id="78814-153">Retrieves the client certificate for an SSL connection.</span></span> |



 

## <a name="url-registration"></a><span data-ttu-id="78814-154">Inscription d’URL</span><span class="sxs-lookup"><span data-stu-id="78814-154">URL Registration</span></span>



| <span data-ttu-id="78814-155">Fonction</span><span class="sxs-lookup"><span data-stu-id="78814-155">Function</span></span>                               | <span data-ttu-id="78814-156">Description</span><span class="sxs-lookup"><span data-stu-id="78814-156">Description</span></span>                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78814-157">**HttpAddUrl**</span><span class="sxs-lookup"><span data-stu-id="78814-157">**HttpAddUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurl)       | <span data-ttu-id="78814-158">Inscrit une URL afin que les requêtes HTTP pour celle-ci soient acheminées vers une file d’attente de demandes spécifiée.</span><span class="sxs-lookup"><span data-stu-id="78814-158">Registers a URL so that HTTP requests for it are routed to a specified request queue.</span></span>           |
| [<span data-ttu-id="78814-159">**HttpRemoveUrl**</span><span class="sxs-lookup"><span data-stu-id="78814-159">**HttpRemoveUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurl) | <span data-ttu-id="78814-160">Annule l’inscription d’une URL spécifiée, afin que les demandes pour celle-ci ne soient plus routées vers une file d’attente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="78814-160">Unregisters a specified URL, so that requests for it are no longer routed to a specified queue.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="78814-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78814-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78814-162">Structures de la version 1,0 de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="78814-162">HTTP Server API Version 1.0 Structures</span></span>](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




