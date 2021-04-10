---
title: Message STM_SETIMAGE (winuser. h)
description: Une application envoie un \_ message STM SETIMAGE pour associer une nouvelle image à un contrôle statique.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- STM_SETIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941797"
---
# <a name="stm_setimage-message"></a><span data-ttu-id="cb7cf-104">\_Message SETIMAGE STM</span><span class="sxs-lookup"><span data-stu-id="cb7cf-104">STM\_SETIMAGE message</span></span>

<span data-ttu-id="cb7cf-105">Une application envoie un message **STM \_ SETIMAGE** pour associer une nouvelle image à un contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-105">An application sends an **STM\_SETIMAGE** message to associate a new image with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb7cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb7cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb7cf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb7cf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb7cf-108">Spécifie le type d’image à associer au contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-108">Specifies the type of image to associate with the static control.</span></span> <span data-ttu-id="cb7cf-109">Ce paramètre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb7cf-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="cb7cf-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb7cf-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="cb7cf-111">Signification</span><span class="sxs-lookup"><span data-stu-id="cb7cf-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="cb7cf-112"><dt>**IMAGE \_ bitmap**</dt></span><span class="sxs-lookup"><span data-stu-id="cb7cf-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="cb7cf-113">Pixels.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="cb7cf-114"><dt>**curseur d’IMAGE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cb7cf-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="cb7cf-115">Mire.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="cb7cf-116"><dt>**IMAGE \_ ENHMETAFILE**</dt></span><span class="sxs-lookup"><span data-stu-id="cb7cf-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="cb7cf-117">Métafichier amélioré.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="cb7cf-118"><dt>**icône d’IMAGE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cb7cf-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="cb7cf-119">Située.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="cb7cf-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb7cf-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb7cf-121">Handle de l’image à associer au contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-121">Handle to the image to associate with the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb7cf-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb7cf-122">Return value</span></span>

<span data-ttu-id="cb7cf-123">La valeur de retour est un handle vers l’image précédemment associée au contrôle statique, le cas échéant ; dans le cas contraire, la **valeur est null**.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-123">The return value is a handle to the image previously associated with the static control, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb7cf-124">Notes</span><span class="sxs-lookup"><span data-stu-id="cb7cf-124">Remarks</span></span>

<span data-ttu-id="cb7cf-125">Pour associer une image à un contrôle statique, le contrôle doit avoir le style approprié.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-125">To associate an image with a static control, the control must have the proper style.</span></span> <span data-ttu-id="cb7cf-126">Le tableau suivant indique le style requis pour chaque type d’image.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-126">The following table shows the style needed for each image type.</span></span>



| <span data-ttu-id="cb7cf-127">Type d’image</span><span class="sxs-lookup"><span data-stu-id="cb7cf-127">Image type</span></span>         | <span data-ttu-id="cb7cf-128">Style de contrôle statique</span><span class="sxs-lookup"><span data-stu-id="cb7cf-128">Static control style</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="cb7cf-129">IMAGE \_ bitmap</span><span class="sxs-lookup"><span data-stu-id="cb7cf-129">IMAGE\_BITMAP</span></span>      | <span data-ttu-id="cb7cf-130">\_bitmap SS</span><span class="sxs-lookup"><span data-stu-id="cb7cf-130">SS\_BITMAP</span></span>           |
| <span data-ttu-id="cb7cf-131">curseur d’IMAGE \_</span><span class="sxs-lookup"><span data-stu-id="cb7cf-131">IMAGE\_CURSOR</span></span>      | <span data-ttu-id="cb7cf-132">\_icône SS</span><span class="sxs-lookup"><span data-stu-id="cb7cf-132">SS\_ICON</span></span>             |
| <span data-ttu-id="cb7cf-133">IMAGE \_ ENHMETAFILE</span><span class="sxs-lookup"><span data-stu-id="cb7cf-133">IMAGE\_ENHMETAFILE</span></span> | <span data-ttu-id="cb7cf-134">\_ENHMETAFILE SS</span><span class="sxs-lookup"><span data-stu-id="cb7cf-134">SS\_ENHMETAFILE</span></span>      |
| <span data-ttu-id="cb7cf-135">icône d’IMAGE \_</span><span class="sxs-lookup"><span data-stu-id="cb7cf-135">IMAGE\_ICON</span></span>        | <span data-ttu-id="cb7cf-136">\_icône SS</span><span class="sxs-lookup"><span data-stu-id="cb7cf-136">SS\_ICON</span></span>             |



 

> [!IMPORTANT]
>
> <span data-ttu-id="cb7cf-137">Dans la version 6 des contrôles Microsoft Win32, une image bitmap transmise à un contrôle statique à l’aide du message **\_ SETIMAGE STM** était la même bitmap que celle retournée par un message **\_ SETIMAGE STM** suivant.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-137">In version 6 of the Microsoft Win32 controls, a bitmap passed to a static control using the **STM\_SETIMAGE** message was the same bitmap returned by a subsequent **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="cb7cf-138">Le client est chargé de supprimer toute bitmap envoyée à un contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-138">The client is responsible to delete any bitmap sent to a static control.</span></span>
>
> <span data-ttu-id="cb7cf-139">Avec Windows XP, si la bitmap transmise dans le message **STM \_ SETIMAGE** contient des pixels avec une valeur alpha différente de zéro, le contrôle statique prend une copie de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-139">With Windows XP, if the bitmap passed in the **STM\_SETIMAGE** message contains pixels with nonzero alpha, the static control takes a copy of the bitmap.</span></span> <span data-ttu-id="cb7cf-140">Cette bitmap copiée est retournée par le prochain message **\_ SETIMAGE STM** .</span><span class="sxs-lookup"><span data-stu-id="cb7cf-140">This copied bitmap is returned by the next **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="cb7cf-141">Le code client peut suivre indépendamment les bitmaps transmises au contrôle statique, mais s’il ne vérifie pas et ne libère pas les bitmaps retournées par les messages **STM \_ SETIMAGE** , les bitmaps sont divulguées.</span><span class="sxs-lookup"><span data-stu-id="cb7cf-141">The client code may independently track the bitmaps passed to the static control, but if it does not check and release the bitmaps returned from **STM\_SETIMAGE** messages, the bitmaps are leaked.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb7cf-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb7cf-142">Requirements</span></span>



| <span data-ttu-id="cb7cf-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb7cf-143">Requirement</span></span> | <span data-ttu-id="cb7cf-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb7cf-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb7cf-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb7cf-145">Minimum supported client</span></span><br/> | <span data-ttu-id="cb7cf-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb7cf-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb7cf-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb7cf-147">Minimum supported server</span></span><br/> | <span data-ttu-id="cb7cf-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb7cf-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb7cf-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb7cf-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb7cf-150"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb7cf-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb7cf-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb7cf-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb7cf-152">**STM \_ GETIMAGE**</span><span class="sxs-lookup"><span data-stu-id="cb7cf-152">**STM\_GETIMAGE**</span></span>](stm-getimage.md)
</dt> </dl>

 

 





