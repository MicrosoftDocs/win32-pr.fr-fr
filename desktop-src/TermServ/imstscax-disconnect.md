---
title: Méthode de déconnexion IMsTscAx
description: Déconnecte la connexion active.
ms.assetid: 9fcffd45-b293-4650-be8f-1b0d01d592a2
ms.tgt_platform: multiple
keywords:
- Méthode Disconnect Services Bureau à distance
- Méthode Disconnect Services Bureau à distance, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode Disconnect
topic_type:
- apiref
api_name:
- IMsTscAx.Disconnect
- IMsRdpClient.Disconnect
- IMsRdpClient2.Disconnect
- IMsRdpClient3.Disconnect
- IMsRdpClient4.Disconnect
- IMsRdpClient5.Disconnect
- IMsRdpClient6.Disconnect
- IMsRdpClient7.Disconnect
- IMsRdpClient8.Disconnect
- IMsRdpClient9.Disconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4f1545a8244209c0b4fa8267fcc8ce2a41e090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508842"
---
# <a name="imstscaxdisconnect-method"></a><span data-ttu-id="a4b66-124">IMsTscAx ::D méthode éconnecter</span><span class="sxs-lookup"><span data-stu-id="a4b66-124">IMsTscAx::Disconnect method</span></span>

<span data-ttu-id="a4b66-125">Déconnecte la connexion active.</span><span class="sxs-lookup"><span data-stu-id="a4b66-125">Disconnects the active connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b66-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4b66-126">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="a4b66-127">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4b66-127">Parameters</span></span>

<span data-ttu-id="a4b66-128">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a4b66-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4b66-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4b66-129">Return value</span></span>

<span data-ttu-id="a4b66-130">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a4b66-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b66-131">Notes</span><span class="sxs-lookup"><span data-stu-id="a4b66-131">Remarks</span></span>

<span data-ttu-id="a4b66-132">Cette méthode retourne une valeur d’erreur d’échec si elle est appelée lorsque le contrôle n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="a4b66-132">This method returns a failure error value if it is called when the control is not connected.</span></span>

<span data-ttu-id="a4b66-133">Il est également possible de déconnecter le contrôle en fermant sa fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="a4b66-133">It is also possible to disconnect the control by closing its main window.</span></span> <span data-ttu-id="a4b66-134">Par exemple, si le contrôle est hébergé dans une page Web, il n’est pas nécessaire d’appeler cette méthode avant de quitter la page ; la fermeture du contrôle déclenche une déconnexion.</span><span class="sxs-lookup"><span data-stu-id="a4b66-134">For example, if the control is hosted in a webpage, it is not necessary to call this method before leaving the page; the closing of the control triggers a disconnection.</span></span>

<span data-ttu-id="a4b66-135">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a4b66-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b66-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4b66-136">Requirements</span></span>



| <span data-ttu-id="a4b66-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4b66-137">Requirement</span></span> | <span data-ttu-id="a4b66-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4b66-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b66-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4b66-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b66-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4b66-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a4b66-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4b66-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b66-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4b66-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a4b66-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a4b66-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4b66-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b66-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4b66-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b66-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4b66-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b66-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4b66-147">IID</span><span class="sxs-lookup"><span data-stu-id="a4b66-147">IID</span></span><br/>                      | <span data-ttu-id="a4b66-148">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="a4b66-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a4b66-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4b66-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b66-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="a4b66-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="a4b66-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="a4b66-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="a4b66-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="a4b66-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="a4b66-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="a4b66-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="a4b66-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a4b66-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a4b66-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a4b66-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a4b66-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a4b66-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a4b66-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a4b66-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a4b66-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a4b66-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a4b66-159">**Se connecter**</span><span class="sxs-lookup"><span data-stu-id="a4b66-159">**Connect**</span></span>](imstscax-connect.md)
</dt> <dt>

[<span data-ttu-id="a4b66-160">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="a4b66-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





