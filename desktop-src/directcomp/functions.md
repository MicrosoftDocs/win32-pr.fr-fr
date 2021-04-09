---
title: DirectComposition, fonctions
description: Cette section décrit les fonctions fournies par Microsoft DirectComposition \ 32 ; MobileVBActiveX.
ms.assetid: 750FDFD5-ADD5-43B3-A596-ECDB82C2EF73
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934e0b7e32f22faaefdf625e0af2a42a03e469d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101816"
---
# <a name="directcomposition-functions"></a><span data-ttu-id="cc1b6-103">DirectComposition, fonctions</span><span class="sxs-lookup"><span data-stu-id="cc1b6-103">DirectComposition functions</span></span>

<span data-ttu-id="cc1b6-104">Cette section décrit les fonctions fournies par l’API Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="cc1b6-104">This section describes the functions provided by the Microsoft DirectComposition API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cc1b6-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="cc1b6-105">In this section</span></span>



| <span data-ttu-id="cc1b6-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="cc1b6-106">Topic</span></span>                                                                                       | <span data-ttu-id="cc1b6-107">Description</span><span class="sxs-lookup"><span data-stu-id="cc1b6-107">Description</span></span>                                                                                                                                          |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc1b6-108">**DCompositionAttachMouseDragToHwnd**</span><span class="sxs-lookup"><span data-stu-id="cc1b6-108">**DCompositionAttachMouseDragToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousedragtohwnd)<br/>   | <span data-ttu-id="cc1b6-109">Crée une interaction/InputSink pour router le bouton de la souris vers le haut et tous les événements de déplacement et de déplacement ultérieurs vers le HWND donné.</span><span class="sxs-lookup"><span data-stu-id="cc1b6-109">Creates an Interaction/InputSink to route mouse button down and any subsequent move and up events to the given HWND.</span></span><br/>                      |
| [<span data-ttu-id="cc1b6-110">**DCompositionAttachMouseWheelToHwnd**</span><span class="sxs-lookup"><span data-stu-id="cc1b6-110">**DCompositionAttachMouseWheelToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousewheeltohwnd)<br/> | <span data-ttu-id="cc1b6-111">Crée une interaction/InputSink pour acheminer les messages de roulette de la souris vers le HWND donné.</span><span class="sxs-lookup"><span data-stu-id="cc1b6-111">Creates an Interaction/InputSink to route mouse wheel messages to the given HWND.</span></span> <br/>                                                        |
| [<span data-ttu-id="cc1b6-112">**DCompositionCreateDevice**</span><span class="sxs-lookup"><span data-stu-id="cc1b6-112">**DCompositionCreateDevice**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice)<br/>                     | <span data-ttu-id="cc1b6-113">Crée un nouvel objet d’appareil qui peut être utilisé pour créer d’autres objets DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="cc1b6-113">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="cc1b6-114">**DCompositionCreateDevice2**</span><span class="sxs-lookup"><span data-stu-id="cc1b6-114">**DCompositionCreateDevice2**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice2)<br/>                   | <span data-ttu-id="cc1b6-115">Crée un nouvel objet d’appareil qui peut être utilisé pour créer d’autres objets DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="cc1b6-115">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="cc1b6-116">**DCompositionCreateDevice3**</span><span class="sxs-lookup"><span data-stu-id="cc1b6-116">**DCompositionCreateDevice3**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositioncreatedevice3)<br/>                   | <span data-ttu-id="cc1b6-117">Crée un nouvel objet d’appareil DirectComposition, qui peut être utilisé pour créer d’autres objets DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="cc1b6-117">Creates a new DirectComposition device object, which can be used to create other DirectComposition objects.</span></span><br/>                               |
| [<span data-ttu-id="cc1b6-118">**DCompositionCreateSurfaceHandle**</span><span class="sxs-lookup"><span data-stu-id="cc1b6-118">**DCompositionCreateSurfaceHandle**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatesurfacehandle)<br/>       | <span data-ttu-id="cc1b6-119">Crée un objet de surface de composition qui peut être lié à une chaîne de permutation Microsoft DirectX ou à un tampon d’échange et associé à un visuel.</span><span class="sxs-lookup"><span data-stu-id="cc1b6-119">Creates a new composition surface object that can be bound to a Microsoft DirectX swap chain or swap buffer and associated with a visual.</span></span><br/> |
| <span data-ttu-id="cc1b6-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc1b6-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span></span><br/>         | <span data-ttu-id="cc1b6-121">Récupère des informations sur les statistiques de la composition.</span><span class="sxs-lookup"><span data-stu-id="cc1b6-121">Retrieves composition statistics information.</span></span><br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="cc1b6-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc1b6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc1b6-123">Référence DirectComposition</span><span class="sxs-lookup"><span data-stu-id="cc1b6-123">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

