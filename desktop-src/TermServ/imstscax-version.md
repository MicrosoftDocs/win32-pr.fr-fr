---
title: Propriété version de IMsTscAx
description: Spécifie le numéro de version du contrôle actuel.
ms.assetid: 91ddeb4c-9d61-41e7-af96-95b0c4884682
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriétés de version
- Propriété version Services Bureau à distance, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété de version
topic_type:
- apiref
api_name:
- IMsTscAx.Version
- IMsTscAx.get_Version
- IMsRdpClient.Version
- IMsRdpClient.get_Version
- IMsRdpClient2.Version
- IMsRdpClient2.get_Version
- IMsRdpClient3.Version
- IMsRdpClient3.get_Version
- IMsRdpClient4.Version
- IMsRdpClient4.get_Version
- IMsRdpClient5.Version
- IMsRdpClient5.get_Version
- IMsRdpClient6.Version
- IMsRdpClient6.get_Version
- IMsRdpClient7.Version
- IMsRdpClient7.get_Version
- IMsRdpClient8.Version
- IMsRdpClient8.get_Version
- IMsRdpClient9.Version
- IMsRdpClient9.get_Version
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff25f274d1f076c9c4119648ccb9cc6d82f43b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465322"
---
# <a name="imstscaxversion-property"></a><span data-ttu-id="503c8-124">IMsTscAx :: version, propriété</span><span class="sxs-lookup"><span data-stu-id="503c8-124">IMsTscAx::Version property</span></span>

<span data-ttu-id="503c8-125">Spécifie le numéro de version du contrôle actuel.</span><span class="sxs-lookup"><span data-stu-id="503c8-125">Specifies the version number of the current control.</span></span>

<span data-ttu-id="503c8-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="503c8-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="503c8-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="503c8-127">Syntax</span></span>


```C++
HRESULT get_Version(
  [out] BSTR *pVersion
);
```



## <a name="property-value"></a><span data-ttu-id="503c8-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="503c8-128">Property value</span></span>

<span data-ttu-id="503c8-129">Numéro de version.</span><span class="sxs-lookup"><span data-stu-id="503c8-129">The version number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="503c8-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="503c8-130">Error codes</span></span>

<span data-ttu-id="503c8-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="503c8-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="503c8-132">Notes</span><span class="sxs-lookup"><span data-stu-id="503c8-132">Remarks</span></span>

<span data-ttu-id="503c8-133">Cette méthode alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pVersion* .</span><span class="sxs-lookup"><span data-stu-id="503c8-133">This method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="503c8-134">L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="503c8-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="503c8-135">Cela n’est pas nécessaire pour les Visual Basic et les clients de script.</span><span class="sxs-lookup"><span data-stu-id="503c8-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="503c8-136">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="503c8-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="503c8-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="503c8-137">Requirements</span></span>



| <span data-ttu-id="503c8-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="503c8-138">Requirement</span></span> | <span data-ttu-id="503c8-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="503c8-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="503c8-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="503c8-140">Minimum supported client</span></span><br/> | <span data-ttu-id="503c8-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="503c8-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="503c8-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="503c8-142">Minimum supported server</span></span><br/> | <span data-ttu-id="503c8-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="503c8-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="503c8-144">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="503c8-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="503c8-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="503c8-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="503c8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="503c8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="503c8-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="503c8-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="503c8-148">IID</span><span class="sxs-lookup"><span data-stu-id="503c8-148">IID</span></span><br/>                      | <span data-ttu-id="503c8-149">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="503c8-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="503c8-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="503c8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="503c8-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="503c8-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="503c8-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="503c8-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="503c8-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="503c8-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="503c8-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="503c8-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="503c8-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="503c8-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="503c8-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="503c8-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="503c8-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="503c8-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="503c8-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="503c8-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="503c8-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="503c8-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="503c8-160">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="503c8-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

