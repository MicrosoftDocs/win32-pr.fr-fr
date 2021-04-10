---
title: Message LVM_SETIMAGELIST (commctrl. h)
description: Affecte une liste d’images à un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetImageList.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- LVM_SETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 779d31fd781a72dbdfbc4738e091482ca4a08528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941670"
---
# <a name="lvm_setimagelist-message"></a><span data-ttu-id="ed723-105">\_Message SETIMAGELIST LVM</span><span class="sxs-lookup"><span data-stu-id="ed723-105">LVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="ed723-106">Affecte une liste d’images à un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="ed723-106">Assigns an image list to a list-view control.</span></span> <span data-ttu-id="ed723-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="ed723-107">You can send this message explicitly or by using the [**ListView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed723-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed723-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed723-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed723-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed723-110">Type de liste d’images.</span><span class="sxs-lookup"><span data-stu-id="ed723-110">Type of image list.</span></span> <span data-ttu-id="ed723-111">Ce paramètre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ed723-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="ed723-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed723-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="ed723-113">Signification</span><span class="sxs-lookup"><span data-stu-id="ed723-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="ed723-114"><dt>**LVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="ed723-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="ed723-115">Liste d’images avec grandes icônes.</span><span class="sxs-lookup"><span data-stu-id="ed723-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="ed723-116"><dt>**LVSIL \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="ed723-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="ed723-117">Liste d’images avec petites icônes.</span><span class="sxs-lookup"><span data-stu-id="ed723-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="ed723-118"><dt>**État de LVSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed723-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="ed723-119">Liste d’images avec images d’État.</span><span class="sxs-lookup"><span data-stu-id="ed723-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="ed723-120"><dt>**LVSIL \_ GROUPHEADER**</dt></span><span class="sxs-lookup"><span data-stu-id="ed723-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="ed723-121">Liste d’images pour l’en-tête de groupe.</span><span class="sxs-lookup"><span data-stu-id="ed723-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="ed723-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed723-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed723-123">Handle de la liste d’images à assigner.</span><span class="sxs-lookup"><span data-stu-id="ed723-123">Handle to the image list to assign.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed723-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed723-124">Return value</span></span>

<span data-ttu-id="ed723-125">Retourne le handle de la liste d’images précédemment associée au contrôle en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ed723-125">Returns the handle to the image list previously associated with the control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed723-126">Notes</span><span class="sxs-lookup"><span data-stu-id="ed723-126">Remarks</span></span>

<span data-ttu-id="ed723-127">La liste d’images actuelle sera détruite quand le contrôle de liste est détruit, sauf si le style [**LVS \_ SHAREIMAGELISTS**](list-view-window-styles.md) est défini.</span><span class="sxs-lookup"><span data-stu-id="ed723-127">The current image list will be destroyed when the list-view control is destroyed unless the [**LVS\_SHAREIMAGELISTS**](list-view-window-styles.md) style is set.</span></span> <span data-ttu-id="ed723-128">Si vous utilisez ce message pour remplacer une liste d’images par une autre, votre application doit détruire explicitement toutes les listes d’images autres que la liste actuelle.</span><span class="sxs-lookup"><span data-stu-id="ed723-128">If you use this message to replace one image list with another, your application must explicitly destroy all image lists other than the current one.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed723-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed723-129">Requirements</span></span>



| <span data-ttu-id="ed723-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed723-130">Requirement</span></span> | <span data-ttu-id="ed723-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed723-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed723-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed723-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ed723-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed723-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed723-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed723-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ed723-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed723-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed723-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed723-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed723-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed723-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





