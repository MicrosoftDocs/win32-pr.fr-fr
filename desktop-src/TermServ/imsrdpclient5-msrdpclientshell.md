---
title: IMsRdpClient5 propriété MsRdpClientShell
description: Récupère l’interface de paramètre client scriptable IMsRdpClientShell.
ms.assetid: cc56cec4-779d-4b51-8e94-ae0dd9bae997
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété MsRdpClientShell
- Services Bureau à distance de la propriété MsRdpClientShell, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété MsRdpClientShell
- Services Bureau à distance de la propriété MsRdpClientShell, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété MsRdpClientShell
- Services Bureau à distance de la propriété MsRdpClientShell, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété MsRdpClientShell
- Services Bureau à distance de la propriété MsRdpClientShell, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété MsRdpClientShell
- Services Bureau à distance de la propriété MsRdpClientShell, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété MsRdpClientShell
- Services Bureau à distance de la propriété MsRdpClientShell, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété MsRdpClientShell
topic_type:
- apiref
api_name:
- IMsRdpClient5.MsRdpClientShell
- IMsRdpClient5.get_MsRdpClientShell
- IMsRdpClient6.MsRdpClientShell
- IMsRdpClient6.get_MsRdpClientShell
- IMsRdpClient7.MsRdpClientShell
- IMsRdpClient7.get_MsRdpClientShell
- IMsRdpClient8.MsRdpClientShell
- IMsRdpClient8.get_MsRdpClientShell
- IMsRdpClient9.MsRdpClientShell
- IMsRdpClient9.get_MsRdpClientShell
- IMsRdpClient10.MsRdpClientShell
- IMsRdpClient10.get_MsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46129dc4736b50e8b6a650cc7a59f9b238da56e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106177"
---
# <a name="imsrdpclient5msrdpclientshell-property"></a><span data-ttu-id="75d61-116">IMsRdpClient5 :: MsRdpClientShell, propriété</span><span class="sxs-lookup"><span data-stu-id="75d61-116">IMsRdpClient5::MsRdpClientShell property</span></span>

<span data-ttu-id="75d61-117">Récupère l’interface de paramètre client scriptable [**IMsRdpClientShell**](imsrdpclientshell.md).</span><span class="sxs-lookup"><span data-stu-id="75d61-117">Retrieves the scriptable client setting interface [**IMsRdpClientShell**](imsrdpclientshell.md).</span></span>

<span data-ttu-id="75d61-118">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="75d61-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d61-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75d61-119">Syntax</span></span>


```C++
HRESULT get_MsRdpClientShell(
  [out] IMsRdpClientShell **ppLauncher
);
```



## <a name="property-value"></a><span data-ttu-id="75d61-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="75d61-120">Property value</span></span>

<span data-ttu-id="75d61-121">Pointeur d’interface [**IMsRdpClientShell**](imsrdpclientshell.md) .</span><span class="sxs-lookup"><span data-stu-id="75d61-121">An [**IMsRdpClientShell**](imsrdpclientshell.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="75d61-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75d61-122">Requirements</span></span>



| <span data-ttu-id="75d61-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75d61-123">Requirement</span></span> | <span data-ttu-id="75d61-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="75d61-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75d61-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75d61-125">Minimum supported client</span></span><br/> | <span data-ttu-id="75d61-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75d61-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="75d61-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75d61-127">Minimum supported server</span></span><br/> | <span data-ttu-id="75d61-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75d61-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="75d61-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="75d61-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="75d61-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d61-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="75d61-131">DLL</span><span class="sxs-lookup"><span data-stu-id="75d61-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75d61-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d61-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="75d61-133">IID</span><span class="sxs-lookup"><span data-stu-id="75d61-133">IID</span></span><br/>                      | <span data-ttu-id="75d61-134">IID \_ IMsRdpClient5 est défini en tant que 4eb5335b-6429-477D-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="75d61-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="75d61-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75d61-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d61-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="75d61-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="75d61-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="75d61-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="75d61-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="75d61-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="75d61-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="75d61-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="75d61-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="75d61-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="75d61-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="75d61-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





