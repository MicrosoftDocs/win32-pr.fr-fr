---
title: IMsTscAdvancedSettings IndexIcône, propriété
description: Spécifie l’index de l’icône dans le fichier icône actuel.
ms.assetid: c29ae1a7-9c54-4e56-bb69-4e929e8a4e5c
ms.tgt_platform: multiple
keywords:
- IndexIcône, propriété Services Bureau à distance
- IndexIcône, Services Bureau à distance de la propriété, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété IndexIcône
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconIndex
- IMsTscAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings.IconIndex
- IMsRdpClientAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings2.IconIndex
- IMsRdpClientAdvancedSettings2.put_IconIndex
- IMsRdpClientAdvancedSettings3.IconIndex
- IMsRdpClientAdvancedSettings3.put_IconIndex
- IMsRdpClientAdvancedSettings4.IconIndex
- IMsRdpClientAdvancedSettings4.put_IconIndex
- IMsRdpClientAdvancedSettings5.IconIndex
- IMsRdpClientAdvancedSettings5.put_IconIndex
- IMsRdpClientAdvancedSettings6.IconIndex
- IMsRdpClientAdvancedSettings6.put_IconIndex
- IMsRdpClientAdvancedSettings7.IconIndex
- IMsRdpClientAdvancedSettings7.put_IconIndex
- IMsRdpClientAdvancedSettings8.IconIndex
- IMsRdpClientAdvancedSettings8.put_IconIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be56eab5dbe7f03155c6082e4e70fc4bd439253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508557"
---
# <a name="imstscadvancedsettingsiconindex-property"></a><span data-ttu-id="f4b40-122">IMsTscAdvancedSettings :: IndexIcône, propriété</span><span class="sxs-lookup"><span data-stu-id="f4b40-122">IMsTscAdvancedSettings::IconIndex property</span></span>

<span data-ttu-id="f4b40-123">Spécifie l’index de l’icône dans le fichier icône actuel.</span><span class="sxs-lookup"><span data-stu-id="f4b40-123">Specifies the index of the icon within the current icon file.</span></span>

> [!Note]  
> <span data-ttu-id="f4b40-124">Cette propriété n’est pas prise en charge dans le contrôle ActiveX (MsRdp. ocx).</span><span class="sxs-lookup"><span data-stu-id="f4b40-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="f4b40-125">Il est pris en charge dans la bibliothèque MsTscAx.dll incluse dans le client standard (MsTsc.exe).</span><span class="sxs-lookup"><span data-stu-id="f4b40-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="f4b40-126">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="f4b40-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4b40-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4b40-127">Syntax</span></span>


```C++
HRESULT put_IconIndex(
  [in] LONG IconIndex
);
```



## <a name="property-value"></a><span data-ttu-id="f4b40-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f4b40-128">Property value</span></span>

<span data-ttu-id="f4b40-129">Index de l’icône.</span><span class="sxs-lookup"><span data-stu-id="f4b40-129">The index of the icon.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f4b40-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f4b40-130">Error codes</span></span>

<span data-ttu-id="f4b40-131">Retourne **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="f4b40-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4b40-132">Notes</span><span class="sxs-lookup"><span data-stu-id="f4b40-132">Remarks</span></span>

<span data-ttu-id="f4b40-133">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f4b40-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4b40-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4b40-134">Requirements</span></span>



| <span data-ttu-id="f4b40-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4b40-135">Requirement</span></span> | <span data-ttu-id="f4b40-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4b40-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4b40-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4b40-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f4b40-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4b40-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="f4b40-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4b40-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f4b40-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4b40-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f4b40-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f4b40-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="f4b40-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4b40-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="f4b40-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f4b40-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4b40-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4b40-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="f4b40-145">IID</span><span class="sxs-lookup"><span data-stu-id="f4b40-145">IID</span></span><br/>                      | <span data-ttu-id="f4b40-146">IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="f4b40-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4b40-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4b40-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4b40-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f4b40-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f4b40-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f4b40-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f4b40-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f4b40-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="f4b40-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f4b40-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f4b40-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f4b40-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f4b40-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f4b40-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f4b40-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f4b40-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f4b40-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f4b40-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f4b40-156">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f4b40-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





