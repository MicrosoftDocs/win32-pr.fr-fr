---
title: Message STM_GETIMAGE (winuser. h)
description: Une application envoie un \_ message STM GETIMAGE pour récupérer un handle de l’image (icône ou bitmap) associé à un contrôle statique.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- STM_GETIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032413"
---
# <a name="stm_getimage-message"></a><span data-ttu-id="accc4-104">\_Message GETIMAGE STM</span><span class="sxs-lookup"><span data-stu-id="accc4-104">STM\_GETIMAGE message</span></span>

<span data-ttu-id="accc4-105">Une application envoie un message **STM \_ GETIMAGE** pour récupérer un handle de l’image (icône ou bitmap) associé à un contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="accc4-105">An application sends an **STM\_GETIMAGE** message to retrieve a handle to the image (icon or bitmap) associated with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="accc4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="accc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="accc4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="accc4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="accc4-108">Spécifie le type d’image à récupérer.</span><span class="sxs-lookup"><span data-stu-id="accc4-108">Specifies the type of image to retrieve.</span></span> <span data-ttu-id="accc4-109">Ce paramètre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="accc4-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="accc4-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="accc4-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="accc4-111">Signification</span><span class="sxs-lookup"><span data-stu-id="accc4-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="accc4-112"><dt>**IMAGE \_ bitmap**</dt></span><span class="sxs-lookup"><span data-stu-id="accc4-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="accc4-113">Pixels.</span><span class="sxs-lookup"><span data-stu-id="accc4-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="accc4-114"><dt>**curseur d’IMAGE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="accc4-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="accc4-115">Mire.</span><span class="sxs-lookup"><span data-stu-id="accc4-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="accc4-116"><dt>**IMAGE \_ ENHMETAFILE**</dt></span><span class="sxs-lookup"><span data-stu-id="accc4-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="accc4-117">Métafichier amélioré.</span><span class="sxs-lookup"><span data-stu-id="accc4-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="accc4-118"><dt>**icône d’IMAGE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="accc4-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="accc4-119">Située.</span><span class="sxs-lookup"><span data-stu-id="accc4-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="accc4-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="accc4-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="accc4-121">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="accc4-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="accc4-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="accc4-122">Return value</span></span>

<span data-ttu-id="accc4-123">La valeur de retour est un handle vers l’image, le cas échéant ; dans le cas contraire, la **valeur est null**.</span><span class="sxs-lookup"><span data-stu-id="accc4-123">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="accc4-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="accc4-124">Requirements</span></span>



| <span data-ttu-id="accc4-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="accc4-125">Requirement</span></span> | <span data-ttu-id="accc4-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="accc4-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="accc4-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="accc4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="accc4-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="accc4-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="accc4-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="accc4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="accc4-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="accc4-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="accc4-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="accc4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="accc4-132"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="accc4-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="accc4-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="accc4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="accc4-134">**\_SETIMAGE STM**</span><span class="sxs-lookup"><span data-stu-id="accc4-134">**STM\_SETIMAGE**</span></span>](stm-setimage.md)
</dt> </dl>

 

 





