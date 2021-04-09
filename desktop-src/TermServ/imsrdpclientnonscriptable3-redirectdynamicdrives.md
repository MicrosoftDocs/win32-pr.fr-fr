---
title: IMsRdpClientNonScriptable3 propriété RedirectDynamicDrives
description: Spécifie ou récupère si les lecteurs PnP (Plug-and-Play attachés dynamiquement) qui sont énumérés dans une session sont disponibles pour la redirection.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété RedirectDynamicDrives
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19c0e6e20f7f73481f6f2ecbc50ab0eda512ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743645"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a><span data-ttu-id="ed44e-120">IMsRdpClientNonScriptable3 :: RedirectDynamicDrives, propriété</span><span class="sxs-lookup"><span data-stu-id="ed44e-120">IMsRdpClientNonScriptable3::RedirectDynamicDrives property</span></span>

<span data-ttu-id="ed44e-121">Spécifie ou récupère si les lecteurs PnP (Plug-and-Play attachés dynamiquement) qui sont énumérés dans une session sont disponibles pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="ed44e-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) drives that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="ed44e-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ed44e-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed44e-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed44e-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a><span data-ttu-id="ed44e-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ed44e-124">Property value</span></span>

<span data-ttu-id="ed44e-125">Spécifie si les lecteurs PnP attachés de manière dynamique et qui sont énumérés dans une session sont disponibles pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="ed44e-125">Specifies whether dynamically attached PnP drives that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed44e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed44e-126">Requirements</span></span>



| <span data-ttu-id="ed44e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed44e-127">Requirement</span></span> | <span data-ttu-id="ed44e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed44e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed44e-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed44e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ed44e-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed44e-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="ed44e-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed44e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ed44e-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed44e-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="ed44e-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ed44e-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="ed44e-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed44e-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="ed44e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ed44e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed44e-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed44e-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="ed44e-137">IID</span><span class="sxs-lookup"><span data-stu-id="ed44e-137">IID</span></span><br/>                      | <span data-ttu-id="ed44e-138">IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="ed44e-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed44e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed44e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed44e-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="ed44e-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="ed44e-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="ed44e-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="ed44e-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="ed44e-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





