---
description: Se produit lorsqu’un mouvement spécifique à l’application est reconnu.
ms.assetid: 5830f7f8-2870-4194-ab3e-b63b71e97063
title: Événement InkCollector. geste (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb68add1a3fbba5781624f1df98c3a637745b95a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514424"
---
# <a name="inkcollectorgesture-event"></a><span data-ttu-id="a12d3-103">Événement InkCollector. geste</span><span class="sxs-lookup"><span data-stu-id="a12d3-103">InkCollector.Gesture event</span></span>

<span data-ttu-id="a12d3-104">Se produit lorsqu’un mouvement spécifique à l’application est reconnu.</span><span class="sxs-lookup"><span data-stu-id="a12d3-104">Occurs when an application-specific gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="a12d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a12d3-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="a12d3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a12d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a12d3-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a12d3-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a12d3-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement de **mouvement** .</span><span class="sxs-lookup"><span data-stu-id="a12d3-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="a12d3-109">*Traits* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a12d3-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a12d3-110">Collection [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que le module de reconnaissance a retourné comme geste.</span><span class="sxs-lookup"><span data-stu-id="a12d3-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="a12d3-111">*Mouvements* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a12d3-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a12d3-112">Tableau d’objets [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , par ordre de confiance, à partir du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a12d3-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="a12d3-113">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="a12d3-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="a12d3-114">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a12d3-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a12d3-115">**Variante \_ TRUE** si ce mouvement doit être annulé ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="a12d3-115">**VARIANT\_TRUE** if this gesture should be cancelled; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a12d3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a12d3-116">Return value</span></span>

<span data-ttu-id="a12d3-117">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a12d3-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a12d3-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a12d3-118">Remarks</span></span>

<span data-ttu-id="a12d3-119">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICEGesture.</span><span class="sxs-lookup"><span data-stu-id="a12d3-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="a12d3-120">Lorsque la propriété [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) est définie sur [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), le délai d’attente entre le moment où un utilisateur ajoute un geste et le moment où l’événement de **mouvement** se produit est une valeur fixe que vous ne pouvez pas modifier par programme.</span><span class="sxs-lookup"><span data-stu-id="a12d3-120">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="a12d3-121">La reconnaissance des mouvements est plus rapide en mode **InkAndGesture** .</span><span class="sxs-lookup"><span data-stu-id="a12d3-121">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="a12d3-122">Pour empêcher la collecte d’encre en mode [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :</span><span class="sxs-lookup"><span data-stu-id="a12d3-122">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="a12d3-123">Définissez [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) sur [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span><span class="sxs-lookup"><span data-stu-id="a12d3-123">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="a12d3-124">Supprimez le trait dans l’événement [**Stroke**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="a12d3-124">Delete the stroke in the [**Stroke**](inkcollector-stroke.md) event.</span></span>
-   <span data-ttu-id="a12d3-125">Traitez le mouvement dans l’événement de **mouvement** .</span><span class="sxs-lookup"><span data-stu-id="a12d3-125">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="a12d3-126">Pour empêcher le passage de l’encre pendant la gesturing, affectez la valeur **false** à la propriété [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) .</span><span class="sxs-lookup"><span data-stu-id="a12d3-126">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="a12d3-127">En plus de lors de l’insertion d’une entrée manuscrite, l’événement de **mouvement** est déclenché en mode de sélection ou d’effacement.</span><span class="sxs-lookup"><span data-stu-id="a12d3-127">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="a12d3-128">Vous êtes chargé de suivre le mode d’édition et vous devez connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="a12d3-128">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="a12d3-129">Pour reconnaître les gestes, vous devez utiliser un objet ou un contrôle qui peut collecter de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a12d3-129">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="a12d3-130">Les mouvements d’application sont définis en tant que mouvements pris en charge dans votre application.</span><span class="sxs-lookup"><span data-stu-id="a12d3-130">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="a12d3-131">Pour que cet événement se produise, l’objet ou le contrôle doit avoir un intérêt dans un ensemble de mouvements d’application.</span><span class="sxs-lookup"><span data-stu-id="a12d3-131">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="a12d3-132">Pour définir les objets ou les contrôles qui présentent un intérêt pour un ensemble de mouvements, appelez la méthode [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) de l’objet ou du contrôle.</span><span class="sxs-lookup"><span data-stu-id="a12d3-132">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="a12d3-133">Pour obtenir la liste des mouvements d’application spécifiques, consultez le type d’énumération [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="a12d3-133">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a12d3-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a12d3-134">Requirements</span></span>



| <span data-ttu-id="a12d3-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a12d3-135">Requirement</span></span> | <span data-ttu-id="a12d3-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="a12d3-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a12d3-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a12d3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a12d3-138">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a12d3-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a12d3-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a12d3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a12d3-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a12d3-140">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a12d3-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="a12d3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a12d3-142"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a12d3-142"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a12d3-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a12d3-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="a12d3-144"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a12d3-144"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a12d3-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a12d3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a12d3-146">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="a12d3-146">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="a12d3-147">**Énumération InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="a12d3-147">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="a12d3-148">**Méthode SetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="a12d3-148">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="a12d3-149">Utilisation des mouvements</span><span class="sxs-lookup"><span data-stu-id="a12d3-149">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

