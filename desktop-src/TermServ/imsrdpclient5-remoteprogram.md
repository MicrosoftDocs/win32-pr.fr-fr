---
title: IMsRdpClient5 propriété RemoteProgram
description: Récupère un objet qui prend en charge l’interface ITSRemoteProgram.
ms.assetid: 013f613b-af7b-4cc5-be1f-d45833806e3b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RemoteProgram
- Services Bureau à distance de la propriété RemoteProgram, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété RemoteProgram
- Services Bureau à distance de la propriété RemoteProgram, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété RemoteProgram
- Services Bureau à distance de la propriété RemoteProgram, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété RemoteProgram
- Services Bureau à distance de la propriété RemoteProgram, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété RemoteProgram
- Services Bureau à distance de la propriété RemoteProgram, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété RemoteProgram
- Services Bureau à distance de la propriété RemoteProgram, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété RemoteProgram
topic_type:
- apiref
api_name:
- IMsRdpClient5.RemoteProgram
- IMsRdpClient5.get_RemoteProgram
- IMsRdpClient6.RemoteProgram
- IMsRdpClient6.get_RemoteProgram
- IMsRdpClient7.RemoteProgram
- IMsRdpClient7.get_RemoteProgram
- IMsRdpClient8.RemoteProgram
- IMsRdpClient8.get_RemoteProgram
- IMsRdpClient9.RemoteProgram
- IMsRdpClient9.get_RemoteProgram
- IMsRdpClient10.RemoteProgram
- IMsRdpClient10.get_RemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267e367af090a7fd70e9482406104fd0403d63f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464690"
---
# <a name="imsrdpclient5remoteprogram-property"></a><span data-ttu-id="1113c-116">IMsRdpClient5 :: RemoteProgram, propriété</span><span class="sxs-lookup"><span data-stu-id="1113c-116">IMsRdpClient5::RemoteProgram property</span></span>

<span data-ttu-id="1113c-117">Récupère un objet qui prend en charge l’interface [**ITSRemoteProgram**](itsremoteprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="1113c-117">Retrieves an object that supports the [**ITSRemoteProgram**](itsremoteprogram.md) interface.</span></span>

<span data-ttu-id="1113c-118">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1113c-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1113c-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1113c-119">Syntax</span></span>


```C++
HRESULT get_RemoteProgram(
  [out] ITSRemoteProgram **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="1113c-120">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1113c-120">Property value</span></span>

<span data-ttu-id="1113c-121">Pointeur d’interface [**ITSRemoteProgram**](itsremoteprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="1113c-121">An [**ITSRemoteProgram**](itsremoteprogram.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1113c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1113c-122">Requirements</span></span>



| <span data-ttu-id="1113c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1113c-123">Requirement</span></span> | <span data-ttu-id="1113c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1113c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1113c-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1113c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1113c-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1113c-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1113c-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1113c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1113c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1113c-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1113c-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1113c-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="1113c-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1113c-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1113c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1113c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1113c-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1113c-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1113c-133">IID</span><span class="sxs-lookup"><span data-stu-id="1113c-133">IID</span></span><br/>                      | <span data-ttu-id="1113c-134">IID \_ IMsRdpClient5 est défini en tant que 4eb5335b-6429-477D-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="1113c-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1113c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1113c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1113c-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="1113c-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="1113c-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="1113c-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="1113c-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="1113c-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="1113c-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="1113c-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="1113c-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="1113c-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="1113c-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="1113c-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





