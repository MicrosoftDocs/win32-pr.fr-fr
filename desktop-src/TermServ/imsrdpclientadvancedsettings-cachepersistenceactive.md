---
title: IMsRdpClientAdvancedSettings propriété CachePersistenceActive
description: Spécifie si la mise en cache des bitmaps persistante doit être utilisée. La mise en cache persistante peut améliorer les performances, mais nécessite de l’espace disque supplémentaire.
ms.assetid: 5eb986c4-98dd-426f-8d55-d3a9a526e1b2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété CachePersistenceActive
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.CachePersistenceActive
- IMsRdpClientAdvancedSettings.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.CachePersistenceActive
- IMsRdpClientAdvancedSettings2.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.CachePersistenceActive
- IMsRdpClientAdvancedSettings3.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.CachePersistenceActive
- IMsRdpClientAdvancedSettings4.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.CachePersistenceActive
- IMsRdpClientAdvancedSettings5.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.CachePersistenceActive
- IMsRdpClientAdvancedSettings6.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.CachePersistenceActive
- IMsRdpClientAdvancedSettings7.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.CachePersistenceActive
- IMsRdpClientAdvancedSettings8.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.put_CachePersistenceActive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb34e90cc028e95c750a444d53f42c9c0ab77400
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517328"
---
# <a name="imsrdpclientadvancedsettingscachepersistenceactive-property"></a><span data-ttu-id="b5242-121">IMsRdpClientAdvancedSettings :: CachePersistenceActive, propriété</span><span class="sxs-lookup"><span data-stu-id="b5242-121">IMsRdpClientAdvancedSettings::CachePersistenceActive property</span></span>

<span data-ttu-id="b5242-122">Spécifie si la mise en cache des bitmaps persistante doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="b5242-122">Specifies whether persistent bitmap caching should be used.</span></span> <span data-ttu-id="b5242-123">La mise en cache persistante peut améliorer les performances, mais nécessite de l’espace disque supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="b5242-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="b5242-124">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b5242-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5242-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5242-125">Syntax</span></span>


```C++
HRESULT put_CachePersistenceActive(
  [in]  LONG cachePersistenceActive
);

HRESULT get_CachePersistenceActive(
  [out] LONG *pcachePersistenceActive
);
```



## <a name="property-value"></a><span data-ttu-id="b5242-126">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b5242-126">Property value</span></span>

<span data-ttu-id="b5242-127">Affectez à ce paramètre la valeur 0 pour désactiver la fonctionnalité ou une valeur différente de zéro pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="b5242-127">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b5242-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b5242-128">Error codes</span></span>

<span data-ttu-id="b5242-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="b5242-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5242-130">Notes</span><span class="sxs-lookup"><span data-stu-id="b5242-130">Remarks</span></span>

<span data-ttu-id="b5242-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b5242-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5242-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5242-132">Requirements</span></span>



| <span data-ttu-id="b5242-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5242-133">Requirement</span></span> | <span data-ttu-id="b5242-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5242-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5242-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5242-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b5242-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5242-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="b5242-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5242-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b5242-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5242-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="b5242-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b5242-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5242-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5242-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b5242-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b5242-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5242-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5242-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b5242-143">IID</span><span class="sxs-lookup"><span data-stu-id="b5242-143">IID</span></span><br/>                      | <span data-ttu-id="b5242-144">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="b5242-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5242-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5242-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5242-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="b5242-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="b5242-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b5242-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b5242-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b5242-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="b5242-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b5242-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b5242-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b5242-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b5242-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b5242-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b5242-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b5242-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b5242-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b5242-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





