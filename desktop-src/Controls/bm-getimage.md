---
title: Message BM_GETIMAGE (winuser. h)
description: Récupère un handle vers l’image (icône ou bitmap) associée au bouton.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- BM_GETIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317365"
---
# <a name="bm_getimage-message"></a><span data-ttu-id="ed7d3-104">\_Message GETIMAGE de BM</span><span class="sxs-lookup"><span data-stu-id="ed7d3-104">BM\_GETIMAGE message</span></span>

<span data-ttu-id="ed7d3-105">Récupère un handle vers l’image (icône ou bitmap) associée au bouton.</span><span class="sxs-lookup"><span data-stu-id="ed7d3-105">Retrieves a handle to the image (icon or bitmap) associated with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed7d3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed7d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed7d3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed7d3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed7d3-108">Type d’image à associer au bouton.</span><span class="sxs-lookup"><span data-stu-id="ed7d3-108">The type of image to associate with the button.</span></span> <span data-ttu-id="ed7d3-109">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ed7d3-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ed7d3-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed7d3-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="ed7d3-111">Signification</span><span class="sxs-lookup"><span data-stu-id="ed7d3-111">Meaning</span></span>              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="ed7d3-112"><dt>**IMAGE \_ bitmap**</dt></span><span class="sxs-lookup"><span data-stu-id="ed7d3-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl> | <span data-ttu-id="ed7d3-113">Bitmap.</span><span class="sxs-lookup"><span data-stu-id="ed7d3-113">A bitmap.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="ed7d3-114"><dt>**icône d’IMAGE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed7d3-114"><dt>**IMAGE\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="ed7d3-115">icône ;</span><span class="sxs-lookup"><span data-stu-id="ed7d3-115">An icon.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="ed7d3-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed7d3-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed7d3-117">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="ed7d3-117">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed7d3-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed7d3-118">Return value</span></span>

<span data-ttu-id="ed7d3-119">La valeur de retour est un handle vers l’image, le cas échéant ; dans le cas contraire, la **valeur est null**.</span><span class="sxs-lookup"><span data-stu-id="ed7d3-119">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed7d3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed7d3-120">Requirements</span></span>



| <span data-ttu-id="ed7d3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed7d3-121">Requirement</span></span> | <span data-ttu-id="ed7d3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed7d3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7d3-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed7d3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ed7d3-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed7d3-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ed7d3-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed7d3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ed7d3-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed7d3-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ed7d3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed7d3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed7d3-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed7d3-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed7d3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed7d3-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed7d3-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ed7d3-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ed7d3-131">**\_SETIMAGE BM**</span><span class="sxs-lookup"><span data-stu-id="ed7d3-131">**BM\_SETIMAGE**</span></span>](bm-setimage.md)
</dt> <dt>

<span data-ttu-id="ed7d3-132">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ed7d3-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ed7d3-133">Boutons</span><span class="sxs-lookup"><span data-stu-id="ed7d3-133">Buttons</span></span>](buttons.md)
</dt> </dl>

 

 





