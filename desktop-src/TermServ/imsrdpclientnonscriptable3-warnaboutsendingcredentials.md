---
title: IMsRdpClientNonScriptable3 propriété WarnAboutSendingCredentials
description: Spécifie ou récupère une valeur indiquant si la boîte de dialogue d’avertissement de sécurité doit inclure un avertissement concernant l’envoi d’informations d’identification au serveur distant avant le démarrage d’une session.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété WarnAboutSendingCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527566"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a><span data-ttu-id="5647a-120">IMsRdpClientNonScriptable3 :: WarnAboutSendingCredentials, propriété</span><span class="sxs-lookup"><span data-stu-id="5647a-120">IMsRdpClientNonScriptable3::WarnAboutSendingCredentials property</span></span>

<span data-ttu-id="5647a-121">Spécifie ou récupère une valeur indiquant si la boîte de dialogue d’avertissement de sécurité doit inclure un avertissement concernant l’envoi d’informations d’identification au serveur distant avant le démarrage d’une session.</span><span class="sxs-lookup"><span data-stu-id="5647a-121">Specifies or retrieves whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

<span data-ttu-id="5647a-122">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5647a-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5647a-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5647a-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="5647a-124">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5647a-124">Property value</span></span>

<span data-ttu-id="5647a-125">Spécifie si la boîte de dialogue d’avertissement de sécurité doit inclure un avertissement concernant l’envoi d’informations d’identification au serveur distant avant le démarrage d’une session.</span><span class="sxs-lookup"><span data-stu-id="5647a-125">Specifies whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="5647a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5647a-126">Requirements</span></span>



| <span data-ttu-id="5647a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5647a-127">Requirement</span></span> | <span data-ttu-id="5647a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5647a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5647a-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5647a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5647a-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5647a-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5647a-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5647a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5647a-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5647a-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="5647a-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5647a-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="5647a-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5647a-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5647a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5647a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5647a-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5647a-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5647a-137">IID</span><span class="sxs-lookup"><span data-stu-id="5647a-137">IID</span></span><br/>                      | <span data-ttu-id="5647a-138">IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="5647a-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5647a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5647a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5647a-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="5647a-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="5647a-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="5647a-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="5647a-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="5647a-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





