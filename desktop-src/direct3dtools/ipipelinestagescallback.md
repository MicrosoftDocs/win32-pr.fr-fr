---
description: Non utilisé. Anciennement un rappel pour les données d’étapes de pipeline.
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPipeLineStagesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a00815fc42f4ac7b56e310fafedc0561f40233
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846765"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span data-ttu-id="f19d0-104"><span id="vspixengine.ipipelinestagescallback"></span>Interface IPipeLineStagesCallback</span><span class="sxs-lookup"><span data-stu-id="f19d0-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback interface</span></span>

<span data-ttu-id="f19d0-105">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="f19d0-105">Not used.</span></span> <span data-ttu-id="f19d0-106">Anciennement un rappel pour les données d’étapes de pipeline.</span><span class="sxs-lookup"><span data-stu-id="f19d0-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="f19d0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f19d0-107">Members</span></span>

<span data-ttu-id="f19d0-108">L’interface **IPipeLineStagesCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f19d0-108">The **IPipeLineStagesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f19d0-109">**IPipeLineStagesCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f19d0-109">**IPipeLineStagesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f19d0-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f19d0-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f19d0-111"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="f19d0-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f19d0-112">L’interface **IPipeLineStagesCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f19d0-112">The **IPipeLineStagesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f19d0-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="f19d0-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f19d0-114">Description</span><span class="sxs-lookup"><span data-stu-id="f19d0-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f19d0-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span><span class="sxs-lookup"><span data-stu-id="f19d0-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f19d0-116">Rappel qui avertit l’hôte des étapes de pipeline utilisées par l’appel de dessin de la demande dans.</span><span class="sxs-lookup"><span data-stu-id="f19d0-116">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="f19d0-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f19d0-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f19d0-118">Rappel qui avertit l’hôte des étapes de pipeline qui ne sont pas en mesure de retourner des données de maillage pour l’événement spécifié dans la demande associée.</span><span class="sxs-lookup"><span data-stu-id="f19d0-118">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f19d0-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f19d0-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f19d0-120">Rappel qui avertit l’hôte des informations de maillage des étapes de pipeline retournées par la requête dans.</span><span class="sxs-lookup"><span data-stu-id="f19d0-120">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="f19d0-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f19d0-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f19d0-122">Rappel qui avertit l’hôte des informations d’image des étapes de pipeline retournées par la requête dans.</span><span class="sxs-lookup"><span data-stu-id="f19d0-122">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f19d0-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f19d0-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f19d0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f19d0-124">Header</span></span></p></td><td><span data-ttu-id="f19d0-125">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f19d0-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
