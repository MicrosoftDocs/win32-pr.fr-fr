---
description: Se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.
ms.assetid: c696b2a9-dc47-4b73-a556-9bb222f5bf59
title: InkOverlay. CursorOutOfRange, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1510013d24bf092a08ba7d57b54c0f94bf7c2dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530908"
---
# <a name="inkoverlaycursoroutofrange-event"></a><span data-ttu-id="5004b-103">Événement InkOverlay. CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="5004b-103">InkOverlay.CursorOutOfRange event</span></span>

<span data-ttu-id="5004b-104">Se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.</span><span class="sxs-lookup"><span data-stu-id="5004b-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="5004b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5004b-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="5004b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5004b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5004b-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5004b-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5004b-108">Objet d' [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) .</span><span class="sxs-lookup"><span data-stu-id="5004b-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5004b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5004b-109">Return value</span></span>

<span data-ttu-id="5004b-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5004b-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5004b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5004b-111">Remarks</span></span>

<span data-ttu-id="5004b-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICECursorOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="5004b-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="5004b-113">L’événement [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) est déclenché même en mode SELECT ou Erase, pas seulement en mode Ink.</span><span class="sxs-lookup"><span data-stu-id="5004b-113">The [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="5004b-114">Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="5004b-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="5004b-115">L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.</span><span class="sxs-lookup"><span data-stu-id="5004b-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="5004b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5004b-116">Requirements</span></span>



| <span data-ttu-id="5004b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5004b-117">Requirement</span></span> | <span data-ttu-id="5004b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5004b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5004b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5004b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5004b-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5004b-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5004b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5004b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5004b-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5004b-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5004b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5004b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5004b-124"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5004b-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5004b-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5004b-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="5004b-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5004b-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5004b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5004b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5004b-128">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="5004b-128">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="5004b-129">**Événement CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="5004b-129">**CursorInRange Event**</span></span>](inkcollector-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="5004b-130">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="5004b-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




