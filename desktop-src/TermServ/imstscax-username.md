---
title: Propriété du nom d’utilisateur IMsTscAx
description: Spécifie les informations d’identification d’ouverture de session de nom d’utilisateur.
ms.assetid: 9be25003-b9aa-41bb-a5a9-512546175114
ms.tgt_platform: multiple
keywords:
- Propriété UserName Services Bureau à distance
- Propriété UserName Services Bureau à distance, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété UserName
topic_type:
- apiref
api_name:
- IMsTscAx.UserName
- IMsTscAx.get_UserName
- IMsTscAx.put_UserName
- IMsRdpClient.UserName
- IMsRdpClient.get_UserName
- IMsRdpClient.put_UserName
- IMsRdpClient2.UserName
- IMsRdpClient2.get_UserName
- IMsRdpClient2.put_UserName
- IMsRdpClient3.UserName
- IMsRdpClient3.get_UserName
- IMsRdpClient3.put_UserName
- IMsRdpClient4.UserName
- IMsRdpClient4.get_UserName
- IMsRdpClient4.put_UserName
- IMsRdpClient5.UserName
- IMsRdpClient5.get_UserName
- IMsRdpClient5.put_UserName
- IMsRdpClient6.UserName
- IMsRdpClient6.get_UserName
- IMsRdpClient6.put_UserName
- IMsRdpClient7.UserName
- IMsRdpClient7.get_UserName
- IMsRdpClient7.put_UserName
- IMsRdpClient8.UserName
- IMsRdpClient8.get_UserName
- IMsRdpClient8.put_UserName
- IMsRdpClient9.UserName
- IMsRdpClient9.get_UserName
- IMsRdpClient9.put_UserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a94a7f7d9fe5d6532de55f36a50094205fe1d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466850"
---
# <a name="imstscaxusername-property"></a><span data-ttu-id="0c71d-124">IMsTscAx :: UserName, propriété</span><span class="sxs-lookup"><span data-stu-id="0c71d-124">IMsTscAx::UserName property</span></span>

<span data-ttu-id="0c71d-125">Spécifie les informations d’identification d’ouverture de session de nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0c71d-125">Specifies the user name logon credential.</span></span>

<span data-ttu-id="0c71d-126">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0c71d-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c71d-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c71d-127">Syntax</span></span>


```C++
HRESULT put_UserName(
  [in]  BSTR newVal
);

HRESULT get_UserName(
  [out] BSTR *pUserName
);
```



## <a name="property-value"></a><span data-ttu-id="0c71d-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0c71d-128">Property value</span></span>

<span data-ttu-id="0c71d-129">Nouveau nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0c71d-129">The new user name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0c71d-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0c71d-130">Error codes</span></span>

<span data-ttu-id="0c71d-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="0c71d-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c71d-132">Notes</span><span class="sxs-lookup"><span data-stu-id="0c71d-132">Remarks</span></span>

<span data-ttu-id="0c71d-133">La définition de la propriété **username** est facultative.</span><span class="sxs-lookup"><span data-stu-id="0c71d-133">Setting the **UserName** property is optional.</span></span> <span data-ttu-id="0c71d-134">Si elle n’est pas spécifiée, l’utilisateur peut fournir un nom d’utilisateur lorsque la boîte de dialogue d’ouverture de session Windows s’affiche pendant la connexion.</span><span class="sxs-lookup"><span data-stu-id="0c71d-134">If it is not specified, the user can provide a user name when the Windows Logon dialog box appears during connection.</span></span>

<span data-ttu-id="0c71d-135">Cette propriété ne peut être définie que si le contrôle n’est pas dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="0c71d-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="0c71d-136">Elle retourne **E \_ Fail** si elle est appelée lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="0c71d-136">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="0c71d-137">Vous pouvez vérifier si le contrôle est connecté en répondant aux événements de connexion dans [**IMsTscAxEvents**](imstscaxevents-interface.md) ou en examinant la propriété [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="0c71d-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="0c71d-138">La méthode de propriété **obtenir le \_ nom d’utilisateur** alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pVersion* .</span><span class="sxs-lookup"><span data-stu-id="0c71d-138">The **get\_UserName** property method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="0c71d-139">L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="0c71d-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="0c71d-140">Cela n’est pas nécessaire pour les Visual Basic et les clients de script.</span><span class="sxs-lookup"><span data-stu-id="0c71d-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="0c71d-141">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0c71d-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c71d-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c71d-142">Requirements</span></span>



| <span data-ttu-id="0c71d-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c71d-143">Requirement</span></span> | <span data-ttu-id="0c71d-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c71d-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c71d-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c71d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0c71d-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c71d-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0c71d-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c71d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0c71d-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c71d-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0c71d-149">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0c71d-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="0c71d-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c71d-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0c71d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="0c71d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c71d-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c71d-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0c71d-153">IID</span><span class="sxs-lookup"><span data-stu-id="0c71d-153">IID</span></span><br/>                      | <span data-ttu-id="0c71d-154">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="0c71d-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0c71d-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c71d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c71d-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="0c71d-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0c71d-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0c71d-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0c71d-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0c71d-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0c71d-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0c71d-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0c71d-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0c71d-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0c71d-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0c71d-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0c71d-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0c71d-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0c71d-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0c71d-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0c71d-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0c71d-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0c71d-165">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="0c71d-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

