---
title: IMsRdpClientAdvancedSettings propriété LoadBalanceInfo
description: Spécifie le cookie d’équilibrage de charge qui sera placé dans le paquet de demande de connexion X. 224 dans la séquence de connexion du protocole du serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété LoadBalanceInfo
- Services Bureau à distance de la propriété LoadBalanceInfo, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété LoadBalanceInfo
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12112eb2a18d38993e905f8d36175f1ab15f58a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384308"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a><span data-ttu-id="2a0e9-120">IMsRdpClientAdvancedSettings :: LoadBalanceInfo, propriété</span><span class="sxs-lookup"><span data-stu-id="2a0e9-120">IMsRdpClientAdvancedSettings::LoadBalanceInfo property</span></span>

<span data-ttu-id="2a0e9-121">Spécifie le cookie d’équilibrage de charge qui sera placé dans le paquet de demande de connexion X. 224 dans la séquence de connexion du protocole du serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="2a0e9-121">Specifies the load balancing cookie that will be placed in the X.224 Connection Request packet in the Remote Desktop Session Host (RD Session Host) server protocol connection sequence.</span></span>

<span data-ttu-id="2a0e9-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2a0e9-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a0e9-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a0e9-123">Syntax</span></span>


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a><span data-ttu-id="2a0e9-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2a0e9-124">Property value</span></span>

<span data-ttu-id="2a0e9-125">Pointeur vers le nouveau cookie.</span><span class="sxs-lookup"><span data-stu-id="2a0e9-125">Pointer to the new cookie.</span></span> <span data-ttu-id="2a0e9-126">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="2a0e9-126">For more information, see the remarks section.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2a0e9-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="2a0e9-127">Error codes</span></span>

<span data-ttu-id="2a0e9-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="2a0e9-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a0e9-129">Notes</span><span class="sxs-lookup"><span data-stu-id="2a0e9-129">Remarks</span></span>

<span data-ttu-id="2a0e9-130">Les informations d’équilibrage de charge sont utilisées par les routeurs d’équilibrage de charge pour choisir le meilleur serveur pour le client lors de l’utilisation de batteries de serveurs hôtes de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2a0e9-130">The load balancing information is used by load balancing routers to choose the best server for the client when using farms of RD Session Host servers.</span></span> <span data-ttu-id="2a0e9-131">Le serveur hôte de session Bureau à distance n’utilise pas ces informations et l’ignore.</span><span class="sxs-lookup"><span data-stu-id="2a0e9-131">The RD Session Host server itself does not use this information and will discard it.</span></span>

<span data-ttu-id="2a0e9-132">Le cookie utilise la syntaxe suivante, qui respecte la casse :</span><span class="sxs-lookup"><span data-stu-id="2a0e9-132">The cookie uses the following, case-sensitive, syntax:</span></span>

<span data-ttu-id="2a0e9-133">**Cookie : MSTS =**_IpAddressAndPortNumber_*_\\ r \\ n_*</span><span class="sxs-lookup"><span data-stu-id="2a0e9-133">**Cookie: msts=**_IpAddressAndPortNumber_*_\\r\\n_*</span></span>

<span data-ttu-id="2a0e9-134">Où *IpAddressAndPortNumber* est l’adresse IP et le numéro de port, dans l’ordre d’octet du réseau.</span><span class="sxs-lookup"><span data-stu-id="2a0e9-134">Where *IpAddressAndPortNumber* is the IP address and port number, in network byte order.</span></span>

<span data-ttu-id="2a0e9-135">Par exemple, le cookie utilisé pour accéder à l’adresse IP de 172.31.249.216, le numéro de port 3389 est le suivant :</span><span class="sxs-lookup"><span data-stu-id="2a0e9-135">For example, the cookie used to access the IP address of 172.31.249.216, port number 3389 is as follows:</span></span>

<span data-ttu-id="2a0e9-136">**Cookie : MSTS = 3640205228.15629.0000 \\ r \\ n**</span><span class="sxs-lookup"><span data-stu-id="2a0e9-136">**Cookie: msts=3640205228.15629.0000\\r\\n**</span></span>

<span data-ttu-id="2a0e9-137">Les quatre derniers zéros sont facultatifs et sont réservés.</span><span class="sxs-lookup"><span data-stu-id="2a0e9-137">The final four zeros are optional and are reserved.</span></span> <span data-ttu-id="2a0e9-138">La dernière virgule décimale est obligatoire, tout comme le retour chariot et le saut de ligne de fin.</span><span class="sxs-lookup"><span data-stu-id="2a0e9-138">The final decimal point is required, as are the trailing carriage return and linefeed.</span></span> <span data-ttu-id="2a0e9-139">La longueur de la chaîne, en caractères, doit être un multiple pair de 2. par conséquent, ajoutez un espace si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2a0e9-139">The length of the string, in characters, must be an even multiple of 2, so add a space if necessary.</span></span>

<span data-ttu-id="2a0e9-140">Si aucun cookie n’est fourni, la valeur par défaut est **cookie : mstshash =**_username_*_\\ r \\ n_*.</span><span class="sxs-lookup"><span data-stu-id="2a0e9-140">If no cookie is supplied, the default is **Cookie: mstshash=**_UserName_*_\\r\\n_*.</span></span>

<span data-ttu-id="2a0e9-141">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2a0e9-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a0e9-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a0e9-142">Requirements</span></span>



| <span data-ttu-id="2a0e9-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a0e9-143">Requirement</span></span> | <span data-ttu-id="2a0e9-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a0e9-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0e9-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a0e9-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2a0e9-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a0e9-146">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="2a0e9-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a0e9-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2a0e9-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a0e9-148">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="2a0e9-149">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2a0e9-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="2a0e9-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a0e9-150"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2a0e9-151">DLL</span><span class="sxs-lookup"><span data-stu-id="2a0e9-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a0e9-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a0e9-152"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2a0e9-153">IID</span><span class="sxs-lookup"><span data-stu-id="2a0e9-153">IID</span></span><br/>                      | <span data-ttu-id="2a0e9-154">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="2a0e9-154">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a0e9-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a0e9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a0e9-156">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="2a0e9-156">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="2a0e9-157">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="2a0e9-157">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2a0e9-158">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="2a0e9-158">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="2a0e9-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="2a0e9-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="2a0e9-160">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2a0e9-160">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="2a0e9-161">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2a0e9-161">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="2a0e9-162">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2a0e9-162">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2a0e9-163">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="2a0e9-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





