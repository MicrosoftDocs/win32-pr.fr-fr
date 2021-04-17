---
title: IMsTscAdvancedSettings propriété BitmapPeristence
description: Spécifie si la mise en cache bitmap est activée.
ms.assetid: 8cabeae8-26bc-4d33-82cc-47bb201d79b6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BitmapPeristence
- Services Bureau à distance de la propriété BitmapPeristence, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété BitmapPeristence
- Services Bureau à distance de la propriété BitmapPeristence, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété BitmapPeristence
- Services Bureau à distance de la propriété BitmapPeristence, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété BitmapPeristence
- Services Bureau à distance de la propriété BitmapPeristence, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété BitmapPeristence
- Services Bureau à distance de la propriété BitmapPeristence, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété BitmapPeristence
- Services Bureau à distance de la propriété BitmapPeristence, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété BitmapPeristence
- Services Bureau à distance de la propriété BitmapPeristence, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété BitmapPeristence
- Services Bureau à distance de la propriété BitmapPeristence, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété BitmapPeristence
- Services Bureau à distance de la propriété BitmapPeristence, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété BitmapPeristence
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.BitmapPeristence
- IMsTscAdvancedSettings.get_BitmapPeristence
- IMsTscAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings.BitmapPeristence
- IMsRdpClientAdvancedSettings.get_BitmapPeristence
- IMsRdpClientAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings2.BitmapPeristence
- IMsRdpClientAdvancedSettings2.get_BitmapPeristence
- IMsRdpClientAdvancedSettings2.put_BitmapPeristence
- IMsRdpClientAdvancedSettings3.BitmapPeristence
- IMsRdpClientAdvancedSettings3.get_BitmapPeristence
- IMsRdpClientAdvancedSettings3.put_BitmapPeristence
- IMsRdpClientAdvancedSettings4.BitmapPeristence
- IMsRdpClientAdvancedSettings4.get_BitmapPeristence
- IMsRdpClientAdvancedSettings4.put_BitmapPeristence
- IMsRdpClientAdvancedSettings5.BitmapPeristence
- IMsRdpClientAdvancedSettings5.get_BitmapPeristence
- IMsRdpClientAdvancedSettings5.put_BitmapPeristence
- IMsRdpClientAdvancedSettings6.BitmapPeristence
- IMsRdpClientAdvancedSettings6.get_BitmapPeristence
- IMsRdpClientAdvancedSettings6.put_BitmapPeristence
- IMsRdpClientAdvancedSettings7.BitmapPeristence
- IMsRdpClientAdvancedSettings7.get_BitmapPeristence
- IMsRdpClientAdvancedSettings7.put_BitmapPeristence
- IMsRdpClientAdvancedSettings8.BitmapPeristence
- IMsRdpClientAdvancedSettings8.get_BitmapPeristence
- IMsRdpClientAdvancedSettings8.put_BitmapPeristence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a543d24b200d8fa484939d5ffeabfeeac0b5f73f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466851"
---
# <a name="imstscadvancedsettingsbitmapperistence-property"></a><span data-ttu-id="5f69e-122">IMsTscAdvancedSettings :: BitmapPeristence, propriété</span><span class="sxs-lookup"><span data-stu-id="5f69e-122">IMsTscAdvancedSettings::BitmapPeristence property</span></span>

<span data-ttu-id="5f69e-123">Spécifie si la mise en cache bitmap est activée.</span><span class="sxs-lookup"><span data-stu-id="5f69e-123">Specifies whether bitmap caching is enabled.</span></span> <span data-ttu-id="5f69e-124">La mise en cache persistante peut améliorer les performances, mais nécessite de l’espace disque supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5f69e-124">Persistent caching can improve performance but requires additional disk space.</span></span>

> [!Note]  
> <span data-ttu-id="5f69e-125">La faute d’orthographe dans le nom de la propriété et son paramètre se trouve dans la version finale du contrôle.</span><span class="sxs-lookup"><span data-stu-id="5f69e-125">The spelling error in the name of the property and its parameter is in the released version of the control.</span></span>

 

<span data-ttu-id="5f69e-126">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5f69e-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f69e-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f69e-127">Syntax</span></span>


```C++
HRESULT put_BitmapPeristence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPeristence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="5f69e-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5f69e-128">Property value</span></span>

<span data-ttu-id="5f69e-129">Affectez à ce paramètre la valeur 0 pour désactiver la mise en cache ou une valeur différente de zéro pour activer la mise en cache.</span><span class="sxs-lookup"><span data-stu-id="5f69e-129">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5f69e-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="5f69e-130">Error codes</span></span>

<span data-ttu-id="5f69e-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="5f69e-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f69e-132">Notes</span><span class="sxs-lookup"><span data-stu-id="5f69e-132">Remarks</span></span>

<span data-ttu-id="5f69e-133">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5f69e-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f69e-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f69e-134">Requirements</span></span>



| <span data-ttu-id="5f69e-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f69e-135">Requirement</span></span> | <span data-ttu-id="5f69e-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f69e-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f69e-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f69e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5f69e-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f69e-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="5f69e-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f69e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5f69e-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f69e-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5f69e-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5f69e-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="5f69e-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f69e-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="5f69e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5f69e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f69e-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f69e-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="5f69e-145">IID</span><span class="sxs-lookup"><span data-stu-id="5f69e-145">IID</span></span><br/>                      | <span data-ttu-id="5f69e-146">IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="5f69e-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f69e-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f69e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f69e-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="5f69e-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5f69e-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="5f69e-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="5f69e-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="5f69e-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="5f69e-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="5f69e-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="5f69e-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="5f69e-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="5f69e-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="5f69e-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="5f69e-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5f69e-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="5f69e-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="5f69e-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="5f69e-156">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="5f69e-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





