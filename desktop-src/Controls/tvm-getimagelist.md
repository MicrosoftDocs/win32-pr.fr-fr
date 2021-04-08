---
title: Message TVM_GETIMAGELIST (commctrl. h)
description: Récupère le handle de la liste d’images normale ou d’État associée à un contrôle d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetImageList TreeView.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- TVM_GETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4e2503d9c6d57743059ee1da3049a36ed17f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743389"
---
# <a name="tvm_getimagelist-message"></a><span data-ttu-id="bba33-105">TVM \_ GETIMAGELIST message</span><span class="sxs-lookup"><span data-stu-id="bba33-105">TVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="bba33-106">Récupère le handle de la liste d’images normale ou d’État associée à un contrôle d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="bba33-106">Retrieves the handle to the normal or state image list associated with a tree-view control.</span></span> <span data-ttu-id="bba33-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetImageList TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="bba33-107">You can send this message explicitly or by using the [**TreeView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bba33-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bba33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba33-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bba33-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bba33-110">Type de liste d’images à récupérer.</span><span class="sxs-lookup"><span data-stu-id="bba33-110">Type of image list to retrieve.</span></span> <span data-ttu-id="bba33-111">Ce paramètre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bba33-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="bba33-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="bba33-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="bba33-113">Signification</span><span class="sxs-lookup"><span data-stu-id="bba33-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="bba33-114"><dt>**TVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="bba33-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="bba33-115">Indique la liste d’images normale, qui contient les images sélectionnées, non sélectionnées et de superposition pour les éléments d’un contrôle d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="bba33-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="bba33-116"><dt>**État de TVSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bba33-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="bba33-117">Indique la liste d’images d’État.</span><span class="sxs-lookup"><span data-stu-id="bba33-117">Indicates the state image list.</span></span> <span data-ttu-id="bba33-118">Vous pouvez utiliser des images d’État pour indiquer les États des éléments définis par l’application.</span><span class="sxs-lookup"><span data-stu-id="bba33-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="bba33-119">Une image d’État s’affiche à gauche de l’image sélectionnée ou non sélectionnée d’un élément.</span><span class="sxs-lookup"><span data-stu-id="bba33-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bba33-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bba33-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bba33-121">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bba33-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba33-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bba33-122">Return value</span></span>

<span data-ttu-id="bba33-123">Retourne un handle HIMAGELIST à la liste d’images spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bba33-123">Returns an HIMAGELIST handle to the specified image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba33-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bba33-124">Requirements</span></span>



| <span data-ttu-id="bba33-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bba33-125">Requirement</span></span> | <span data-ttu-id="bba33-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="bba33-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bba33-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bba33-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bba33-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bba33-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bba33-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bba33-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bba33-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bba33-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bba33-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="bba33-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bba33-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bba33-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bba33-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bba33-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba33-134">**TVM \_ SETIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="bba33-134">**TVM\_SETIMAGELIST**</span></span>](tvm-setimagelist.md)
</dt> </dl>

 

 





