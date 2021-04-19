---
description: Se produit lorsque le InkCollector détecte un bouton de curseur en haut.
ms.assetid: f07daad7-e0d1-45cf-a708-5486a5dfda8b
title: Événement InkCollector. CursorButtonUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932d768c13da953d1926b28fb651c63dc26be572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515415"
---
# <a name="inkcollectorcursorbuttonup-event"></a><span data-ttu-id="6ad11-103">Événement InkCollector. CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="6ad11-103">InkCollector.CursorButtonUp event</span></span>

<span data-ttu-id="6ad11-104">Se produit lorsque le [**InkCollector**](inkcollector-class.md) détecte un bouton de curseur en haut.</span><span class="sxs-lookup"><span data-stu-id="6ad11-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad11-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ad11-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="6ad11-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ad11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ad11-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ad11-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad11-108">Objet d' [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **CursorButtonUp** .</span><span class="sxs-lookup"><span data-stu-id="6ad11-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="6ad11-109">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ad11-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad11-110">Bouton qui a été relâché.</span><span class="sxs-lookup"><span data-stu-id="6ad11-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ad11-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ad11-111">Return value</span></span>

<span data-ttu-id="6ad11-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6ad11-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ad11-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6ad11-113">Remarks</span></span>

<span data-ttu-id="6ad11-114">Un bouton sur une pointe de stylet est activé lorsque l’utilisateur termine un trait et soulève le stylet du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="6ad11-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="6ad11-115">Un bouton sur un tonneau est activé lorsque le bouton n’est pas enfoncé.</span><span class="sxs-lookup"><span data-stu-id="6ad11-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="6ad11-116">Lorsque vous relâchez le bouton droit de la souris, vous recevez deux événements **CursorButtonUp** : un pour le bouton droit et un pour le bouton gauche vers le haut.</span><span class="sxs-lookup"><span data-stu-id="6ad11-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="6ad11-117">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICECursorButtonUp.</span><span class="sxs-lookup"><span data-stu-id="6ad11-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad11-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ad11-118">Requirements</span></span>



| <span data-ttu-id="6ad11-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ad11-119">Requirement</span></span> | <span data-ttu-id="6ad11-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ad11-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad11-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ad11-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6ad11-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ad11-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6ad11-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ad11-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6ad11-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ad11-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6ad11-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ad11-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ad11-126"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6ad11-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6ad11-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6ad11-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ad11-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ad11-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6ad11-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ad11-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad11-130">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="6ad11-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="6ad11-131">**Événement CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="6ad11-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="6ad11-132">**Événement CursorDown**</span><span class="sxs-lookup"><span data-stu-id="6ad11-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="6ad11-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="6ad11-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="6ad11-134">**Interface IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="6ad11-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




