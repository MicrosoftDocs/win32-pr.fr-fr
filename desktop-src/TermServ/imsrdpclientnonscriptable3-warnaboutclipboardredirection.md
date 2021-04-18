---
title: IMsRdpClientNonScriptable3 propriété WarnAboutClipboardRedirection
description: Spécifie ou récupère une valeur indiquant si la boîte de dialogue d’avertissement de sécurité doit être affichée pour avertir les utilisateurs de la redirection du presse-papiers.
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété WarnAboutClipboardRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutClipboardRedirection
- MsRdpClient5.WarnAboutClipboardRedirection
- MsRdpClient6.WarnAboutClipboardRedirection
- MsRdpClient7.WarnAboutClipboardRedirection
- MsRdpClient8.WarnAboutClipboardRedirection
- MsRdpClient9.WarnAboutClipboardRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8da6fa2f7fb36a110666c8b14a818264813d816
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508421"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a><span data-ttu-id="aa1b7-120">IMsRdpClientNonScriptable3 :: WarnAboutClipboardRedirection, propriété</span><span class="sxs-lookup"><span data-stu-id="aa1b7-120">IMsRdpClientNonScriptable3::WarnAboutClipboardRedirection property</span></span>

<span data-ttu-id="aa1b7-121">Spécifie ou récupère une valeur indiquant si la boîte de dialogue d’avertissement de sécurité doit être affichée pour avertir les utilisateurs de la redirection du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="aa1b7-121">Specifies or retrieves whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

<span data-ttu-id="aa1b7-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="aa1b7-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa1b7-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa1b7-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutClipboardRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutClipboardRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="aa1b7-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="aa1b7-124">Property value</span></span>

<span data-ttu-id="aa1b7-125">Spécifie si la boîte de dialogue d’avertissement de sécurité doit être affichée pour avertir les utilisateurs de la redirection du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="aa1b7-125">Specifies whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa1b7-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa1b7-126">Requirements</span></span>



| <span data-ttu-id="aa1b7-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa1b7-127">Requirement</span></span> | <span data-ttu-id="aa1b7-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa1b7-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa1b7-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa1b7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="aa1b7-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa1b7-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="aa1b7-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa1b7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="aa1b7-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa1b7-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="aa1b7-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="aa1b7-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa1b7-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa1b7-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="aa1b7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="aa1b7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa1b7-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa1b7-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="aa1b7-137">IID</span><span class="sxs-lookup"><span data-stu-id="aa1b7-137">IID</span></span><br/>                      | <span data-ttu-id="aa1b7-138">IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="aa1b7-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa1b7-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa1b7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa1b7-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="aa1b7-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="aa1b7-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="aa1b7-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="aa1b7-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="aa1b7-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





