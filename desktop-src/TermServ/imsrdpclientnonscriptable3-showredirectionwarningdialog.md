---
title: IMsRdpClientNonScriptable3 propriété ShowRedirectionWarningDialog
description: Spécifie ou récupère une valeur indiquant si la boîte de dialogue d’avertissement de redirection doit s’afficher.
ms.assetid: 7ed37288-77c3-4551-a553-1ca679e1047a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ShowRedirectionWarningDialog
- Services Bureau à distance de la propriété ShowRedirectionWarningDialog, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété ShowRedirectionWarningDialog
- Services Bureau à distance de la propriété ShowRedirectionWarningDialog, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété ShowRedirectionWarningDialog
- Services Bureau à distance de la propriété ShowRedirectionWarningDialog, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété ShowRedirectionWarningDialog
- Services Bureau à distance de la propriété ShowRedirectionWarningDialog, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété ShowRedirectionWarningDialog
- Services Bureau à distance de la propriété ShowRedirectionWarningDialog, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété ShowRedirectionWarningDialog
- Services Bureau à distance de la propriété ShowRedirectionWarningDialog, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété ShowRedirectionWarningDialog
- Services Bureau à distance de la propriété ShowRedirectionWarningDialog, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété ShowRedirectionWarningDialog
- Services Bureau à distance de la propriété ShowRedirectionWarningDialog, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété ShowRedirectionWarningDialog
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.put_ShowRedirectionWarningDialog
- MsRdpClient5.ShowRedirectionWarningDialog
- MsRdpClient6.ShowRedirectionWarningDialog
- MsRdpClient7.ShowRedirectionWarningDialog
- MsRdpClient8.ShowRedirectionWarningDialog
- MsRdpClient9.ShowRedirectionWarningDialog
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468e1721de3395067ca570c2051f3906df626071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032582"
---
# <a name="imsrdpclientnonscriptable3showredirectionwarningdialog-property"></a><span data-ttu-id="dd61f-120">IMsRdpClientNonScriptable3 :: ShowRedirectionWarningDialog, propriété</span><span class="sxs-lookup"><span data-stu-id="dd61f-120">IMsRdpClientNonScriptable3::ShowRedirectionWarningDialog property</span></span>

<span data-ttu-id="dd61f-121">Spécifie ou récupère une valeur indiquant si la boîte de dialogue d’avertissement de redirection doit s’afficher.</span><span class="sxs-lookup"><span data-stu-id="dd61f-121">Specifies or retrieves whether the redirection warning dialog box should be shown.</span></span>

<span data-ttu-id="dd61f-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="dd61f-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd61f-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd61f-123">Syntax</span></span>


```C++
HRESULT put_ShowRedirectionWarningDialog(
  [in]  VARIANT_BOOL fShowRdrDlg
);

HRESULT get_ShowRedirectionWarningDialog(
  [out] VARIANT_BOOL *pfShowRdrDlg
);
```



## <a name="property-value"></a><span data-ttu-id="dd61f-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="dd61f-124">Property value</span></span>

<span data-ttu-id="dd61f-125">Spécifie si la boîte de dialogue d’avertissement de redirection doit s’afficher.</span><span class="sxs-lookup"><span data-stu-id="dd61f-125">Specifies whether the redirection warning dialog box should be shown.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd61f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd61f-126">Requirements</span></span>



| <span data-ttu-id="dd61f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd61f-127">Requirement</span></span> | <span data-ttu-id="dd61f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd61f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd61f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd61f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd61f-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd61f-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="dd61f-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd61f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd61f-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd61f-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="dd61f-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="dd61f-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd61f-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd61f-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="dd61f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="dd61f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd61f-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd61f-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="dd61f-137">IID</span><span class="sxs-lookup"><span data-stu-id="dd61f-137">IID</span></span><br/>                      | <span data-ttu-id="dd61f-138">IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="dd61f-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd61f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd61f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd61f-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="dd61f-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="dd61f-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="dd61f-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="dd61f-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="dd61f-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





