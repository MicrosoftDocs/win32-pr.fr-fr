---
title: IMsRdpClientAdvancedSettings propriété BitmapPersistence
description: Spécifie si la mise en cache des bitmaps persistante doit être utilisée. La mise en cache persistante peut améliorer les performances, mais nécessite de l’espace disque supplémentaire.
ms.assetid: ffaa9277-9dd7-4b2a-9de5-009b7e8766bc
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété BitmapPersistence
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapPersistence
- IMsRdpClientAdvancedSettings.get_BitmapPersistence
- IMsRdpClientAdvancedSettings.put_BitmapPersistence
- IMsRdpClientAdvancedSettings2.BitmapPersistence
- IMsRdpClientAdvancedSettings2.get_BitmapPersistence
- IMsRdpClientAdvancedSettings2.put_BitmapPersistence
- IMsRdpClientAdvancedSettings3.BitmapPersistence
- IMsRdpClientAdvancedSettings3.get_BitmapPersistence
- IMsRdpClientAdvancedSettings3.put_BitmapPersistence
- IMsRdpClientAdvancedSettings4.BitmapPersistence
- IMsRdpClientAdvancedSettings4.get_BitmapPersistence
- IMsRdpClientAdvancedSettings4.put_BitmapPersistence
- IMsRdpClientAdvancedSettings5.BitmapPersistence
- IMsRdpClientAdvancedSettings5.get_BitmapPersistence
- IMsRdpClientAdvancedSettings5.put_BitmapPersistence
- IMsRdpClientAdvancedSettings6.BitmapPersistence
- IMsRdpClientAdvancedSettings6.get_BitmapPersistence
- IMsRdpClientAdvancedSettings6.put_BitmapPersistence
- IMsRdpClientAdvancedSettings7.BitmapPersistence
- IMsRdpClientAdvancedSettings7.get_BitmapPersistence
- IMsRdpClientAdvancedSettings7.put_BitmapPersistence
- IMsRdpClientAdvancedSettings8.BitmapPersistence
- IMsRdpClientAdvancedSettings8.get_BitmapPersistence
- IMsRdpClientAdvancedSettings8.put_BitmapPersistence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65795b5217c785befe0db6ac529d5760a6211d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384323"
---
# <a name="imsrdpclientadvancedsettingsbitmappersistence-property"></a><span data-ttu-id="0eb45-121">IMsRdpClientAdvancedSettings :: BitmapPersistence, propriété</span><span class="sxs-lookup"><span data-stu-id="0eb45-121">IMsRdpClientAdvancedSettings::BitmapPersistence property</span></span>

<span data-ttu-id="0eb45-122">Spécifie si la mise en cache des bitmaps persistante doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="0eb45-122">Specifies if persistent bitmap caching should be used.</span></span> <span data-ttu-id="0eb45-123">La mise en cache persistante peut améliorer les performances, mais nécessite de l’espace disque supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="0eb45-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="0eb45-124">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0eb45-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eb45-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0eb45-125">Syntax</span></span>


```C++
HRESULT put_BitmapPersistence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPersistence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="0eb45-126">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0eb45-126">Property value</span></span>

<span data-ttu-id="0eb45-127">Affectez à ce paramètre la valeur 0 pour désactiver la mise en cache ou une valeur différente de zéro pour activer la mise en cache.</span><span class="sxs-lookup"><span data-stu-id="0eb45-127">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

> [!Note]  
> <span data-ttu-id="0eb45-128">La faute d’orthographe dans le nom du paramètre se trouve dans la version finale du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0eb45-128">The spelling error in the name of the parameter is in the released version of the control.</span></span>

 

## <a name="error-codes"></a><span data-ttu-id="0eb45-129">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0eb45-129">Error codes</span></span>

<span data-ttu-id="0eb45-130">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="0eb45-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eb45-131">Notes</span><span class="sxs-lookup"><span data-stu-id="0eb45-131">Remarks</span></span>

<span data-ttu-id="0eb45-132">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0eb45-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0eb45-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0eb45-133">Requirements</span></span>



| <span data-ttu-id="0eb45-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0eb45-134">Requirement</span></span> | <span data-ttu-id="0eb45-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="0eb45-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eb45-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0eb45-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0eb45-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0eb45-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="0eb45-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0eb45-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0eb45-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0eb45-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="0eb45-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0eb45-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="0eb45-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0eb45-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0eb45-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0eb45-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0eb45-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0eb45-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0eb45-144">IID</span><span class="sxs-lookup"><span data-stu-id="0eb45-144">IID</span></span><br/>                      | <span data-ttu-id="0eb45-145">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="0eb45-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0eb45-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0eb45-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eb45-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0eb45-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0eb45-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0eb45-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0eb45-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0eb45-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0eb45-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0eb45-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="0eb45-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0eb45-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0eb45-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0eb45-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0eb45-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0eb45-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0eb45-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0eb45-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





