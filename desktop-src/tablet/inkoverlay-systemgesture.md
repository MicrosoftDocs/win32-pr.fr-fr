---
description: Se produit lorsqu’un mouvement système est reconnu.
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: InkOverlay.Sysévénement temGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b1e6ac7c02bc308856a89043bc0b1824b0fab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544912"
---
# <a name="inkoverlaysystemgesture-event"></a><span data-ttu-id="2703b-103">InkOverlay.Sysévénement temGesture</span><span class="sxs-lookup"><span data-stu-id="2703b-103">InkOverlay.SystemGesture event</span></span>

<span data-ttu-id="2703b-104">Se produit lorsqu’un mouvement système est reconnu.</span><span class="sxs-lookup"><span data-stu-id="2703b-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="2703b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2703b-105">Syntax</span></span>


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a><span data-ttu-id="2703b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2703b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2703b-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2703b-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2703b-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**SystemGesture**](inkcollector-systemgesture.md) .</span><span class="sxs-lookup"><span data-stu-id="2703b-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**SystemGesture**](inkcollector-systemgesture.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="2703b-109">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2703b-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2703b-110">Valeur du mouvement système.</span><span class="sxs-lookup"><span data-stu-id="2703b-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="2703b-111">*X* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2703b-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2703b-112">Coordonnée x de l’emplacement du mouvement.</span><span class="sxs-lookup"><span data-stu-id="2703b-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="2703b-113">*Y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2703b-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2703b-114">Coordonnée y de l’emplacement du mouvement.</span><span class="sxs-lookup"><span data-stu-id="2703b-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="2703b-115">*Modificateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2703b-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2703b-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="2703b-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2703b-117">*Caractère* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2703b-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2703b-118">Réservé.</span><span class="sxs-lookup"><span data-stu-id="2703b-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2703b-119">*CursorMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2703b-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2703b-120">Valeur qui indique si l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) est en mode normal ou en mode gomme.</span><span class="sxs-lookup"><span data-stu-id="2703b-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="2703b-121">1 est pour le mode normal et 2 pour le mode gomme.</span><span class="sxs-lookup"><span data-stu-id="2703b-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2703b-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2703b-122">Return value</span></span>

<span data-ttu-id="2703b-123">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2703b-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2703b-124">Notes</span><span class="sxs-lookup"><span data-stu-id="2703b-124">Remarks</span></span>

<span data-ttu-id="2703b-125">Les gestes système sont utiles car ils fournissent des informations sur l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) utilisé pour créer le mouvement.</span><span class="sxs-lookup"><span data-stu-id="2703b-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="2703b-126">Ils fournissent également des raccourcis vers des combinaisons d’événements de souris et sont des méthodes « moins chères » pour détecter les événements de souris.</span><span class="sxs-lookup"><span data-stu-id="2703b-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="2703b-127">Par exemple, au lieu de rechercher une paire d’événements [**MouseUp événements**](inkcollector-mouseup.md)  /  [**MouseDown**](inkcollector-mousedown.md) sans aucun autre événement de souris se produisant dans between, vous pouvez rechercher les gestes système [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) ou **RightTap** .</span><span class="sxs-lookup"><span data-stu-id="2703b-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="2703b-128">Autre exemple : au lieu d’écouter les événements d’événement MouseMove d' [**événements MouseDown**](inkcollector-mousedown.md)  /  [](inkcollector-mousemove.md) et d’obtenir un grand nombre de messages d' **événement MouseMove** , vous pouvez surveiller les gestes du système [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) ou **RightDrag** tant que vous n’êtes pas intéressé par les coordonnées (x, y) de chaque position de la souris.</span><span class="sxs-lookup"><span data-stu-id="2703b-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="2703b-129">Cela vous permet de recevoir un seul message au lieu de nombreux messages d' **événement MouseMove** .</span><span class="sxs-lookup"><span data-stu-id="2703b-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="2703b-130">Pour obtenir la liste des mouvements système spécifiques, consultez le type d’énumération [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="2703b-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="2703b-131">Pour plus d’informations sur les gestes système, consultez [utilisation des gestes](using-gestures.md) et [entrée de commande sur le Tablet PC](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2703b-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="2703b-132">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICESystemGesture.</span><span class="sxs-lookup"><span data-stu-id="2703b-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="2703b-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2703b-133">Requirements</span></span>



| <span data-ttu-id="2703b-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2703b-134">Requirement</span></span> | <span data-ttu-id="2703b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="2703b-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2703b-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2703b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2703b-137">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2703b-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2703b-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2703b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2703b-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2703b-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2703b-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="2703b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2703b-141"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2703b-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2703b-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2703b-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="2703b-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2703b-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2703b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2703b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2703b-145">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="2703b-145">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="2703b-146">**Énumération InkSystemGesture**</span><span class="sxs-lookup"><span data-stu-id="2703b-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="2703b-147">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="2703b-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="2703b-148">Utilisation des mouvements</span><span class="sxs-lookup"><span data-stu-id="2703b-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="2703b-149">Entrée, encre et reconnaissance du stylet</span><span class="sxs-lookup"><span data-stu-id="2703b-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="2703b-150">[Entrée de commande sur le Tablet PC](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2703b-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

