---
title: Propriété de domaine IMsTscAx
description: Spécifie le domaine auquel l’utilisateur actuel se connecte.
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété de domaine
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf95c02de10fe8db38a53b75d4d20cf796020f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942723"
---
# <a name="imstscaxdomain-property"></a><span data-ttu-id="e3787-124">IMsTscAx ::D propriété omaine</span><span class="sxs-lookup"><span data-stu-id="e3787-124">IMsTscAx::Domain property</span></span>

<span data-ttu-id="e3787-125">Spécifie le domaine auquel l’utilisateur actuel se connecte.</span><span class="sxs-lookup"><span data-stu-id="e3787-125">Specifies the domain to which the current user logs on.</span></span>

<span data-ttu-id="e3787-126">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e3787-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3787-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3787-127">Syntax</span></span>


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a><span data-ttu-id="e3787-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e3787-128">Property value</span></span>

<span data-ttu-id="e3787-129">Nouveau nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="e3787-129">The new domain name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e3787-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e3787-130">Error codes</span></span>

<span data-ttu-id="e3787-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="e3787-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3787-132">Notes</span><span class="sxs-lookup"><span data-stu-id="e3787-132">Remarks</span></span>

<span data-ttu-id="e3787-133">La définition de la propriété de **domaine** est facultative.</span><span class="sxs-lookup"><span data-stu-id="e3787-133">Setting the **Domain** property is optional.</span></span> <span data-ttu-id="e3787-134">S’il n’est pas défini, l’utilisateur peut choisir un domaine lorsque la boîte de dialogue d’ouverture de session Windows s’affiche pendant la connexion.</span><span class="sxs-lookup"><span data-stu-id="e3787-134">If it is not set, the user can choose a domain when the Windows Logon dialog box appears during the connection.</span></span>

<span data-ttu-id="e3787-135">La méthode **obtenir le \_ domaine** alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pDomain* .</span><span class="sxs-lookup"><span data-stu-id="e3787-135">The **get\_Domain** method allocates the memory required for the buffer pointed to by the *pDomain* parameter.</span></span> <span data-ttu-id="e3787-136">L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="e3787-136">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="e3787-137">Cela n’est pas nécessaire pour les Visual Basic et les clients de script.</span><span class="sxs-lookup"><span data-stu-id="e3787-137">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="e3787-138">Cette propriété ne peut être définie que si le contrôle n’est pas dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="e3787-138">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="e3787-139">Elle retourne **E \_ Fail** si elle est appelée lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="e3787-139">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="e3787-140">Vous pouvez vérifier si le contrôle est connecté en répondant aux événements de connexion dans [**IMsTscAxEvents**](imstscaxevents-interface.md) ou en examinant la propriété [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="e3787-140">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="e3787-141">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e3787-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3787-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3787-142">Requirements</span></span>



| <span data-ttu-id="e3787-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3787-143">Requirement</span></span> | <span data-ttu-id="e3787-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3787-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3787-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3787-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e3787-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3787-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e3787-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3787-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e3787-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3787-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e3787-149">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e3787-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3787-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3787-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e3787-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e3787-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3787-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3787-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e3787-153">IID</span><span class="sxs-lookup"><span data-stu-id="e3787-153">IID</span></span><br/>                      | <span data-ttu-id="e3787-154">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="e3787-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e3787-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3787-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3787-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="e3787-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="e3787-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e3787-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e3787-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e3787-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e3787-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e3787-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e3787-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e3787-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e3787-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e3787-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e3787-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e3787-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e3787-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e3787-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e3787-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e3787-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e3787-165">**Connecté**</span><span class="sxs-lookup"><span data-stu-id="e3787-165">**Connected**</span></span>](imstscax-connected.md)
</dt> <dt>

[<span data-ttu-id="e3787-166">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="e3787-166">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="e3787-167">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="e3787-167">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

