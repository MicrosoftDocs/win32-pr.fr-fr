---
title: Méthode IMsRdpClient GetVirtualChannelOptions
description: Récupère les options définies pour un canal virtuel.
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetVirtualChannelOptions
- Méthode GetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, méthode GetVirtualChannelOptions
- Méthode GetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, méthode GetVirtualChannelOptions
- Méthode GetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, méthode GetVirtualChannelOptions
- Méthode GetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, méthode GetVirtualChannelOptions
- Méthode GetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode GetVirtualChannelOptions
- Méthode GetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode GetVirtualChannelOptions
- Méthode GetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode GetVirtualChannelOptions
- Méthode GetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode GetVirtualChannelOptions
- Méthode GetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode GetVirtualChannelOptions
- Méthode GetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode GetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71548002ebc67dae8dc1a49e8144da3de608afb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510778"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a><span data-ttu-id="642d9-124">IMsRdpClient :: GetVirtualChannelOptions, méthode</span><span class="sxs-lookup"><span data-stu-id="642d9-124">IMsRdpClient::GetVirtualChannelOptions method</span></span>

<span data-ttu-id="642d9-125">Récupère les options définies pour un canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="642d9-125">Retrieves the options set for a virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="642d9-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="642d9-126">Syntax</span></span>


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="642d9-127">Paramètres</span><span class="sxs-lookup"><span data-stu-id="642d9-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="642d9-128">*ChanName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="642d9-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="642d9-129">Nom d’un canal virtuel qui a été spécifié dans l’appel à la méthode [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="642d9-129">The name of a virtual channel that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="642d9-130">*pChanOptions* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="642d9-130">*pChanOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="642d9-131">Options définies pour le canal virtuel spécifié par le paramètre *ChanName* .</span><span class="sxs-lookup"><span data-stu-id="642d9-131">The options set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="642d9-132">Pour obtenir une description des options possibles, consultez la page [**\_ définition de canal**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="642d9-132">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="642d9-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="642d9-133">Return value</span></span>

<span data-ttu-id="642d9-134">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="642d9-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="642d9-135">Notes</span><span class="sxs-lookup"><span data-stu-id="642d9-135">Remarks</span></span>

<span data-ttu-id="642d9-136">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="642d9-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="642d9-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="642d9-137">Requirements</span></span>



| <span data-ttu-id="642d9-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="642d9-138">Requirement</span></span> | <span data-ttu-id="642d9-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="642d9-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="642d9-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="642d9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="642d9-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="642d9-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="642d9-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="642d9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="642d9-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="642d9-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="642d9-144">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="642d9-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="642d9-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="642d9-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="642d9-146">DLL</span><span class="sxs-lookup"><span data-stu-id="642d9-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="642d9-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="642d9-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="642d9-148">IID</span><span class="sxs-lookup"><span data-stu-id="642d9-148">IID</span></span><br/>                      | <span data-ttu-id="642d9-149">IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="642d9-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="642d9-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="642d9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="642d9-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="642d9-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="642d9-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="642d9-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="642d9-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="642d9-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="642d9-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="642d9-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="642d9-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="642d9-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="642d9-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="642d9-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="642d9-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="642d9-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="642d9-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="642d9-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="642d9-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="642d9-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="642d9-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="642d9-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="642d9-161">**définition de canal \_**</span><span class="sxs-lookup"><span data-stu-id="642d9-161">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="642d9-162">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="642d9-162">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="642d9-163">**SetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="642d9-163">**SetVirtualChannelOptions**</span></span>](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





