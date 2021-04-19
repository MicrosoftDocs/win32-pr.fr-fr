---
title: IMsRdpClient2 propriété ConnectedStatusText
description: Contient le texte affiché dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.
ms.assetid: c3d8433b-2fb0-413d-88a3-667149f858ba
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété ConnectedStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient2.ConnectedStatusText
- IMsRdpClient2.get_ConnectedStatusText
- IMsRdpClient2.put_ConnectedStatusText
- IMsRdpClient3.ConnectedStatusText
- IMsRdpClient3.get_ConnectedStatusText
- IMsRdpClient3.put_ConnectedStatusText
- IMsRdpClient4.ConnectedStatusText
- IMsRdpClient4.get_ConnectedStatusText
- IMsRdpClient4.put_ConnectedStatusText
- IMsRdpClient5.ConnectedStatusText
- IMsRdpClient5.get_ConnectedStatusText
- IMsRdpClient5.put_ConnectedStatusText
- IMsRdpClient6.ConnectedStatusText
- IMsRdpClient6.get_ConnectedStatusText
- IMsRdpClient6.put_ConnectedStatusText
- IMsRdpClient7.ConnectedStatusText
- IMsRdpClient7.get_ConnectedStatusText
- IMsRdpClient7.put_ConnectedStatusText
- IMsRdpClient8.ConnectedStatusText
- IMsRdpClient8.get_ConnectedStatusText
- IMsRdpClient8.put_ConnectedStatusText
- IMsRdpClient9.ConnectedStatusText
- IMsRdpClient9.get_ConnectedStatusText
- IMsRdpClient9.put_ConnectedStatusText
- IMsRdpClient10.ConnectedStatusText
- IMsRdpClient10.get_ConnectedStatusText
- IMsRdpClient10.put_ConnectedStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd6ee2ac155aa3fc4873ee1a5eb890774b50978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510945"
---
# <a name="imsrdpclient2connectedstatustext-property"></a><span data-ttu-id="78af4-122">IMsRdpClient2 :: ConnectedStatusText, propriété</span><span class="sxs-lookup"><span data-stu-id="78af4-122">IMsRdpClient2::ConnectedStatusText property</span></span>

<span data-ttu-id="78af4-123">Contient le texte affiché dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="78af4-123">Contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

<span data-ttu-id="78af4-124">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="78af4-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="78af4-125">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78af4-125">Syntax</span></span>


```C++
HRESULT put_ConnectedStatusText(
  [in]  BSTR newVal
);

HRESULT get_ConnectedStatusText(
  [out] BSTR *pConnectedStatusText
);
```



## <a name="property-value"></a><span data-ttu-id="78af4-126">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="78af4-126">Property value</span></span>

<span data-ttu-id="78af4-127">La propriété **ConnectedStatusText** contient le texte affiché dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="78af4-127">The **ConnectedStatusText** property contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

## <a name="error-codes"></a><span data-ttu-id="78af4-128">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="78af4-128">Error codes</span></span>

<span data-ttu-id="78af4-129">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="78af4-129">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="78af4-130">Notes</span><span class="sxs-lookup"><span data-stu-id="78af4-130">Remarks</span></span>

<span data-ttu-id="78af4-131">Texte à afficher dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="78af4-131">Text to display in the client area of the control while the control is in the connected state.</span></span> <span data-ttu-id="78af4-132">Il s’agit du texte qui est visible, par exemple, lorsque l’utilisateur bascule le contrôle en mode plein écran dans un navigateur Web, un scénario qui laisse une partie du contrôle hébergé dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="78af4-132">This is the text that is visible, for example, when the user switches the control to the full-screen mode in a web browser, a scenario that leaves a portion of the control hosted in the browser.</span></span>

<span data-ttu-id="78af4-133">La méthode **obtenir \_ ConnectedStatusText** alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pConnectedStatusText* .</span><span class="sxs-lookup"><span data-stu-id="78af4-133">The **get\_ConnectedStatusText** method allocates the memory required for the buffer pointed to by the *pConnectedStatusText* parameter.</span></span> <span data-ttu-id="78af4-134">L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="78af4-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="78af4-135">Cela n’est pas nécessaire pour les Visual Basic et les clients de script.</span><span class="sxs-lookup"><span data-stu-id="78af4-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="78af4-136">Cette propriété ne peut pas être définie lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="78af4-136">This property cannot be set when the control is connected.</span></span> <span data-ttu-id="78af4-137">Vous pouvez vérifier si le contrôle est connecté en appelant la méthode [**IMsTscAx :: \_ Connect Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="78af4-137">You can check if the control is connected by calling the [**IMsTscAx::get\_Connected**](imstscax-connected.md) method.</span></span>

<span data-ttu-id="78af4-138">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="78af4-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78af4-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78af4-139">Requirements</span></span>



| <span data-ttu-id="78af4-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78af4-140">Requirement</span></span> | <span data-ttu-id="78af4-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="78af4-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78af4-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78af4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="78af4-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78af4-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="78af4-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78af4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="78af4-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78af4-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="78af4-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="78af4-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="78af4-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78af4-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="78af4-148">DLL</span><span class="sxs-lookup"><span data-stu-id="78af4-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78af4-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78af4-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="78af4-150">IID</span><span class="sxs-lookup"><span data-stu-id="78af4-150">IID</span></span><br/>                      | <span data-ttu-id="78af4-151">IID \_ IMsRdpClient2 est défini en tant que e7e17dc4-3b71-4BA7-a8e6-281ffadca28f</span><span class="sxs-lookup"><span data-stu-id="78af4-151">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="78af4-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78af4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78af4-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="78af4-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="78af4-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="78af4-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="78af4-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="78af4-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="78af4-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="78af4-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="78af4-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="78af4-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="78af4-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="78af4-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="78af4-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="78af4-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="78af4-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="78af4-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="78af4-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="78af4-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

