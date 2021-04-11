---
description: Se produit lorsqu’un mouvement d’application est reconnu.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: InkEdit. geste, événement (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203432"
---
# <a name="inkeditgesture-event"></a><span data-ttu-id="b6d3b-103">InkEdit. geste (événement)</span><span class="sxs-lookup"><span data-stu-id="b6d3b-103">InkEdit.Gesture event</span></span>

<span data-ttu-id="b6d3b-104">Se produit lorsqu’un mouvement d’application est reconnu.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-104">Occurs when an application gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6d3b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6d3b-105">Syntax</span></span>


```C++
HRESULT Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="b6d3b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6d3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6d3b-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6d3b-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6d3b-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a été utilisé pour créer ce geste.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that was used to create this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="b6d3b-109">*Traits* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6d3b-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6d3b-110">Collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) qui contient les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) qui composent ce geste.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-110">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that contains the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that make up this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="b6d3b-111">*Mouvements* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6d3b-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6d3b-112">Tableau d’objets [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , par ordre de confiance.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence.</span></span>

<span data-ttu-id="b6d3b-113">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="b6d3b-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6d3b-114">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b6d3b-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6d3b-115">Si la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) qui compose ce geste doit être annulée, pour ne pas effacer l’encre et déclencher l’événement [**Stroke**](inkedit-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="b6d3b-115">Whether the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that makes up this gesture should be canceled, so as not to erase the ink and to fire the [**Stroke**](inkedit-stroke.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6d3b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6d3b-116">Return value</span></span>

<span data-ttu-id="b6d3b-117">Si cet événement a la valeur, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-117">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b6d3b-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b6d3b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6d3b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b6d3b-119">Remarks</span></span>

<span data-ttu-id="b6d3b-120">Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="b6d3b-120">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="b6d3b-121">L’interface **\_ IInkEditEvents** implémente l’interface IDispatch avec un identificateur de DISPID \_ IeeGesture.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-121">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of DISPID\_IeeGesture.</span></span>

<span data-ttu-id="b6d3b-122">Un événement de **mouvement** est déclenché uniquement si le [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de l’objet [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) est le premier objet **IInkStrokeDisp** depuis le dernier appel à la méthode [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) ou le dernier déclenchement du délai de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-122">A **Gesture** event is raised only if the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) for the [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object is the first **IInkStrokeDisp** object since the last call to the [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or the last firing of the recognition timeout.</span></span>

<span data-ttu-id="b6d3b-123">Si l’événement de **mouvement** est annulé, l’événement [**Stroke**](inkedit-stroke.md) est déclenché pour la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) qui a déclenché l’événement de **mouvement** .</span><span class="sxs-lookup"><span data-stu-id="b6d3b-123">If the **Gesture** event is canceled, the [**Stroke**](inkedit-stroke.md) event is raised for the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that raised the **Gesture** event.</span></span>

<span data-ttu-id="b6d3b-124">Pour que cet événement se produise, le contrôle [InkEdit](inkedit-control-reference.md) doit s’abonner à un ensemble de mouvements d’application.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-124">For this event to occur, the [InkEdit](inkedit-control-reference.md) control must subscribe to a set of application gestures.</span></span> <span data-ttu-id="b6d3b-125">Pour définir l’intérêt du contrôle InkEdit dans un ensemble de mouvements, appelez la méthode [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) .</span><span class="sxs-lookup"><span data-stu-id="b6d3b-125">To set the InkEdit control's interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) method.</span></span>

<span data-ttu-id="b6d3b-126">Pour obtenir la liste des mouvements d’application, consultez le type d’énumération [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="b6d3b-126">For a list of application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

<span data-ttu-id="b6d3b-127">Le contrôle [InkEdit](inkedit-control-reference.md) ne reconnaît pas les gestes à plusieurs traits.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-127">The [InkEdit](inkedit-control-reference.md) control does not recognize multiple stroke gestures.</span></span>

<span data-ttu-id="b6d3b-128">Le contrôle [InkEdit](inkedit-control-reference.md) s’abonne aux gestes suivants.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-128">The [InkEdit](inkedit-control-reference.md) control subscribes to the following gestures.</span></span>



| <span data-ttu-id="b6d3b-129">Mouvement</span><span class="sxs-lookup"><span data-stu-id="b6d3b-129">Gesture</span></span>                              | <span data-ttu-id="b6d3b-130">Action</span><span class="sxs-lookup"><span data-stu-id="b6d3b-130">Action</span></span>               |
|--------------------------------------|----------------------|
| <span data-ttu-id="b6d3b-131">En baisse à gauche, en dessous de la gauche</span><span class="sxs-lookup"><span data-stu-id="b6d3b-131">Down-left ,Down-left-long</span></span><br/> | <span data-ttu-id="b6d3b-132">Entrez</span><span class="sxs-lookup"><span data-stu-id="b6d3b-132">Enter</span></span><br/>     |
| <span data-ttu-id="b6d3b-133">Right</span><span class="sxs-lookup"><span data-stu-id="b6d3b-133">Right</span></span><br/>                     | <span data-ttu-id="b6d3b-134">Espace</span><span class="sxs-lookup"><span data-stu-id="b6d3b-134">Space</span></span><br/>     |
| <span data-ttu-id="b6d3b-135">Gauche</span><span class="sxs-lookup"><span data-stu-id="b6d3b-135">Left</span></span><br/>                      | <span data-ttu-id="b6d3b-136">Retour arrière</span><span class="sxs-lookup"><span data-stu-id="b6d3b-136">Backspace</span></span><br/> |
| <span data-ttu-id="b6d3b-137">En haut à droite, en haut à droite</span><span class="sxs-lookup"><span data-stu-id="b6d3b-137">Up-right, Up-right-long</span></span><br/>   | <span data-ttu-id="b6d3b-138">Onglet</span><span class="sxs-lookup"><span data-stu-id="b6d3b-138">Tab</span></span><br/>       |



 

<span data-ttu-id="b6d3b-139">Pour modifier l’action par défaut pour un mouvement :</span><span class="sxs-lookup"><span data-stu-id="b6d3b-139">To alter the default action for a gesture:</span></span>

1.  <span data-ttu-id="b6d3b-140">Ajoutez des gestionnaires d’événements pour les événements de **mouvement** et de [**trait**](inkedit-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="b6d3b-140">Add event handlers for the **Gesture** and [**Stroke**](inkedit-stroke.md) events.</span></span>
2.  <span data-ttu-id="b6d3b-141">Dans le gestionnaire d’événements de **mouvement** , annulez l’événement de **mouvement** pour le mouvement et exécutez l’autre action pour le mouvement.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-141">In the **Gesture** event handler, cancel the **Gesture** event for the gesture, and perform the alternate action for the gesture.</span></span>
3.  <span data-ttu-id="b6d3b-142">Dans le gestionnaire d’événements [**Stroke**](inkedit-stroke.md) , annulez l’événement **Stroke** pour l’objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) qui a déclenché l’événement de **mouvement** annulé.</span><span class="sxs-lookup"><span data-stu-id="b6d3b-142">In the [**Stroke**](inkedit-stroke.md) event handler, cancel the **Stroke** event for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that raised the canceled **Gesture** event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6d3b-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6d3b-143">Requirements</span></span>



| <span data-ttu-id="b6d3b-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6d3b-144">Requirement</span></span> | <span data-ttu-id="b6d3b-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6d3b-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d3b-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6d3b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b6d3b-147">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6d3b-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b6d3b-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6d3b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b6d3b-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6d3b-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b6d3b-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6d3b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6d3b-151"><dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b6d3b-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b6d3b-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6d3b-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6d3b-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6d3b-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b6d3b-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6d3b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6d3b-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="b6d3b-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b6d3b-156">**Énumération InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="b6d3b-156">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

<span data-ttu-id="b6d3b-157">[**Méthode SetGestureStatus \[ contrôle InkEdit\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span><span class="sxs-lookup"><span data-stu-id="b6d3b-157">[**SetGestureStatus Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span></span>
</dt> <dt>

[<span data-ttu-id="b6d3b-158">**Propriété RecoTimeout**</span><span class="sxs-lookup"><span data-stu-id="b6d3b-158">**RecoTimeout Property**</span></span>](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

<span data-ttu-id="b6d3b-159">[**Stroke, événement \[ contrôle InkEdit\]**](inkedit-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="b6d3b-159">[**Stroke Event \[InkEdit Control\]**](inkedit-stroke.md)</span></span>
</dt> <dt>

[<span data-ttu-id="b6d3b-160">Utilisation des mouvements</span><span class="sxs-lookup"><span data-stu-id="b6d3b-160">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

