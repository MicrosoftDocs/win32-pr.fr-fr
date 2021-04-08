---
title: IMsRdpClient5 propriété AdvancedSettings6
description: Récupère l’interface IMsRdpClientAdvancedSettings5.
ms.assetid: b6a4efcf-87c3-438c-b6de-8a497ee5939d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AdvancedSettings6
- Services Bureau à distance de la propriété AdvancedSettings6, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété AdvancedSettings6
- Services Bureau à distance de la propriété AdvancedSettings6, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété AdvancedSettings6
- Services Bureau à distance de la propriété AdvancedSettings6, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété AdvancedSettings6
- Services Bureau à distance de la propriété AdvancedSettings6, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété AdvancedSettings6
- Services Bureau à distance de la propriété AdvancedSettings6, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété AdvancedSettings6
- Services Bureau à distance de la propriété AdvancedSettings6, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété AdvancedSettings6
topic_type:
- apiref
api_name:
- IMsRdpClient5.AdvancedSettings6
- IMsRdpClient5.get_AdvancedSettings6
- IMsRdpClient6.AdvancedSettings6
- IMsRdpClient6.get_AdvancedSettings6
- IMsRdpClient7.AdvancedSettings6
- IMsRdpClient7.get_AdvancedSettings6
- IMsRdpClient8.AdvancedSettings6
- IMsRdpClient8.get_AdvancedSettings6
- IMsRdpClient9.AdvancedSettings6
- IMsRdpClient9.get_AdvancedSettings6
- IMsRdpClient10.AdvancedSettings6
- IMsRdpClient10.get_AdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b93d2395ec7e673e50023867f4602eea5c2d9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844310"
---
# <a name="imsrdpclient5advancedsettings6-property"></a><span data-ttu-id="201c7-116">IMsRdpClient5 :: AdvancedSettings6, propriété</span><span class="sxs-lookup"><span data-stu-id="201c7-116">IMsRdpClient5::AdvancedSettings6 property</span></span>

<span data-ttu-id="201c7-117">Récupère l’interface [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="201c7-117">Retrieves the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="201c7-118">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="201c7-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="201c7-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="201c7-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings6(
  [out] IMsRdpClientAdvancedSettings5 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="201c7-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="201c7-120">Property value</span></span>

<span data-ttu-id="201c7-121">Pointeur d’interface [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="201c7-121">An [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="201c7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="201c7-122">Requirements</span></span>



| <span data-ttu-id="201c7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="201c7-123">Requirement</span></span> | <span data-ttu-id="201c7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="201c7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="201c7-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="201c7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="201c7-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="201c7-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="201c7-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="201c7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="201c7-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="201c7-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="201c7-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="201c7-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="201c7-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="201c7-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="201c7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="201c7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="201c7-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="201c7-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="201c7-133">IID</span><span class="sxs-lookup"><span data-stu-id="201c7-133">IID</span></span><br/>                      | <span data-ttu-id="201c7-134">IID \_ IMsRdpClient5 est défini en tant que 4eb5335b-6429-477D-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="201c7-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="201c7-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="201c7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="201c7-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="201c7-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="201c7-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="201c7-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="201c7-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="201c7-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="201c7-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="201c7-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="201c7-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="201c7-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="201c7-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="201c7-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





