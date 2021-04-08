---
title: IMsTscNonScriptable propriété ClearTextPassword
description: Définit le mot de passe du contrôle ActiveX Bureau à distance au format texte brut.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsTscNonScriptable
- Services Bureau à distance de l’interface IMsTscNonScriptable, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientNonScriptable
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientNonScriptable2
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété ClearTextPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743525"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a><span data-ttu-id="a8825-124">IMsTscNonScriptable :: ClearTextPassword, propriété</span><span class="sxs-lookup"><span data-stu-id="a8825-124">IMsTscNonScriptable::ClearTextPassword property</span></span>

<span data-ttu-id="a8825-125">Définit le mot de passe du contrôle ActiveX Bureau à distance au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="a8825-125">Sets the Remote Desktop ActiveX control password in plaintext format.</span></span>

<span data-ttu-id="a8825-126">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="a8825-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8825-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8825-127">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a><span data-ttu-id="a8825-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a8825-128">Property value</span></span>

<span data-ttu-id="a8825-129">Mot de passe à utiliser pour la connexion, spécifié au format texte en clair.</span><span class="sxs-lookup"><span data-stu-id="a8825-129">The password to be used to connect, specified in plaintext format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a8825-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a8825-130">Error codes</span></span>

<span data-ttu-id="a8825-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a8825-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8825-132">Notes</span><span class="sxs-lookup"><span data-stu-id="a8825-132">Remarks</span></span>

<span data-ttu-id="a8825-133">Le mot de passe est transmis au serveur dans le canal de communications RDP chiffré en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="a8825-133">The password is passed to the server in the safely encrypted RDP communications channel.</span></span> <span data-ttu-id="a8825-134">Une fois qu’un mot de passe en texte clair est défini, il ne peut pas être récupéré au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="a8825-134">After a plaintext password is set, it cannot be retrieved in plaintext format.</span></span>

