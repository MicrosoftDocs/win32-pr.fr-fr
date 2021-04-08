---
title: IMsTscAdvancedSettings Propriété IconFile
description: Spécifie le nom du fichier contenant les données d’icône qui seront accessibles lors de l’affichage du client en mode plein écran.
ms.assetid: 2b6ac2ad-9745-4b80-a415-4840cd8aa8b3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété IconFile
- Services Bureau à distance de la propriété IconFile, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété IconFile
- Services Bureau à distance de la propriété IconFile, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété IconFile
- Services Bureau à distance de la propriété IconFile, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété IconFile
- Services Bureau à distance de la propriété IconFile, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété IconFile
- Services Bureau à distance de la propriété IconFile, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété IconFile
- Services Bureau à distance de la propriété IconFile, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété IconFile
- Services Bureau à distance de la propriété IconFile, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété IconFile
- Services Bureau à distance de la propriété IconFile, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété IconFile
- Services Bureau à distance de la propriété IconFile, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété IconFile
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconFile
- IMsTscAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings.IconFile
- IMsRdpClientAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings2.IconFile
- IMsRdpClientAdvancedSettings2.put_IconFile
- IMsRdpClientAdvancedSettings3.IconFile
- IMsRdpClientAdvancedSettings3.put_IconFile
- IMsRdpClientAdvancedSettings4.IconFile
- IMsRdpClientAdvancedSettings4.put_IconFile
- IMsRdpClientAdvancedSettings5.IconFile
- IMsRdpClientAdvancedSettings5.put_IconFile
- IMsRdpClientAdvancedSettings6.IconFile
- IMsRdpClientAdvancedSettings6.put_IconFile
- IMsRdpClientAdvancedSettings7.IconFile
- IMsRdpClientAdvancedSettings7.put_IconFile
- IMsRdpClientAdvancedSettings8.IconFile
- IMsRdpClientAdvancedSettings8.put_IconFile
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d8f996e70873d5584bb80bbf4f40f71a7deae8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741508"
---
# <a name="imstscadvancedsettingsiconfile-property"></a><span data-ttu-id="50f57-122">IMsTscAdvancedSettings :: IconFile, propriété</span><span class="sxs-lookup"><span data-stu-id="50f57-122">IMsTscAdvancedSettings::IconFile property</span></span>

<span data-ttu-id="50f57-123">Spécifie le nom du fichier contenant les données d’icône qui seront accessibles lors de l’affichage du client en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="50f57-123">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="50f57-124">Cette propriété n’est pas prise en charge dans le contrôle ActiveX (MsRdp. ocx).</span><span class="sxs-lookup"><span data-stu-id="50f57-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="50f57-125">Il est pris en charge dans la bibliothèque MsTscAx.dll incluse dans le client standard (MsTsc.exe).</span><span class="sxs-lookup"><span data-stu-id="50f57-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="50f57-126">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="50f57-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50f57-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50f57-127">Syntax</span></span>


```C++
HRESULT put_IconFile(
  [in] BSTR IconFile
);
```



## <a name="property-value"></a><span data-ttu-id="50f57-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="50f57-128">Property value</span></span>

<span data-ttu-id="50f57-129">Chemin d’accès qualifié complet du fichier icône ou fichier contenant les données d’icône, par exemple une DLL.</span><span class="sxs-lookup"><span data-stu-id="50f57-129">The fully qualified path of icon file or a file containing icon data, such as a DLL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="50f57-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="50f57-130">Error codes</span></span>

<span data-ttu-id="50f57-131">Retourne **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="50f57-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="50f57-132">Notes</span><span class="sxs-lookup"><span data-stu-id="50f57-132">Remarks</span></span>

<span data-ttu-id="50f57-133">L’extension de nom de fichier d’un fichier d’icône est « . ico ».</span><span class="sxs-lookup"><span data-stu-id="50f57-133">The file name extension of an icon file is ".ico".</span></span>

<span data-ttu-id="50f57-134">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="50f57-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50f57-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50f57-135">Requirements</span></span>



| <span data-ttu-id="50f57-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50f57-136">Requirement</span></span> | <span data-ttu-id="50f57-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="50f57-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f57-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50f57-138">Minimum supported client</span></span><br/> | <span data-ttu-id="50f57-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50f57-139">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="50f57-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50f57-140">Minimum supported server</span></span><br/> | <span data-ttu-id="50f57-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50f57-141">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="50f57-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="50f57-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="50f57-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50f57-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="50f57-144">DLL</span><span class="sxs-lookup"><span data-stu-id="50f57-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50f57-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50f57-145"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="50f57-146">IID</span><span class="sxs-lookup"><span data-stu-id="50f57-146">IID</span></span><br/>                      | <span data-ttu-id="50f57-147">IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="50f57-147">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50f57-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50f57-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50f57-149">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="50f57-149">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="50f57-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="50f57-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="50f57-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="50f57-151">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="50f57-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="50f57-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="50f57-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="50f57-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="50f57-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="50f57-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="50f57-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="50f57-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="50f57-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="50f57-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="50f57-157">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="50f57-157">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





