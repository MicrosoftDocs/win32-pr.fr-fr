---
title: IMsTscAx propriété SecuredSettingsEnabled
description: Indique si l’interface IMsTscSecuredSettings est disponible. Autrement dit, si la page Web contenant le contrôle se trouve actuellement dans l’une des zones de sécurité d’URL Internet Explorer autorisées.
ms.assetid: 0747eab0-9d62-4c10-b02d-fc65ca2f752e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettingsEnabled
- IMsTscAx.get_SecuredSettingsEnabled
- IMsRdpClient.SecuredSettingsEnabled
- IMsRdpClient.get_SecuredSettingsEnabled
- IMsRdpClient2.SecuredSettingsEnabled
- IMsRdpClient2.get_SecuredSettingsEnabled
- IMsRdpClient3.SecuredSettingsEnabled
- IMsRdpClient3.get_SecuredSettingsEnabled
- IMsRdpClient4.SecuredSettingsEnabled
- IMsRdpClient4.get_SecuredSettingsEnabled
- IMsRdpClient5.SecuredSettingsEnabled
- IMsRdpClient5.get_SecuredSettingsEnabled
- IMsRdpClient6.SecuredSettingsEnabled
- IMsRdpClient6.get_SecuredSettingsEnabled
- IMsRdpClient7.SecuredSettingsEnabled
- IMsRdpClient7.get_SecuredSettingsEnabled
- IMsRdpClient8.SecuredSettingsEnabled
- IMsRdpClient8.get_SecuredSettingsEnabled
- IMsRdpClient9.SecuredSettingsEnabled
- IMsRdpClient9.get_SecuredSettingsEnabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0601ac64ab0ca55f3d92ec460861a4347f70b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511968"
---
# <a name="imstscaxsecuredsettingsenabled-property"></a><span data-ttu-id="a92f1-125">IMsTscAx :: SecuredSettingsEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="a92f1-125">IMsTscAx::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="a92f1-126">Indique si l’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) est disponible.</span><span class="sxs-lookup"><span data-stu-id="a92f1-126">Indicates whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available.</span></span> <span data-ttu-id="a92f1-127">Autrement dit, si la page Web contenant le contrôle se trouve actuellement dans l’une des zones de sécurité d’URL Internet Explorer autorisées.</span><span class="sxs-lookup"><span data-stu-id="a92f1-127">That is, whether the webpage containing the control is currently in one of the allowed Internet Explorer URL security zones.</span></span>

<span data-ttu-id="a92f1-128">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a92f1-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a92f1-129">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a92f1-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="a92f1-130">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a92f1-130">Property value</span></span>

<span data-ttu-id="a92f1-131">La valeur de ce paramètre est **true** si l’interface est disponible ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="a92f1-131">The value of this parameter is **TRUE** if the interface is available, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a92f1-132">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a92f1-132">Error codes</span></span>

<span data-ttu-id="a92f1-133">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a92f1-133">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a92f1-134">Notes</span><span class="sxs-lookup"><span data-stu-id="a92f1-134">Remarks</span></span>

<span data-ttu-id="a92f1-135">Utilisez cette méthode pour demander si l’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) est disponible avant de récupérer la propriété [**SecuredSettings**](imstscax-securedsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="a92f1-135">Use this method to query whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available before retrieving the [**SecuredSettings**](imstscax-securedsettings.md) property.</span></span>

<span data-ttu-id="a92f1-136">Pour obtenir la liste des zones de sécurité d’URL restreintes, consultez la rubrique [fourniture de RDP Client Security](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="a92f1-136">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for a list of restricted URL security zones.</span></span>

<span data-ttu-id="a92f1-137">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a92f1-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a92f1-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a92f1-138">Requirements</span></span>



| <span data-ttu-id="a92f1-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a92f1-139">Requirement</span></span> | <span data-ttu-id="a92f1-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="a92f1-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a92f1-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a92f1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a92f1-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a92f1-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a92f1-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a92f1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a92f1-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a92f1-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a92f1-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a92f1-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="a92f1-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a92f1-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a92f1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a92f1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a92f1-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a92f1-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a92f1-149">IID</span><span class="sxs-lookup"><span data-stu-id="a92f1-149">IID</span></span><br/>                      | <span data-ttu-id="a92f1-150">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="a92f1-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a92f1-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a92f1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a92f1-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="a92f1-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="a92f1-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="a92f1-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="a92f1-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="a92f1-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="a92f1-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="a92f1-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="a92f1-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a92f1-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a92f1-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a92f1-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a92f1-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a92f1-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a92f1-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a92f1-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a92f1-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a92f1-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a92f1-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="a92f1-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="a92f1-162">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="a92f1-162">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





