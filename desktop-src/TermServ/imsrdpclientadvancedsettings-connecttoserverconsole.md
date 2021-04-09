---
title: IMsRdpClientAdvancedSettings propriété ConnectToServerConsole
description: Cette propriété n'est pas prise en charge. Les appels à ConnectToServerConsole retournent toujours S \_ false.
ms.assetid: 58f79085-4364-408f-8bf1-97a82ad68f4b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectToServerConsole
- Services Bureau à distance de la propriété ConnectToServerConsole, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété ConnectToServerConsole
- Services Bureau à distance de la propriété ConnectToServerConsole, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété ConnectToServerConsole
- Services Bureau à distance de la propriété ConnectToServerConsole, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété ConnectToServerConsole
- Services Bureau à distance de la propriété ConnectToServerConsole, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété ConnectToServerConsole
- Services Bureau à distance de la propriété ConnectToServerConsole, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété ConnectToServerConsole
- Services Bureau à distance de la propriété ConnectToServerConsole, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ConnectToServerConsole
- Services Bureau à distance de la propriété ConnectToServerConsole, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ConnectToServerConsole
- Services Bureau à distance de la propriété ConnectToServerConsole, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ConnectToServerConsole
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ConnectToServerConsole
- IMsRdpClientAdvancedSettings.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.put_ConnectToServerConsole
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e3385b25a9dbe3e77085ae011b85e9be21b224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942050"
---
# <a name="imsrdpclientadvancedsettingsconnecttoserverconsole-property"></a><span data-ttu-id="f1fa2-121">IMsRdpClientAdvancedSettings :: ConnectToServerConsole, propriété</span><span class="sxs-lookup"><span data-stu-id="f1fa2-121">IMsRdpClientAdvancedSettings::ConnectToServerConsole property</span></span>

<span data-ttu-id="f1fa2-122">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f1fa2-122">This property is not supported.</span></span> <span data-ttu-id="f1fa2-123">Les appels à **ConnectToServerConsole** retournent toujours **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="f1fa2-123">Calls to **ConnectToServerConsole** always return **S\_FALSE**.</span></span>

<span data-ttu-id="f1fa2-124">Utilisez la propriété [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) pour vous connecter à la session utilisée à des fins d’administration.</span><span class="sxs-lookup"><span data-stu-id="f1fa2-124">Use the [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) property to connect to the session that is used for administrative purposes.</span></span>

<span data-ttu-id="f1fa2-125">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f1fa2-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1fa2-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1fa2-126">Syntax</span></span>


```C++
HRESULT put_ConnectToServerConsole(
  [in]  VARIANT_BOOL connectToServerConsole
);

HRESULT get_ConnectToServerConsole(
  [out] VARIANT_BOOL *pconnectToServerConsole
);
```



## <a name="property-value"></a><span data-ttu-id="f1fa2-127">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f1fa2-127">Property value</span></span>

<span data-ttu-id="f1fa2-128">Affectez à ce paramètre la valeur **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="f1fa2-128">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="f1fa2-129">**Variante \_ TRUE** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f1fa2-129">**VARIANT\_TRUE** is not supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f1fa2-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f1fa2-130">Error codes</span></span>

<span data-ttu-id="f1fa2-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="f1fa2-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1fa2-132">Notes</span><span class="sxs-lookup"><span data-stu-id="f1fa2-132">Remarks</span></span>

<span data-ttu-id="f1fa2-133">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f1fa2-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1fa2-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1fa2-134">Requirements</span></span>



| <span data-ttu-id="f1fa2-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1fa2-135">Requirement</span></span> | <span data-ttu-id="f1fa2-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1fa2-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1fa2-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1fa2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f1fa2-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1fa2-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="f1fa2-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1fa2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f1fa2-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1fa2-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="f1fa2-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f1fa2-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="f1fa2-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1fa2-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f1fa2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f1fa2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1fa2-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1fa2-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f1fa2-145">IID</span><span class="sxs-lookup"><span data-stu-id="f1fa2-145">IID</span></span><br/>                      | <span data-ttu-id="f1fa2-146">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f1fa2-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1fa2-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1fa2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1fa2-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f1fa2-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f1fa2-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f1fa2-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f1fa2-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f1fa2-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f1fa2-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f1fa2-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f1fa2-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f1fa2-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f1fa2-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f1fa2-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f1fa2-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f1fa2-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f1fa2-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f1fa2-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





