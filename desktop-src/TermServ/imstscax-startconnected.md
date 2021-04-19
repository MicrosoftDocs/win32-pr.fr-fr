---
title: IMsTscAx propriété StartConnected
description: Indique si le contrôle établira la connexion au serveur de l’hôte de session Bureau à distance Bureau à distance dès le démarrage.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété StartConnected
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bda77a06723a6df63055374a3fc96cb80f7654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510939"
---
# <a name="imstscaxstartconnected-property"></a><span data-ttu-id="07bd4-124">IMsTscAx :: StartConnected, propriété</span><span class="sxs-lookup"><span data-stu-id="07bd4-124">IMsTscAx::StartConnected property</span></span>

<span data-ttu-id="07bd4-125">Indique si le contrôle établira la connexion au serveur de l’hôte de session Bureau à distance Bureau à distance dès le démarrage.</span><span class="sxs-lookup"><span data-stu-id="07bd4-125">Indicates whether the control will establish the Remote Desktop Session Host (RD Session Host) server connection immediately upon startup.</span></span>

<span data-ttu-id="07bd4-126">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="07bd4-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="07bd4-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07bd4-127">Syntax</span></span>


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a><span data-ttu-id="07bd4-128">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="07bd4-128">Property value</span></span>

<span data-ttu-id="07bd4-129">Affectez la valeur **true** à ce paramètre si le contrôle doit se connecter immédiatement au démarrage, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="07bd4-129">Set this parameter to **TRUE** if the control should connect immediately on startup, or **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="07bd4-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="07bd4-130">Error codes</span></span>

<span data-ttu-id="07bd4-131">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="07bd4-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="07bd4-132">Notes</span><span class="sxs-lookup"><span data-stu-id="07bd4-132">Remarks</span></span>

<span data-ttu-id="07bd4-133">Cette propriété est particulièrement utile lorsque les propriétés de contrôle sont définies dans la liste de paramètres d’une <OBJECT> balise, plutôt qu’à l’aide d’appels de script.</span><span class="sxs-lookup"><span data-stu-id="07bd4-133">This property is most useful when the control properties are set in the parameter list of an <OBJECT> tag, rather than through script calls.</span></span>

<span data-ttu-id="07bd4-134">Cette propriété ne peut être utilisée que si le nom du serveur est également spécifié à l’aide de la propriété de serveur.</span><span class="sxs-lookup"><span data-stu-id="07bd4-134">This property can be used only if the server name is also specified using the server property.</span></span> <span data-ttu-id="07bd4-135">Ce paramètre doit être défini avant le démarrage du contrôle, par exemple, en l’incluant dans la liste des paramètres d’une <OBJECT> balise lors de l’utilisation du contrôle à partir d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="07bd4-135">This parameter has to be set before the control starts up for example, by including it in the parameter list of an <OBJECT> tag when using the control from a webpage.</span></span>

<span data-ttu-id="07bd4-136">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="07bd4-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07bd4-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07bd4-137">Requirements</span></span>



| <span data-ttu-id="07bd4-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07bd4-138">Requirement</span></span> | <span data-ttu-id="07bd4-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="07bd4-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07bd4-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07bd4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="07bd4-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07bd4-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="07bd4-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07bd4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="07bd4-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07bd4-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="07bd4-144">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="07bd4-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="07bd4-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07bd4-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="07bd4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="07bd4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07bd4-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07bd4-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="07bd4-148">IID</span><span class="sxs-lookup"><span data-stu-id="07bd4-148">IID</span></span><br/>                      | <span data-ttu-id="07bd4-149">IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="07bd4-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="07bd4-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07bd4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07bd4-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="07bd4-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="07bd4-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="07bd4-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="07bd4-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="07bd4-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="07bd4-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="07bd4-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="07bd4-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="07bd4-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="07bd4-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="07bd4-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="07bd4-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="07bd4-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="07bd4-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="07bd4-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="07bd4-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="07bd4-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="07bd4-160">Incorporation du contrôle Bureau à distance ActiveX dans une page Web</span><span class="sxs-lookup"><span data-stu-id="07bd4-160">Embedding the Remote Desktop ActiveX Control in a Webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[<span data-ttu-id="07bd4-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="07bd4-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





