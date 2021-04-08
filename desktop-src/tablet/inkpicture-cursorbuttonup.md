---
description: Se produit lorsque le InkCollector détecte un bouton de curseur en haut.
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: InkPicture. CursorButtonUp, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6dbee586b3179f35593c95c2d62109a379c3216
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867726"
---
# <a name="inkpicturecursorbuttonup-event"></a><span data-ttu-id="36b0d-103">InkPicture. CursorButtonUp, événement</span><span class="sxs-lookup"><span data-stu-id="36b0d-103">InkPicture.CursorButtonUp event</span></span>

<span data-ttu-id="36b0d-104">Se produit lorsque le [**InkCollector**](inkcollector-class.md) détecte un bouton de curseur en haut.</span><span class="sxs-lookup"><span data-stu-id="36b0d-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="36b0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36b0d-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="36b0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36b0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36b0d-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36b0d-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36b0d-108">Objet d' [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **CursorButtonUp** .</span><span class="sxs-lookup"><span data-stu-id="36b0d-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="36b0d-109">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36b0d-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36b0d-110">Bouton qui a été relâché.</span><span class="sxs-lookup"><span data-stu-id="36b0d-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36b0d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36b0d-111">Return value</span></span>

<span data-ttu-id="36b0d-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="36b0d-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36b0d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="36b0d-113">Remarks</span></span>

<span data-ttu-id="36b0d-114">Un bouton sur une pointe de stylet est activé lorsque l’utilisateur termine un trait et soulève le stylet du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="36b0d-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="36b0d-115">Un bouton sur un tonneau est activé lorsque le bouton n’est pas enfoncé.</span><span class="sxs-lookup"><span data-stu-id="36b0d-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="36b0d-116">Lorsque vous relâchez le bouton droit de la souris, vous recevez deux événements **CursorButtonUp** : un pour le bouton droit et un pour le bouton gauche vers le haut.</span><span class="sxs-lookup"><span data-stu-id="36b0d-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="36b0d-117">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** avec l’ID DISPID \_ ICECursorButtonUp.</span><span class="sxs-lookup"><span data-stu-id="36b0d-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="36b0d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36b0d-118">Requirements</span></span>



| <span data-ttu-id="36b0d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36b0d-119">Requirement</span></span> | <span data-ttu-id="36b0d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="36b0d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36b0d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36b0d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="36b0d-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36b0d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="36b0d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36b0d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="36b0d-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="36b0d-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="36b0d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="36b0d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="36b0d-126"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="36b0d-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="36b0d-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="36b0d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="36b0d-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36b0d-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="36b0d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36b0d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b0d-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="36b0d-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="36b0d-131">**Événement CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="36b0d-131">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="36b0d-132">**Événement CursorDown**</span><span class="sxs-lookup"><span data-stu-id="36b0d-132">**CursorDown Event**</span></span>](inkpicture-cursordown.md)
</dt> <dt>

[<span data-ttu-id="36b0d-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="36b0d-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="36b0d-134">**Interface IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="36b0d-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




