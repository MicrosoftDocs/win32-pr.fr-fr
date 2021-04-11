---
title: Message BM_SETIMAGE (winuser. h)
description: Associe une nouvelle image (icône ou bitmap) au bouton.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- BM_SETIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d083c4fb509d51eb017bb7d3d38fab07b4c006
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103133"
---
# <a name="bm_setimage-message"></a><span data-ttu-id="12c77-104">\_Message SETIMAGE BM</span><span class="sxs-lookup"><span data-stu-id="12c77-104">BM\_SETIMAGE message</span></span>

<span data-ttu-id="12c77-105">Associe une nouvelle image (icône ou bitmap) au bouton.</span><span class="sxs-lookup"><span data-stu-id="12c77-105">Associates a new image (icon or bitmap) with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="12c77-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12c77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c77-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12c77-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12c77-108">Type d’image à associer au bouton.</span><span class="sxs-lookup"><span data-stu-id="12c77-108">The type of image to associate with the button.</span></span> <span data-ttu-id="12c77-109">Ce paramètre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="12c77-109">This parameter can be one of the following values:</span></span>

-   <span data-ttu-id="12c77-110">IMAGE \_ bitmap</span><span class="sxs-lookup"><span data-stu-id="12c77-110">IMAGE\_BITMAP</span></span>
-   <span data-ttu-id="12c77-111">icône d’IMAGE \_</span><span class="sxs-lookup"><span data-stu-id="12c77-111">IMAGE\_ICON</span></span>

</dd> <dt>

<span data-ttu-id="12c77-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12c77-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12c77-113">Handle (**HICON** ou **HBITMAP**) de l’image à associer au bouton.</span><span class="sxs-lookup"><span data-stu-id="12c77-113">A handle (**HICON** or **HBITMAP**) to the image to associate with the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12c77-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12c77-114">Return value</span></span>

<span data-ttu-id="12c77-115">La valeur de retour est un handle vers l’image précédemment associée au bouton, le cas échéant ; dans le cas contraire, la **valeur est null**.</span><span class="sxs-lookup"><span data-stu-id="12c77-115">The return value is a handle to the image previously associated with the button, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="12c77-116">Notes</span><span class="sxs-lookup"><span data-stu-id="12c77-116">Remarks</span></span>

<span data-ttu-id="12c77-117">L’apparence du texte, une icône ou les deux sur un contrôle Button dépend de l' [**\_ icône BS**](button-styles.md) et des styles [**\_ bitmap BS**](button-styles.md) , et de l’appel ou non du message **\_ SETIMAGE BM** .</span><span class="sxs-lookup"><span data-stu-id="12c77-117">The appearance of text, an icon, or both on a button control depends on the [**BS\_ICON**](button-styles.md) and [**BS\_BITMAP**](button-styles.md) styles, and whether the **BM\_SETIMAGE** message is called.</span></span> <span data-ttu-id="12c77-118">Les résultats possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="12c77-118">The possible results are as follows:</span></span>



| <span data-ttu-id="12c77-119">\_Icône BS ou \_ ensemble de bitmaps BS ?</span><span class="sxs-lookup"><span data-stu-id="12c77-119">BS\_ICON or BS\_BITMAP Set?</span></span> | <span data-ttu-id="12c77-120">BM \_ SETIMAGE appelé ?</span><span class="sxs-lookup"><span data-stu-id="12c77-120">BM\_SETIMAGE Called?</span></span> | <span data-ttu-id="12c77-121">Résultats</span><span class="sxs-lookup"><span data-stu-id="12c77-121">Result</span></span>              |
|-----------------------------|----------------------|---------------------|
| <span data-ttu-id="12c77-122">Oui</span><span class="sxs-lookup"><span data-stu-id="12c77-122">Yes</span></span>                         | <span data-ttu-id="12c77-123">Oui</span><span class="sxs-lookup"><span data-stu-id="12c77-123">Yes</span></span>                  | <span data-ttu-id="12c77-124">Afficher l’icône uniquement.</span><span class="sxs-lookup"><span data-stu-id="12c77-124">Show icon only.</span></span>     |
| <span data-ttu-id="12c77-125">Non</span><span class="sxs-lookup"><span data-stu-id="12c77-125">No</span></span>                          | <span data-ttu-id="12c77-126">Oui</span><span class="sxs-lookup"><span data-stu-id="12c77-126">Yes</span></span>                  | <span data-ttu-id="12c77-127">Affichez l’icône et le texte.</span><span class="sxs-lookup"><span data-stu-id="12c77-127">Show icon and text.</span></span> |
| <span data-ttu-id="12c77-128">Oui</span><span class="sxs-lookup"><span data-stu-id="12c77-128">Yes</span></span>                         | <span data-ttu-id="12c77-129">Non</span><span class="sxs-lookup"><span data-stu-id="12c77-129">No</span></span>                   | <span data-ttu-id="12c77-130">Afficher uniquement le texte.</span><span class="sxs-lookup"><span data-stu-id="12c77-130">Show text only.</span></span>     |
| <span data-ttu-id="12c77-131">Non</span><span class="sxs-lookup"><span data-stu-id="12c77-131">No</span></span>                          | <span data-ttu-id="12c77-132">Non</span><span class="sxs-lookup"><span data-stu-id="12c77-132">No</span></span>                   | <span data-ttu-id="12c77-133">Afficher le texte uniquement</span><span class="sxs-lookup"><span data-stu-id="12c77-133">Show text only</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="12c77-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12c77-134">Requirements</span></span>



| <span data-ttu-id="12c77-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12c77-135">Requirement</span></span> | <span data-ttu-id="12c77-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="12c77-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12c77-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12c77-137">Minimum supported client</span></span><br/> | <span data-ttu-id="12c77-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12c77-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12c77-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12c77-139">Minimum supported server</span></span><br/> | <span data-ttu-id="12c77-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12c77-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="12c77-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="12c77-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="12c77-142"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12c77-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12c77-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12c77-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c77-144">**GETIMAGE de BM \_**</span><span class="sxs-lookup"><span data-stu-id="12c77-144">**BM\_GETIMAGE**</span></span>](bm-getimage.md)
</dt> </dl>

 

 





