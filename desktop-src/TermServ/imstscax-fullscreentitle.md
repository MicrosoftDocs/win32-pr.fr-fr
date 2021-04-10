---
title: IMsTscAx propriété FullScreenTitle
description: Spécifie le titre de la fenêtre qui s’affiche lorsque le contrôle est en mode plein écran.
ms.assetid: 441aea43-2d1c-44b7-a74f-e375e711fb4f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété FullScreenTitle
topic_type:
- apiref
api_name:
- IMsTscAx.FullScreenTitle
- IMsTscAx.put_FullScreenTitle
- IMsRdpClient.FullScreenTitle
- IMsRdpClient.put_FullScreenTitle
- IMsRdpClient2.FullScreenTitle
- IMsRdpClient2.put_FullScreenTitle
- IMsRdpClient3.FullScreenTitle
- IMsRdpClient3.put_FullScreenTitle
- IMsRdpClient4.FullScreenTitle
- IMsRdpClient4.put_FullScreenTitle
- IMsRdpClient5.FullScreenTitle
- IMsRdpClient5.put_FullScreenTitle
- IMsRdpClient6.FullScreenTitle
- IMsRdpClient6.put_FullScreenTitle
- IMsRdpClient7.FullScreenTitle
- IMsRdpClient7.put_FullScreenTitle
- IMsRdpClient8.FullScreenTitle
- IMsRdpClient8.put_FullScreenTitle
- IMsRdpClient9.FullScreenTitle
- IMsRdpClient9.put_FullScreenTitle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1384d1582f4f0089df55030c22471438575bd072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104326"
---
# <a name="imstscaxfullscreentitle-property"></a><span data-ttu-id="f6a50-124">IMsTscAx :: FullScreenTitle, propriété</span><span class="sxs-lookup"><span data-stu-id="f6a50-124">IMsTscAx::FullScreenTitle property</span></span>

<span data-ttu-id="f6a50-125">Spécifie le titre de la fenêtre qui s’affiche lorsque le contrôle est en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="f6a50-125">Specifies the window title displayed when the control is in full-screen mode.</span></span>

<span data-ttu-id="f6a50-126">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="f6a50-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6a50-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6a50-127">Syntax</span></span>


```C++
HRESULT put_FullScreenTitle(
  [in] BSTR fullScreenTitle
);
```



## <a name="property-value"></a><span data-ttu-id="f6a50-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f6a50-128">Property value</span></span>

<span data-ttu-id="f6a50-129">Titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f6a50-129">The window title.</span></span> <span data-ttu-id="f6a50-130">La longueur maximale de cette chaîne est le \_ chemin d’accès maximal-1 caractères.</span><span class="sxs-lookup"><span data-stu-id="f6a50-130">The maximum length of this string is MAX\_PATH-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f6a50-131">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f6a50-131">Error codes</span></span>

<span data-ttu-id="f6a50-132">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="f6a50-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6a50-133">Notes</span><span class="sxs-lookup"><span data-stu-id="f6a50-133">Remarks</span></span>

<span data-ttu-id="f6a50-134">Cette propriété est utilisée pour définir le titre de la fenêtre du contrôle lorsque la connexion est ouverte en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="f6a50-134">This property is used to set the title of the control's window when the connection is opened in full-screen mode.</span></span> <span data-ttu-id="f6a50-135">N’utilisez pas cette propriété pour le mode plein écran géré par le conteneur.</span><span class="sxs-lookup"><span data-stu-id="f6a50-135">Do not use this property for container-handled full-screen mode.</span></span> <span data-ttu-id="f6a50-136">Lorsque la méthode [**IMsTscAdvancedSettings ::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) est appelée, la fenêtre de conteneur affiche le titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f6a50-136">When the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called, the container window displays the window title.</span></span>

<span data-ttu-id="f6a50-137">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f6a50-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6a50-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6a50-138">Requirements</span></span>



| <span data-ttu-id="f6a50-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6a50-139">Requirement</span></span> | <span data-ttu-id="f6a50-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6a50-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a50-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6a50-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f6a50-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6a50-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f6a50-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6a50-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f6a50-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6a50-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f6a50-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f6a50-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="f6a50-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6a50-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6a50-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f6a50-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6a50-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6a50-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6a50-149">IID</span><span class="sxs-lookup"><span data-stu-id="f6a50-149">IID</span></span><br/>                      | <span data-ttu-id="f6a50-150">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="f6a50-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f6a50-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6a50-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6a50-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="f6a50-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="f6a50-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="f6a50-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="f6a50-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="f6a50-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="f6a50-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="f6a50-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="f6a50-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="f6a50-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="f6a50-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f6a50-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f6a50-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f6a50-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f6a50-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f6a50-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f6a50-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f6a50-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f6a50-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="f6a50-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





