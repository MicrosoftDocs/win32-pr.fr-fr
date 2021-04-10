---
title: IMsTscAx Connect, méthode
description: Établit une connexion à l’aide des propriétés actuellement définies sur le contrôle.
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Méthode Connect Services Bureau à distance
- Connect, méthode Services Bureau à distance, IMsTscAx, interface
- Services Bureau à distance de l’interface IMsTscAx, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient, interface
- Services Bureau à distance de l’interface IMsRdpClient, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient2, interface
- Services Bureau à distance de l’interface IMsRdpClient2, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient3, interface
- Services Bureau à distance de l’interface IMsRdpClient3, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient4, interface
- Services Bureau à distance de l’interface IMsRdpClient4, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient5, interface
- Services Bureau à distance de l’interface IMsRdpClient5, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient6, interface
- Services Bureau à distance de l’interface IMsRdpClient6, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient7, interface
- Services Bureau à distance de l’interface IMsRdpClient7, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient8, interface
- Services Bureau à distance de l’interface IMsRdpClient8, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient9, interface
- Services Bureau à distance de l’interface IMsRdpClient9, méthode Connect
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c267b24c3dd27dd875d895674d98e1350f757c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941873"
---
# <a name="imstscaxconnect-method"></a><span data-ttu-id="0b245-124">IMsTscAx :: Connect, méthode</span><span class="sxs-lookup"><span data-stu-id="0b245-124">IMsTscAx::Connect method</span></span>

<span data-ttu-id="0b245-125">Établit une connexion à l’aide des propriétés actuellement définies sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0b245-125">Initiates a connection using the properties currently set on the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b245-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b245-126">Syntax</span></span>


```C++
HRESULT Connect();
```



## <a name="parameters"></a><span data-ttu-id="0b245-127">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b245-127">Parameters</span></span>

<span data-ttu-id="0b245-128">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0b245-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b245-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b245-129">Return value</span></span>

<span data-ttu-id="0b245-130">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="0b245-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b245-131">Notes</span><span class="sxs-lookup"><span data-stu-id="0b245-131">Remarks</span></span>

<span data-ttu-id="0b245-132">La seule propriété requise est le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="0b245-132">The only required property is the server name.</span></span> <span data-ttu-id="0b245-133">Reportez-vous à la propriété de [**serveur**](imstscax-server.md) .</span><span class="sxs-lookup"><span data-stu-id="0b245-133">Refer to the [**Server**](imstscax-server.md) property.</span></span>

<span data-ttu-id="0b245-134">Le contrôle se connecte de manière asynchrone, de sorte qu’un retour d’un appel de connexion indique uniquement que la connexion a été lancée avec succès, et non qu’elle est terminée.</span><span class="sxs-lookup"><span data-stu-id="0b245-134">The control connects asynchronously, so a return from a Connect call indicates only that the connection has been initiated successfully, not that it has been completed.</span></span> <span data-ttu-id="0b245-135">Vous devez répondre aux événements sur l’interface [**IMsTscAxEvents**](imstscaxevents-interface.md) pour déterminer quand le contrôle s’est connecté avec succès (ou a été déconnecté).</span><span class="sxs-lookup"><span data-stu-id="0b245-135">You should respond to events on the [**IMsTscAxEvents**](imstscaxevents-interface.md) interface to determine when the control has successfully connected (or has been disconnected.)</span></span>

<span data-ttu-id="0b245-136">Cette méthode retourne **E \_ Fail** si elle est appelée alors que le contrôle est déjà connecté ou à l’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="0b245-136">This method returns **E\_FAIL** if it is called while the control is already connected or in the connecting state.</span></span>

<span data-ttu-id="0b245-137">Une fois que la **connexion** a été appelée, la plupart des propriétés de contrôle ne peuvent plus être définies tant que le contrôle n’est pas retourné à l’État Disconnected.</span><span class="sxs-lookup"><span data-stu-id="0b245-137">After **Connect** has been called, most of the control properties can no longer be set until the control returns to the disconnected state.</span></span>

<span data-ttu-id="0b245-138">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0b245-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b245-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b245-139">Requirements</span></span>



| <span data-ttu-id="0b245-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b245-140">Requirement</span></span> | <span data-ttu-id="0b245-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b245-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b245-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b245-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0b245-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b245-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0b245-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b245-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0b245-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b245-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0b245-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0b245-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b245-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b245-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b245-148">DLL</span><span class="sxs-lookup"><span data-stu-id="0b245-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b245-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b245-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b245-150">IID</span><span class="sxs-lookup"><span data-stu-id="0b245-150">IID</span></span><br/>                      | <span data-ttu-id="0b245-151">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="0b245-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0b245-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b245-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b245-153">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="0b245-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0b245-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0b245-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0b245-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0b245-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0b245-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0b245-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0b245-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0b245-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0b245-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0b245-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0b245-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0b245-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0b245-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0b245-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0b245-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0b245-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0b245-162">**Déconnecter**</span><span class="sxs-lookup"><span data-stu-id="0b245-162">**Disconnect**</span></span>](imstscax-disconnect.md)
</dt> <dt>

[<span data-ttu-id="0b245-163">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="0b245-163">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





