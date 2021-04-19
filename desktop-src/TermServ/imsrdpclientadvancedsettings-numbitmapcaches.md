---
title: IMsRdpClientAdvancedSettings propriété NumBitmapCaches
description: Cette propriété n'est pas prise en charge. | IMsRdpClientAdvancedSettings propriété NumBitmapCaches
ms.assetid: a413b2c0-7661-415d-bc38-e8fd55006e8c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété NumBitmapCaches
- Services Bureau à distance de la propriété NumBitmapCaches, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété NumBitmapCaches
- Services Bureau à distance de la propriété NumBitmapCaches, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété NumBitmapCaches
- Services Bureau à distance de la propriété NumBitmapCaches, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété NumBitmapCaches
- Services Bureau à distance de la propriété NumBitmapCaches, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété NumBitmapCaches
- Services Bureau à distance de la propriété NumBitmapCaches, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété NumBitmapCaches
- Services Bureau à distance de la propriété NumBitmapCaches, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété NumBitmapCaches
- Services Bureau à distance de la propriété NumBitmapCaches, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété NumBitmapCaches
- Services Bureau à distance de la propriété NumBitmapCaches, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété NumBitmapCaches
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.NumBitmapCaches
- IMsRdpClientAdvancedSettings.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.NumBitmapCaches
- IMsRdpClientAdvancedSettings2.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.NumBitmapCaches
- IMsRdpClientAdvancedSettings3.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.NumBitmapCaches
- IMsRdpClientAdvancedSettings4.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.NumBitmapCaches
- IMsRdpClientAdvancedSettings5.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.NumBitmapCaches
- IMsRdpClientAdvancedSettings6.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.NumBitmapCaches
- IMsRdpClientAdvancedSettings7.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.NumBitmapCaches
- IMsRdpClientAdvancedSettings8.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.put_NumBitmapCaches
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae60423287da041e3f84b28d8d51388e9a4050b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106539411"
---
# <a name="imsrdpclientadvancedsettingsnumbitmapcaches-property"></a><span data-ttu-id="7127a-121">IMsRdpClientAdvancedSettings :: NumBitmapCaches, propriété</span><span class="sxs-lookup"><span data-stu-id="7127a-121">IMsRdpClientAdvancedSettings::NumBitmapCaches property</span></span>

<span data-ttu-id="7127a-122">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7127a-122">This property is not supported.</span></span>

<span data-ttu-id="7127a-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7127a-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7127a-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7127a-124">Syntax</span></span>


```C++
HRESULT put_NumBitmapCaches(
  [in]  LONG numBitmapCaches
);

HRESULT get_NumBitmapCaches(
  [out] LONG *pnumBitmapCaches
);
```



## <a name="property-value"></a><span data-ttu-id="7127a-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7127a-125">Property value</span></span>

<span data-ttu-id="7127a-126">Nouveau nombre de caches.</span><span class="sxs-lookup"><span data-stu-id="7127a-126">The new number of caches.</span></span> <span data-ttu-id="7127a-127">La valeur par défaut est 3, ce qui se traduit par des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="7127a-127">The default value is 3, which results in the best performance.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7127a-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7127a-128">Error codes</span></span>

<span data-ttu-id="7127a-129">Retourne **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="7127a-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7127a-130">Notes</span><span class="sxs-lookup"><span data-stu-id="7127a-130">Remarks</span></span>

<span data-ttu-id="7127a-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7127a-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7127a-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7127a-132">Requirements</span></span>



| <span data-ttu-id="7127a-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7127a-133">Requirement</span></span> | <span data-ttu-id="7127a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="7127a-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7127a-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7127a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7127a-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7127a-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="7127a-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7127a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7127a-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7127a-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="7127a-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7127a-139">End of client support</span></span><br/>    | <span data-ttu-id="7127a-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7127a-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="7127a-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7127a-141">End of server support</span></span><br/>    | <span data-ttu-id="7127a-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7127a-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="7127a-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7127a-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="7127a-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7127a-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7127a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7127a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7127a-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7127a-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7127a-147">IID</span><span class="sxs-lookup"><span data-stu-id="7127a-147">IID</span></span><br/>                      | <span data-ttu-id="7127a-148">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="7127a-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7127a-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7127a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7127a-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7127a-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="7127a-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7127a-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7127a-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7127a-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7127a-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7127a-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="7127a-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7127a-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="7127a-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7127a-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7127a-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7127a-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7127a-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7127a-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





