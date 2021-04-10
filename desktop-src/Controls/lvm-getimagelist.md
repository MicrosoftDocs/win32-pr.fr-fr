---
title: Message LVM_GETIMAGELIST (commctrl. h)
description: Récupère le handle d’une liste d’images utilisée pour dessiner des éléments de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetImageList.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- LVM_GETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104452"
---
# <a name="lvm_getimagelist-message"></a><span data-ttu-id="24e2b-105">\_Message GETIMAGELIST LVM</span><span class="sxs-lookup"><span data-stu-id="24e2b-105">LVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="24e2b-106">Récupère le handle d’une liste d’images utilisée pour dessiner des éléments de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="24e2b-106">Retrieves the handle to an image list used for drawing list-view items.</span></span> <span data-ttu-id="24e2b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="24e2b-107">You can send this message explicitly or by using the [**ListView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="24e2b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24e2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24e2b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24e2b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24e2b-110">Liste d’images à récupérer.</span><span class="sxs-lookup"><span data-stu-id="24e2b-110">Image list to retrieve.</span></span> <span data-ttu-id="24e2b-111">Ce paramètre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="24e2b-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="24e2b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e2b-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="24e2b-113">Signification</span><span class="sxs-lookup"><span data-stu-id="24e2b-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="24e2b-114"><dt>**LVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="24e2b-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="24e2b-115">Liste d’images avec grandes icônes.</span><span class="sxs-lookup"><span data-stu-id="24e2b-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="24e2b-116"><dt>**LVSIL \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="24e2b-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="24e2b-117">Liste d’images avec petites icônes.</span><span class="sxs-lookup"><span data-stu-id="24e2b-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="24e2b-118"><dt>**État de LVSIL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="24e2b-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="24e2b-119">Liste d’images avec images d’État.</span><span class="sxs-lookup"><span data-stu-id="24e2b-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="24e2b-120"><dt>**LVSIL \_ GROUPHEADER**</dt></span><span class="sxs-lookup"><span data-stu-id="24e2b-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="24e2b-121">Liste d’images pour l’en-tête de groupe.</span><span class="sxs-lookup"><span data-stu-id="24e2b-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="24e2b-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24e2b-122">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="24e2b-123">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="24e2b-123">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24e2b-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24e2b-124">Return value</span></span>

<span data-ttu-id="24e2b-125">Retourne le handle de la liste d’images spécifiée en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="24e2b-125">Returns the handle to the specified image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="24e2b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24e2b-126">Requirements</span></span>



| <span data-ttu-id="24e2b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24e2b-127">Requirement</span></span> | <span data-ttu-id="24e2b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e2b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24e2b-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24e2b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="24e2b-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24e2b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24e2b-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24e2b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="24e2b-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24e2b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24e2b-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="24e2b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="24e2b-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="24e2b-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





