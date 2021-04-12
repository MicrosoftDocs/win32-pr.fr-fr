---
description: Se produit lorsqu’un ou plusieurs traits sont supprimés de la collection InkStrokes.
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: Événement InkStrokes. StrokesRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86448f9676e07a11effe683ecd883874791ff3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320933"
---
# <a name="inkstrokesstrokesremoved-event"></a><span data-ttu-id="99411-103">Événement InkStrokes. StrokesRemoved</span><span class="sxs-lookup"><span data-stu-id="99411-103">InkStrokes.StrokesRemoved event</span></span>

<span data-ttu-id="99411-104">Se produit lorsqu’un ou plusieurs traits sont supprimés de la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="99411-104">Occurs when one or more strokes are deleted from the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="99411-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99411-105">Syntax</span></span>


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="99411-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99411-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99411-107">*StrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99411-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99411-108">Tableau d’entiers des identificateurs pour chaque objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) supprimé lorsque cet événement se produit.</span><span class="sxs-lookup"><span data-stu-id="99411-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object deleted when this event occurs.</span></span>

<span data-ttu-id="99411-109">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="99411-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99411-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99411-110">Return value</span></span>

<span data-ttu-id="99411-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="99411-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99411-112">Notes</span><span class="sxs-lookup"><span data-stu-id="99411-112">Remarks</span></span>

<span data-ttu-id="99411-113">Cette méthode d’événement est définie dans l' \_ interface IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="99411-113">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="99411-114">L' \_ interface IInkEvents implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ SEStrokesRemoved.</span><span class="sxs-lookup"><span data-stu-id="99411-114">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="99411-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99411-115">Requirements</span></span>



| <span data-ttu-id="99411-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99411-116">Requirement</span></span> | <span data-ttu-id="99411-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="99411-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99411-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99411-118">Minimum supported client</span></span><br/> | <span data-ttu-id="99411-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99411-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="99411-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99411-120">Minimum supported server</span></span><br/> | <span data-ttu-id="99411-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="99411-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="99411-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="99411-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="99411-123"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="99411-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="99411-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99411-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="99411-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99411-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="99411-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99411-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="99411-127">[Collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99411-127">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="99411-128">[**Supprimer la méthode \[ InkStrokes collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span><span class="sxs-lookup"><span data-stu-id="99411-128">[**Remove Method \[InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span></span>
</dt> <dt>

[<span data-ttu-id="99411-129">**InkDisp, classe**</span><span class="sxs-lookup"><span data-stu-id="99411-129">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> </dl>

 

