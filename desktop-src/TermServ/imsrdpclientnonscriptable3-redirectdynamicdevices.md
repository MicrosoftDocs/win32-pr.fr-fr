---
title: IMsRdpClientNonScriptable3 propriété RedirectDynamicDevices
description: Spécifie ou récupère si les périphériques PnP (Plug-and-Play attachés dynamiquement) qui sont énumérés dans une session sont disponibles pour la redirection.
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété RedirectDynamicDevices
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740397"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a><span data-ttu-id="6d063-120">IMsRdpClientNonScriptable3 :: RedirectDynamicDevices, propriété</span><span class="sxs-lookup"><span data-stu-id="6d063-120">IMsRdpClientNonScriptable3::RedirectDynamicDevices property</span></span>

<span data-ttu-id="6d063-121">Spécifie ou récupère si les périphériques PnP (Plug-and-Play attachés dynamiquement) qui sont énumérés dans une session sont disponibles pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="6d063-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) devices that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="6d063-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6d063-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d063-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d063-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a><span data-ttu-id="6d063-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6d063-124">Property value</span></span>

<span data-ttu-id="6d063-125">Spécifie si les appareils PnP attachés de manière dynamique et qui sont énumérés dans une session sont disponibles pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="6d063-125">Specifies whether dynamically attached PnP devices that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d063-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d063-126">Requirements</span></span>



| <span data-ttu-id="6d063-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d063-127">Requirement</span></span> | <span data-ttu-id="6d063-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d063-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d063-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d063-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6d063-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d063-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="6d063-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d063-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6d063-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d063-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="6d063-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6d063-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d063-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d063-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="6d063-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6d063-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d063-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d063-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="6d063-137">IID</span><span class="sxs-lookup"><span data-stu-id="6d063-137">IID</span></span><br/>                      | <span data-ttu-id="6d063-138">IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="6d063-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d063-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d063-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d063-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="6d063-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="6d063-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="6d063-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="6d063-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="6d063-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





