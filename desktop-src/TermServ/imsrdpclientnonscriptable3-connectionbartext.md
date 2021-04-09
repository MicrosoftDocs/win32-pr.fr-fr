---
title: IMsRdpClientNonScriptable3 propriété ConnectionBarText
description: Définit ou récupère le texte pour mettre à jour la barre de connexion.
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété ConnectionBarText
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ConnectionBarText
- IMsRdpClientNonScriptable3.get_ConnectionBarText
- IMsRdpClientNonScriptable3.put_ConnectionBarText
- IMsRdpClientNonScriptable4.ConnectionBarText
- IMsRdpClientNonScriptable4.get_ConnectionBarText
- IMsRdpClientNonScriptable4.put_ConnectionBarText
- IMsRdpClientNonScriptable5.ConnectionBarText
- IMsRdpClientNonScriptable5.get_ConnectionBarText
- IMsRdpClientNonScriptable5.put_ConnectionBarText
- MsRdpClient5.ConnectionBarText
- MsRdpClient6.ConnectionBarText
- MsRdpClient7.ConnectionBarText
- MsRdpClient8.ConnectionBarText
- MsRdpClient9.ConnectionBarText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76819dd28ffd8b2ee5e2dfb30017e341dd49db5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743293"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a><span data-ttu-id="adfff-120">IMsRdpClientNonScriptable3 :: ConnectionBarText, propriété</span><span class="sxs-lookup"><span data-stu-id="adfff-120">IMsRdpClientNonScriptable3::ConnectionBarText property</span></span>

<span data-ttu-id="adfff-121">Définit ou récupère le texte pour mettre à jour la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="adfff-121">Sets or retrieves the text to update the connection bar.</span></span>

<span data-ttu-id="adfff-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="adfff-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="adfff-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adfff-123">Syntax</span></span>


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a><span data-ttu-id="adfff-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="adfff-124">Property value</span></span>

<span data-ttu-id="adfff-125">Définit la chaîne de texte à afficher dans la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="adfff-125">Sets the text string to display on the connection bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="adfff-126">Notes</span><span class="sxs-lookup"><span data-stu-id="adfff-126">Remarks</span></span>

<span data-ttu-id="adfff-127">Vous devez appeler la méthode **IMsRdpClientNonScriptable3 ::p ut \_ ConnectionBarText** avant d’appeler la méthode [**IMsTscSecuredSettings ::P ut \_ fullscreen**](imstscsecuredsettings-fullscreen.md) ou [**IMsRdpClient ::p ut \_ fullscreen**](imsrdpclient-fullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="adfff-127">You must call the **IMsRdpClientNonScriptable3::put\_ConnectionBarText** method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="adfff-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adfff-128">Requirements</span></span>



| <span data-ttu-id="adfff-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adfff-129">Requirement</span></span> | <span data-ttu-id="adfff-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="adfff-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="adfff-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adfff-131">Minimum supported client</span></span><br/> | <span data-ttu-id="adfff-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="adfff-132">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="adfff-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adfff-133">Minimum supported server</span></span><br/> | <span data-ttu-id="adfff-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adfff-134">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="adfff-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="adfff-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="adfff-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adfff-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="adfff-137">DLL</span><span class="sxs-lookup"><span data-stu-id="adfff-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adfff-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adfff-138"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="adfff-139">IID</span><span class="sxs-lookup"><span data-stu-id="adfff-139">IID</span></span><br/>                      | <span data-ttu-id="adfff-140">IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="adfff-140">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="adfff-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adfff-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adfff-142">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="adfff-142">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="adfff-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="adfff-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="adfff-144">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="adfff-144">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





