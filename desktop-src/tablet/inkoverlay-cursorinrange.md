---
description: L’événement InkOverlay. CursorInRange-se produit lorsqu’un curseur entre dans la plage de détection physique (proximité) du contexte de la tablette.
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: InkOverlay. CursorInRange, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1b48cba731720072aae88aa59b80c569a4aa07b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086837"
---
# <a name="inkoverlaycursorinrange-event"></a><span data-ttu-id="f36cc-103">Événement InkOverlay. CursorInRange</span><span class="sxs-lookup"><span data-stu-id="f36cc-103">InkOverlay.CursorInRange event</span></span>

<span data-ttu-id="f36cc-104">Se produit lorsqu’un curseur entre dans la plage de détection physique (proximité) du contexte de la tablette.</span><span class="sxs-lookup"><span data-stu-id="f36cc-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="f36cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f36cc-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="f36cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f36cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f36cc-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f36cc-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f36cc-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**CursorInRange**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="f36cc-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="f36cc-109">*NewCursor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f36cc-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f36cc-110">Indique s’il s’agit de la première fois que ce collecteur d’encres est en contact avec l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**CursorInRange**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="f36cc-110">Whether this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="f36cc-111">*ButtonsState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f36cc-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f36cc-112">État des boutons pour le curseur qui a généré l’événement [**CursorInRange**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="f36cc-112">The state of the buttons for the cursor that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

<span data-ttu-id="f36cc-113">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="f36cc-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f36cc-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f36cc-114">Return value</span></span>

<span data-ttu-id="f36cc-115">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f36cc-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f36cc-116">Notes </span><span class="sxs-lookup"><span data-stu-id="f36cc-116">Remarks</span></span>

<span data-ttu-id="f36cc-117">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICECursorInRange.</span><span class="sxs-lookup"><span data-stu-id="f36cc-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="f36cc-118">L’événement [**CursorInRange**](inkcollector-cursorinrange.md) est déclenché même en mode SELECT ou Erase, pas seulement en mode Ink.</span><span class="sxs-lookup"><span data-stu-id="f36cc-118">The [**CursorInRange**](inkcollector-cursorinrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="f36cc-119">Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="f36cc-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="f36cc-120">L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.</span><span class="sxs-lookup"><span data-stu-id="f36cc-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="f36cc-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f36cc-121">Requirements</span></span>



| <span data-ttu-id="f36cc-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f36cc-122">Requirement</span></span> | <span data-ttu-id="f36cc-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f36cc-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f36cc-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f36cc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f36cc-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f36cc-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f36cc-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f36cc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f36cc-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f36cc-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f36cc-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f36cc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f36cc-129"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f36cc-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f36cc-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f36cc-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f36cc-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f36cc-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f36cc-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f36cc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f36cc-133">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="f36cc-133">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="f36cc-134">**Événement CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="f36cc-134">**CursorOutOfRange Event**</span></span>](inkcollector-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="f36cc-135">**Énumération InkCursorButtonState**</span><span class="sxs-lookup"><span data-stu-id="f36cc-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="f36cc-136">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="f36cc-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




