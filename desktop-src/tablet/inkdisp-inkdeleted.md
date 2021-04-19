---
description: Se produit lorsqu’un trait est supprimé de l’objet InkDisp.
ms.assetid: 59ada470-6620-411d-889e-882f41ccea3e
title: Événement InkDisp. InkDeleted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9022b34b128f92530761a0093b2e7c1823dd88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513980"
---
# <a name="inkdispinkdeleted-event"></a><span data-ttu-id="8be5c-103">Événement InkDisp. InkDeleted</span><span class="sxs-lookup"><span data-stu-id="8be5c-103">InkDisp.InkDeleted event</span></span>

<span data-ttu-id="8be5c-104">Se produit lorsqu’un trait est supprimé de l’objet [**InkDisp**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="8be5c-104">Occurs when a stroke is deleted from the [**InkDisp**](inkdisp-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be5c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8be5c-105">Syntax</span></span>


```C++
void InkDeleted(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="8be5c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8be5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be5c-107">*StrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8be5c-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8be5c-108">Spécifie le tableau d’entiers des informations d’ID de trait pour tous les traits qui ont été supprimés lorsque cet événement se produit.</span><span class="sxs-lookup"><span data-stu-id="8be5c-108">Specifies the integer array of stroke ID information for all of the strokes that have been deleted when this event occurs.</span></span>

<span data-ttu-id="8be5c-109">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="8be5c-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be5c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8be5c-110">Return value</span></span>

<span data-ttu-id="8be5c-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8be5c-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8be5c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8be5c-112">Remarks</span></span>

<span data-ttu-id="8be5c-113">Si vous utilisez l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control-reference.md) (où [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) est égal à [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) et [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) est égal à [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) et que vous transmettez la gomme sur un trait, vous recevez la séquence d’événements suivante :</span><span class="sxs-lookup"><span data-stu-id="8be5c-113">If you use the [**InkOverlay**](inkoverlay-class.md) object or the [InkPicture](inkpicture-control-reference.md) control (where [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) equals [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) and [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) and pass the eraser over a stroke, you get the following sequence of events:</span></span>

-   <span data-ttu-id="8be5c-114">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="8be5c-114">**InkDeleted**</span></span>
-   [<span data-ttu-id="8be5c-115">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="8be5c-115">**InkAdded**</span></span>](inkdisp-inkadded.md)
-   <span data-ttu-id="8be5c-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="8be5c-116">**InkDeleted**</span></span>

<span data-ttu-id="8be5c-117">Les événements [**InkAdded**](inkdisp-inkadded.md) et **InkDeleted** supplémentaires se produisent parce que le code sous-jacent ajoute un trait invisible interne pour effectuer le suivi de la gomme.</span><span class="sxs-lookup"><span data-stu-id="8be5c-117">The additional [**InkAdded**](inkdisp-inkadded.md) and **InkDeleted** events occur because the underlying code adds an internal, invisible stroke to track the eraser.</span></span>

<span data-ttu-id="8be5c-118">Cette méthode d’événement est définie dans l' \_ interface IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="8be5c-118">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="8be5c-119">L' \_ interface IInkEvents implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IEInkDeleted.</span><span class="sxs-lookup"><span data-stu-id="8be5c-119">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IEInkDeleted.</span></span>

<span data-ttu-id="8be5c-120">L’événement **InkDeleted** est déclenché même en mode SELECT ou Erase, pas uniquement lors de l’insertion d’une entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="8be5c-120">The **InkDeleted** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="8be5c-121">Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="8be5c-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="8be5c-122">L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.</span><span class="sxs-lookup"><span data-stu-id="8be5c-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be5c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8be5c-123">Requirements</span></span>



| <span data-ttu-id="8be5c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8be5c-124">Requirement</span></span> | <span data-ttu-id="8be5c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8be5c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be5c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8be5c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8be5c-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8be5c-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8be5c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8be5c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8be5c-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8be5c-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8be5c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="8be5c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8be5c-131"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8be5c-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8be5c-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8be5c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="8be5c-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8be5c-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8be5c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8be5c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be5c-135">**InkDisp, classe**</span><span class="sxs-lookup"><span data-stu-id="8be5c-135">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

<span data-ttu-id="8be5c-136">[**Propriété EditingMode \[ classe InkOverlay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span><span class="sxs-lookup"><span data-stu-id="8be5c-136">[**EditingMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span></span>
</dt> <dt>

<span data-ttu-id="8be5c-137">[**Propriété EraserMode \[ classe InkOverlay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span><span class="sxs-lookup"><span data-stu-id="8be5c-137">[**EraserMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span></span>
</dt> <dt>

[<span data-ttu-id="8be5c-138">**Événement InkAdded**</span><span class="sxs-lookup"><span data-stu-id="8be5c-138">**InkAdded Event**</span></span>](inkdisp-inkadded.md)
</dt> <dt>

[<span data-ttu-id="8be5c-139">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="8be5c-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="8be5c-140">Référence du contrôle InkPicture</span><span class="sxs-lookup"><span data-stu-id="8be5c-140">InkPicture Control Reference</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="8be5c-141">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="8be5c-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

