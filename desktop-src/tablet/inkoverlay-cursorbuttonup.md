---
description: L’événement InkOverlay. CursorButtonUp-se produit lorsque le InkCollector détecte un bouton de curseur en haut.
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: InkOverlay. CursorButtonUp, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f22590362c6eb9a987da94bf3adb4e99943c12cd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086847"
---
# <a name="inkoverlaycursorbuttonup-event"></a><span data-ttu-id="30c42-103">Événement InkOverlay. CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="30c42-103">InkOverlay.CursorButtonUp event</span></span>

<span data-ttu-id="30c42-104">Se produit lorsque le [**InkCollector**](inkcollector-class.md) détecte un bouton de curseur en haut.</span><span class="sxs-lookup"><span data-stu-id="30c42-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="30c42-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30c42-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="30c42-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30c42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30c42-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30c42-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30c42-108">Objet d' [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**CursorButtonUp**](inkcollector-cursorbuttonup.md) .</span><span class="sxs-lookup"><span data-stu-id="30c42-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonUp**](inkcollector-cursorbuttonup.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="30c42-109">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30c42-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30c42-110">Bouton qui a été relâché.</span><span class="sxs-lookup"><span data-stu-id="30c42-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30c42-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="30c42-111">Return value</span></span>

<span data-ttu-id="30c42-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="30c42-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30c42-113">Notes </span><span class="sxs-lookup"><span data-stu-id="30c42-113">Remarks</span></span>

<span data-ttu-id="30c42-114">Un bouton sur une pointe de stylet est activé lorsque l’utilisateur termine un trait et soulève le stylet du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="30c42-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="30c42-115">Un bouton sur un tonneau est activé lorsque le bouton n’est pas enfoncé.</span><span class="sxs-lookup"><span data-stu-id="30c42-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="30c42-116">Lorsque vous relâchez le bouton droit de la souris, vous recevez deux événements [**CursorButtonUp**](inkcollector-cursorbuttonup.md) : un pour le bouton droit et un pour le bouton gauche vers le haut.</span><span class="sxs-lookup"><span data-stu-id="30c42-116">When you release the right mouse button, you actually receive two [**CursorButtonUp**](inkcollector-cursorbuttonup.md) events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="30c42-117">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICECursorButtonUp.</span><span class="sxs-lookup"><span data-stu-id="30c42-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="30c42-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30c42-118">Requirements</span></span>



| <span data-ttu-id="30c42-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30c42-119">Requirement</span></span> | <span data-ttu-id="30c42-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="30c42-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30c42-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30c42-121">Minimum supported client</span></span><br/> | <span data-ttu-id="30c42-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30c42-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="30c42-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30c42-123">Minimum supported server</span></span><br/> | <span data-ttu-id="30c42-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="30c42-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="30c42-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="30c42-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="30c42-126"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="30c42-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="30c42-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="30c42-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="30c42-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30c42-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="30c42-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30c42-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c42-130">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="30c42-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="30c42-131">**Événement CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="30c42-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="30c42-132">**Événement CursorDown**</span><span class="sxs-lookup"><span data-stu-id="30c42-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="30c42-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="30c42-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="30c42-134">**Interface IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="30c42-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




