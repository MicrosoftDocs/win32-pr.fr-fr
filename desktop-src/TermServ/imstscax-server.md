---
title: Propriété de serveur IMsTscAx (Asptlb. h)
description: Spécifie le nom du serveur auquel le contrôle actuel est connecté.
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriétés de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété de serveur
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7be04c149e2ac10c1a3e905678bd2b5f663cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941749"
---
# <a name="imstscaxserver-property"></a><span data-ttu-id="ebbb2-124">IMsTscAx :: Server, propriété</span><span class="sxs-lookup"><span data-stu-id="ebbb2-124">IMsTscAx::Server property</span></span>

<span data-ttu-id="ebbb2-125">Spécifie le nom du serveur auquel le contrôle actuel est connecté.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-125">Specifies the name of the server to which the current control is connected.</span></span>

<span data-ttu-id="ebbb2-126">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebbb2-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebbb2-127">Syntax</span></span>


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a><span data-ttu-id="ebbb2-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ebbb2-128">Property value</span></span>

<span data-ttu-id="ebbb2-129">Nouveau nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-129">The new server name.</span></span> <span data-ttu-id="ebbb2-130">Ce paramètre peut être un nom DNS ou une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-130">This parameter can be a DNS name or IP address.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ebbb2-131">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ebbb2-131">Error codes</span></span>

<span data-ttu-id="ebbb2-132">Si les méthodes sont correctement exécutées, la méthode **S \_ OK** est retournée.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="ebbb2-133">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebbb2-134">Notes</span><span class="sxs-lookup"><span data-stu-id="ebbb2-134">Remarks</span></span>

<span data-ttu-id="ebbb2-135">Cette propriété doit être définie avant d’appeler la méthode [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="ebbb2-135">This property must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="ebbb2-136">Il s’agit de la seule propriété qui doit être définie avant la connexion.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-136">It is the only property that must be set before connecting.</span></span>

<span data-ttu-id="ebbb2-137">Cette propriété ne peut être définie que si le contrôle n’est pas dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="ebbb2-138">Cette propriété retourne **E \_ Fail** si elle est appelée lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-138">This property returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="ebbb2-139">Vous pouvez vérifier l’état connecté à l’aide de la propriété [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="ebbb2-139">You can check for the connected state by using the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="ebbb2-140">Cette méthode alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pserver* .</span><span class="sxs-lookup"><span data-stu-id="ebbb2-140">This method allocates the memory required for the buffer pointed to by the *pServer* parameter.</span></span> <span data-ttu-id="ebbb2-141">L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="ebbb2-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="ebbb2-142">Cela n’est pas nécessaire pour les Visual Basic et les clients de script.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="ebbb2-143">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ebbb2-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebbb2-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebbb2-144">Requirements</span></span>



| <span data-ttu-id="ebbb2-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebbb2-145">Requirement</span></span> | <span data-ttu-id="ebbb2-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebbb2-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebbb2-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebbb2-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ebbb2-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebbb2-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ebbb2-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebbb2-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ebbb2-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebbb2-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ebbb2-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebbb2-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebbb2-152"><dt>Asptlb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebbb2-152"><dt>Asptlb.h</dt></span></span> </dl>    |
| <span data-ttu-id="ebbb2-153">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ebbb2-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebbb2-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebbb2-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebbb2-155">DLL</span><span class="sxs-lookup"><span data-stu-id="ebbb2-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebbb2-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebbb2-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebbb2-157">IID</span><span class="sxs-lookup"><span data-stu-id="ebbb2-157">IID</span></span><br/>                      | <span data-ttu-id="ebbb2-158">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="ebbb2-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ebbb2-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebbb2-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebbb2-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="ebbb2-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="ebbb2-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="ebbb2-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="ebbb2-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ebbb2-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ebbb2-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ebbb2-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ebbb2-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ebbb2-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

