---
title: IMsTscAdvancedSettings propriété PluginDlls
description: Spécifie les noms des dll clientes du canal virtuel à charger.
ms.assetid: 4b248fb8-200a-4ce0-8c8e-ce1692a80d88
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PluginDlls
- Services Bureau à distance de la propriété PluginDlls, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété PluginDlls
- Services Bureau à distance de la propriété PluginDlls, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété PluginDlls
- Services Bureau à distance de la propriété PluginDlls, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété PluginDlls
- Services Bureau à distance de la propriété PluginDlls, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété PluginDlls
- Services Bureau à distance de la propriété PluginDlls, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété PluginDlls
- Services Bureau à distance de la propriété PluginDlls, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété PluginDlls
- Services Bureau à distance de la propriété PluginDlls, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété PluginDlls
- Services Bureau à distance de la propriété PluginDlls, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété PluginDlls
- Services Bureau à distance de la propriété PluginDlls, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété PluginDlls
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.PluginDlls
- IMsTscAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings.PluginDlls
- IMsRdpClientAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings2.PluginDlls
- IMsRdpClientAdvancedSettings2.put_PluginDlls
- IMsRdpClientAdvancedSettings3.PluginDlls
- IMsRdpClientAdvancedSettings3.put_PluginDlls
- IMsRdpClientAdvancedSettings4.PluginDlls
- IMsRdpClientAdvancedSettings4.put_PluginDlls
- IMsRdpClientAdvancedSettings5.PluginDlls
- IMsRdpClientAdvancedSettings5.put_PluginDlls
- IMsRdpClientAdvancedSettings6.PluginDlls
- IMsRdpClientAdvancedSettings6.put_PluginDlls
- IMsRdpClientAdvancedSettings7.PluginDlls
- IMsRdpClientAdvancedSettings7.put_PluginDlls
- IMsRdpClientAdvancedSettings8.PluginDlls
- IMsRdpClientAdvancedSettings8.put_PluginDlls
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ef2e518145ae34533477bcbefb92e15d9c8d94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465326"
---
# <a name="imstscadvancedsettingsplugindlls-property"></a><span data-ttu-id="697d3-122">IMsTscAdvancedSettings ::P propriété luginDlls</span><span class="sxs-lookup"><span data-stu-id="697d3-122">IMsTscAdvancedSettings::PluginDlls property</span></span>

<span data-ttu-id="697d3-123">Spécifie les noms des dll clientes du canal virtuel à charger.</span><span class="sxs-lookup"><span data-stu-id="697d3-123">Specifies the names of virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="697d3-124">Les dll du client de canal virtuel sont également appelées « dll de plug-in ».</span><span class="sxs-lookup"><span data-stu-id="697d3-124">Virtual channel client DLLs are also referred to as Plug-in DLLs.</span></span>

<span data-ttu-id="697d3-125">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="697d3-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="697d3-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="697d3-126">Syntax</span></span>


```C++
HRESULT put_PluginDlls(
  [in] BSTR PluginDlls
);
```



## <a name="property-value"></a><span data-ttu-id="697d3-127">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="697d3-127">Property value</span></span>

<span data-ttu-id="697d3-128">Liste séparée par des virgules des noms des dll clientes du canal virtuel à charger.</span><span class="sxs-lookup"><span data-stu-id="697d3-128">Comma-separated list of the names of the virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="697d3-129">Les noms de DLL doivent contenir uniquement des caractères alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="697d3-129">The DLL names must contain only alphanumeric characters.</span></span> <span data-ttu-id="697d3-130">Pour plus d’informations sur le format de ces noms, consultez [inscription du plug-in DVC](dvc-plug-in-registration.md).</span><span class="sxs-lookup"><span data-stu-id="697d3-130">For more information about the format of these names, see [DVC plug-in registration](dvc-plug-in-registration.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="697d3-131">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="697d3-131">Error codes</span></span>

<span data-ttu-id="697d3-132">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="697d3-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="697d3-133">Notes</span><span class="sxs-lookup"><span data-stu-id="697d3-133">Remarks</span></span>

<span data-ttu-id="697d3-134">Pour des raisons de sécurité, si le contrôle est hébergé dans une page Web, la propriété **PluginDlls** accepte uniquement une liste nommée de dll clientes de canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="697d3-134">For security reasons, if the control is hosted in a webpage the **PluginDlls** property only accepts a named list of virtual channel client DLLs.</span></span> <span data-ttu-id="697d3-135">Le contrôle retourne une erreur si un système de fichiers ou un chemin d’accès UNC est spécifié.</span><span class="sxs-lookup"><span data-stu-id="697d3-135">The control returns an error if a file system or UNC path is specified.</span></span>

<span data-ttu-id="697d3-136">Les dll du client de canal virtuel qui seront accessibles à partir d’une page Web doivent être installées dans le répertoire « % WinDir% \\ system32 », car le contrôle ActiveX Bureau à distance accède uniquement aux fichiers dll situés à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="697d3-136">Virtual channel client DLLs that will be accessed from a webpage must be installed in the "%WinDir%\\system32" directory because the Remote Desktop ActiveX control only accesses DLL files in that location.</span></span> <span data-ttu-id="697d3-137">Si le contrôle n’est pas hébergé dans une page Web, cette restriction de sécurité n’existe pas et des chemins d’accès complets peuvent être utilisés pour accéder et charger des dll clientes de canal virtuel situées n’importe où sur le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="697d3-137">If the control is not hosted in a webpage, this security restriction does not exist and full paths may be used to access and load virtual channel client DLLs located anywhere on the file system.</span></span>

<span data-ttu-id="697d3-138">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="697d3-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="697d3-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="697d3-139">Requirements</span></span>



| <span data-ttu-id="697d3-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="697d3-140">Requirement</span></span> | <span data-ttu-id="697d3-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="697d3-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="697d3-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="697d3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="697d3-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="697d3-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="697d3-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="697d3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="697d3-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="697d3-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="697d3-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="697d3-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="697d3-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="697d3-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="697d3-148">DLL</span><span class="sxs-lookup"><span data-stu-id="697d3-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="697d3-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="697d3-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="697d3-150">IID</span><span class="sxs-lookup"><span data-stu-id="697d3-150">IID</span></span><br/>                      | <span data-ttu-id="697d3-151">IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="697d3-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="697d3-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="697d3-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="697d3-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="697d3-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="697d3-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="697d3-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="697d3-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="697d3-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="697d3-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="697d3-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="697d3-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="697d3-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="697d3-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="697d3-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="697d3-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="697d3-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="697d3-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="697d3-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="697d3-161">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="697d3-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





