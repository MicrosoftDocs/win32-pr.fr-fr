---
description: L’événement InkOverlay. CursorOutOfRange-se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.
ms.assetid: c696b2a9-dc47-4b73-a556-9bb222f5bf59
title: InkOverlay. CursorOutOfRange, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a30bfde1e96edfa286e9afeac147dc141c4942
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116957"
---
# <a name="inkoverlaycursoroutofrange-event"></a><span data-ttu-id="ad431-103">Événement InkOverlay. CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="ad431-103">InkOverlay.CursorOutOfRange event</span></span>

<span data-ttu-id="ad431-104">Se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.</span><span class="sxs-lookup"><span data-stu-id="ad431-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad431-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad431-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="ad431-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad431-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad431-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad431-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad431-108">Objet d' [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) .</span><span class="sxs-lookup"><span data-stu-id="ad431-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad431-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ad431-109">Return value</span></span>

<span data-ttu-id="ad431-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ad431-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad431-111">Notes </span><span class="sxs-lookup"><span data-stu-id="ad431-111">Remarks</span></span>

<span data-ttu-id="ad431-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICECursorOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="ad431-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="ad431-113">L’événement [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) est déclenché même en mode SELECT ou Erase, pas seulement en mode Ink.</span><span class="sxs-lookup"><span data-stu-id="ad431-113">The [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="ad431-114">Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="ad431-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="ad431-115">L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.</span><span class="sxs-lookup"><span data-stu-id="ad431-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad431-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad431-116">Requirements</span></span>



| <span data-ttu-id="ad431-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad431-117">Requirement</span></span> | <span data-ttu-id="ad431-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad431-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad431-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad431-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ad431-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad431-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ad431-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad431-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ad431-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad431-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ad431-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad431-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad431-124"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ad431-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ad431-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad431-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="ad431-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad431-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ad431-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad431-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad431-128">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="ad431-128">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="ad431-129">**Événement CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="ad431-129">**CursorInRange Event**</span></span>](inkcollector-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="ad431-130">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="ad431-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




