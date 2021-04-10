---
title: IMsTscAx propriété AdvancedSettings
description: Récupère un pointeur d’interface IMsTscAdvancedSettings.
ms.assetid: 1c0e2216-0c65-48ad-b0f6-3a766c8fa44e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AdvancedSettings
- Services Bureau à distance de la propriété AdvancedSettings, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété AdvancedSettings
- Services Bureau à distance de la propriété AdvancedSettings, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété AdvancedSettings
- Services Bureau à distance de la propriété AdvancedSettings, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété AdvancedSettings
- Services Bureau à distance de la propriété AdvancedSettings, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété AdvancedSettings
- Services Bureau à distance de la propriété AdvancedSettings, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété AdvancedSettings
- Services Bureau à distance de la propriété AdvancedSettings, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété AdvancedSettings
- Services Bureau à distance de la propriété AdvancedSettings, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété AdvancedSettings
- Services Bureau à distance de la propriété AdvancedSettings, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété AdvancedSettings
- Services Bureau à distance de la propriété AdvancedSettings, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété AdvancedSettings
- Services Bureau à distance de la propriété AdvancedSettings, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété AdvancedSettings
topic_type:
- apiref
api_name:
- IMsTscAx.AdvancedSettings
- IMsTscAx.get_AdvancedSettings
- IMsRdpClient.AdvancedSettings
- IMsRdpClient.get_AdvancedSettings
- IMsRdpClient2.AdvancedSettings
- IMsRdpClient2.get_AdvancedSettings
- IMsRdpClient3.AdvancedSettings
- IMsRdpClient3.get_AdvancedSettings
- IMsRdpClient4.AdvancedSettings
- IMsRdpClient4.get_AdvancedSettings
- IMsRdpClient5.AdvancedSettings
- IMsRdpClient5.get_AdvancedSettings
- IMsRdpClient6.AdvancedSettings
- IMsRdpClient6.get_AdvancedSettings
- IMsRdpClient7.AdvancedSettings
- IMsRdpClient7.get_AdvancedSettings
- IMsRdpClient8.AdvancedSettings
- IMsRdpClient8.get_AdvancedSettings
- IMsRdpClient9.AdvancedSettings
- IMsRdpClient9.get_AdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb6b1d581704a0638a47310004777f020ce9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942120"
---
# <a name="imstscaxadvancedsettings-property"></a><span data-ttu-id="c9332-124">IMsTscAx :: AdvancedSettings, propriété</span><span class="sxs-lookup"><span data-stu-id="c9332-124">IMsTscAx::AdvancedSettings property</span></span>

<span data-ttu-id="c9332-125">Récupère un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="c9332-125">Retrieves an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="c9332-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c9332-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9332-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9332-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings(
  [out] IMsTscAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="c9332-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c9332-128">Property value</span></span>

<span data-ttu-id="c9332-129">Pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="c9332-129">An [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c9332-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c9332-130">Error codes</span></span>

<span data-ttu-id="c9332-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="c9332-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9332-132">Notes</span><span class="sxs-lookup"><span data-stu-id="c9332-132">Remarks</span></span>

<span data-ttu-id="c9332-133">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c9332-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9332-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9332-134">Requirements</span></span>



| <span data-ttu-id="c9332-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9332-135">Requirement</span></span> | <span data-ttu-id="c9332-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9332-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9332-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9332-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c9332-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9332-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c9332-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9332-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c9332-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9332-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c9332-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c9332-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="c9332-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9332-142"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c9332-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c9332-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9332-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9332-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c9332-145">IID</span><span class="sxs-lookup"><span data-stu-id="c9332-145">IID</span></span><br/>                      | <span data-ttu-id="c9332-146">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="c9332-146">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c9332-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9332-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9332-148">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="c9332-148">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="c9332-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="c9332-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="c9332-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="c9332-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="c9332-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="c9332-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="c9332-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="c9332-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="c9332-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="c9332-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="c9332-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="c9332-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="c9332-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c9332-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c9332-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c9332-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c9332-157">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="c9332-157">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





