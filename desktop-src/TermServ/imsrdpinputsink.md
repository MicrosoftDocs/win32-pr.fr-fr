---
title: Interface IMsRdpInputSink
description: Récepteur d’entrée Bureau à distance.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpInputSink
- Services Bureau à distance de l’interface IMsRdpInputSink, Description
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3112b3bb6df92bfb7e403e779773a2203f2cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941876"
---
# <a name="imsrdpinputsink-interface"></a><span data-ttu-id="09ce6-105">Interface IMsRdpInputSink</span><span class="sxs-lookup"><span data-stu-id="09ce6-105">IMsRdpInputSink interface</span></span>

<span data-ttu-id="09ce6-106">Récepteur d’entrée Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="09ce6-106">Remote desktop input sink.</span></span>

## <a name="members"></a><span data-ttu-id="09ce6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="09ce6-107">Members</span></span>

<span data-ttu-id="09ce6-108">L’interface **IMsRdpInputSink** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="09ce6-108">The **IMsRdpInputSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="09ce6-109">**IMsRdpInputSink** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="09ce6-109">**IMsRdpInputSink** also has these types of members:</span></span>

-   [<span data-ttu-id="09ce6-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="09ce6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="09ce6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="09ce6-111">Methods</span></span>

<span data-ttu-id="09ce6-112">L’interface **IMsRdpInputSink** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="09ce6-112">The **IMsRdpInputSink** interface has these methods.</span></span>



| <span data-ttu-id="09ce6-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="09ce6-113">Method</span></span>                                                               | <span data-ttu-id="09ce6-114">Description</span><span class="sxs-lookup"><span data-stu-id="09ce6-114">Description</span></span>                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| <span data-ttu-id="09ce6-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09ce6-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span></span>               | <span data-ttu-id="09ce6-116">Ajoute une entrée tactile.</span><span class="sxs-lookup"><span data-stu-id="09ce6-116">Adds touch input.</span></span><br/>         |
| <span data-ttu-id="09ce6-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09ce6-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span></span>           | <span data-ttu-id="09ce6-118">Commencez le cadre tactile.</span><span class="sxs-lookup"><span data-stu-id="09ce6-118">Begin touch frame.</span></span><br/>        |
| <span data-ttu-id="09ce6-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09ce6-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span></span>               | <span data-ttu-id="09ce6-120">Cadre tactile final.</span><span class="sxs-lookup"><span data-stu-id="09ce6-120">End touch frame.</span></span><br/>          |
| <span data-ttu-id="09ce6-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09ce6-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span></span>       | <span data-ttu-id="09ce6-122">Envoie un événement de clavier.</span><span class="sxs-lookup"><span data-stu-id="09ce6-122">Sends keyboard event.</span></span><br/>     |
| <span data-ttu-id="09ce6-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09ce6-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span></span> | <span data-ttu-id="09ce6-124">Envoie l’événement du bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="09ce6-124">Sends mouse button event.</span></span><br/> |
| <span data-ttu-id="09ce6-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09ce6-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span></span>     | <span data-ttu-id="09ce6-126">Envoie l’événement de déplacement de la souris.</span><span class="sxs-lookup"><span data-stu-id="09ce6-126">Sends mouse move event.</span></span><br/>   |
| <span data-ttu-id="09ce6-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09ce6-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span></span>   | <span data-ttu-id="09ce6-128">Envoie l’événement de roulette de la souris.</span><span class="sxs-lookup"><span data-stu-id="09ce6-128">Sends mouse wheel event.</span></span><br/>  |
| <span data-ttu-id="09ce6-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09ce6-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span></span>               | <span data-ttu-id="09ce6-130">Envoie l’événement de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="09ce6-130">Sends sync event.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="09ce6-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09ce6-131">Requirements</span></span>



| <span data-ttu-id="09ce6-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09ce6-132">Requirement</span></span> | <span data-ttu-id="09ce6-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="09ce6-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09ce6-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09ce6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="09ce6-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="09ce6-135">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="09ce6-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09ce6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="09ce6-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="09ce6-137">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="09ce6-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="09ce6-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="09ce6-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09ce6-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="09ce6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="09ce6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09ce6-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09ce6-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="09ce6-142">IID</span><span class="sxs-lookup"><span data-stu-id="09ce6-142">IID</span></span><br/>                      | <span data-ttu-id="09ce6-143">IID \_ IMsRdpInputSink est défini en tant que 4606850E-76A7-4E28-A47E-C7174F619351</span><span class="sxs-lookup"><span data-stu-id="09ce6-143">IID\_IMsRdpInputSink is defined as 4606850E-76A7-4E28-A47E-C7174F619351</span></span><br/>     |



 

