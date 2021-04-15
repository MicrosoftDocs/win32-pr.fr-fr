---
title: Méthode IMsTscAx SendOnVirtualChannel
description: Envoie des données au serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance) sur un canal virtuel qui a été créé précédemment à l’aide de la méthode CreateVirtualChannels.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode SendOnVirtualChannel
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1371ae17978601a3194f755dd364d9227b8fc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464571"
---
# <a name="imstscaxsendonvirtualchannel-method"></a><span data-ttu-id="a91da-124">IMsTscAx :: SendOnVirtualChannel, méthode</span><span class="sxs-lookup"><span data-stu-id="a91da-124">IMsTscAx::SendOnVirtualChannel method</span></span>

<span data-ttu-id="a91da-125">Envoie des données au serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance) sur un canal virtuel qui a été créé précédemment à l’aide de la méthode [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="a91da-125">Sends data to the Remote Desktop Session Host (RD Session Host) server over a virtual channel that was created previously by using the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a91da-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a91da-126">Syntax</span></span>


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a><span data-ttu-id="a91da-127">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a91da-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a91da-128">*ChanName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a91da-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a91da-129">Nom du canal virtuel qui a été spécifié dans l’appel à [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span><span class="sxs-lookup"><span data-stu-id="a91da-129">The virtual channel name that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="a91da-130">*ChanData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a91da-130">*ChanData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a91da-131">Données à envoyer sur le canal virtuel, sous forme **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="a91da-131">The data to send over the virtual channel, in **BSTR** form.</span></span> <span data-ttu-id="a91da-132">Il n’existe aucune restriction indiquant que ces données doivent être des chaînes terminées par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="a91da-132">There is no restriction that this data must be null-terminated strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a91da-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a91da-133">Return value</span></span>

<span data-ttu-id="a91da-134">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a91da-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a91da-135">Notes</span><span class="sxs-lookup"><span data-stu-id="a91da-135">Remarks</span></span>

<span data-ttu-id="a91da-136">Pour plus d’informations sur les restrictions de nom de canal virtuel, consultez [inscription du client du canal virtuel](virtual-channel-client-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="a91da-136">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="a91da-137">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a91da-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a91da-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a91da-138">Requirements</span></span>



| <span data-ttu-id="a91da-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a91da-139">Requirement</span></span> | <span data-ttu-id="a91da-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="a91da-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a91da-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a91da-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a91da-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a91da-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a91da-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a91da-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a91da-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a91da-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a91da-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a91da-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="a91da-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a91da-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a91da-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a91da-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a91da-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a91da-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a91da-149">IID</span><span class="sxs-lookup"><span data-stu-id="a91da-149">IID</span></span><br/>                      | <span data-ttu-id="a91da-150">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="a91da-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a91da-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a91da-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a91da-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="a91da-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="a91da-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="a91da-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="a91da-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="a91da-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="a91da-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="a91da-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="a91da-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a91da-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a91da-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a91da-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a91da-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a91da-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a91da-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a91da-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a91da-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a91da-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a91da-161">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="a91da-161">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="a91da-162">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="a91da-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





