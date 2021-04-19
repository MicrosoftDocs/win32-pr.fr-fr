---
title: IMsRdpClient6 propriété TransportSettings2
description: Récupère l’interface IMsRdpClientTransportSettings2.
ms.assetid: 5cd3c745-b360-43fb-b780-c526ed539db0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TransportSettings2
- Services Bureau à distance de la propriété TransportSettings2, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété TransportSettings2
- Services Bureau à distance de la propriété TransportSettings2, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété TransportSettings2
- Services Bureau à distance de la propriété TransportSettings2, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété TransportSettings2
- Services Bureau à distance de la propriété TransportSettings2, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété TransportSettings2
- Services Bureau à distance de la propriété TransportSettings2, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété TransportSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient6.TransportSettings2
- IMsRdpClient6.get_TransportSettings2
- IMsRdpClient7.TransportSettings2
- IMsRdpClient7.get_TransportSettings2
- IMsRdpClient8.TransportSettings2
- IMsRdpClient8.get_TransportSettings2
- IMsRdpClient9.TransportSettings2
- IMsRdpClient9.get_TransportSettings2
- IMsRdpClient10.TransportSettings2
- IMsRdpClient10.get_TransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ba11975e0e065e0cfcce91eb22402153acf236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509906"
---
# <a name="imsrdpclient6transportsettings2-property"></a><span data-ttu-id="f9394-114">IMsRdpClient6 :: TransportSettings2, propriété</span><span class="sxs-lookup"><span data-stu-id="f9394-114">IMsRdpClient6::TransportSettings2 property</span></span>

<span data-ttu-id="f9394-115">Récupère l’interface [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="f9394-115">Retrieves the [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface.</span></span>

<span data-ttu-id="f9394-116">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f9394-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9394-117">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9394-117">Syntax</span></span>


```C++
HRESULT get_TransportSettings2(
  [out] IMsRdpClientTransportSettings2 **ppXportSet2
);
```



## <a name="property-value"></a><span data-ttu-id="f9394-118">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f9394-118">Property value</span></span>

<span data-ttu-id="f9394-119">Pointeur d’interface [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="f9394-119">An [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9394-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9394-120">Requirements</span></span>



| <span data-ttu-id="f9394-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9394-121">Requirement</span></span> | <span data-ttu-id="f9394-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9394-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9394-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9394-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f9394-124">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="f9394-124">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="f9394-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9394-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f9394-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9394-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f9394-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f9394-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9394-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9394-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9394-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f9394-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9394-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9394-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9394-131">IID</span><span class="sxs-lookup"><span data-stu-id="f9394-131">IID</span></span><br/>                      | <span data-ttu-id="f9394-132">IID \_ IMsRdpClient6 est défini en tant que d43b7d80-8517-4B6D-9eac-96ad6800d7f2</span><span class="sxs-lookup"><span data-stu-id="f9394-132">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f9394-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9394-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9394-134">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f9394-134">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f9394-135">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f9394-135">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f9394-136">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f9394-136">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f9394-137">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f9394-137">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f9394-138">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="f9394-138">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





