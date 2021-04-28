---
description: <span id="vspixengine.ipipelinestagescallback2"></span>Interface IPipeLineStagesCallback2-non utilisée. Anciennement un rappel pour les données d’étapes de pipeline.
MS-HAID: vspixengine.IPipeLineStagesCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPipeLineStagesCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C27F94D2-D038-4D4E-9445-D0FF4C17F769
api_name:
- IPipeLineStagesCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 941a056a5c2af00cfa1bb53f038cbeb923a777bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097387"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span data-ttu-id="6f50e-104"><span id="vspixengine.ipipelinestagescallback2"></span>Interface IPipeLineStagesCallback2</span><span class="sxs-lookup"><span data-stu-id="6f50e-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 interface</span></span>

<span data-ttu-id="6f50e-105">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="6f50e-105">Not used.</span></span> <span data-ttu-id="6f50e-106">Anciennement un rappel pour les données d’étapes de pipeline.</span><span class="sxs-lookup"><span data-stu-id="6f50e-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="6f50e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6f50e-107">Members</span></span>

<span data-ttu-id="6f50e-108">L’interface **IPipeLineStagesCallback2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6f50e-108">The **IPipeLineStagesCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6f50e-109">**IPipeLineStagesCallback2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6f50e-109">**IPipeLineStagesCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="6f50e-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f50e-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="6f50e-111"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f50e-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="6f50e-112">L’interface **IPipeLineStagesCallback2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6f50e-112">The **IPipeLineStagesCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="6f50e-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="6f50e-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="6f50e-114">Description</span><span class="sxs-lookup"><span data-stu-id="6f50e-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="6f50e-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f50e-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6f50e-116">Rappel qui avertit l’hôte du nombre de threads et de groupes du nuanceur de calcul dans la requête associée.</span><span class="sxs-lookup"><span data-stu-id="6f50e-116">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="6f50e-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f50e-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6f50e-118">Rappel qui avertit l’hôte que ThreadData n’est pas disponible pour une étape et un événement de pipeline particuliers.</span><span class="sxs-lookup"><span data-stu-id="6f50e-118">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="6f50e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f50e-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6f50e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f50e-120">Header</span></span></p></td><td><span data-ttu-id="6f50e-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6f50e-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
