---
title: IMsTscAdvancedSettings compression, propriété
description: Spécifie si la compression est activée.
ms.assetid: 274774b3-0442-4a46-95f8-7857f885bfdb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriétés compress
- Compresser la propriété Services Bureau à distance, IMsTscAdvancedSettings, interface
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings2, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings3, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings4, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings5, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings6, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings7, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings8, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété Compress
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.Compress
- IMsTscAdvancedSettings.get_Compress
- IMsTscAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings.Compress
- IMsRdpClientAdvancedSettings.get_Compress
- IMsRdpClientAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings2.Compress
- IMsRdpClientAdvancedSettings2.get_Compress
- IMsRdpClientAdvancedSettings2.put_Compress
- IMsRdpClientAdvancedSettings3.Compress
- IMsRdpClientAdvancedSettings3.get_Compress
- IMsRdpClientAdvancedSettings3.put_Compress
- IMsRdpClientAdvancedSettings4.Compress
- IMsRdpClientAdvancedSettings4.get_Compress
- IMsRdpClientAdvancedSettings4.put_Compress
- IMsRdpClientAdvancedSettings5.Compress
- IMsRdpClientAdvancedSettings5.get_Compress
- IMsRdpClientAdvancedSettings5.put_Compress
- IMsRdpClientAdvancedSettings6.Compress
- IMsRdpClientAdvancedSettings6.get_Compress
- IMsRdpClientAdvancedSettings6.put_Compress
- IMsRdpClientAdvancedSettings7.Compress
- IMsRdpClientAdvancedSettings7.get_Compress
- IMsRdpClientAdvancedSettings7.put_Compress
- IMsRdpClientAdvancedSettings8.Compress
- IMsRdpClientAdvancedSettings8.get_Compress
- IMsRdpClientAdvancedSettings8.put_Compress
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c588784d9b06bd2e8e1605a96c8aa9fd157c10eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942330"
---
# <a name="imstscadvancedsettingscompress-property"></a><span data-ttu-id="cb6fa-122">IMsTscAdvancedSettings :: compress, propriété</span><span class="sxs-lookup"><span data-stu-id="cb6fa-122">IMsTscAdvancedSettings::Compress property</span></span>

<span data-ttu-id="cb6fa-123">Spécifie si la compression est activée.</span><span class="sxs-lookup"><span data-stu-id="cb6fa-123">Specifies whether compression is enabled.</span></span>

<span data-ttu-id="cb6fa-124">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="cb6fa-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb6fa-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb6fa-125">Syntax</span></span>


```C++
HRESULT put_Compress(
  [in]  LONG compress
);

HRESULT get_Compress(
  [out] LONG *pcompress
);
```



## <a name="property-value"></a><span data-ttu-id="cb6fa-126">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cb6fa-126">Property value</span></span>

<span data-ttu-id="cb6fa-127">Définissez ce paramètre sur 0 pour désactiver la compression ou sur une valeur différente de zéro pour activer la compression.</span><span class="sxs-lookup"><span data-stu-id="cb6fa-127">Set this parameter to 0 to disable compression or a nonzero value to enable compression.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb6fa-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="cb6fa-128">Error codes</span></span>

<span data-ttu-id="cb6fa-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="cb6fa-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb6fa-130">Notes</span><span class="sxs-lookup"><span data-stu-id="cb6fa-130">Remarks</span></span>

<span data-ttu-id="cb6fa-131">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cb6fa-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb6fa-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb6fa-132">Requirements</span></span>



| <span data-ttu-id="cb6fa-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb6fa-133">Requirement</span></span> | <span data-ttu-id="cb6fa-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb6fa-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6fa-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb6fa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cb6fa-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb6fa-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="cb6fa-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb6fa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cb6fa-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb6fa-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="cb6fa-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cb6fa-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="cb6fa-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb6fa-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="cb6fa-141">DLL</span><span class="sxs-lookup"><span data-stu-id="cb6fa-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb6fa-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb6fa-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="cb6fa-143">IID</span><span class="sxs-lookup"><span data-stu-id="cb6fa-143">IID</span></span><br/>                      | <span data-ttu-id="cb6fa-144">IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="cb6fa-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cb6fa-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb6fa-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb6fa-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="cb6fa-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="cb6fa-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="cb6fa-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="cb6fa-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="cb6fa-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="cb6fa-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="cb6fa-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="cb6fa-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="cb6fa-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="cb6fa-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="cb6fa-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="cb6fa-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="cb6fa-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="cb6fa-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="cb6fa-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="cb6fa-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="cb6fa-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