<span data-ttu-id="a8825-135">La propriété **ClearTextPassword** peut uniquement être définie lorsque le contrôle ActiveX Bureau à distance n’est pas dans l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="a8825-135">The **ClearTextPassword** property can only be set when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="a8825-136">La définition de cette propriété échoue si le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="a8825-136">Setting this property fails if the control is connected.</span></span> <span data-ttu-id="a8825-137">Pour vérifier l’état connecté, récupérez la propriété [**IMsTscAx :: Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="a8825-137">To check for the connected state, retrieve the [**IMsTscAx::Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="a8825-138">Vous pouvez également appeler cette méthode pour définir un mot de passe en texte clair avant de le convertir en un mot de passe encodé portable ou en un mot de passe encodé binaire (non transférable).</span><span class="sxs-lookup"><span data-stu-id="a8825-138">You can also call this method to set a plaintext password before converting it to either a portable encoded password or to a binary (nonportable) encoded password.</span></span> <span data-ttu-id="a8825-139">Notez cependant que les mots de passe encodés ne doivent pas être considérés comme étant chiffrés de manière sécurisée.</span><span class="sxs-lookup"><span data-stu-id="a8825-139">Note however that encoded passwords should not be considered securely encrypted.</span></span>

<span data-ttu-id="a8825-140">Si vous appelez pour la première fois cette méthode pour définir un mot de passe au format texte brut, vous pouvez convertir le mot de passe au format encodé.</span><span class="sxs-lookup"><span data-stu-id="a8825-140">If you first call this method to set a password in plaintext format, you can then convert the password to encoded format.</span></span>

<span data-ttu-id="a8825-141">**Pour convertir un mot de passe en texte clair au format encodé**</span><span class="sxs-lookup"><span data-stu-id="a8825-141">**To convert a plaintext password to encoded format**</span></span>

1.  <span data-ttu-id="a8825-142">Définissez le mot de passe au format texte en clair dans la propriété **ClearTextPassword** .</span><span class="sxs-lookup"><span data-stu-id="a8825-142">Set the password in plaintext format in the **ClearTextPassword** property.</span></span>
2.  <span data-ttu-id="a8825-143">Pour récupérer le mot de passe dans un format encodé binaire (à l’importable), récupérez la propriété [**BinaryPassword**](imstscnonscriptable-binarypassword.md) et les propriétés [**BinarySalt**](imstscnonscriptable-binarysalt.md) .</span><span class="sxs-lookup"><span data-stu-id="a8825-143">To retrieve the password in binary (nonportable) encoded format, retrieve the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) property and the [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties.</span></span> <span data-ttu-id="a8825-144">La partie de mot de passe encodée et la partie Salt sont requises pour définir un mot de passe au format encodé binaire.</span><span class="sxs-lookup"><span data-stu-id="a8825-144">Both the encoded password part and the salt part are required to set a password in binary encoded format.</span></span>
3.  <span data-ttu-id="a8825-145">Pour récupérer le mot de passe dans un format encodé portable, récupérez la méthode [**PortablePassword**](imstscnonscriptable-portablepassword.md) et les propriétés [**PortableSalt**](imstscnonscriptable-portablesalt.md) .</span><span class="sxs-lookup"><span data-stu-id="a8825-145">To retrieve the password in portable encoded format, retrieve the [**PortablePassword**](imstscnonscriptable-portablepassword.md) method and the [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="a8825-146">Les deux parties sont requises pour définir un mot de passe dans un format encodé portable.</span><span class="sxs-lookup"><span data-stu-id="a8825-146">Both parts are required to set a password in portable encoded format.</span></span>

<span data-ttu-id="a8825-147">Après avoir suivi les trois étapes précédentes, vous pouvez définir le mot de passe au format encodé en définissant les propriétés [**BinaryPassword**](imstscnonscriptable-binarypassword.md) et [**BinarySalt**](imstscnonscriptable-binarysalt.md) , ou les propriétés [**PortablePassword**](imstscnonscriptable-portablepassword.md) et [**PortableSalt**](imstscnonscriptable-portablesalt.md) .</span><span class="sxs-lookup"><span data-stu-id="a8825-147">After following the preceding three steps, you can set the password in encoded format by setting the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) and [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties, or [**PortablePassword**](imstscnonscriptable-portablepassword.md) and [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="a8825-148">Les deux parties sont requises.</span><span class="sxs-lookup"><span data-stu-id="a8825-148">Both parts are required.</span></span>

<span data-ttu-id="a8825-149">Pour activer l’ouverture de session automatique, vous devez également définir les propriétés de [**nom d’utilisateur**](imstscax-username.md) et de [**domaine**](imstscax-domain.md) .</span><span class="sxs-lookup"><span data-stu-id="a8825-149">To enable automatic logon, you must also set the [**UserName**](imstscax-username.md) and [**Domain**](imstscax-domain.md) properties.</span></span> <span data-ttu-id="a8825-150">Si le mot de passe ne parvient pas à authentifier l’utilisateur, la boîte de dialogue d’ouverture de session Windows s’affiche sur le serveur pour inviter l’utilisateur à entrer le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a8825-150">If the password fails to authenticate the user, the Windows Logon dialog box is displayed at the server to prompt the user for the password.</span></span>

<span data-ttu-id="a8825-151">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a8825-151">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8825-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8825-152">Requirements</span></span>



| <span data-ttu-id="a8825-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8825-153">Requirement</span></span> | <span data-ttu-id="a8825-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8825-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8825-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8825-155">Minimum supported client</span></span><br/> | <span data-ttu-id="a8825-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8825-156">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a8825-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8825-157">Minimum supported server</span></span><br/> | <span data-ttu-id="a8825-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8825-158">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a8825-159">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a8825-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8825-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8825-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8825-161">DLL</span><span class="sxs-lookup"><span data-stu-id="a8825-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8825-162"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8825-162"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8825-163">IID</span><span class="sxs-lookup"><span data-stu-id="a8825-163">IID</span></span><br/>                      | <span data-ttu-id="a8825-164">IID \_ IMsTscNonScriptable est défini en tant que c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="a8825-164">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8825-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8825-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8825-166">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="a8825-166">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="a8825-167">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="a8825-167">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="a8825-168">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="a8825-168">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="a8825-169">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="a8825-169">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="a8825-170">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a8825-170">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="a8825-171">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="a8825-171">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





