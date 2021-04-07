---
description: Il existe plusieurs types de requêtes conçus pour interroger l’état des ressources.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Requêtes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845733"
---
# <a name="queries-direct3d-9"></a><span data-ttu-id="3b925-103">Requêtes (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3b925-103">Queries (Direct3D 9)</span></span>

<span data-ttu-id="3b925-104">Il existe plusieurs types de requêtes conçus pour interroger l’état des ressources.</span><span class="sxs-lookup"><span data-stu-id="3b925-104">There are several types of queries which are designed to query the status of resources.</span></span> <span data-ttu-id="3b925-105">L’état d’une ressource donnée comprend l’état de l’unité de traitement graphique (GPU), l’état du pilote ou l’état d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3b925-105">The status of a given resource includes graphics processing unit (GPU) status, driver status, or runtime status.</span></span> <span data-ttu-id="3b925-106">Pour comprendre la différence entre les différents types de requêtes, vous devez comprendre les États de requête.</span><span class="sxs-lookup"><span data-stu-id="3b925-106">To understand the difference between the different query types, you need to understand the query states.</span></span> <span data-ttu-id="3b925-107">Le diagramme de transition d’état suivant explique chacun des États de requête.</span><span class="sxs-lookup"><span data-stu-id="3b925-107">The following state transition diagram explains each of the query states.</span></span>

![Diagramme montrant les transitions entre les États de requête](images/queries.png)

<span data-ttu-id="3b925-109">Le diagramme montre trois États, chacun défini par des cercles.</span><span class="sxs-lookup"><span data-stu-id="3b925-109">The diagram shows three states, each defined by circles.</span></span> <span data-ttu-id="3b925-110">Chaque ligne pleine est un événement piloté par l’application qui provoque une transition d’État.</span><span class="sxs-lookup"><span data-stu-id="3b925-110">Each of the solid lines are application-driven events that cause a state transition.</span></span> <span data-ttu-id="3b925-111">La ligne en pointillés est un événement piloté par les ressources qui bascule une requête de l’État émis à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="3b925-111">The dashed line is a resource-driven event that switches a query from the issued state to the signaled state.</span></span> <span data-ttu-id="3b925-112">Chacun de ces États a un objectif différent :</span><span class="sxs-lookup"><span data-stu-id="3b925-112">Each of these states has a different purpose:</span></span>

-   <span data-ttu-id="3b925-113">L’état signalé est comme un état inactif.</span><span class="sxs-lookup"><span data-stu-id="3b925-113">The signaled state is like an idle state.</span></span> <span data-ttu-id="3b925-114">L’objet de requête a été généré et attend que l’application émette la requête.</span><span class="sxs-lookup"><span data-stu-id="3b925-114">The query object has been generated and is waiting for the application to issue the query.</span></span> <span data-ttu-id="3b925-115">Une fois qu’une requête est terminée et repassée à l’état signalé, la réponse à la requête peut être récupérée.</span><span class="sxs-lookup"><span data-stu-id="3b925-115">Once a query has completed and transitioned back to the signaled state, the answer to the query can be retrieved.</span></span>
-   <span data-ttu-id="3b925-116">L’état de construction est comme une zone de transit pour une requête.</span><span class="sxs-lookup"><span data-stu-id="3b925-116">The building state is like a staging area for a query.</span></span> <span data-ttu-id="3b925-117">À partir de l’État immeuble, une requête a été émise (en appelant [**D3DISSUE \_ Begin**](d3dissue-begin.md)) mais n’a pas encore été transportée à l’État émis.</span><span class="sxs-lookup"><span data-stu-id="3b925-117">From the building state, a query has been issued (by calling [**D3DISSUE\_BEGIN**](d3dissue-begin.md)) but has not yet transitioned to the issued state.</span></span> <span data-ttu-id="3b925-118">Lorsqu’une application émet une fin de requête (en appelant [**D3DISSUE \_ end**](d3dissue-end.md)), la requête passe à l’État émis.</span><span class="sxs-lookup"><span data-stu-id="3b925-118">When an application issues a query end (by calling [**D3DISSUE\_END**](d3dissue-end.md)), the query transitions to the issued state.</span></span>
-   <span data-ttu-id="3b925-119">L’État émis signifie que la ressource interrogée contrôle la requête.</span><span class="sxs-lookup"><span data-stu-id="3b925-119">The issued state means that the resource being queried has control of the query.</span></span> <span data-ttu-id="3b925-120">Une fois que la ressource a terminé son travail, la ressource fait passer l’ordinateur d’État à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="3b925-120">Once the resource finishes its work, the resource transitions the state machine to the signaled state.</span></span> <span data-ttu-id="3b925-121">Au cours de l’État émis, l’application doit interroger pour détecter la transition vers l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="3b925-121">During the issued state, the application must poll to detect the transition to the signaled state.</span></span> <span data-ttu-id="3b925-122">Une fois la transition vers l’état signalé effectuée, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retourne le résultat de la requête (par le biais d’un argument) à l’application.</span><span class="sxs-lookup"><span data-stu-id="3b925-122">Once the transition to the signaled state occurs, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns the query result (through an argument) to the application.</span></span>

