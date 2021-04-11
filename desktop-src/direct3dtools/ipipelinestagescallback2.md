---
description: Non utilisé. Anciennement un rappel pour les données d’étapes de pipeline.
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
ms.openlocfilehash: 9d14e080d4381405f32c6def51d8c64d78aaa422
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950080"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span data-ttu-id="ffc94-104"><span id="vspixengine.ipipelinestagescallback2"></span>Interface IPipeLineStagesCallback2</span><span class="sxs-lookup"><span data-stu-id="ffc94-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 interface</span></span>

<span data-ttu-id="ffc94-105">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ffc94-105">Not used.</span></span> <span data-ttu-id="ffc94-106">Anciennement un rappel pour les données d’étapes de pipeline.</span><span class="sxs-lookup"><span data-stu-id="ffc94-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="ffc94-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ffc94-107">Members</span></span>

<span data-ttu-id="ffc94-108">L’interface **IPipeLineStagesCallback2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ffc94-108">The **IPipeLineStagesCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ffc94-109">**IPipeLineStagesCallback2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffc94-109">**IPipeLineStagesCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="ffc94-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ffc94-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ffc94-111"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="ffc94-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ffc94-112">L’interface **IPipeLineStagesCallback2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ffc94-112">The **IPipeLineStagesCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ffc94-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="ffc94-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ffc94-114">Description</span><span class="sxs-lookup"><span data-stu-id="ffc94-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ffc94-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="ffc94-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ffc94-116">Rappel qui avertit l’hôte du nombre de threads et de groupes du nuanceur de calcul dans la requête associée.</span><span class="sxs-lookup"><span data-stu-id="ffc94-116">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ffc94-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="ffc94-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ffc94-118">Rappel qui avertit l’hôte que ThreadData n’est pas disponible pour une étape et un événement de pipeline particuliers.</span><span class="sxs-lookup"><span data-stu-id="ffc94-118">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ffc94-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffc94-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ffc94-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffc94-120">Header</span></span></p></td><td><span data-ttu-id="ffc94-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ffc94-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
