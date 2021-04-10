---
title: IMsRdpClientNonScriptable4 propriété WarnAboutPrinterRedirection
description: Contrôle si la boîte de dialogue de redirection affiche un message sur la redirection de l’imprimante avant de démarrer une session.
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété WarnAboutPrinterRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutPrinterRedirection
- MsRdpClient6.WarnAboutPrinterRedirection
- MsRdpClient7.WarnAboutPrinterRedirection
- MsRdpClient8.WarnAboutPrinterRedirection
- MsRdpClient9.WarnAboutPrinterRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e2fa93995946e741caa76f1ee5b84be79d9c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317298"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a><span data-ttu-id="53f87-116">IMsRdpClientNonScriptable4 :: WarnAboutPrinterRedirection, propriété</span><span class="sxs-lookup"><span data-stu-id="53f87-116">IMsRdpClientNonScriptable4::WarnAboutPrinterRedirection property</span></span>

<span data-ttu-id="53f87-117">Contrôle si la boîte de dialogue de redirection affiche un message sur la redirection de l’imprimante avant de démarrer une session.</span><span class="sxs-lookup"><span data-stu-id="53f87-117">Controls whether the redirection dialog box displays a message about printer redirection before starting a session.</span></span>

<span data-ttu-id="53f87-118">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="53f87-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f87-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53f87-119">Syntax</span></span>


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="53f87-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="53f87-120">Property value</span></span>

<span data-ttu-id="53f87-121">Définit si la boîte de dialogue de redirection affiche un message sur la redirection de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="53f87-121">Sets whether the redirection dialog box displays a message about printer redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="53f87-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="53f87-122">Error codes</span></span>

<span data-ttu-id="53f87-123">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="53f87-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f87-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53f87-124">Requirements</span></span>



| <span data-ttu-id="53f87-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53f87-125">Requirement</span></span> | <span data-ttu-id="53f87-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="53f87-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="53f87-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53f87-127">Minimum supported client</span></span><br/> | <span data-ttu-id="53f87-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53f87-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="53f87-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53f87-129">Minimum supported server</span></span><br/> | <span data-ttu-id="53f87-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53f87-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="53f87-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="53f87-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="53f87-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53f87-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="53f87-133">DLL</span><span class="sxs-lookup"><span data-stu-id="53f87-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53f87-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53f87-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="53f87-135">IID</span><span class="sxs-lookup"><span data-stu-id="53f87-135">IID</span></span><br/>                      | <span data-ttu-id="53f87-136">IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="53f87-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53f87-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53f87-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f87-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="53f87-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="53f87-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="53f87-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





