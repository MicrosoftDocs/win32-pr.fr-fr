---
title: IMsRdpClientNonScriptable4 propriété LaunchedViaClientShellInterface
description: Spécifie si l’utilisateur a lancé le contrôle client à l’aide de l’interface Bureau à distance Accès web (RD Accès web).
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété LaunchedViaClientShellInterface
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942332"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a><span data-ttu-id="40c77-118">IMsRdpClientNonScriptable4 :: LaunchedViaClientShellInterface, propriété</span><span class="sxs-lookup"><span data-stu-id="40c77-118">IMsRdpClientNonScriptable4::LaunchedViaClientShellInterface property</span></span>

<span data-ttu-id="40c77-119">Spécifie si l’utilisateur a lancé le contrôle client à l’aide de l’interface Bureau à distance Accès web (RD Accès web).</span><span class="sxs-lookup"><span data-stu-id="40c77-119">Specifies whether the user launched the client control by using the Remote Desktop Web Access (RD Web Access) interface.</span></span>

<span data-ttu-id="40c77-120">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="40c77-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="40c77-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40c77-121">Syntax</span></span>


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a><span data-ttu-id="40c77-122">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="40c77-122">Property value</span></span>

<span data-ttu-id="40c77-123">Définit la propriété **LaunchedViaClientShellInterface** .</span><span class="sxs-lookup"><span data-stu-id="40c77-123">Sets the **LaunchedViaClientShellInterface** property.</span></span>

## <a name="error-codes"></a><span data-ttu-id="40c77-124">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="40c77-124">Error codes</span></span>

<span data-ttu-id="40c77-125">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="40c77-125">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="40c77-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40c77-126">Requirements</span></span>



| <span data-ttu-id="40c77-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40c77-127">Requirement</span></span> | <span data-ttu-id="40c77-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="40c77-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="40c77-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40c77-129">Minimum supported client</span></span><br/> | <span data-ttu-id="40c77-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40c77-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="40c77-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40c77-131">Minimum supported server</span></span><br/> | <span data-ttu-id="40c77-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40c77-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="40c77-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="40c77-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="40c77-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40c77-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="40c77-135">DLL</span><span class="sxs-lookup"><span data-stu-id="40c77-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40c77-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40c77-136"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="40c77-137">IID</span><span class="sxs-lookup"><span data-stu-id="40c77-137">IID</span></span><br/>                      | <span data-ttu-id="40c77-138">IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="40c77-138">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40c77-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40c77-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c77-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="40c77-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="40c77-141">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="40c77-141">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





