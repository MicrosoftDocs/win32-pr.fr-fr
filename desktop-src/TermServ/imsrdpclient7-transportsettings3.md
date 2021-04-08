---
title: IMsRdpClient7 propriété TransportSettings3
description: Récupère un objet qui prend en charge l’interface IMsRdpClientTransportSettings3.
ms.assetid: d11f0943-241e-44cd-a98c-595916ab0718
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TransportSettings3
- Services Bureau à distance de la propriété TransportSettings3, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété TransportSettings3
- Services Bureau à distance de la propriété TransportSettings3, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété TransportSettings3
- Services Bureau à distance de la propriété TransportSettings3, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété TransportSettings3
- Services Bureau à distance de la propriété TransportSettings3, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété TransportSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.TransportSettings3
- IMsRdpClient7.get_TransportSettings3
- IMsRdpClient8.TransportSettings3
- IMsRdpClient8.get_TransportSettings3
- IMsRdpClient9.TransportSettings3
- IMsRdpClient9.get_TransportSettings3
- IMsRdpClient10.TransportSettings3
- IMsRdpClient10.get_TransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c60b58f8f2438de0d43f69ce0b3bb73607e7551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740564"
---
# <a name="imsrdpclient7transportsettings3-property"></a><span data-ttu-id="a5296-112">IMsRdpClient7 :: TransportSettings3, propriété</span><span class="sxs-lookup"><span data-stu-id="a5296-112">IMsRdpClient7::TransportSettings3 property</span></span>

<span data-ttu-id="a5296-113">Récupère un objet qui prend en charge l’interface [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="a5296-113">Retrieves an object that supports the [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface.</span></span>

<span data-ttu-id="a5296-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a5296-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5296-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5296-115">Syntax</span></span>


```C++
HRESULT get_TransportSettings3(
  [out, retval] IMsRdpClientTransportSettings3 **ppXportSet3
);
```



## <a name="property-value"></a><span data-ttu-id="a5296-116">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a5296-116">Property value</span></span>

<span data-ttu-id="a5296-117">Adresse d’un pointeur d’interface [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) qui reçoit l’objet.</span><span class="sxs-lookup"><span data-stu-id="a5296-117">The address of an [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5296-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5296-118">Requirements</span></span>



| <span data-ttu-id="a5296-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5296-119">Requirement</span></span> | <span data-ttu-id="a5296-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5296-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5296-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5296-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5296-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a5296-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="a5296-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5296-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5296-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a5296-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="a5296-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a5296-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="a5296-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5296-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a5296-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a5296-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5296-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5296-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a5296-129">IID</span><span class="sxs-lookup"><span data-stu-id="a5296-129">IID</span></span><br/>                      | <span data-ttu-id="a5296-130">IID \_ IMsRdpClient7 est défini en tant que b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="a5296-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a5296-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5296-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5296-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a5296-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a5296-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a5296-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a5296-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a5296-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a5296-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="a5296-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





