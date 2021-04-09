---
title: IMsRdpClientAdvancedSettings propriété BitmapVirtualCacheSize
description: Spécifie la taille, en mégaoctets, du fichier cache de bitmaps persistant à utiliser pour la couleur de 8 bits par pixel.
ms.assetid: 4efcabd2-8671-40a3-ad12-af0b2b6e495a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BitmapVirtualCacheSize
- Services Bureau à distance de la propriété BitmapVirtualCacheSize, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété BitmapVirtualCacheSize
- Services Bureau à distance de la propriété BitmapVirtualCacheSize, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété BitmapVirtualCacheSize
- Services Bureau à distance de la propriété BitmapVirtualCacheSize, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété BitmapVirtualCacheSize
- Services Bureau à distance de la propriété BitmapVirtualCacheSize, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété BitmapVirtualCacheSize
- Services Bureau à distance de la propriété BitmapVirtualCacheSize, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété BitmapVirtualCacheSize
- Services Bureau à distance de la propriété BitmapVirtualCacheSize, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété BitmapVirtualCacheSize
- Services Bureau à distance de la propriété BitmapVirtualCacheSize, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété BitmapVirtualCacheSize
- Services Bureau à distance de la propriété BitmapVirtualCacheSize, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété BitmapVirtualCacheSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb652c0f235cf7438b49e68a544188ac4622acad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032584"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcachesize-property"></a><span data-ttu-id="99be0-120">IMsRdpClientAdvancedSettings :: BitmapVirtualCacheSize, propriété</span><span class="sxs-lookup"><span data-stu-id="99be0-120">IMsRdpClientAdvancedSettings::BitmapVirtualCacheSize property</span></span>

<span data-ttu-id="99be0-121">Spécifie la taille, en mégaoctets, du fichier cache de bitmaps persistant à utiliser pour la couleur de 8 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="99be0-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for 8-bits-per-pixel color.</span></span>

<span data-ttu-id="99be0-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="99be0-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="99be0-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99be0-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCacheSize(
  [in]  LONG bitmapVirtualCacheSize
);

HRESULT get_BitmapVirtualCacheSize(
  [out] LONG *pbitmapVirtualCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="99be0-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="99be0-124">Property value</span></span>

<span data-ttu-id="99be0-125">Nouvelle taille du cache.</span><span class="sxs-lookup"><span data-stu-id="99be0-125">The new cache size.</span></span> <span data-ttu-id="99be0-126">Les valeurs valides sont comprises entre 1 et 32 inclus.</span><span class="sxs-lookup"><span data-stu-id="99be0-126">The valid values are 1 to 32 inclusive.</span></span> <span data-ttu-id="99be0-127">Notez que la taille maximale de tous les fichiers de cache virtuel est de 128 Mo.</span><span class="sxs-lookup"><span data-stu-id="99be0-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="99be0-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="99be0-128">Error codes</span></span>

<span data-ttu-id="99be0-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="99be0-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="99be0-130">Notes</span><span class="sxs-lookup"><span data-stu-id="99be0-130">Remarks</span></span>

<span data-ttu-id="99be0-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="99be0-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99be0-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99be0-132">Requirements</span></span>



| <span data-ttu-id="99be0-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99be0-133">Requirement</span></span> | <span data-ttu-id="99be0-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="99be0-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99be0-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99be0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="99be0-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99be0-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="99be0-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99be0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="99be0-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99be0-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="99be0-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="99be0-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="99be0-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99be0-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="99be0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="99be0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99be0-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99be0-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="99be0-143">IID</span><span class="sxs-lookup"><span data-stu-id="99be0-143">IID</span></span><br/>                      | <span data-ttu-id="99be0-144">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="99be0-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99be0-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99be0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99be0-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="99be0-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="99be0-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="99be0-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="99be0-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="99be0-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="99be0-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="99be0-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="99be0-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="99be0-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="99be0-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="99be0-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="99be0-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="99be0-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="99be0-153">**BitmapVirtualCache16BppSize**</span><span class="sxs-lookup"><span data-stu-id="99be0-153">**BitmapVirtualCache16BppSize**</span></span>](imsrdpclientadvancedsettings-bitmapvirtualcache16bppsize.md)
</dt> <dt>

[<span data-ttu-id="99be0-154">**BitmapVirtualCache24BppSize**</span><span class="sxs-lookup"><span data-stu-id="99be0-154">**BitmapVirtualCache24BppSize**</span></span>](imsrdpclientadvancedsettings-bitmapvirtualcache24bppsize.md)
</dt> <dt>

[<span data-ttu-id="99be0-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="99be0-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





