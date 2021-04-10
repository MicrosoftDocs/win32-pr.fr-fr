---
title: IMsRdpClientAdvancedSettings propriété EnableMouse
description: Cette propriété n'est pas prise en charge. | IMsRdpClientAdvancedSettings propriété EnableMouse
ms.assetid: 4f60fdfc-e1b9-4ac2-98e4-49331b072883
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété EnableMouse
- Services Bureau à distance de la propriété EnableMouse, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété EnableMouse
- Services Bureau à distance de la propriété EnableMouse, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété EnableMouse
- Services Bureau à distance de la propriété EnableMouse, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété EnableMouse
- Services Bureau à distance de la propriété EnableMouse, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété EnableMouse
- Services Bureau à distance de la propriété EnableMouse, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété EnableMouse
- Services Bureau à distance de la propriété EnableMouse, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété EnableMouse
- Services Bureau à distance de la propriété EnableMouse, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété EnableMouse
- Services Bureau à distance de la propriété EnableMouse, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété EnableMouse
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableMouse
- IMsRdpClientAdvancedSettings.get_EnableMouse
- IMsRdpClientAdvancedSettings.put_EnableMouse
- IMsRdpClientAdvancedSettings2.EnableMouse
- IMsRdpClientAdvancedSettings2.get_EnableMouse
- IMsRdpClientAdvancedSettings2.put_EnableMouse
- IMsRdpClientAdvancedSettings3.EnableMouse
- IMsRdpClientAdvancedSettings3.get_EnableMouse
- IMsRdpClientAdvancedSettings3.put_EnableMouse
- IMsRdpClientAdvancedSettings4.EnableMouse
- IMsRdpClientAdvancedSettings4.get_EnableMouse
- IMsRdpClientAdvancedSettings4.put_EnableMouse
- IMsRdpClientAdvancedSettings5.EnableMouse
- IMsRdpClientAdvancedSettings5.get_EnableMouse
- IMsRdpClientAdvancedSettings5.put_EnableMouse
- IMsRdpClientAdvancedSettings6.EnableMouse
- IMsRdpClientAdvancedSettings6.get_EnableMouse
- IMsRdpClientAdvancedSettings6.put_EnableMouse
- IMsRdpClientAdvancedSettings7.EnableMouse
- IMsRdpClientAdvancedSettings7.get_EnableMouse
- IMsRdpClientAdvancedSettings7.put_EnableMouse
- IMsRdpClientAdvancedSettings8.EnableMouse
- IMsRdpClientAdvancedSettings8.get_EnableMouse
- IMsRdpClientAdvancedSettings8.put_EnableMouse
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0495ba7b48e431efe5746f40b353b5c1ad701d6a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953536"
---
# <a name="imsrdpclientadvancedsettingsenablemouse-property"></a><span data-ttu-id="b432e-121">IMsRdpClientAdvancedSettings :: EnableMouse, propriété</span><span class="sxs-lookup"><span data-stu-id="b432e-121">IMsRdpClientAdvancedSettings::EnableMouse property</span></span>

<span data-ttu-id="b432e-122">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b432e-122">This property is not supported.</span></span>

<span data-ttu-id="b432e-123">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b432e-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b432e-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b432e-124">Syntax</span></span>


```C++
HRESULT put_EnableMouse(
  [in]  LONG enableMouse
);

HRESULT get_EnableMouse(
  [out] LONG *penableMouse
);
```



## <a name="property-value"></a><span data-ttu-id="b432e-125">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b432e-125">Property value</span></span>

<span data-ttu-id="b432e-126">Affectez à ce paramètre la valeur 0 pour désactiver la fonctionnalité ou une valeur différente de zéro pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="b432e-126">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b432e-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b432e-127">Error codes</span></span>

<span data-ttu-id="b432e-128">Retourne **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="b432e-128">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b432e-129">Notes</span><span class="sxs-lookup"><span data-stu-id="b432e-129">Remarks</span></span>

<span data-ttu-id="b432e-130">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b432e-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b432e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b432e-131">Requirements</span></span>



| <span data-ttu-id="b432e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b432e-132">Requirement</span></span> | <span data-ttu-id="b432e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b432e-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b432e-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b432e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b432e-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b432e-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b432e-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b432e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b432e-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b432e-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b432e-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b432e-138">End of client support</span></span><br/>    | <span data-ttu-id="b432e-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b432e-139">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b432e-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b432e-140">End of server support</span></span><br/>    | <span data-ttu-id="b432e-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b432e-141">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b432e-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b432e-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="b432e-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b432e-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b432e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b432e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b432e-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b432e-145"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b432e-146">IID</span><span class="sxs-lookup"><span data-stu-id="b432e-146">IID</span></span><br/>                      | <span data-ttu-id="b432e-147">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="b432e-147">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b432e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b432e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b432e-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="b432e-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="b432e-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b432e-150">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b432e-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b432e-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="b432e-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b432e-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b432e-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b432e-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b432e-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b432e-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b432e-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b432e-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b432e-156">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b432e-156">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





