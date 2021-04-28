---
description: L’événement InkCollector. CursorButtonDown-se produit lorsque la classe InkCollector détecte un bouton de curseur inactif.
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: Événement InkCollector. CursorButtonDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd1a820445a1ba3ed07dad8a22a11ad86e8da96f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110327"
---
# <a name="inkcollectorcursorbuttondown-event"></a><span data-ttu-id="b4b5a-103">Événement InkCollector. CursorButtonDown</span><span class="sxs-lookup"><span data-stu-id="b4b5a-103">InkCollector.CursorButtonDown event</span></span>

<span data-ttu-id="b4b5a-104">Se produit lorsque la [**classe InkCollector**](inkcollector-class.md) détecte un bouton de curseur en dessous.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b5a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4b5a-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="b4b5a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4b5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4b5a-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4b5a-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4b5a-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **CursorButtonDown** .</span><span class="sxs-lookup"><span data-stu-id="b4b5a-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="b4b5a-109">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4b5a-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4b5a-110">Bouton qui a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4b5a-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4b5a-111">Return value</span></span>

<span data-ttu-id="b4b5a-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4b5a-113">Notes </span><span class="sxs-lookup"><span data-stu-id="b4b5a-113">Remarks</span></span>

<span data-ttu-id="b4b5a-114">Un bouton sur une info-bulle est enfoncé lorsque l’utilisateur réduit le stylet au digitaliseur et démarre le traçage d’un trait.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="b4b5a-115">Un bouton sur un tonneau est enfoncé lorsque le bouton est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="b4b5a-116">Lorsque vous appuyez sur le bouton droit de la souris, vous recevez deux événements **CursorButtonDown** : un pour le bouton droit enfoncé et un bouton gauche enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="b4b5a-117">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICECursorButtonDown.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b5a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4b5a-118">Requirements</span></span>



| <span data-ttu-id="b4b5a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4b5a-119">Requirement</span></span> | <span data-ttu-id="b4b5a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4b5a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b5a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4b5a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b5a-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4b5a-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b4b5a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4b5a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b5a-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4b5a-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b4b5a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4b5a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4b5a-126"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b4b5a-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b4b5a-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4b5a-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4b5a-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4b5a-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b4b5a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4b5a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b5a-130">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="b4b5a-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="b4b5a-131">**Événement CursorDown**</span><span class="sxs-lookup"><span data-stu-id="b4b5a-131">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="b4b5a-132">**Événement CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="b4b5a-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="b4b5a-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="b4b5a-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="b4b5a-134">**Interface IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="b4b5a-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




