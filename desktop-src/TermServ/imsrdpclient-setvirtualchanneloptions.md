---
title: Méthode IMsRdpClient SetVirtualChannelOptions
description: Définit les options de canal virtuel pour le contrôle ActiveX Bureau à distance.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode SetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e727fd3486b9d1b31fb3a421ea6ff268949790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384203"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a><span data-ttu-id="620f7-124">IMsRdpClient :: SetVirtualChannelOptions, méthode</span><span class="sxs-lookup"><span data-stu-id="620f7-124">IMsRdpClient::SetVirtualChannelOptions method</span></span>

<span data-ttu-id="620f7-125">Définit les options de canal virtuel pour le contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="620f7-125">Sets the virtual channel options for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="620f7-126">Appelez cette méthode après avoir appelé la méthode [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) , mais avant d’établir une connexion à l’aide de la méthode [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="620f7-126">Call this method after calling the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method, but before establishing a connection with the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="620f7-127">Cette méthode définit des options supplémentaires sur les canaux virtuels qui ont été créés avec **CreateVirtualChannels**.</span><span class="sxs-lookup"><span data-stu-id="620f7-127">This method sets additional options on virtual channels that have been created with **CreateVirtualChannels**.</span></span>

## <a name="syntax"></a><span data-ttu-id="620f7-128">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="620f7-128">Syntax</span></span>


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="620f7-129">Paramètres</span><span class="sxs-lookup"><span data-stu-id="620f7-129">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="620f7-130">*ChanName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="620f7-130">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="620f7-131">Nom du canal virtuel qui a été spécifié dans l’appel à la méthode [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="620f7-131">The name of the virtual channel that was specified in the call to the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="620f7-132">*chanOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="620f7-132">*chanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="620f7-133">Options à définir pour le canal virtuel spécifié par le paramètre *ChanName* .</span><span class="sxs-lookup"><span data-stu-id="620f7-133">The options to set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="620f7-134">Pour obtenir une description des options possibles, consultez la page [**\_ définition de canal**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="620f7-134">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span> <span data-ttu-id="620f7-135">Pour plus d'informations, consultez la section Notes qui suit.</span><span class="sxs-lookup"><span data-stu-id="620f7-135">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="620f7-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="620f7-136">Return value</span></span>

<span data-ttu-id="620f7-137">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="620f7-137">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="620f7-138">Notes</span><span class="sxs-lookup"><span data-stu-id="620f7-138">Remarks</span></span>

<span data-ttu-id="620f7-139">Un exemple d’utilisation de cette méthode serait de déclarer le canal comme un contrôle à distance persistant en définissant l' **option de canal indicateur \_ \_ \_ \_ permanent de contrôle à distance** .</span><span class="sxs-lookup"><span data-stu-id="620f7-139">An example of using this method would be to declare the channel as remote control persistent by setting the **CHANNEL\_OPTION\_REMOTE\_CONTROL\_PERSISTENT** flag.</span></span> <span data-ttu-id="620f7-140">Cela signifie que le canal n’est pas fermé lorsqu’un contrôle à distance se connecte à ou se déconnecte de la session connectée au client.</span><span class="sxs-lookup"><span data-stu-id="620f7-140">This means that the channel would not be closed when a remote control connects to or disconnects from the session connected to the client.</span></span> <span data-ttu-id="620f7-141">Pour plus d’informations, consultez [contrôle à distance des canaux virtuels persistants](remote-control-persistent-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="620f7-141">For more information, see [Remote Control Persistent Virtual Channels](remote-control-persistent-virtual-channels.md).</span></span>

<span data-ttu-id="620f7-142">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="620f7-142">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="620f7-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="620f7-143">Requirements</span></span>



| <span data-ttu-id="620f7-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="620f7-144">Requirement</span></span> | <span data-ttu-id="620f7-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="620f7-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="620f7-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="620f7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="620f7-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="620f7-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="620f7-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="620f7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="620f7-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="620f7-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="620f7-150">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="620f7-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="620f7-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="620f7-151"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="620f7-152">DLL</span><span class="sxs-lookup"><span data-stu-id="620f7-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="620f7-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="620f7-153"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="620f7-154">IID</span><span class="sxs-lookup"><span data-stu-id="620f7-154">IID</span></span><br/>                      | <span data-ttu-id="620f7-155">IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="620f7-155">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="620f7-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="620f7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="620f7-157">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="620f7-157">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="620f7-158">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="620f7-158">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="620f7-159">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="620f7-159">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="620f7-160">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="620f7-160">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="620f7-161">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="620f7-161">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="620f7-162">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="620f7-162">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="620f7-163">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="620f7-163">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="620f7-164">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="620f7-164">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="620f7-165">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="620f7-165">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="620f7-166">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="620f7-166">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="620f7-167">**définition de canal \_**</span><span class="sxs-lookup"><span data-stu-id="620f7-167">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="620f7-168">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="620f7-168">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="620f7-169">**GetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="620f7-169">**GetVirtualChannelOptions**</span></span>](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





