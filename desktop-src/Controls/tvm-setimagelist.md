---
title: Message TVM_SETIMAGELIST (commctrl. h)
description: Définit la liste d’images normale ou d’État pour un contrôle d’arborescence et redessine le contrôle à l’aide des nouvelles images. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetImageList TreeView.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- TVM_SETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741556"
---
# <a name="tvm_setimagelist-message"></a><span data-ttu-id="c2cbf-105">TVM \_ SETIMAGELIST message</span><span class="sxs-lookup"><span data-stu-id="c2cbf-105">TVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="c2cbf-106">Définit la liste d’images normale ou d’État pour un contrôle d’arborescence et redessine le contrôle à l’aide des nouvelles images.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-106">Sets the normal or state image list for a tree-view control and redraws the control using the new images.</span></span> <span data-ttu-id="c2cbf-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetImageList TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="c2cbf-107">You can send this message explicitly or by using the [**TreeView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2cbf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2cbf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2cbf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2cbf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cbf-110">Type de liste d’images à définir.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-110">Type of image list to set.</span></span> <span data-ttu-id="c2cbf-111">Ce paramètre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2cbf-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="c2cbf-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2cbf-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="c2cbf-113">Signification</span><span class="sxs-lookup"><span data-stu-id="c2cbf-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="c2cbf-114"><dt>**TVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="c2cbf-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="c2cbf-115">Indique la liste d’images normale, qui contient les images sélectionnées, non sélectionnées et de superposition pour les éléments d’un contrôle d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="c2cbf-116"><dt>**État de TVSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2cbf-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="c2cbf-117">Indique la liste d’images d’État.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-117">Indicates the state image list.</span></span> <span data-ttu-id="c2cbf-118">Vous pouvez utiliser des images d’État pour indiquer les États des éléments définis par l’application.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="c2cbf-119">Une image d’État s’affiche à gauche de l’image sélectionnée ou non sélectionnée d’un élément.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c2cbf-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2cbf-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cbf-121">Handle de la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-121">Handle to the image list.</span></span> <span data-ttu-id="c2cbf-122">Si *lParam* a la **valeur null**, le message supprime la liste d’images spécifiée du contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-122">If *lParam* is **NULL**, the message removes the specified image list from the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2cbf-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2cbf-123">Return value</span></span>

<span data-ttu-id="c2cbf-124">Retourne le handle vers la liste d’images précédente, le cas échéant, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-124">Returns the handle to the previous image list, if any, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2cbf-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c2cbf-125">Remarks</span></span>

<span data-ttu-id="c2cbf-126">Le contrôle Tree-View ne détruit pas la liste d’images spécifiée avec ce message.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-126">The tree-view control will not destroy the image list specified with this message.</span></span> <span data-ttu-id="c2cbf-127">Votre application doit détruire la liste d’images lorsqu’elle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c2cbf-127">Your application must destroy the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2cbf-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2cbf-128">Requirements</span></span>



| <span data-ttu-id="c2cbf-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2cbf-129">Requirement</span></span> | <span data-ttu-id="c2cbf-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2cbf-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cbf-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2cbf-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c2cbf-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2cbf-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2cbf-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2cbf-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c2cbf-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2cbf-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2cbf-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2cbf-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2cbf-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2cbf-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2cbf-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2cbf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2cbf-138">**TVM \_ GETIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="c2cbf-138">**TVM\_GETIMAGELIST**</span></span>](tvm-getimagelist.md)
</dt> </dl>

 

 





