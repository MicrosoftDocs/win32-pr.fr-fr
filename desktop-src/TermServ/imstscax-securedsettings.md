---
title: IMsTscAx propriété SecuredSettings
description: Récupère un pointeur d’interface IMsTscSecuredSettings.
ms.assetid: 64d4059b-e617-449d-a733-c19c1d281132
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété SecuredSettings
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettings
- IMsTscAx.get_SecuredSettings
- IMsRdpClient.SecuredSettings
- IMsRdpClient.get_SecuredSettings
- IMsRdpClient2.SecuredSettings
- IMsRdpClient2.get_SecuredSettings
- IMsRdpClient3.SecuredSettings
- IMsRdpClient3.get_SecuredSettings
- IMsRdpClient4.SecuredSettings
- IMsRdpClient4.get_SecuredSettings
- IMsRdpClient5.SecuredSettings
- IMsRdpClient5.get_SecuredSettings
- IMsRdpClient6.SecuredSettings
- IMsRdpClient6.get_SecuredSettings
- IMsRdpClient7.SecuredSettings
- IMsRdpClient7.get_SecuredSettings
- IMsRdpClient8.SecuredSettings
- IMsRdpClient8.get_SecuredSettings
- IMsRdpClient9.SecuredSettings
- IMsRdpClient9.get_SecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6610448d822fe75082c225686dc6d809229a325f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103684"
---
# <a name="imstscaxsecuredsettings-property"></a><span data-ttu-id="9490c-124">IMsTscAx :: SecuredSettings, propriété</span><span class="sxs-lookup"><span data-stu-id="9490c-124">IMsTscAx::SecuredSettings property</span></span>

<span data-ttu-id="9490c-125">Récupère un pointeur d’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="9490c-125">Retrieves an [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="9490c-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9490c-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9490c-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9490c-127">Syntax</span></span>


```C++
HRESULT get_SecuredSettings(
  [out] IMsTscSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="9490c-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9490c-128">Property value</span></span>

<span data-ttu-id="9490c-129">Pointeur d’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="9490c-129">An [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9490c-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9490c-130">Error codes</span></span>

<span data-ttu-id="9490c-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="9490c-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9490c-132">Notes</span><span class="sxs-lookup"><span data-stu-id="9490c-132">Remarks</span></span>

<span data-ttu-id="9490c-133">Si le contrôle est hébergé dans une page Web et que la zone de sécurité URL d’Internet Explorer actuelle n’autorise pas la récupération de l’adresse de l’interface, cette méthode retourne **E \_ Fail**.</span><span class="sxs-lookup"><span data-stu-id="9490c-133">If the control is hosted in a webpage and the current Internet Explorer URL security zone does not permit the retrieval of the interface address, this method returns **E\_FAIL**.</span></span>

<span data-ttu-id="9490c-134">Reportez-vous à [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) pour des restrictions sur la disponibilité de l’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="9490c-134">Refer to [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) for restrictions on the availability of the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface.</span></span>

<span data-ttu-id="9490c-135">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9490c-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9490c-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9490c-136">Requirements</span></span>



| <span data-ttu-id="9490c-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9490c-137">Requirement</span></span> | <span data-ttu-id="9490c-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="9490c-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9490c-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9490c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9490c-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9490c-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9490c-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9490c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9490c-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9490c-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9490c-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9490c-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="9490c-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9490c-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9490c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9490c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9490c-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9490c-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9490c-147">IID</span><span class="sxs-lookup"><span data-stu-id="9490c-147">IID</span></span><br/>                      | <span data-ttu-id="9490c-148">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="9490c-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9490c-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9490c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9490c-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="9490c-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="9490c-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="9490c-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="9490c-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="9490c-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="9490c-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="9490c-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="9490c-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="9490c-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="9490c-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="9490c-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="9490c-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9490c-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9490c-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9490c-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9490c-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9490c-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9490c-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="9490c-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="9490c-160">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="9490c-160">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





