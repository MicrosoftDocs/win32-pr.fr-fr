---
description: InkPicture.Sysévénement temGesture-se produit lorsqu’un mouvement système est reconnu.
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.Sysévénement temGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cde11b73b6b0d3861a79538a7f9ee19487b6384
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113687"
---
# <a name="inkpicturesystemgesture-event"></a><span data-ttu-id="6eeb9-103">InkPicture.Sysévénement temGesture</span><span class="sxs-lookup"><span data-stu-id="6eeb9-103">InkPicture.SystemGesture event</span></span>

<span data-ttu-id="6eeb9-104">Se produit lorsqu’un mouvement système est reconnu.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eeb9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6eeb9-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="6eeb9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6eeb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eeb9-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6eeb9-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb9-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **SystemGesture** .</span><span class="sxs-lookup"><span data-stu-id="6eeb9-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="6eeb9-109">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6eeb9-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb9-110">Valeur du mouvement système.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="6eeb9-111">*X* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6eeb9-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb9-112">Coordonnée x de l’emplacement du mouvement.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="6eeb9-113">*Y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6eeb9-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb9-114">Coordonnée y de l’emplacement du mouvement.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="6eeb9-115">*Modificateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6eeb9-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb9-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6eeb9-117">*Caractère* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6eeb9-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb9-118">Réservé.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6eeb9-119">*CursorMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6eeb9-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb9-120">Valeur qui indique si l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) est en mode normal ou en mode gomme.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="6eeb9-121">1 est pour le mode normal et 2 pour le mode gomme.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eeb9-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6eeb9-122">Return value</span></span>

<span data-ttu-id="6eeb9-123">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eeb9-124">Notes </span><span class="sxs-lookup"><span data-stu-id="6eeb9-124">Remarks</span></span>

<span data-ttu-id="6eeb9-125">Les gestes système fournissent des informations sur l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) utilisé pour créer le mouvement.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-125">System gestures give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="6eeb9-126">Ils fournissent également des raccourcis vers des combinaisons d’événements de souris et sont des moyens de détecter les événements de souris avec moins d’impact sur les performances.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-126">They also provide shortcuts to combinations of mouse events and are ways to detect mouse events with less impact on performance.</span></span>

<span data-ttu-id="6eeb9-127">Par exemple, au lieu de rechercher une paire d’événements de contrôle d' [**événement \[ \]**](inkpicture-mouseup.md)de point de contrôle de l’événement / [**MouseDown événements \[ \] MouseDown**](inkpicture-mousedown.md) sans aucun autre événement de souris qui se produit entre, vous pouvez rechercher les gestes système TAP ou RightTap.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-127">For example, instead of looking for a [**MouseUp Event \[InkPicture Control\]**](inkpicture-mouseup.md)/[**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the Tap or RightTap system gestures.</span></span>

<span data-ttu-id="6eeb9-128">En guise d’autre exemple, au lieu d’écouter les événements de contrôle d’événement de survol d’événements [**MouseDown \[ \]**](inkpicture-mousedown.md) / [**\[ \]**](inkpicture-mousemove.md) et d’obtenir de nombreux messages de **\[ contrôle \]** d’événement MouseMove, vous pouvez surveiller les gestes du système Drag ou RightDrag tant que vous n’êtes pas intéressé par les coordonnées (x, y) de chaque position de la souris.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-128">As another example, instead of listening for [**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md)/[**MouseMove Event \[InkPicture Control\]**](inkpicture-mousemove.md) events and getting numerous **MouseMove Event \[InkPicture Control\]** messages, you can watch for the Drag or RightDrag system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="6eeb9-129">Cela vous permet de recevoir un seul message au lieu de nombreux messages de **\[ contrôle \] d’événement MouseMove** .</span><span class="sxs-lookup"><span data-stu-id="6eeb9-129">This allows you to receive only one message instead of numerous **MouseMove Event \[InkPicture Control\]** messages.</span></span>

<span data-ttu-id="6eeb9-130">Pour obtenir la liste des mouvements système spécifiques, consultez le type d’énumération [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="6eeb9-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="6eeb9-131">Pour plus d’informations sur les gestes système, consultez [utilisation des gestes](using-gestures.md) et [entrée de commande sur le Tablet PC](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6eeb9-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="6eeb9-132">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ ICESystemGesture.</span><span class="sxs-lookup"><span data-stu-id="6eeb9-132">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eeb9-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6eeb9-133">Requirements</span></span>



| <span data-ttu-id="6eeb9-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6eeb9-134">Requirement</span></span> | <span data-ttu-id="6eeb9-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="6eeb9-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eeb9-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eeb9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6eeb9-137">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6eeb9-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6eeb9-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eeb9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6eeb9-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6eeb9-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6eeb9-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="6eeb9-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eeb9-141"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6eeb9-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6eeb9-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6eeb9-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="6eeb9-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6eeb9-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6eeb9-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6eeb9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eeb9-145">InkPicture</span><span class="sxs-lookup"><span data-stu-id="6eeb9-145">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="6eeb9-146">**Énumération InkSystemGesture**</span><span class="sxs-lookup"><span data-stu-id="6eeb9-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="6eeb9-147">Utilisation des mouvements</span><span class="sxs-lookup"><span data-stu-id="6eeb9-147">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

