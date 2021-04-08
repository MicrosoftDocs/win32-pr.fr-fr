---
title: IMsTscAx propriété DisconnectedText
description: Spécifie le texte qui apparaît centré dans le contrôle avant qu’une connexion ne soit terminée.
ms.assetid: ec7efe7a-8fb9-4c45-8e16-78951365de13
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété DisconnectedText
topic_type:
- apiref
api_name:
- IMsTscAx.DisconnectedText
- IMsTscAx.get_DisconnectedText
- IMsTscAx.put_DisconnectedText
- IMsRdpClient.DisconnectedText
- IMsRdpClient.get_DisconnectedText
- IMsRdpClient.put_DisconnectedText
- IMsRdpClient2.DisconnectedText
- IMsRdpClient2.get_DisconnectedText
- IMsRdpClient2.put_DisconnectedText
- IMsRdpClient3.DisconnectedText
- IMsRdpClient3.get_DisconnectedText
- IMsRdpClient3.put_DisconnectedText
- IMsRdpClient4.DisconnectedText
- IMsRdpClient4.get_DisconnectedText
- IMsRdpClient4.put_DisconnectedText
- IMsRdpClient5.DisconnectedText
- IMsRdpClient5.get_DisconnectedText
- IMsRdpClient5.put_DisconnectedText
- IMsRdpClient6.DisconnectedText
- IMsRdpClient6.get_DisconnectedText
- IMsRdpClient6.put_DisconnectedText
- IMsRdpClient7.DisconnectedText
- IMsRdpClient7.get_DisconnectedText
- IMsRdpClient7.put_DisconnectedText
- IMsRdpClient8.DisconnectedText
- IMsRdpClient8.get_DisconnectedText
- IMsRdpClient8.put_DisconnectedText
- IMsRdpClient9.DisconnectedText
- IMsRdpClient9.get_DisconnectedText
- IMsRdpClient9.put_DisconnectedText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4768e639cbfb1543e06c03f2d9e6566d0adb147e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742125"
---
# <a name="imstscaxdisconnectedtext-property"></a><span data-ttu-id="a72e5-124">IMsTscAx ::D propriété isconnectedText</span><span class="sxs-lookup"><span data-stu-id="a72e5-124">IMsTscAx::DisconnectedText property</span></span>

<span data-ttu-id="a72e5-125">Spécifie le texte qui apparaît centré dans le contrôle avant qu’une connexion ne soit terminée.</span><span class="sxs-lookup"><span data-stu-id="a72e5-125">Specifies the text that appears centered in the control before a connection is terminated.</span></span>

<span data-ttu-id="a72e5-126">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a72e5-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a72e5-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a72e5-127">Syntax</span></span>


```C++
HRESULT put_DisconnectedText(
  [in]  BSTR newVal
);

HRESULT get_DisconnectedText(
  [out] BSTR *pDisconnectedText
);
```



## <a name="property-value"></a><span data-ttu-id="a72e5-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a72e5-128">Property value</span></span>

<span data-ttu-id="a72e5-129">Nouveau texte affiché.</span><span class="sxs-lookup"><span data-stu-id="a72e5-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a72e5-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a72e5-130">Error codes</span></span>

<span data-ttu-id="a72e5-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a72e5-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a72e5-132">Notes</span><span class="sxs-lookup"><span data-stu-id="a72e5-132">Remarks</span></span>

<span data-ttu-id="a72e5-133">La définition de la propriété **DisconnectedText** est facultative.</span><span class="sxs-lookup"><span data-stu-id="a72e5-133">Setting the **DisconnectedText** property is optional.</span></span> <span data-ttu-id="a72e5-134">S’il n’est pas spécifié, le contrôle apparaît vide avant l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="a72e5-134">If it is not specified the control appears blank before a connection is established.</span></span>

<span data-ttu-id="a72e5-135">Cette propriété ne peut être définie que si le contrôle n’est pas dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="a72e5-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="a72e5-136">La méthode retourne **E \_ Fail** si elle est appelée après la connexion du contrôle.</span><span class="sxs-lookup"><span data-stu-id="a72e5-136">The method returns **E\_FAIL** if it is called after the control is connected.</span></span> <span data-ttu-id="a72e5-137">Vous pouvez vérifier si le contrôle est connecté en répondant aux événements de connexion dans [**IMsTscAxEvents**](imstscaxevents-interface.md) ou en examinant la propriété [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="a72e5-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="a72e5-138">Cette méthode alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pDisconnectedText* .</span><span class="sxs-lookup"><span data-stu-id="a72e5-138">This method allocates the memory required for the buffer pointed to by the *pDisconnectedText* parameter.</span></span> <span data-ttu-id="a72e5-139">L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="a72e5-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="a72e5-140">Cela n’est pas nécessaire pour les Visual Basic et les clients de script.</span><span class="sxs-lookup"><span data-stu-id="a72e5-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="a72e5-141">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a72e5-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a72e5-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a72e5-142">Requirements</span></span>



| <span data-ttu-id="a72e5-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a72e5-143">Requirement</span></span> | <span data-ttu-id="a72e5-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="a72e5-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a72e5-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a72e5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a72e5-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a72e5-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a72e5-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a72e5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a72e5-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a72e5-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a72e5-149">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a72e5-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="a72e5-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a72e5-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a72e5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="a72e5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a72e5-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a72e5-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a72e5-153">IID</span><span class="sxs-lookup"><span data-stu-id="a72e5-153">IID</span></span><br/>                      | <span data-ttu-id="a72e5-154">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="a72e5-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a72e5-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a72e5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a72e5-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="a72e5-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="a72e5-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="a72e5-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="a72e5-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="a72e5-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="a72e5-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="a72e5-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="a72e5-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a72e5-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a72e5-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a72e5-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a72e5-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a72e5-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a72e5-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a72e5-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a72e5-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a72e5-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a72e5-165">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="a72e5-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

