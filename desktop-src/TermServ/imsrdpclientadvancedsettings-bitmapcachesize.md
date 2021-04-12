---
title: IMsRdpClientAdvancedSettings propriété BitmapCacheSize
description: Taille, en kilo-octets, du fichier de cache bitmap utilisé pour les bitmaps de 8 bits par pixel.
ms.assetid: a2a4b739-0fa3-4a76-87ae-3cba913b7703
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BitmapCacheSize
- Services Bureau à distance de la propriété BitmapCacheSize, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété BitmapCacheSize
- Services Bureau à distance de la propriété BitmapCacheSize, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété BitmapCacheSize
- Services Bureau à distance de la propriété BitmapCacheSize, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété BitmapCacheSize
- Services Bureau à distance de la propriété BitmapCacheSize, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété BitmapCacheSize
- Services Bureau à distance de la propriété BitmapCacheSize, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété BitmapCacheSize
- Services Bureau à distance de la propriété BitmapCacheSize, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété BitmapCacheSize
- Services Bureau à distance de la propriété BitmapCacheSize, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété BitmapCacheSize
- Services Bureau à distance de la propriété BitmapCacheSize, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété BitmapCacheSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.BitmapCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.BitmapCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.BitmapCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.BitmapCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.BitmapCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.BitmapCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.BitmapCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a38376bb0b06bd4efea36d3c4cad4e4aec0f35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384324"
---
# <a name="imsrdpclientadvancedsettingsbitmapcachesize-property"></a><span data-ttu-id="eba19-120">IMsRdpClientAdvancedSettings :: BitmapCacheSize, propriété</span><span class="sxs-lookup"><span data-stu-id="eba19-120">IMsRdpClientAdvancedSettings::BitmapCacheSize property</span></span>

<span data-ttu-id="eba19-121">Taille, en kilo-octets, du fichier de cache bitmap utilisé pour les bitmaps de 8 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="eba19-121">The size, in kilobytes, of the bitmap cache file used for 8-bits-per-pixel bitmaps.</span></span>

<span data-ttu-id="eba19-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="eba19-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba19-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eba19-123">Syntax</span></span>


```C++
HRESULT put_BitmapCacheSize(
  [in]  LONG bitmapCacheSize
);

HRESULT get_BitmapCacheSize(
  [out] LONG *pbitmapCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="eba19-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="eba19-124">Property value</span></span>

<span data-ttu-id="eba19-125">Nouvelle taille du cache, en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="eba19-125">The new cache size, in kilobytes.</span></span> <span data-ttu-id="eba19-126">Les valeurs numériques valides sont comprises entre 1 et 32 inclus.</span><span class="sxs-lookup"><span data-stu-id="eba19-126">The valid numeric values are 1 to 32 inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eba19-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="eba19-127">Error codes</span></span>

<span data-ttu-id="eba19-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="eba19-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="eba19-129">Notes</span><span class="sxs-lookup"><span data-stu-id="eba19-129">Remarks</span></span>

<span data-ttu-id="eba19-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="eba19-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eba19-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eba19-131">Requirements</span></span>



| <span data-ttu-id="eba19-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eba19-132">Requirement</span></span> | <span data-ttu-id="eba19-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="eba19-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eba19-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eba19-134">Minimum supported client</span></span><br/> | <span data-ttu-id="eba19-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eba19-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="eba19-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eba19-136">Minimum supported server</span></span><br/> | <span data-ttu-id="eba19-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eba19-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="eba19-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="eba19-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="eba19-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eba19-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="eba19-140">DLL</span><span class="sxs-lookup"><span data-stu-id="eba19-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eba19-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eba19-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="eba19-142">IID</span><span class="sxs-lookup"><span data-stu-id="eba19-142">IID</span></span><br/>                      | <span data-ttu-id="eba19-143">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="eba19-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eba19-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eba19-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eba19-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="eba19-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="eba19-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="eba19-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="eba19-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="eba19-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="eba19-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="eba19-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="eba19-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="eba19-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="eba19-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="eba19-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="eba19-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="eba19-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="eba19-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="eba19-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





