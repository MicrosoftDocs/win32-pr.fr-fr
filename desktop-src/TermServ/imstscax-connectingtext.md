---
title: IMsTscAx propriété ConnectingText
description: Spécifie le texte qui apparaît centré dans le contrôle pendant la connexion du contrôle.
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété ConnectingText
topic_type:
- apiref
api_name:
- IMsTscAx.ConnectingText
- IMsTscAx.get_ConnectingText
- IMsTscAx.put_ConnectingText
- IMsRdpClient.ConnectingText
- IMsRdpClient.get_ConnectingText
- IMsRdpClient.put_ConnectingText
- IMsRdpClient2.ConnectingText
- IMsRdpClient2.get_ConnectingText
- IMsRdpClient2.put_ConnectingText
- IMsRdpClient3.ConnectingText
- IMsRdpClient3.get_ConnectingText
- IMsRdpClient3.put_ConnectingText
- IMsRdpClient4.ConnectingText
- IMsRdpClient4.get_ConnectingText
- IMsRdpClient4.put_ConnectingText
- IMsRdpClient5.ConnectingText
- IMsRdpClient5.get_ConnectingText
- IMsRdpClient5.put_ConnectingText
- IMsRdpClient6.ConnectingText
- IMsRdpClient6.get_ConnectingText
- IMsRdpClient6.put_ConnectingText
- IMsRdpClient7.ConnectingText
- IMsRdpClient7.get_ConnectingText
- IMsRdpClient7.put_ConnectingText
- IMsRdpClient8.ConnectingText
- IMsRdpClient8.get_ConnectingText
- IMsRdpClient8.put_ConnectingText
- IMsRdpClient9.ConnectingText
- IMsRdpClient9.get_ConnectingText
- IMsRdpClient9.put_ConnectingText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433da7d159f1fe5bf44114a0b76ed9b4d807046f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384980"
---
# <a name="imstscaxconnectingtext-property"></a><span data-ttu-id="062d1-124">IMsTscAx :: ConnectingText, propriété</span><span class="sxs-lookup"><span data-stu-id="062d1-124">IMsTscAx::ConnectingText property</span></span>

<span data-ttu-id="062d1-125">Spécifie le texte qui apparaît centré dans le contrôle pendant la connexion du contrôle.</span><span class="sxs-lookup"><span data-stu-id="062d1-125">Specifies the text that appears centered in the control while the control is connecting.</span></span>

<span data-ttu-id="062d1-126">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="062d1-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="062d1-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="062d1-127">Syntax</span></span>


```C++
HRESULT put_ConnectingText(
  [in]  BSTR newVal
);

HRESULT get_ConnectingText(
  [out] BSTR *pConnectingText
);
```



## <a name="property-value"></a><span data-ttu-id="062d1-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="062d1-128">Property value</span></span>

<span data-ttu-id="062d1-129">Nouveau texte affiché.</span><span class="sxs-lookup"><span data-stu-id="062d1-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="062d1-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="062d1-130">Error codes</span></span>

<span data-ttu-id="062d1-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="062d1-131">Return **S\_OK** if successful.</span></span>

<span data-ttu-id="062d1-132">Retourne un **HRESULT** différent de zéro si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="062d1-132">Return a nonzero **HRESULT** if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="062d1-133">Notes</span><span class="sxs-lookup"><span data-stu-id="062d1-133">Remarks</span></span>

<span data-ttu-id="062d1-134">Exemple de texte de connexion : « connexion au serveur... ».</span><span class="sxs-lookup"><span data-stu-id="062d1-134">An example of connection text is "Connecting to server ...".</span></span>

<span data-ttu-id="062d1-135">La définition de la propriété **ConnectingText** est facultative.</span><span class="sxs-lookup"><span data-stu-id="062d1-135">Setting the **ConnectingText** property is optional.</span></span> <span data-ttu-id="062d1-136">S’il n’est pas défini, le contrôle apparaît vide avant l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="062d1-136">If it is not set, the control appears blank before a connection is established.</span></span>

<span data-ttu-id="062d1-137">Cette propriété ne peut être définie que si le contrôle n’est pas dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="062d1-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="062d1-138">Elle retourne **E \_ Fail** si elle est appelée lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="062d1-138">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="062d1-139">Vous pouvez vérifier si le contrôle est connecté en répondant aux événements de connexion dans [**IMsTscAxEvents**](imstscaxevents-interface.md) ou en examinant la propriété [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="062d1-139">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="062d1-140">La méthode de propriété **obtenir \_ ConnectingText** alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pConnectingText* .</span><span class="sxs-lookup"><span data-stu-id="062d1-140">The **get\_ConnectingText** property method allocates the memory required for the buffer pointed to by the *pConnectingText* parameter.</span></span> <span data-ttu-id="062d1-141">L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="062d1-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="062d1-142">Cela n’est pas nécessaire pour les Visual Basic et les clients de script.</span><span class="sxs-lookup"><span data-stu-id="062d1-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="062d1-143">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="062d1-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="062d1-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="062d1-144">Requirements</span></span>



| <span data-ttu-id="062d1-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="062d1-145">Requirement</span></span> | <span data-ttu-id="062d1-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="062d1-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="062d1-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="062d1-147">Minimum supported client</span></span><br/> | <span data-ttu-id="062d1-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="062d1-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="062d1-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="062d1-149">Minimum supported server</span></span><br/> | <span data-ttu-id="062d1-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="062d1-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="062d1-151">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="062d1-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="062d1-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="062d1-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="062d1-153">DLL</span><span class="sxs-lookup"><span data-stu-id="062d1-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="062d1-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="062d1-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="062d1-155">IID</span><span class="sxs-lookup"><span data-stu-id="062d1-155">IID</span></span><br/>                      | <span data-ttu-id="062d1-156">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="062d1-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="062d1-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="062d1-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="062d1-158">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="062d1-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="062d1-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="062d1-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="062d1-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="062d1-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="062d1-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="062d1-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="062d1-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="062d1-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="062d1-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="062d1-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="062d1-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="062d1-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="062d1-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="062d1-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="062d1-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="062d1-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="062d1-167">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="062d1-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

