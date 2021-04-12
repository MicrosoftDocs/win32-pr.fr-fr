---
description: Se produit après la suppression de traits de la propriété Ink.
ms.assetid: 60ee8bbd-9230-4b6a-a4b0-4783195e3173
title: InkOverlay. StrokesDeleted, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc37b0de7f86f7d2b68df7074a0f3bb6c9e075e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203250"
---
# <a name="inkoverlaystrokesdeleted-event"></a><span data-ttu-id="8fbd7-103">Événement InkOverlay. StrokesDeleted</span><span class="sxs-lookup"><span data-stu-id="8fbd7-103">InkOverlay.StrokesDeleted event</span></span>

<span data-ttu-id="8fbd7-104">Se produit après la suppression de traits de la propriété [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="8fbd7-104">Occurs after strokes have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbd7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fbd7-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="8fbd7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fbd7-106">Parameters</span></span>

<span data-ttu-id="8fbd7-107">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="8fbd7-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fbd7-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8fbd7-108">Return value</span></span>

<span data-ttu-id="8fbd7-109">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8fbd7-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fbd7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8fbd7-110">Remarks</span></span>

<span data-ttu-id="8fbd7-111">Il n’y a aucune donnée d’événement.</span><span class="sxs-lookup"><span data-stu-id="8fbd7-111">There is no event data.</span></span>

<span data-ttu-id="8fbd7-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IOEStrokesDeleted.</span><span class="sxs-lookup"><span data-stu-id="8fbd7-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fbd7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fbd7-113">Requirements</span></span>



| <span data-ttu-id="8fbd7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fbd7-114">Requirement</span></span> | <span data-ttu-id="8fbd7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fbd7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbd7-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fbd7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8fbd7-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fbd7-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8fbd7-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fbd7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8fbd7-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fbd7-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8fbd7-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8fbd7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fbd7-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8fbd7-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8fbd7-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8fbd7-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="8fbd7-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fbd7-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8fbd7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fbd7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fbd7-125">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="8fbd7-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="8fbd7-126">[**Propriété Ink, \[ classe InkCollector/InkOverLay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="8fbd7-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

 