<span data-ttu-id="3b925-123">Le tableau suivant répertorie les types de requêtes disponibles.</span><span class="sxs-lookup"><span data-stu-id="3b925-123">The following table lists the available query types.</span></span>



| <span data-ttu-id="3b925-124">Type de requête</span><span class="sxs-lookup"><span data-stu-id="3b925-124">Query Type</span></span>        | <span data-ttu-id="3b925-125">Événement de problème</span><span class="sxs-lookup"><span data-stu-id="3b925-125">Issue Event</span></span>                                                                      | <span data-ttu-id="3b925-126">Mémoire tampon GetData</span><span class="sxs-lookup"><span data-stu-id="3b925-126">GetData buffer</span></span>                                                              | <span data-ttu-id="3b925-127">Runtime</span><span class="sxs-lookup"><span data-stu-id="3b925-127">Runtime</span></span>      | <span data-ttu-id="3b925-128">Début de requête implicite</span><span class="sxs-lookup"><span data-stu-id="3b925-128">Implicit beginning of query</span></span>                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| <span data-ttu-id="3b925-129">BANDWIDTHTIMINGS</span><span class="sxs-lookup"><span data-stu-id="3b925-129">BANDWIDTHTIMINGS</span></span>  | <span data-ttu-id="3b925-130">[**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="3b925-130">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="3b925-131">**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="3b925-131">**D3DDEVINFO\_D3D9BANDWIDTHTIMINGS**</span></span>](d3ddevinfo-d3d9bandwidthtimings.md) | <span data-ttu-id="3b925-132">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="3b925-132">Retail/Debug</span></span> | <span data-ttu-id="3b925-133">N/A</span><span class="sxs-lookup"><span data-stu-id="3b925-133">N/A</span></span>                                              |
| <span data-ttu-id="3b925-134">CACHEUTILIZATION</span><span class="sxs-lookup"><span data-stu-id="3b925-134">CACHEUTILIZATION</span></span>  | <span data-ttu-id="3b925-135">[**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="3b925-135">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="3b925-136">**D3DDEVINFO \_ D3D9CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="3b925-136">**D3DDEVINFO\_D3D9CACHEUTILIZATION**</span></span>](d3ddevinfo-d3d9cacheutilization.md) | <span data-ttu-id="3b925-137">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="3b925-137">Retail/Debug</span></span> | <span data-ttu-id="3b925-138">N/A</span><span class="sxs-lookup"><span data-stu-id="3b925-138">N/A</span></span>                                              |
| <span data-ttu-id="3b925-139">ÉVÉNEMENT</span><span class="sxs-lookup"><span data-stu-id="3b925-139">EVENT</span></span>             | [<span data-ttu-id="3b925-140">**Fin de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-140">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="3b925-141">BOOL</span><span class="sxs-lookup"><span data-stu-id="3b925-141">BOOL</span></span>                                                                        | <span data-ttu-id="3b925-142">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="3b925-142">Retail/Debug</span></span> | [<span data-ttu-id="3b925-143">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="3b925-143">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="3b925-144">INTERFACETIMINGS</span><span class="sxs-lookup"><span data-stu-id="3b925-144">INTERFACETIMINGS</span></span>  | <span data-ttu-id="3b925-145">[**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="3b925-145">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="3b925-146">**D3DDEVINFO \_ D3D9INTERFACETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="3b925-146">**D3DDEVINFO\_D3D9INTERFACETIMINGS**</span></span>](d3ddevinfo-d3d9interfacetimings.md) | <span data-ttu-id="3b925-147">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="3b925-147">Retail/Debug</span></span> | <span data-ttu-id="3b925-148">N/A</span><span class="sxs-lookup"><span data-stu-id="3b925-148">N/A</span></span>                                              |
| <span data-ttu-id="3b925-149">OCCLUSION</span><span class="sxs-lookup"><span data-stu-id="3b925-149">OCCLUSION</span></span>         | <span data-ttu-id="3b925-150">[**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="3b925-150">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="3b925-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="3b925-151">DWORD</span></span>                                                                       | <span data-ttu-id="3b925-152">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="3b925-152">Retail/Debug</span></span> | <span data-ttu-id="3b925-153">N/A</span><span class="sxs-lookup"><span data-stu-id="3b925-153">N/A</span></span>                                              |
| <span data-ttu-id="3b925-154">PIPELINETIMINGS</span><span class="sxs-lookup"><span data-stu-id="3b925-154">PIPELINETIMINGS</span></span>   | <span data-ttu-id="3b925-155">[**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="3b925-155">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="3b925-156">**D3DDEVINFO \_ D3D9PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="3b925-156">**D3DDEVINFO\_D3D9PIPELINETIMINGS**</span></span>](d3ddevinfo-d3d9pipelinetimings.md)   | <span data-ttu-id="3b925-157">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="3b925-157">Retail/Debug</span></span> | <span data-ttu-id="3b925-158">N/A</span><span class="sxs-lookup"><span data-stu-id="3b925-158">N/A</span></span>                                              |
| <span data-ttu-id="3b925-159">RESOURCEMANAGER</span><span class="sxs-lookup"><span data-stu-id="3b925-159">RESOURCEMANAGER</span></span>   | [<span data-ttu-id="3b925-160">**Fin de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-160">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="3b925-161">**D3DDEVINFO \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="3b925-161">**D3DDEVINFO\_ResourceManager**</span></span>](d3ddevinfo-resourcemanager.md)           | <span data-ttu-id="3b925-162">Déboguer uniquement</span><span class="sxs-lookup"><span data-stu-id="3b925-162">Debug only</span></span>   | [<span data-ttu-id="3b925-163">**Présent**</span><span class="sxs-lookup"><span data-stu-id="3b925-163">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="3b925-164">timestamp</span><span class="sxs-lookup"><span data-stu-id="3b925-164">TIMESTAMP</span></span>         | [<span data-ttu-id="3b925-165">**Fin de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-165">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="3b925-166">UINT64</span><span class="sxs-lookup"><span data-stu-id="3b925-166">UINT64</span></span>                                                                      | <span data-ttu-id="3b925-167">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="3b925-167">Retail/Debug</span></span> | <span data-ttu-id="3b925-168">N/A</span><span class="sxs-lookup"><span data-stu-id="3b925-168">N/A</span></span>                                              |
| <span data-ttu-id="3b925-169">TIMESTAMPDISJOINT</span><span class="sxs-lookup"><span data-stu-id="3b925-169">TIMESTAMPDISJOINT</span></span> | <span data-ttu-id="3b925-170">[**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="3b925-170">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="3b925-171">BOOL</span><span class="sxs-lookup"><span data-stu-id="3b925-171">BOOL</span></span>                                                                        | <span data-ttu-id="3b925-172">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="3b925-172">Retail/Debug</span></span> | <span data-ttu-id="3b925-173">N/A</span><span class="sxs-lookup"><span data-stu-id="3b925-173">N/A</span></span>                                              |
| <span data-ttu-id="3b925-174">TIMESTAMPFREQ</span><span class="sxs-lookup"><span data-stu-id="3b925-174">TIMESTAMPFREQ</span></span>     | [<span data-ttu-id="3b925-175">**Fin de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-175">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="3b925-176">UINT64</span><span class="sxs-lookup"><span data-stu-id="3b925-176">UINT64</span></span>                                                                      | <span data-ttu-id="3b925-177">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="3b925-177">Retail/Debug</span></span> | <span data-ttu-id="3b925-178">N/A</span><span class="sxs-lookup"><span data-stu-id="3b925-178">N/A</span></span>                                              |
| <span data-ttu-id="3b925-179">VCACHE</span><span class="sxs-lookup"><span data-stu-id="3b925-179">VCACHE</span></span>            | [<span data-ttu-id="3b925-180">**Fin de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-180">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="3b925-181">**D3DDEVINFO \_ Vcache**</span><span class="sxs-lookup"><span data-stu-id="3b925-181">**D3DDEVINFO\_VCACHE**</span></span>](d3ddevinfo-vcache.md)                             | <span data-ttu-id="3b925-182">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="3b925-182">Retail/Debug</span></span> | [<span data-ttu-id="3b925-183">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="3b925-183">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="3b925-184">VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="3b925-184">VERTEXSTATS</span></span>       | [<span data-ttu-id="3b925-185">**Fin de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-185">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="3b925-186">**D3DDEVINFO \_ D3DVERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="3b925-186">**D3DDEVINFO\_D3DVERTEXSTATS**</span></span>](d3ddevinfo-d3dvertexstats.md)             | <span data-ttu-id="3b925-187">Déboguer uniquement</span><span class="sxs-lookup"><span data-stu-id="3b925-187">Debug only</span></span>   | [<span data-ttu-id="3b925-188">**Présent**</span><span class="sxs-lookup"><span data-stu-id="3b925-188">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="3b925-189">VERTEXTIMINGS</span><span class="sxs-lookup"><span data-stu-id="3b925-189">VERTEXTIMINGS</span></span>     | <span data-ttu-id="3b925-190">[**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="3b925-190">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="3b925-191">**D3DDEVINFO \_ D3D9STAGETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="3b925-191">**D3DDEVINFO\_D3D9STAGETIMINGS**</span></span>](d3ddevinfo-d3d9stagetimings.md)         | <span data-ttu-id="3b925-192">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="3b925-192">Retail/Debug</span></span> | <span data-ttu-id="3b925-193">N/A</span><span class="sxs-lookup"><span data-stu-id="3b925-193">N/A</span></span>                                              |



 

<span data-ttu-id="3b925-194">Certaines des requêtes requièrent un événement de début et de fin, tandis que d’autres requièrent uniquement un événement de fin.</span><span class="sxs-lookup"><span data-stu-id="3b925-194">Some of the queries require a begin and end event, while others only require an end event.</span></span> <span data-ttu-id="3b925-195">Les requêtes qui requièrent uniquement un événement de fin commencent lorsqu’un autre événement implicite se produit (qui est listé dans le tableau).</span><span class="sxs-lookup"><span data-stu-id="3b925-195">The queries that only require an end event begin when another implicit event occurs (which is listed in the table).</span></span> <span data-ttu-id="3b925-196">Toutes les requêtes retournent une réponse, à l’exception de la requête d’événement dont la réponse est toujours **true**.</span><span class="sxs-lookup"><span data-stu-id="3b925-196">All queries return an answer, except the event query whose answer is always **TRUE**.</span></span> <span data-ttu-id="3b925-197">Une application utilise l’état de la requête ou le code de retour de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="3b925-197">An application uses either the state of the query or the return code of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>

## <a name="create-a-query"></a><span data-ttu-id="3b925-198">Créer une requête</span><span class="sxs-lookup"><span data-stu-id="3b925-198">Create a Query</span></span>

<span data-ttu-id="3b925-199">Avant de créer une requête, vous pouvez vérifier si le runtime prend en charge les requêtes en appelant [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) avec un pointeur **null** comme suit :</span><span class="sxs-lookup"><span data-stu-id="3b925-199">Before you create a query, you can check to see if the runtime supports queries by calling [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) with a **NULL** pointer like this:</span></span>


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



<span data-ttu-id="3b925-200">Cette méthode retourne un code de réussite si une requête peut être créée ; Sinon, elle retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3b925-200">This method returns a success code if a query can be created; otherwise it returns an error code.</span></span> <span data-ttu-id="3b925-201">Une fois l’opération [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) effectuée, vous pouvez créer un objet de requête comme suit :</span><span class="sxs-lookup"><span data-stu-id="3b925-201">Once [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) succeeds, you can create a query object like this:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



<span data-ttu-id="3b925-202">Si cet appel a échoué, un objet de requête est créé.</span><span class="sxs-lookup"><span data-stu-id="3b925-202">If this call succeeds, a query object is created.</span></span> <span data-ttu-id="3b925-203">La requête est essentiellement inactive dans l’état signalé (avec une réponse non initialisée) en attente d’émission.</span><span class="sxs-lookup"><span data-stu-id="3b925-203">The query is essentially idle in the signaled state (with an uninitialized answer) waiting to be issued.</span></span> <span data-ttu-id="3b925-204">Lorsque vous avez terminé avec la requête, libérez-la comme n’importe quelle autre interface.</span><span class="sxs-lookup"><span data-stu-id="3b925-204">When you are finished with the query, release it like any other interface.</span></span>

## <a name="issue-a-query"></a><span data-ttu-id="3b925-205">Émettre une requête</span><span class="sxs-lookup"><span data-stu-id="3b925-205">Issue a Query</span></span>

<span data-ttu-id="3b925-206">Une application modifie un état de requête en émettant une requête.</span><span class="sxs-lookup"><span data-stu-id="3b925-206">An application changes a query state by issuing a query.</span></span> <span data-ttu-id="3b925-207">Voici un exemple d’émission d’une requête :</span><span class="sxs-lookup"><span data-stu-id="3b925-207">Here is an example of issuing a query:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



<span data-ttu-id="3b925-208">Une requête dans l’état signalé suit une transition similaire à celle-ci lorsqu’elle est émise :</span><span class="sxs-lookup"><span data-stu-id="3b925-208">A query in the signaled state will transition like this when issued:</span></span>



| <span data-ttu-id="3b925-209">Type de problème</span><span class="sxs-lookup"><span data-stu-id="3b925-209">Issue Type</span></span>                                | <span data-ttu-id="3b925-210">Les transitions de requête vers le.</span><span class="sxs-lookup"><span data-stu-id="3b925-210">Query Transitions to the .</span></span> <span data-ttu-id="3b925-211">.</span><span class="sxs-lookup"><span data-stu-id="3b925-211">.</span></span> <span data-ttu-id="3b925-212">.</span><span class="sxs-lookup"><span data-stu-id="3b925-212">.</span></span> |
|-------------------------------------------|--------------------------------|
| [<span data-ttu-id="3b925-213">**Début de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-213">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="3b925-214">État de création.</span><span class="sxs-lookup"><span data-stu-id="3b925-214">Building state.</span></span>                |
| [<span data-ttu-id="3b925-215">**Fin de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-215">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="3b925-216">État émis.</span><span class="sxs-lookup"><span data-stu-id="3b925-216">Issued state.</span></span>                  |



 

<span data-ttu-id="3b925-217">Une requête dans l’état de génération suit une transition similaire à celle-ci lorsqu’elle est émise :</span><span class="sxs-lookup"><span data-stu-id="3b925-217">A query in the building state will transition like this when issued:</span></span>



| <span data-ttu-id="3b925-218">Type de problème</span><span class="sxs-lookup"><span data-stu-id="3b925-218">Issue Type</span></span>                                | <span data-ttu-id="3b925-219">Les transitions de requête vers le.</span><span class="sxs-lookup"><span data-stu-id="3b925-219">Query Transitions to the .</span></span> <span data-ttu-id="3b925-220">.</span><span class="sxs-lookup"><span data-stu-id="3b925-220">.</span></span> <span data-ttu-id="3b925-221">.</span><span class="sxs-lookup"><span data-stu-id="3b925-221">.</span></span>                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="3b925-222">**Début de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-222">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="3b925-223">(Aucune transition, reste dans l’état de construction.</span><span class="sxs-lookup"><span data-stu-id="3b925-223">(No transition, stays in the building state.</span></span> <span data-ttu-id="3b925-224">Redémarre le crochet de requête.)</span><span class="sxs-lookup"><span data-stu-id="3b925-224">Restarts the query bracket.)</span></span> |
| [<span data-ttu-id="3b925-225">**Fin de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-225">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="3b925-226">État émis.</span><span class="sxs-lookup"><span data-stu-id="3b925-226">Issued state.</span></span>                                                             |



 

<span data-ttu-id="3b925-227">Une requête dans l’État émis passera comme suit lorsqu’elle est émise :</span><span class="sxs-lookup"><span data-stu-id="3b925-227">A query in the issued state will transition like this when issued:</span></span>



| <span data-ttu-id="3b925-228">Type de problème</span><span class="sxs-lookup"><span data-stu-id="3b925-228">Issue Type</span></span>                                | <span data-ttu-id="3b925-229">Les transitions de requête vers le.</span><span class="sxs-lookup"><span data-stu-id="3b925-229">Query Transitions to the .</span></span> <span data-ttu-id="3b925-230">.</span><span class="sxs-lookup"><span data-stu-id="3b925-230">.</span></span> <span data-ttu-id="3b925-231">.</span><span class="sxs-lookup"><span data-stu-id="3b925-231">.</span></span>                    |
|-------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="3b925-232">**Début de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-232">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="3b925-233">Génération de l’État et redémarrage du crochet de requête.</span><span class="sxs-lookup"><span data-stu-id="3b925-233">Building state and restarts the query bracket.</span></span>    |
| [<span data-ttu-id="3b925-234">**Fin de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="3b925-234">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="3b925-235">État émis après l’abandon de la requête existante.</span><span class="sxs-lookup"><span data-stu-id="3b925-235">Issued state after abandoning the existing query.</span></span> |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a><span data-ttu-id="3b925-236">Vérifier l’état de la requête et obtenir la réponse à la requête</span><span class="sxs-lookup"><span data-stu-id="3b925-236">Check the Query State and Get the Answer to the Query</span></span>

<span data-ttu-id="3b925-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) effectue deux opérations :</span><span class="sxs-lookup"><span data-stu-id="3b925-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) does two things:</span></span>

1.  <span data-ttu-id="3b925-238">Retourne l’état de requête dans le code de retour.</span><span class="sxs-lookup"><span data-stu-id="3b925-238">Returns the query state in the return code.</span></span>
2.  <span data-ttu-id="3b925-239">Retourne la réponse à la requête dans *pData*.</span><span class="sxs-lookup"><span data-stu-id="3b925-239">Returns the answer to the query in *pData*.</span></span>

<span data-ttu-id="3b925-240">À partir de chacun des trois États de requête, Voici les codes de retour [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) :</span><span class="sxs-lookup"><span data-stu-id="3b925-240">From each of the three query states, here are the [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) return codes:</span></span>



| <span data-ttu-id="3b925-241">État de requête</span><span class="sxs-lookup"><span data-stu-id="3b925-241">Query State</span></span> | <span data-ttu-id="3b925-242">GetData (code de retour)</span><span class="sxs-lookup"><span data-stu-id="3b925-242">GetData return code</span></span> |
|-------------|---------------------|
| <span data-ttu-id="3b925-243">Signalé</span><span class="sxs-lookup"><span data-stu-id="3b925-243">Signaled</span></span>    | <span data-ttu-id="3b925-244">\_OK</span><span class="sxs-lookup"><span data-stu-id="3b925-244">S\_OK</span></span>               |
| <span data-ttu-id="3b925-245">Génération</span><span class="sxs-lookup"><span data-stu-id="3b925-245">Building</span></span>    | <span data-ttu-id="3b925-246">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="3b925-246">Error code</span></span>          |
| <span data-ttu-id="3b925-247">Émis</span><span class="sxs-lookup"><span data-stu-id="3b925-247">Issued</span></span>      | <span data-ttu-id="3b925-248">S \_ false</span><span class="sxs-lookup"><span data-stu-id="3b925-248">S\_FALSE</span></span>            |



 

<span data-ttu-id="3b925-249">Par exemple, lorsqu’une requête est dans l’État émis et que la réponse à la requête n’est pas disponible, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retourne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="3b925-249">For example, when a query is in the issued state and the answer to the query is not available, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns S\_FALSE.</span></span> <span data-ttu-id="3b925-250">Lorsque la ressource termine son travail et que l’application a émis une fin de requête, la ressource fait passer la requête à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="3b925-250">When the resource finishes its work and the application has issued a query end, the resource transitions the query to the signaled state.</span></span> <span data-ttu-id="3b925-251">À partir de l’état signalé, **GetData** retourne \_ « S OK », ce qui signifie que la réponse à la requête est également retournée dans *pData*.</span><span class="sxs-lookup"><span data-stu-id="3b925-251">From the signaled state, **GetData** returns S\_OK which means that the answer to the query is also returned in *pData*.</span></span> <span data-ttu-id="3b925-252">Par exemple, voici la séquence d’événements pour retourner le nombre de pixels dessinés dans une séquence de rendu :</span><span class="sxs-lookup"><span data-stu-id="3b925-252">For instance, here is the sequence of events to return the number of pixels drawn in a render sequence:</span></span>

-   <span data-ttu-id="3b925-253">Création de la requête</span><span class="sxs-lookup"><span data-stu-id="3b925-253">Create the query.</span></span>
-   <span data-ttu-id="3b925-254">Émettez un événement de début.</span><span class="sxs-lookup"><span data-stu-id="3b925-254">Issue a begin event.</span></span>
-   <span data-ttu-id="3b925-255">Dessinez un texte.</span><span class="sxs-lookup"><span data-stu-id="3b925-255">Draw something.</span></span>
-   <span data-ttu-id="3b925-256">Émettez un événement de fin.</span><span class="sxs-lookup"><span data-stu-id="3b925-256">Issue an end event.</span></span>

<span data-ttu-id="3b925-257">Voici la séquence de code correspondante :</span><span class="sxs-lookup"><span data-stu-id="3b925-257">The following is the corresponding sequence of code:</span></span>


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="3b925-258">Ces lignes de code effectuent plusieurs opérations :</span><span class="sxs-lookup"><span data-stu-id="3b925-258">These lines of code do several things:</span></span>

-   <span data-ttu-id="3b925-259">Appelez [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) pour retourner le nombre de pixels dessinés.</span><span class="sxs-lookup"><span data-stu-id="3b925-259">Call [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to return the number of pixels drawn.</span></span>
-   <span data-ttu-id="3b925-260">Spécifiez [**D3DGETDATA \_ flush**](d3dgetdata-flush.md) pour permettre à la ressource de faire passer la requête à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="3b925-260">Specify [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md) to enable the resource to transition the query to the signaled state.</span></span>
-   <span data-ttu-id="3b925-261">Interrogez la ressource de requête en appelant [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) à partir d’une boucle.</span><span class="sxs-lookup"><span data-stu-id="3b925-261">Poll the query resource by calling [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) from a loop.</span></span> <span data-ttu-id="3b925-262">Tant que **GetData** retourne S \_ false, cela signifie que la ressource n’a pas encore retourné la réponse.</span><span class="sxs-lookup"><span data-stu-id="3b925-262">As long as **GetData** returns S\_FALSE, this means the resource has not returned the answer yet.</span></span>

<span data-ttu-id="3b925-263">La valeur de retour de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) vous indique essentiellement l’état de la requête.</span><span class="sxs-lookup"><span data-stu-id="3b925-263">The return value of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) essentially tells you in what state the query is.</span></span> <span data-ttu-id="3b925-264">Les valeurs possibles sont S \_ OK, s \_ false et une erreur.</span><span class="sxs-lookup"><span data-stu-id="3b925-264">Possible values are S\_OK, S\_FALSE, and an error.</span></span> <span data-ttu-id="3b925-265">N’appelez pas **GetData** sur une requête qui se trouve dans l’État Building.</span><span class="sxs-lookup"><span data-stu-id="3b925-265">Do not call **GetData** on a query that is in the building state.</span></span>

-   <span data-ttu-id="3b925-266">S \_ OK signifie que la ressource (GPU ou pilote, ou Runtime) est terminée.</span><span class="sxs-lookup"><span data-stu-id="3b925-266">S\_OK means the resource (GPU or driver, or runtime) is finished.</span></span> <span data-ttu-id="3b925-267">La requête revient à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="3b925-267">The query is returning to the signaled state.</span></span> <span data-ttu-id="3b925-268">La réponse (le cas échéant) est retournée par [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="3b925-268">The answer (if any) is being returned by [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>
-   <span data-ttu-id="3b925-269">S \_ false signifie que la ressource (GPU ou pilote, ou Runtime) ne peut pas encore retourner une réponse.</span><span class="sxs-lookup"><span data-stu-id="3b925-269">S\_FALSE means the resource (GPU or driver, or runtime) cannot return an answer yet.</span></span> <span data-ttu-id="3b925-270">Cela peut être dû au fait que le GPU n’est pas terminé ou n’a pas encore vu le travail.</span><span class="sxs-lookup"><span data-stu-id="3b925-270">This could be because the GPU is not finished or has not seen the work yet.</span></span>
-   <span data-ttu-id="3b925-271">Une erreur signifie que la requête a généré une erreur à partir de laquelle elle ne peut pas être récupérée.</span><span class="sxs-lookup"><span data-stu-id="3b925-271">An error means that the query has generated an error from which it cannot recover.</span></span> <span data-ttu-id="3b925-272">Cela peut être le cas si l’appareil est perdu au cours d’une requête.</span><span class="sxs-lookup"><span data-stu-id="3b925-272">This could be the case if the device is lost during a query.</span></span> <span data-ttu-id="3b925-273">Une fois qu’une requête a généré une erreur (autre que la \_ valeur S false), la requête doit être recréée, ce qui permet de redémarrer la séquence de requête à partir de l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="3b925-273">Once a query has generated an error (other than S\_FALSE), the query must be recreated which will restart the query sequence from the signaled state.</span></span>

<span data-ttu-id="3b925-274">Au lieu de spécifier [**D3DGETDATA \_ flush**](d3dgetdata-flush.md), qui fournit des informations plus récentes, vous pouvez fournir zéro qui est un contrôle plus clair si la requête est dans l’État émis.</span><span class="sxs-lookup"><span data-stu-id="3b925-274">Instead of specifying [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md), which provides more up-to-date information, you could supply zero which is a more light-weight check if the query is in the issued state.</span></span> <span data-ttu-id="3b925-275">Si vous fournissez zéro, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) n’efface pas le tampon de commande.</span><span class="sxs-lookup"><span data-stu-id="3b925-275">Supplying zero will cause [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to not flush the command buffer.</span></span> <span data-ttu-id="3b925-276">Pour cette raison, il faut veiller à éviter les boucles infinate (pour plus d’informations, consultez **GetData** ).</span><span class="sxs-lookup"><span data-stu-id="3b925-276">For this reason, care must be taken to avoid infinate loops (see **GetData** for details).</span></span> <span data-ttu-id="3b925-277">Dans la mesure où le Runtime met en file d’attente le travail dans le tampon de commande, le **\_ vidage D3DGETDATA** est un mécanisme permettant de vider le tampon de commande sur le pilote (et par conséquent, le GPU ; consultez [profilage des appels d’API Direct3D avec précision](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="3b925-277">Since the runtime queues up work in the command buffer, **D3DGETDATA\_FLUSH** is a mechanism for flushing the command buffer to the driver (and hence the GPU; see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="3b925-278">Pendant le vidage de la mémoire tampon de commande, une requête peut passer à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="3b925-278">During the command buffer flush, a query may transition to the signaled state.</span></span>

## <a name="example-an-event-query"></a><span data-ttu-id="3b925-279">Exemple : une requête d’événement</span><span class="sxs-lookup"><span data-stu-id="3b925-279">Example: An Event Query</span></span>

<span data-ttu-id="3b925-280">Une requête d’événement ne prend pas en charge un événement de début.</span><span class="sxs-lookup"><span data-stu-id="3b925-280">An event query does not support a begin event.</span></span>

-   <span data-ttu-id="3b925-281">Création de la requête</span><span class="sxs-lookup"><span data-stu-id="3b925-281">Create the query.</span></span>
-   <span data-ttu-id="3b925-282">Émettez un événement de fin.</span><span class="sxs-lookup"><span data-stu-id="3b925-282">Issue an end event.</span></span>
-   <span data-ttu-id="3b925-283">Interroger jusqu’à ce que le GPU soit inactif.</span><span class="sxs-lookup"><span data-stu-id="3b925-283">Poll until the GPU is idle.</span></span>
-   <span data-ttu-id="3b925-284">Émettez un événement de fin.</span><span class="sxs-lookup"><span data-stu-id="3b925-284">Issue an end event.</span></span>


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="3b925-285">Il s’agit de la séquence de commandes utilisée par une requête d’événement pour profiler les appels de l’interface de programmation d’applications (API) (consultez Profiler [avec précision les appels d’API Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="3b925-285">This is the sequence of commands an event query uses to profile application programming interface (API) calls (see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="3b925-286">Cette séquence utilise des marqueurs pour aider à contrôler la quantité de travail dans le tampon de commande.</span><span class="sxs-lookup"><span data-stu-id="3b925-286">This sequence uses markers to help control the amount of work in the command buffer.</span></span>

<span data-ttu-id="3b925-287">Notez que les applications doivent prêter une attention particulière au grand coût associé au vidage du tampon de commande, car cela amène le système d’exploitation à basculer en mode noyau, ce qui se traduit par une baisse notable des performances.</span><span class="sxs-lookup"><span data-stu-id="3b925-287">Note that applications should pay special attention to the large cost associated with flushing the command buffer because this causes the operating system to switch into kernel mode, thus incurring a sizeable performance penalty.</span></span> <span data-ttu-id="3b925-288">Les applications doivent également être conscientes du gaspillage des cycles processeur en attendant la fin des requêtes.</span><span class="sxs-lookup"><span data-stu-id="3b925-288">Applications should also be aware of wasting CPU cycles by waiting for queries to complete.</span></span>

<span data-ttu-id="3b925-289">Les requêtes sont une optimisation à utiliser pendant le rendu pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="3b925-289">Queries are an optimization to be used during rendering to increase performance.</span></span> <span data-ttu-id="3b925-290">Par conséquent, il n’est pas judicieux de consacrer du temps à attendre la fin d’une requête.</span><span class="sxs-lookup"><span data-stu-id="3b925-290">Therefore, it is not beneficial to spend time waiting for a query to finish.</span></span> <span data-ttu-id="3b925-291">Si une requête est émise et si les résultats ne sont pas encore prêts au moment où l’application les vérifie, la tentative d’optimisation n’a pas été effectuée et le rendu doit se poursuivre normalement.</span><span class="sxs-lookup"><span data-stu-id="3b925-291">If a query is issued and if the results are not yet ready by the time the application checks for them, the attempt at optimizing did not succeed and rendering should continue as normal.</span></span>

<span data-ttu-id="3b925-292">L’exemple classique est l’élimination de l’occlusion.</span><span class="sxs-lookup"><span data-stu-id="3b925-292">The classic example of this is during Occlusion Culling.</span></span> <span data-ttu-id="3b925-293">Au lieu de la boucle **while** ci-dessus, une application utilisant des requêtes peut implémenter l’élimination d’occlusion pour vérifier si une requête s’est terminée au moment où elle a besoin du résultat.</span><span class="sxs-lookup"><span data-stu-id="3b925-293">Instead of the **while** loop above, an application using queries can implement occlusion culling to check to see if a query had finished by the time it needs the result.</span></span> <span data-ttu-id="3b925-294">Si la requête n’est pas terminée, poursuivez (dans le pire des cas) comme si l’objet testé par rapport à n’est pas bloqués (c.-à-d. qu’elle est visible) et qu’elle est rendue.</span><span class="sxs-lookup"><span data-stu-id="3b925-294">If the query has not finished, continue (as a worst-case scenario) as if the object being tested against is not occluded (i.e. it is visible) and render it.</span></span> <span data-ttu-id="3b925-295">Le code doit ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="3b925-295">The code would look similar to the following.</span></span>


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a><span data-ttu-id="3b925-296">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b925-296">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b925-297">Rubriques avancées</span><span class="sxs-lookup"><span data-stu-id="3b925-297">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
