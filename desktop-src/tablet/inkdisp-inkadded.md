---
description: Se produit lorsqu’un trait est ajouté à l’objet InkDisp.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: Événement InkDisp. InkAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d25266a8cd75f873c5a7c1c18fa20fcf5126faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033955"
---
# <a name="inkdispinkadded-event"></a><span data-ttu-id="e7d6a-103">Événement InkDisp. InkAdded</span><span class="sxs-lookup"><span data-stu-id="e7d6a-103">InkDisp.InkAdded event</span></span>

<span data-ttu-id="e7d6a-104">Se produit lorsqu’un trait est ajouté à l’objet [**InkDisp**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e7d6a-104">Occurs when a stroke is added to the [**InkDisp**](inkdisp-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d6a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7d6a-105">Syntax</span></span>


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="e7d6a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7d6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d6a-107">*StrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7d6a-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d6a-108">Tableau d’entiers des informations d’ID de trait pour tous les traits qui ont été ajoutés lorsque cet événement se produit.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-108">The integer array of stroke ID information for all of the strokes that have been added when this event occurs.</span></span>

<span data-ttu-id="e7d6a-109">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="e7d6a-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d6a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7d6a-110">Return value</span></span>

<span data-ttu-id="e7d6a-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7d6a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e7d6a-112">Remarks</span></span>

<span data-ttu-id="e7d6a-113">Si vous utilisez l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control-reference.md) (où [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) est égal à [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) et [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) est égal à [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) et que vous transmettez la gomme sur un trait, vous recevez la séquence d’événements suivante :</span><span class="sxs-lookup"><span data-stu-id="e7d6a-113">If you use the [**InkOverlay**](inkoverlay-class.md) object or the [InkPicture](inkpicture-control-reference.md) control (where [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) equals [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) and [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) and pass the eraser over a stroke, you get the following sequence of events:</span></span>

-   [<span data-ttu-id="e7d6a-114">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="e7d6a-114">**InkDeleted**</span></span>](inkdisp-inkdeleted.md)
-   <span data-ttu-id="e7d6a-115">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="e7d6a-115">**InkAdded**</span></span>
-   [<span data-ttu-id="e7d6a-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="e7d6a-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md)

<span data-ttu-id="e7d6a-117">Les événements **InkAdded** et [**InkDeleted**](inkdisp-inkdeleted.md) supplémentaires se produisent parce que le code sous-jacent ajoute un trait invisible interne pour effectuer le suivi de la gomme.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-117">The additional **InkAdded** and [**InkDeleted**](inkdisp-inkdeleted.md) events occur because the underlying code adds an internal, invisible stroke to track the eraser.</span></span>

<span data-ttu-id="e7d6a-118">Cette méthode d’événement est définie dans l' \_ interface IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-118">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="e7d6a-119">L' \_ interface IInkEvents implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IEInkAdded.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-119">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IEInkAdded.</span></span>

<span data-ttu-id="e7d6a-120">L’événement **InkAdded** est déclenché même en mode SELECT ou Erase, pas uniquement lors de l’insertion d’une entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-120">The **InkAdded** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="e7d6a-121">Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="e7d6a-122">L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d6a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7d6a-123">Requirements</span></span>



| <span data-ttu-id="e7d6a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7d6a-124">Requirement</span></span> | <span data-ttu-id="e7d6a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7d6a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d6a-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7d6a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e7d6a-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7d6a-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e7d6a-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7d6a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e7d6a-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7d6a-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e7d6a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7d6a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7d6a-131"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e7d6a-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e7d6a-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7d6a-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7d6a-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7d6a-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e7d6a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7d6a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d6a-135">**InkDisp, classe**</span><span class="sxs-lookup"><span data-stu-id="e7d6a-135">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

<span data-ttu-id="e7d6a-136">[**Propriété EditingMode \[ classe InkOverlay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span><span class="sxs-lookup"><span data-stu-id="e7d6a-136">[**EditingMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span></span>
</dt> <dt>

<span data-ttu-id="e7d6a-137">[**Propriété EraserMode \[ classe InkOverlay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span><span class="sxs-lookup"><span data-stu-id="e7d6a-137">[**EraserMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span></span>
</dt> <dt>

[<span data-ttu-id="e7d6a-138">**Événement InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="e7d6a-138">**InkDeleted Event**</span></span>](inkdisp-inkdeleted.md)
</dt> <dt>

[<span data-ttu-id="e7d6a-139">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="e7d6a-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="e7d6a-140">Référence du contrôle InkPicture</span><span class="sxs-lookup"><span data-stu-id="e7d6a-140">InkPicture Control Reference</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e7d6a-141">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="e7d6a-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

