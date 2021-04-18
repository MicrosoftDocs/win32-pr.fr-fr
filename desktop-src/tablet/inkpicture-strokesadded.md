---
description: Se produit lorsqu’un ou plusieurs objets IInkStrokeDisp sont ajoutés à la collection InkStrokes.
ms.assetid: 577ad52b-ecd3-4a49-8997-481ebdb47203
title: InkPicture. StrokesAdded, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e79d87a4315068cbb0cf9db25b6532bc4c09943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526180"
---
# <a name="inkpicturestrokesadded-event"></a><span data-ttu-id="a3100-103">InkPicture. StrokesAdded, événement</span><span class="sxs-lookup"><span data-stu-id="a3100-103">InkPicture.StrokesAdded event</span></span>

<span data-ttu-id="a3100-104">Se produit lorsqu’un ou plusieurs objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) sont ajoutés à la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a3100-104">Occurs when one or more [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3100-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3100-105">Syntax</span></span>


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="a3100-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3100-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3100-107">*StrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3100-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3100-108">Tableau d’entiers des identificateurs pour chaque objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ajouté lorsque cet événement se produit.</span><span class="sxs-lookup"><span data-stu-id="a3100-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object added when this event occurs.</span></span>

<span data-ttu-id="a3100-109">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="a3100-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3100-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3100-110">Return value</span></span>

<span data-ttu-id="a3100-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a3100-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3100-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a3100-112">Remarks</span></span>

<span data-ttu-id="a3100-113">Cette méthode d’événement est définie dans l’interface **\_ IInkStrokesEvents** .</span><span class="sxs-lookup"><span data-stu-id="a3100-113">This event method is defined in the **\_IInkStrokesEvents** interface.</span></span> <span data-ttu-id="a3100-114">L’interface **\_ IInkStrokesEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ SEStrokesAdded.</span><span class="sxs-lookup"><span data-stu-id="a3100-114">The **\_IInkStrokesEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3100-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3100-115">Requirements</span></span>



| <span data-ttu-id="a3100-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3100-116">Requirement</span></span> | <span data-ttu-id="a3100-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3100-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3100-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3100-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a3100-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3100-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a3100-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3100-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a3100-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3100-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a3100-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3100-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3100-123"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a3100-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a3100-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a3100-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3100-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3100-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a3100-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3100-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3100-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="a3100-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

