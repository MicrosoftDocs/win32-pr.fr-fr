---
description: 'L’interface IRenderEngine affiche un projet DES services de modification DirectShow (DES) en construisant un graphique de filtre à partir d’une chronologie. DES fournit deux composants qui implémentent cette interface : le moteur de rendu de base crée une sortie non compressée.'
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Interface IRenderEngine (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d8c57e976fac877a02c3f3993fb3fe4d27f9033b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541494"
---
# <a name="irenderengine-interface"></a><span data-ttu-id="2f18f-103">Interface IRenderEngine</span><span class="sxs-lookup"><span data-stu-id="2f18f-103">IRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="2f18f-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="2f18f-104">\[Deprecated.</span></span> <span data-ttu-id="2f18f-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2f18f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2f18f-106">L' `IRenderEngine` interface restitue un projet de [services de modification DirectShow](directshow-editing-services.md) (des) en construisant un graphique de filtre à partir d’une chronologie.</span><span class="sxs-lookup"><span data-stu-id="2f18f-106">The `IRenderEngine` interface renders a [DirectShow Editing Services](directshow-editing-services.md) (DES) project by constructing a filter graph from a timeline.</span></span>

<span data-ttu-id="2f18f-107">DES fournit deux composants qui implémentent cette interface :</span><span class="sxs-lookup"><span data-stu-id="2f18f-107">DES provides two components that implement this interface:</span></span>

-   <span data-ttu-id="2f18f-108">Le *moteur de rendu de base* crée une sortie non compressée.</span><span class="sxs-lookup"><span data-stu-id="2f18f-108">The *basic render engine* creates uncompressed output.</span></span> <span data-ttu-id="2f18f-109">Vous pouvez utiliser la sortie pour l’aperçu ou l’acheminer via des filtres de compression et l’écrire dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="2f18f-109">You can use the output for preview, or route it through compression filters and write it to a file.</span></span>
-   <span data-ttu-id="2f18f-110">Le *moteur de rendu intelligent* crée une sortie compressée à l’aide de la *recompression intelligente*.</span><span class="sxs-lookup"><span data-stu-id="2f18f-110">The *smart render engine* creates compressed output, using *smart recompression*.</span></span> <span data-ttu-id="2f18f-111">Avec la recompression intelligente, un fichier source est recompressé uniquement si son format diffère du format de sortie.</span><span class="sxs-lookup"><span data-stu-id="2f18f-111">With smart recompression, a source file is recompressed only if its format differs from the output format.</span></span> <span data-ttu-id="2f18f-112">Une source avec un format correspondant est écrite directement dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="2f18f-112">A source with a matching format is written directly to the output file.</span></span> <span data-ttu-id="2f18f-113">Selon le scénario, la recompression intelligente peut améliorer beaucoup le temps de rendu.</span><span class="sxs-lookup"><span data-stu-id="2f18f-113">Depending on the scenario, smart recompression can greatly improve rendering time.</span></span>

<span data-ttu-id="2f18f-114">Le moteur de rendu intelligent prend également en charge l’interface [**ISmartRenderEngine**](ismartrenderengine.md) .</span><span class="sxs-lookup"><span data-stu-id="2f18f-114">The smart render engine also supports the [**ISmartRenderEngine**](ismartrenderengine.md) interface.</span></span>

<span data-ttu-id="2f18f-115">Bien qu’une application puisse créer un graphique de filtre et la passer à un moteur de rendu, le scénario classique consiste à ce que le moteur de rendu crée le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="2f18f-115">Although an application can create a filter graph and pass it to a render engine, the typical scenario is for the render engine to create the filter graph.</span></span> <span data-ttu-id="2f18f-116">La création du graphique est un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="2f18f-116">Building the graph is a two-stage process.</span></span> <span data-ttu-id="2f18f-117">Tout d’abord, générez le serveur frontal en appelant la méthode [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="2f18f-117">First, build the front end by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="2f18f-118">Connectez ensuite les broches de sortie du serveur frontal aux filtres de rendu souhaités :</span><span class="sxs-lookup"><span data-stu-id="2f18f-118">Then connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="2f18f-119">Convertisseurs vidéo et audio pour la version préliminaire, ou</span><span class="sxs-lookup"><span data-stu-id="2f18f-119">Video and audio renderers for preview, or</span></span>
-   <span data-ttu-id="2f18f-120">Compresseurs, multiplexeurs et Writers de fichiers pour générer la sortie finale.</span><span class="sxs-lookup"><span data-stu-id="2f18f-120">Compressors, multiplexers, and file writers to generate the final output.</span></span>

## <a name="members"></a><span data-ttu-id="2f18f-121">Membres</span><span class="sxs-lookup"><span data-stu-id="2f18f-121">Members</span></span>

<span data-ttu-id="2f18f-122">L’interface **IRenderEngine** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2f18f-122">The **IRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2f18f-123">**IRenderEngine** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2f18f-123">**IRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="2f18f-124">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f18f-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2f18f-125">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f18f-125">Methods</span></span>

<span data-ttu-id="2f18f-126">L’interface **IRenderEngine** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2f18f-126">The **IRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="2f18f-127">Méthode</span><span class="sxs-lookup"><span data-stu-id="2f18f-127">Method</span></span>                                                                             | <span data-ttu-id="2f18f-128">Description</span><span class="sxs-lookup"><span data-stu-id="2f18f-128">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f18f-129">**Valider**</span><span class="sxs-lookup"><span data-stu-id="2f18f-129">**Commit**</span></span>](irenderengine-commit.md)                                             | <span data-ttu-id="2f18f-130">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="2f18f-130">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="2f18f-131">**ConnectFrontEnd**</span><span class="sxs-lookup"><span data-stu-id="2f18f-131">**ConnectFrontEnd**</span></span>](irenderengine-connectfrontend.md)                           | <span data-ttu-id="2f18f-132">Génère la partie frontale du graphique de filtre à partir de la chronologie actuelle.</span><span class="sxs-lookup"><span data-stu-id="2f18f-132">Builds the front end of the filter graph from the current timeline.</span></span><br/>        |
| [<span data-ttu-id="2f18f-133">**Annulation**</span><span class="sxs-lookup"><span data-stu-id="2f18f-133">**Decommit**</span></span>](irenderengine-decommit.md)                                         | <span data-ttu-id="2f18f-134">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="2f18f-134">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="2f18f-135">**DoSmartRecompression**</span><span class="sxs-lookup"><span data-stu-id="2f18f-135">**DoSmartRecompression**</span></span>](irenderengine-dosmartrecompression.md)                 | <span data-ttu-id="2f18f-136">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2f18f-136">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="2f18f-137">**GetCaps**</span><span class="sxs-lookup"><span data-stu-id="2f18f-137">**GetCaps**</span></span>](irenderengine-getcaps.md)                                           | <span data-ttu-id="2f18f-138">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="2f18f-138">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="2f18f-139">**GetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="2f18f-139">**GetFilterGraph**</span></span>](irenderengine-getfiltergraph.md)                             | <span data-ttu-id="2f18f-140">Récupère le graphique de filtre que le moteur de rendu a construit, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2f18f-140">Retrieves the filter graph that the render engine has constructed, if any.</span></span><br/> |
| [<span data-ttu-id="2f18f-141">**GetGroupOutputPin**</span><span class="sxs-lookup"><span data-stu-id="2f18f-141">**GetGroupOutputPin**</span></span>](irenderengine-getgroupoutputpin.md)                       | <span data-ttu-id="2f18f-142">Récupère la broche de sortie pour le groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="2f18f-142">Retrieves the output pin for the specified group.</span></span><br/>                          |
| [<span data-ttu-id="2f18f-143">**GetTimelineObject**</span><span class="sxs-lookup"><span data-stu-id="2f18f-143">**GetTimelineObject**</span></span>](irenderengine-gettimelineobject.md)                       | <span data-ttu-id="2f18f-144">Récupère la chronologie que le moteur de rendu utilise actuellement.</span><span class="sxs-lookup"><span data-stu-id="2f18f-144">Retrieves the timeline that the render engine is currently using.</span></span><br/>          |
| [<span data-ttu-id="2f18f-145">**GetVendorString**</span><span class="sxs-lookup"><span data-stu-id="2f18f-145">**GetVendorString**</span></span>](irenderengine-getvendorstring.md)                           | <span data-ttu-id="2f18f-146">Récupère la chaîne du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2f18f-146">Retrieves the vendor string.</span></span><br/>                                               |
| [<span data-ttu-id="2f18f-147">**RenderOutputPins**</span><span class="sxs-lookup"><span data-stu-id="2f18f-147">**RenderOutputPins**</span></span>](irenderengine-renderoutputpins.md)                         | <span data-ttu-id="2f18f-148">Crée la partie aperçu du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="2f18f-148">Creates the previewing portion of the filter graph.</span></span><br/>                        |
| [<span data-ttu-id="2f18f-149">**ScrapIt**</span><span class="sxs-lookup"><span data-stu-id="2f18f-149">**ScrapIt**</span></span>](irenderengine-scrapit.md)                                           | <span data-ttu-id="2f18f-150">Ignore le graphique de filtre du moteur de rendu et tous les objets associés.</span><span class="sxs-lookup"><span data-stu-id="2f18f-150">Discards the render engine's filter graph and all associated objects.</span></span><br/>      |
| [<span data-ttu-id="2f18f-151">**SetDynamicReconnectLevel**</span><span class="sxs-lookup"><span data-stu-id="2f18f-151">**SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)         | <span data-ttu-id="2f18f-152">Définit le niveau de reconnexion dynamique lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="2f18f-152">Sets the level of dynamic reconnection during rendering.</span></span><br/>                   |
| [<span data-ttu-id="2f18f-153">**SetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="2f18f-153">**SetFilterGraph**</span></span>](irenderengine-setfiltergraph.md)                             | <span data-ttu-id="2f18f-154">Spécifie un graphique de filtre que le moteur de rendu doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="2f18f-154">Specifies a filter graph for the render engine to use.</span></span><br/>                     |
| [<span data-ttu-id="2f18f-155">**SetInterestRange**</span><span class="sxs-lookup"><span data-stu-id="2f18f-155">**SetInterestRange**</span></span>](irenderengine-setinterestrange.md)                         | <span data-ttu-id="2f18f-156">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2f18f-156">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="2f18f-157">**SetInterestRange2**</span><span class="sxs-lookup"><span data-stu-id="2f18f-157">**SetInterestRange2**</span></span>](irenderengine-setinterestrange2.md)                       | <span data-ttu-id="2f18f-158">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2f18f-158">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="2f18f-159">**SetRenderRange**</span><span class="sxs-lookup"><span data-stu-id="2f18f-159">**SetRenderRange**</span></span>](irenderengine-setrenderrange.md)                             | <span data-ttu-id="2f18f-160">Définit la plage de temps à restituer.</span><span class="sxs-lookup"><span data-stu-id="2f18f-160">Sets the range of time to be rendered.</span></span><br/>                                     |
| [<span data-ttu-id="2f18f-161">**SetRenderRange2**</span><span class="sxs-lookup"><span data-stu-id="2f18f-161">**SetRenderRange2**</span></span>](irenderengine-setrenderrange2.md)                           | <span data-ttu-id="2f18f-162">Définit la plage de temps à restituer, sous la forme d’un **double**.</span><span class="sxs-lookup"><span data-stu-id="2f18f-162">Sets the range of time to be rendered, as a **double**.</span></span><br/>                    |
| [<span data-ttu-id="2f18f-163">**SetSourceConnectCallback**</span><span class="sxs-lookup"><span data-stu-id="2f18f-163">**SetSourceConnectCallback**</span></span>](irenderengine-setsourceconnectcallback.md)         | <span data-ttu-id="2f18f-164">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2f18f-164">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="2f18f-165">**SetSourceNameValidation**</span><span class="sxs-lookup"><span data-stu-id="2f18f-165">**SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)           | <span data-ttu-id="2f18f-166">Spécifie comment le moteur de rendu valide les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2f18f-166">Specifies how the render engine validates file names.</span></span><br/>                      |
| [<span data-ttu-id="2f18f-167">**SetTimelineObject**</span><span class="sxs-lookup"><span data-stu-id="2f18f-167">**SetTimelineObject**</span></span>](irenderengine-settimelineobject.md)                       | <span data-ttu-id="2f18f-168">Définit la chronologie que le moteur de rendu utilise.</span><span class="sxs-lookup"><span data-stu-id="2f18f-168">Sets the timeline for the render engine to use.</span></span><br/>                            |
| [<span data-ttu-id="2f18f-169">**UseInSmartRecompressionGraph**</span><span class="sxs-lookup"><span data-stu-id="2f18f-169">**UseInSmartRecompressionGraph**</span></span>](irenderengine-useinsmartrecompressiongraph.md) | <span data-ttu-id="2f18f-170">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2f18f-170">Not supported.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="2f18f-171">Notes</span><span class="sxs-lookup"><span data-stu-id="2f18f-171">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2f18f-172">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="2f18f-172">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2f18f-173">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2f18f-173">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2f18f-174">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2f18f-174">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2f18f-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f18f-175">Requirements</span></span>



| <span data-ttu-id="2f18f-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f18f-176">Requirement</span></span> | <span data-ttu-id="2f18f-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f18f-177">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f18f-178">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f18f-178">Header</span></span><br/>  | <dl> <span data-ttu-id="2f18f-179"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f18f-179"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2f18f-180">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f18f-180">Library</span></span><br/> | <dl> <span data-ttu-id="2f18f-181"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f18f-181"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f18f-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f18f-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f18f-183">Rendu d’un projet</span><span class="sxs-lookup"><span data-stu-id="2f18f-183">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
