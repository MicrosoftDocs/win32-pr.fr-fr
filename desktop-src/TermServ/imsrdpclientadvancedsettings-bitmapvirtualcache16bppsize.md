---
title: IMsRdpClientAdvancedSettings propriété BitmapVirtualCache16BppSize
description: Spécifie la taille, en mégaoctets, du fichier cache de bitmaps persistant à utiliser pour les paramètres de haute couleur de 15 et 16 bits par pixel.
ms.assetid: f2558c88-d60f-4be3-9941-8e0e18bbb778
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BitmapVirtualCache16BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache16BppSize, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété BitmapVirtualCache16BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache16BppSize, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété BitmapVirtualCache16BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache16BppSize, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété BitmapVirtualCache16BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache16BppSize, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété BitmapVirtualCache16BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache16BppSize, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété BitmapVirtualCache16BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache16BppSize, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété BitmapVirtualCache16BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache16BppSize, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété BitmapVirtualCache16BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache16BppSize, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété BitmapVirtualCache16BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache16BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fd0a11a1cf3b313c1f6f2c12d1a73b61c6f45a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540768"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcache16bppsize-property"></a><span data-ttu-id="20745-120">IMsRdpClientAdvancedSettings :: BitmapVirtualCache16BppSize, propriété</span><span class="sxs-lookup"><span data-stu-id="20745-120">IMsRdpClientAdvancedSettings::BitmapVirtualCache16BppSize property</span></span>

<span data-ttu-id="20745-121">Spécifie la taille, en mégaoctets, du fichier cache de bitmaps persistant à utiliser pour les paramètres de haute couleur de 15 et 16 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="20745-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for the 15 and 16 bits-per-pixel high-color settings.</span></span>

<span data-ttu-id="20745-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="20745-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="20745-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20745-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache16BppSize(
  [in]  LONG bitmapVirtualCache16BppSize
);

HRESULT get_BitmapVirtualCache16BppSize(
  [out] LONG *pbitmapVirtualCache16BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="20745-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="20745-124">Property value</span></span>

<span data-ttu-id="20745-125">Nouvelle taille du cache.</span><span class="sxs-lookup"><span data-stu-id="20745-125">The new cache size.</span></span> <span data-ttu-id="20745-126">Les valeurs valides sont comprises entre 1 et 32 inclus, et la valeur par défaut est 20.</span><span class="sxs-lookup"><span data-stu-id="20745-126">The valid values are 1 to 32 inclusive, and the default value is 20.</span></span> <span data-ttu-id="20745-127">Notez que la taille maximale de tous les fichiers de cache virtuel est de 128 Mo.</span><span class="sxs-lookup"><span data-stu-id="20745-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="20745-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="20745-128">Error codes</span></span>

<span data-ttu-id="20745-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="20745-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="20745-130">Notes</span><span class="sxs-lookup"><span data-stu-id="20745-130">Remarks</span></span>

<span data-ttu-id="20745-131">Les propriétés associées incluent les propriétés **BitmapVirtualCacheSize** et **BitmapVirtualCache24BppSize** .</span><span class="sxs-lookup"><span data-stu-id="20745-131">Related properties include the **BitmapVirtualCacheSize** and **BitmapVirtualCache24BppSize** properties.</span></span>

<span data-ttu-id="20745-132">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="20745-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20745-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20745-133">Requirements</span></span>



| <span data-ttu-id="20745-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20745-134">Requirement</span></span> | <span data-ttu-id="20745-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="20745-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20745-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20745-136">Minimum supported client</span></span><br/> | <span data-ttu-id="20745-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20745-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="20745-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20745-138">Minimum supported server</span></span><br/> | <span data-ttu-id="20745-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20745-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="20745-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="20745-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="20745-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20745-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="20745-142">DLL</span><span class="sxs-lookup"><span data-stu-id="20745-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20745-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20745-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="20745-144">IID</span><span class="sxs-lookup"><span data-stu-id="20745-144">IID</span></span><br/>                      | <span data-ttu-id="20745-145">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="20745-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20745-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20745-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20745-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="20745-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="20745-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="20745-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="20745-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="20745-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="20745-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="20745-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="20745-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="20745-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="20745-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="20745-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="20745-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="20745-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="20745-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="20745-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





