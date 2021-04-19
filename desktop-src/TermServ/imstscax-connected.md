---
title: Propriété Connected IMsTscAx (Tsvirtualchannels. h)
description: Récupère l’état de connexion du contrôle actuel.
ms.assetid: f6f65ef6-d321-4362-b192-1ea5ffd2b712
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété connectée
- Services Bureau à distance de propriété connected, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété connectée
topic_type:
- apiref
api_name:
- IMsTscAx.Connected
- IMsTscAx.get_Connected
- IMsRdpClient.Connected
- IMsRdpClient.get_Connected
- IMsRdpClient2.Connected
- IMsRdpClient2.get_Connected
- IMsRdpClient3.Connected
- IMsRdpClient3.get_Connected
- IMsRdpClient4.Connected
- IMsRdpClient4.get_Connected
- IMsRdpClient5.Connected
- IMsRdpClient5.get_Connected
- IMsRdpClient6.Connected
- IMsRdpClient6.get_Connected
- IMsRdpClient7.Connected
- IMsRdpClient7.get_Connected
- IMsRdpClient8.Connected
- IMsRdpClient8.get_Connected
- IMsRdpClient9.Connected
- IMsRdpClient9.get_Connected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883ba670ab9a6b5d4e4a065c35f263734929ba02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543428"
---
# <a name="imstscaxconnected-property"></a><span data-ttu-id="cb252-124">IMsTscAx :: connected, propriété</span><span class="sxs-lookup"><span data-stu-id="cb252-124">IMsTscAx::Connected property</span></span>

<span data-ttu-id="cb252-125">Récupère l’état de connexion du contrôle actuel.</span><span class="sxs-lookup"><span data-stu-id="cb252-125">Retrieves the connection state of the current control.</span></span>

<span data-ttu-id="cb252-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cb252-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb252-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb252-127">Syntax</span></span>


```C++
HRESULT get_Connected(
  [out] short *pIsConnected
);
```



## <a name="property-value"></a><span data-ttu-id="cb252-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cb252-128">Property value</span></span>

<span data-ttu-id="cb252-129">Indique l’état de la connexion du contrôle.</span><span class="sxs-lookup"><span data-stu-id="cb252-129">Indicates the connection state of the control.</span></span> <span data-ttu-id="cb252-130">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb252-130">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="cb252-131">0</span><span class="sxs-lookup"><span data-stu-id="cb252-131">0</span></span>
</dt> <dd>

<span data-ttu-id="cb252-132">Le contrôle n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="cb252-132">The control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="cb252-133">1</span><span class="sxs-lookup"><span data-stu-id="cb252-133">1</span></span>
</dt> <dd>

<span data-ttu-id="cb252-134">Le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="cb252-134">The control is connected.</span></span>

</dd> <dt>

<span data-ttu-id="cb252-135">2</span><span class="sxs-lookup"><span data-stu-id="cb252-135">2</span></span>
</dt> <dd>

<span data-ttu-id="cb252-136">Le contrôle établit une connexion.</span><span class="sxs-lookup"><span data-stu-id="cb252-136">The control is establishing a connection.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="cb252-137">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="cb252-137">Error codes</span></span>

<span data-ttu-id="cb252-138">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="cb252-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb252-139">Notes</span><span class="sxs-lookup"><span data-stu-id="cb252-139">Remarks</span></span>

<span data-ttu-id="cb252-140">La meilleure façon de déterminer l’état de la connexion du contrôle consiste à répondre aux événements de connexion dans [**IMsTscAxEvents**](imstscaxevents-interface.md).</span><span class="sxs-lookup"><span data-stu-id="cb252-140">The preferred way to determine the control's connection state is to respond to the connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md).</span></span>

<span data-ttu-id="cb252-141">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cb252-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb252-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb252-142">Requirements</span></span>



| <span data-ttu-id="cb252-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb252-143">Requirement</span></span> | <span data-ttu-id="cb252-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb252-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb252-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb252-145">Minimum supported client</span></span><br/> | <span data-ttu-id="cb252-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb252-146">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="cb252-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb252-147">Minimum supported server</span></span><br/> | <span data-ttu-id="cb252-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb252-148">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="cb252-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb252-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb252-150"><dt>Tsvirtualchannels. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb252-150"><dt>Tsvirtualchannels.h</dt></span></span> </dl> |
| <span data-ttu-id="cb252-151">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cb252-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="cb252-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb252-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="cb252-153">DLL</span><span class="sxs-lookup"><span data-stu-id="cb252-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb252-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb252-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="cb252-155">IID</span><span class="sxs-lookup"><span data-stu-id="cb252-155">IID</span></span><br/>                      | <span data-ttu-id="cb252-156">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="cb252-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="cb252-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb252-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb252-158">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="cb252-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="cb252-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="cb252-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="cb252-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="cb252-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="cb252-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="cb252-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="cb252-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="cb252-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="cb252-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="cb252-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="cb252-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="cb252-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="cb252-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="cb252-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="cb252-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="cb252-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="cb252-167">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="cb252-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





