---
title: IMsRdpClient5 propriété TransportSettings
description: Récupère ce qui a été passé via un script à l’interface IMsRdpClientTransportSettings.
ms.assetid: 38f5a735-55c7-425a-835b-22f6e0900d57
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TransportSettings
- Services Bureau à distance de la propriété TransportSettings, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété TransportSettings
- Services Bureau à distance de la propriété TransportSettings, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété TransportSettings
- Services Bureau à distance de la propriété TransportSettings, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété TransportSettings
- Services Bureau à distance de la propriété TransportSettings, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété TransportSettings
- Services Bureau à distance de la propriété TransportSettings, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété TransportSettings
- Services Bureau à distance de la propriété TransportSettings, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété TransportSettings
topic_type:
- apiref
api_name:
- IMsRdpClient5.TransportSettings
- IMsRdpClient5.get_TransportSettings
- IMsRdpClient6.TransportSettings
- IMsRdpClient6.get_TransportSettings
- IMsRdpClient7.TransportSettings
- IMsRdpClient7.get_TransportSettings
- IMsRdpClient8.TransportSettings
- IMsRdpClient8.get_TransportSettings
- IMsRdpClient9.TransportSettings
- IMsRdpClient9.get_TransportSettings
- IMsRdpClient10.TransportSettings
- IMsRdpClient10.get_TransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077ed94253c0ebadeed775e54c4db2ae6cbacf13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103164"
---
# <a name="imsrdpclient5transportsettings-property"></a><span data-ttu-id="9d550-116">IMsRdpClient5 :: TransportSettings, propriété</span><span class="sxs-lookup"><span data-stu-id="9d550-116">IMsRdpClient5::TransportSettings property</span></span>

<span data-ttu-id="9d550-117">Récupère ce qui a été passé via un script à l’interface [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="9d550-117">Retrieves what was passed through a script to the [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface.</span></span>

<span data-ttu-id="9d550-118">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9d550-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d550-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d550-119">Syntax</span></span>


```C++
HRESULT get_TransportSettings(
  [out] IMsRdpClientTransportSettings **ppXportSet
);
```



## <a name="property-value"></a><span data-ttu-id="9d550-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9d550-120">Property value</span></span>

<span data-ttu-id="9d550-121">Pointeur d’interface [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="9d550-121">An [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d550-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d550-122">Requirements</span></span>



| <span data-ttu-id="9d550-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d550-123">Requirement</span></span> | <span data-ttu-id="9d550-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d550-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d550-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d550-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9d550-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d550-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9d550-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d550-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9d550-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d550-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9d550-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9d550-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="9d550-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d550-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d550-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9d550-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d550-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d550-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d550-133">IID</span><span class="sxs-lookup"><span data-stu-id="9d550-133">IID</span></span><br/>                      | <span data-ttu-id="9d550-134">IID \_ IMsRdpClient5 est défini en tant que 4eb5335b-6429-477D-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="9d550-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9d550-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d550-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d550-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="9d550-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="9d550-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="9d550-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="9d550-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9d550-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9d550-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9d550-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9d550-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9d550-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9d550-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="9d550-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





