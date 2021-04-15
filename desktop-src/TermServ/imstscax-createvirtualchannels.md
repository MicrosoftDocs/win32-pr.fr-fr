---
title: Méthode IMsTscAx CreateVirtualChannels
description: Crée un objet de canal virtuel côté client pour chaque nom de canal virtuel spécifié.
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode CreateVirtualChannels
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d59c185763ddd3685e5e566f88e26a6aa6211b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465986"
---
# <a name="imstscaxcreatevirtualchannels-method"></a><span data-ttu-id="da15c-124">IMsTscAx :: CreateVirtualChannels, méthode</span><span class="sxs-lookup"><span data-stu-id="da15c-124">IMsTscAx::CreateVirtualChannels method</span></span>

<span data-ttu-id="da15c-125">Crée un objet de canal virtuel côté client pour chaque nom de canal virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="da15c-125">Creates a client-side virtual channel object for each specified virtual channel name.</span></span>

## <a name="syntax"></a><span data-ttu-id="da15c-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da15c-126">Syntax</span></span>


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="da15c-127">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da15c-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da15c-128">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da15c-128">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da15c-129">Liste séparée par des virgules de noms de canaux virtuels valides.</span><span class="sxs-lookup"><span data-stu-id="da15c-129">A comma-separated list of valid virtual channel names.</span></span> <span data-ttu-id="da15c-130">La longueur de chaque nom de cette liste peut être au minimum un et un maximum de sept caractères alphabétiques.</span><span class="sxs-lookup"><span data-stu-id="da15c-130">The length of each name in this list can be a minimum of one and a maximum of seven alphabetical characters.</span></span> <span data-ttu-id="da15c-131">La longueur de la chaîne entière peut être au minimum un et un maximum de 300 caractères alphabétiques.</span><span class="sxs-lookup"><span data-stu-id="da15c-131">The length of the entire string can be a minimum of one and a maximum of 300 alphabetical characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da15c-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da15c-132">Return value</span></span>

<span data-ttu-id="da15c-133">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="da15c-133">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="da15c-134">Retourne **E \_ INVALIDARG** si le paramètre passé ne répond pas aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="da15c-134">Returns **E\_INVALIDARG** if the parameter that is passed does not meet the criteria that is specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="da15c-135">Notes</span><span class="sxs-lookup"><span data-stu-id="da15c-135">Remarks</span></span>

<span data-ttu-id="da15c-136">Appelez cette méthode avant d’appeler la méthode [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="da15c-136">Call this method before calling the [**Connect**](imstscax-connect.md) method.</span></span>

<span data-ttu-id="da15c-137">Pour plus d’informations sur les restrictions de nom de canal virtuel, consultez [inscription du client du canal virtuel](virtual-channel-client-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="da15c-137">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="da15c-138">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="da15c-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da15c-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da15c-139">Requirements</span></span>



| <span data-ttu-id="da15c-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da15c-140">Requirement</span></span> | <span data-ttu-id="da15c-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="da15c-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da15c-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da15c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="da15c-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da15c-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="da15c-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da15c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="da15c-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da15c-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="da15c-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="da15c-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="da15c-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da15c-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="da15c-148">DLL</span><span class="sxs-lookup"><span data-stu-id="da15c-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da15c-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da15c-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="da15c-150">IID</span><span class="sxs-lookup"><span data-stu-id="da15c-150">IID</span></span><br/>                      | <span data-ttu-id="da15c-151">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="da15c-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="da15c-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da15c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da15c-153">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="da15c-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="da15c-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="da15c-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="da15c-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="da15c-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="da15c-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="da15c-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="da15c-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="da15c-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="da15c-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="da15c-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="da15c-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="da15c-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="da15c-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="da15c-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="da15c-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="da15c-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="da15c-162">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="da15c-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





