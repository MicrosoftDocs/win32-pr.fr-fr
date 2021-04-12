---
title: IMsRdpClientNonScriptable4 propriété TrustedZoneSite
description: Spécifie si le site Web à partir duquel l’utilisateur a lancé la connexion se trouve dans la liste des sites de confiance de l’ordinateur client de l’utilisateur.
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété TrustedZoneSite
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384892"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a><span data-ttu-id="950c8-116">IMsRdpClientNonScriptable4 :: TrustedZoneSite, propriété</span><span class="sxs-lookup"><span data-stu-id="950c8-116">IMsRdpClientNonScriptable4::TrustedZoneSite property</span></span>

<span data-ttu-id="950c8-117">Spécifie si le site Web à partir duquel l’utilisateur a lancé la connexion se trouve dans la liste des sites de confiance de l’ordinateur client de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="950c8-117">Specifies whether the website from which the user launched the connection is in the trusted sites list of the user's client computer.</span></span>

<span data-ttu-id="950c8-118">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="950c8-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="950c8-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="950c8-119">Syntax</span></span>


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a><span data-ttu-id="950c8-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="950c8-120">Property value</span></span>

<span data-ttu-id="950c8-121">Définit la propriété TrustedZoneSite.</span><span class="sxs-lookup"><span data-stu-id="950c8-121">Sets the TrustedZoneSite property.</span></span> <span data-ttu-id="950c8-122">Cette méthode n’a aucun effet sur le fait que le site Web à partir duquel l’utilisateur a lancé la connexion se trouve dans la liste des sites de confiance de l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="950c8-122">This method has no effect on whether the website from which the user launched the connection is in the trusted sites list of the client computer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="950c8-123">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="950c8-123">Error codes</span></span>

<span data-ttu-id="950c8-124">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="950c8-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="950c8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="950c8-125">Requirements</span></span>



| <span data-ttu-id="950c8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="950c8-126">Requirement</span></span> | <span data-ttu-id="950c8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="950c8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="950c8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="950c8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="950c8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="950c8-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="950c8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="950c8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="950c8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="950c8-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="950c8-132">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="950c8-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="950c8-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="950c8-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="950c8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="950c8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="950c8-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="950c8-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="950c8-136">IID</span><span class="sxs-lookup"><span data-stu-id="950c8-136">IID</span></span><br/>                      | <span data-ttu-id="950c8-137">IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="950c8-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="950c8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="950c8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="950c8-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="950c8-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="950c8-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="950c8-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





