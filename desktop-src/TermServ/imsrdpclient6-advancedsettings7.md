---
title: IMsRdpClient6 propriété AdvancedSettings7
description: Récupère l’interface IMsRdpClientAdvancedSettings6.
ms.assetid: 64b05c66-ac6a-4190-9df8-4a88dbc46c3f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AdvancedSettings7
- Services Bureau à distance de la propriété AdvancedSettings7, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété AdvancedSettings7
- Services Bureau à distance de la propriété AdvancedSettings7, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété AdvancedSettings7
- Services Bureau à distance de la propriété AdvancedSettings7, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété AdvancedSettings7
- Services Bureau à distance de la propriété AdvancedSettings7, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété AdvancedSettings7
- Services Bureau à distance de la propriété AdvancedSettings7, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété AdvancedSettings7
- Services Bureau à distance de la propriété AdvancedSettings7, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété AdvancedSettings7
topic_type:
- apiref
api_name:
- IMsRdpClient6.AdvancedSettings7
- IMsRdpClient6.get_AdvancedSettings7
- IMsRdpClient7.AdvancedSettings7
- IMsRdpClient7.get_AdvancedSettings7
- IMsRdpClient8.AdvancedSettings7
- IMsRdpClient8.get_AdvancedSettings7
- IMsRdpClient9.AdvancedSettings7
- IMsRdpClient9.get_AdvancedSettings7
- IMsRdpClient10.AdvancedSettings7
- IMsRdpClient10.get_AdvancedSettings7
- MsRdpClient6.AdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51d364c14be3311272455e040d55f277f3fb136
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384192"
---
# <a name="imsrdpclient6advancedsettings7-property"></a><span data-ttu-id="3ecfa-116">IMsRdpClient6 :: AdvancedSettings7, propriété</span><span class="sxs-lookup"><span data-stu-id="3ecfa-116">IMsRdpClient6::AdvancedSettings7 property</span></span>

<span data-ttu-id="3ecfa-117">Récupère l’interface [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="3ecfa-117">Retrieves the [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="3ecfa-118">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3ecfa-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ecfa-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ecfa-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings7(
  [out] IMsRdpClientAdvancedSettings6 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="3ecfa-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3ecfa-120">Property value</span></span>

<span data-ttu-id="3ecfa-121">Pointeur d’interface [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md) .</span><span class="sxs-lookup"><span data-stu-id="3ecfa-121">An [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ecfa-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ecfa-122">Requirements</span></span>



| <span data-ttu-id="3ecfa-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ecfa-123">Requirement</span></span> | <span data-ttu-id="3ecfa-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ecfa-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ecfa-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ecfa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3ecfa-126">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="3ecfa-126">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="3ecfa-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ecfa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3ecfa-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ecfa-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3ecfa-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3ecfa-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ecfa-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ecfa-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ecfa-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3ecfa-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ecfa-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ecfa-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ecfa-133">IID</span><span class="sxs-lookup"><span data-stu-id="3ecfa-133">IID</span></span><br/>                      | <span data-ttu-id="3ecfa-134">IID \_ IMsRdpClient6 est défini en tant que d43b7d80-8517-4B6D-9eac-96ad6800d7f2</span><span class="sxs-lookup"><span data-stu-id="3ecfa-134">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3ecfa-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ecfa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecfa-136">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="3ecfa-136">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="3ecfa-137">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="3ecfa-137">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="3ecfa-138">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="3ecfa-138">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="3ecfa-139">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="3ecfa-139">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="3ecfa-140">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="3ecfa-140">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





