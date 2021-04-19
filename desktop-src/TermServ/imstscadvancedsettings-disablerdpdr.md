---
title: IMsTscAdvancedSettings propriété DisableRdpdr
description: Spécifie si l’imprimante et la redirection du presse-papiers sont activées.
ms.assetid: 63e0e024-4792-4efe-a6c5-d122f8adcb0a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété DisableRdpdr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.DisableRdpdr
- IMsTscAdvancedSettings.get_DisableRdpdr
- IMsTscAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings.DisableRdpdr
- IMsRdpClientAdvancedSettings.get_DisableRdpdr
- IMsRdpClientAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings2.DisableRdpdr
- IMsRdpClientAdvancedSettings2.get_DisableRdpdr
- IMsRdpClientAdvancedSettings2.put_DisableRdpdr
- IMsRdpClientAdvancedSettings3.DisableRdpdr
- IMsRdpClientAdvancedSettings3.get_DisableRdpdr
- IMsRdpClientAdvancedSettings3.put_DisableRdpdr
- IMsRdpClientAdvancedSettings4.DisableRdpdr
- IMsRdpClientAdvancedSettings4.get_DisableRdpdr
- IMsRdpClientAdvancedSettings4.put_DisableRdpdr
- IMsRdpClientAdvancedSettings5.DisableRdpdr
- IMsRdpClientAdvancedSettings5.get_DisableRdpdr
- IMsRdpClientAdvancedSettings5.put_DisableRdpdr
- IMsRdpClientAdvancedSettings6.DisableRdpdr
- IMsRdpClientAdvancedSettings6.get_DisableRdpdr
- IMsRdpClientAdvancedSettings6.put_DisableRdpdr
- IMsRdpClientAdvancedSettings7.DisableRdpdr
- IMsRdpClientAdvancedSettings7.get_DisableRdpdr
- IMsRdpClientAdvancedSettings7.put_DisableRdpdr
- IMsRdpClientAdvancedSettings8.DisableRdpdr
- IMsRdpClientAdvancedSettings8.get_DisableRdpdr
- IMsRdpClientAdvancedSettings8.put_DisableRdpdr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0747f37cd5e85c62946c9b8e3a1587f736dd8af9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518086"
---
# <a name="imstscadvancedsettingsdisablerdpdr-property"></a><span data-ttu-id="f3c6e-122">IMsTscAdvancedSettings ::D propriété isableRdpdr</span><span class="sxs-lookup"><span data-stu-id="f3c6e-122">IMsTscAdvancedSettings::DisableRdpdr property</span></span>

<span data-ttu-id="f3c6e-123">Spécifie si l’imprimante et la redirection du presse-papiers sont activées.</span><span class="sxs-lookup"><span data-stu-id="f3c6e-123">Specifies whether printer and clipboard redirection is enabled.</span></span>

<span data-ttu-id="f3c6e-124">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f3c6e-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3c6e-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3c6e-125">Syntax</span></span>


```C++
HRESULT put_DisableRdpdr(
  [in]  BOOL DisableRdpdr
);

HRESULT get_DisableRdpdr(
  [out] BOOL *pDisableRdpdr
);
```



## <a name="property-value"></a><span data-ttu-id="f3c6e-126">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f3c6e-126">Property value</span></span>

<span data-ttu-id="f3c6e-127">Affectez la valeur **true** à ce paramètre pour désactiver la redirection ou **false** pour activer la redirection.</span><span class="sxs-lookup"><span data-stu-id="f3c6e-127">Set this parameter to **TRUE** to disable redirection or **FALSE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f3c6e-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f3c6e-128">Error codes</span></span>

<span data-ttu-id="f3c6e-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="f3c6e-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3c6e-130">Notes</span><span class="sxs-lookup"><span data-stu-id="f3c6e-130">Remarks</span></span>

<span data-ttu-id="f3c6e-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f3c6e-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3c6e-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3c6e-132">Requirements</span></span>



| <span data-ttu-id="f3c6e-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3c6e-133">Requirement</span></span> | <span data-ttu-id="f3c6e-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3c6e-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c6e-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3c6e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c6e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3c6e-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="f3c6e-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3c6e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c6e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3c6e-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f3c6e-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f3c6e-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="f3c6e-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3c6e-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="f3c6e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f3c6e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3c6e-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3c6e-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="f3c6e-143">IID</span><span class="sxs-lookup"><span data-stu-id="f3c6e-143">IID</span></span><br/>                      | <span data-ttu-id="f3c6e-144">IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="f3c6e-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3c6e-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3c6e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c6e-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f3c6e-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f3c6e-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="f3c6e-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f3c6e-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f3c6e-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f3c6e-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f3c6e-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f3c6e-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





