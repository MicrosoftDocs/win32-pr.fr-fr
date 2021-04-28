---
description: L’événement InkPicture. geste se produit lorsqu’un mouvement spécifique à l’application est reconnu.
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: InkPicture. geste, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 915557f304d722ed2819af75dd40284db119abfb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086587"
---
# <a name="inkpicturegesture-event"></a><span data-ttu-id="220e5-103">InkPicture. geste (événement)</span><span class="sxs-lookup"><span data-stu-id="220e5-103">InkPicture.Gesture event</span></span>

<span data-ttu-id="220e5-104">Se produit lorsqu’un *mouvement* spécifique à l’application est reconnu.</span><span class="sxs-lookup"><span data-stu-id="220e5-104">Occurs when an application-specific *gesture* is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="220e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="220e5-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="220e5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="220e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="220e5-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="220e5-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220e5-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement de **mouvement** .</span><span class="sxs-lookup"><span data-stu-id="220e5-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="220e5-109">*Traits* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="220e5-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220e5-110">Collection [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que le module de reconnaissance a retourné comme geste.</span><span class="sxs-lookup"><span data-stu-id="220e5-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="220e5-111">*Mouvements* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="220e5-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220e5-112">Tableau d’objets [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , par ordre de confiance, à partir du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="220e5-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="220e5-113">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="220e5-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="220e5-114">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="220e5-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="220e5-115">**Variante \_ TRUE** si cet événement doit être annulé, par exemple pour ne pas effacer l’encre et déclencher l’événement [**Stroke**](inkpicture-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="220e5-115">**VARIANT\_TRUE** if this event should be cancelled, such as not to erase the ink and to fire the [**Stroke**](inkpicture-stroke.md) event.</span></span> <span data-ttu-id="220e5-116">Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="220e5-116">Otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="220e5-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="220e5-117">Return value</span></span>

<span data-ttu-id="220e5-118">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="220e5-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="220e5-119">Notes </span><span class="sxs-lookup"><span data-stu-id="220e5-119">Remarks</span></span>

<span data-ttu-id="220e5-120">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ ICEGesture.</span><span class="sxs-lookup"><span data-stu-id="220e5-120">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="220e5-121">Lorsque la propriété [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) est définie sur [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), le délai d’attente entre le moment où un utilisateur ajoute un geste et le moment où l’événement de **mouvement** se produit est une valeur fixe que vous ne pouvez pas modifier par programme.</span><span class="sxs-lookup"><span data-stu-id="220e5-121">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="220e5-122">La reconnaissance des mouvements est plus rapide en mode **InkAndGesture** .</span><span class="sxs-lookup"><span data-stu-id="220e5-122">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="220e5-123">Pour empêcher la collecte d’encre en mode [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :</span><span class="sxs-lookup"><span data-stu-id="220e5-123">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="220e5-124">Définissez [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) sur [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span><span class="sxs-lookup"><span data-stu-id="220e5-124">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="220e5-125">Supprimez le trait dans l’événement [**Stroke**](inkpicture-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="220e5-125">Delete the stroke in the [**Stroke**](inkpicture-stroke.md) event.</span></span>
-   <span data-ttu-id="220e5-126">Traitez le mouvement dans l’événement de **mouvement** .</span><span class="sxs-lookup"><span data-stu-id="220e5-126">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="220e5-127">Pour empêcher le passage de l’encre pendant la gesturing, affectez la valeur **false** à la propriété [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) .</span><span class="sxs-lookup"><span data-stu-id="220e5-127">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="220e5-128">En plus de lors de l’insertion d’une entrée manuscrite, l’événement de **mouvement** est déclenché en mode de sélection ou d’effacement.</span><span class="sxs-lookup"><span data-stu-id="220e5-128">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="220e5-129">Vous êtes chargé de suivre le mode d’édition et vous devez connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="220e5-129">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="220e5-130">Pour reconnaître les gestes, vous devez utiliser un objet ou un contrôle qui peut collecter de l’encre.</span><span class="sxs-lookup"><span data-stu-id="220e5-130">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="220e5-131">Les mouvements d’application sont définis en tant que mouvements pris en charge dans votre application.</span><span class="sxs-lookup"><span data-stu-id="220e5-131">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="220e5-132">Pour que cet événement se produise, l’objet ou le contrôle doit avoir un intérêt dans un ensemble de mouvements d’application.</span><span class="sxs-lookup"><span data-stu-id="220e5-132">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="220e5-133">Pour définir les objets ou les contrôles qui présentent un intérêt pour un ensemble de mouvements, appelez la méthode [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) de l’objet ou du contrôle.</span><span class="sxs-lookup"><span data-stu-id="220e5-133">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="220e5-134">Pour obtenir la liste des mouvements d’application spécifiques, consultez le type d’énumération [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="220e5-134">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="220e5-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="220e5-135">Requirements</span></span>



| <span data-ttu-id="220e5-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="220e5-136">Requirement</span></span> | <span data-ttu-id="220e5-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="220e5-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="220e5-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="220e5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="220e5-139">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="220e5-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="220e5-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="220e5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="220e5-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="220e5-141">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="220e5-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="220e5-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="220e5-143"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="220e5-143"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="220e5-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="220e5-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="220e5-145"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="220e5-145"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="220e5-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="220e5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="220e5-147">InkPicture</span><span class="sxs-lookup"><span data-stu-id="220e5-147">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="220e5-148">**Énumération InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="220e5-148">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="220e5-149">**Méthode SetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="220e5-149">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="220e5-150">Utilisation des mouvements</span><span class="sxs-lookup"><span data-stu-id="220e5-150">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

