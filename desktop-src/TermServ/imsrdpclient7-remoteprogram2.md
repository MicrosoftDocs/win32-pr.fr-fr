---
title: IMsRdpClient7 propriété RemoteProgram2
description: Récupère un objet qui prend en charge l’interface ITSRemoteProgram2.
ms.assetid: fabdc933-c941-487f-9e49-c20a39e0c86e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RemoteProgram2
- Services Bureau à distance de la propriété RemoteProgram2, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété RemoteProgram2
- Services Bureau à distance de la propriété RemoteProgram2, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété RemoteProgram2
- Services Bureau à distance de la propriété RemoteProgram2, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété RemoteProgram2
- Services Bureau à distance de la propriété RemoteProgram2, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété RemoteProgram2
topic_type:
- apiref
api_name:
- IMsRdpClient7.RemoteProgram2
- IMsRdpClient7.get_RemoteProgram2
- IMsRdpClient8.RemoteProgram2
- IMsRdpClient8.get_RemoteProgram2
- IMsRdpClient9.RemoteProgram2
- IMsRdpClient9.get_RemoteProgram2
- IMsRdpClient10.RemoteProgram2
- IMsRdpClient10.get_RemoteProgram2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1572aada1384a7edfe88b198826050927ae3cff5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941815"
---
# <a name="imsrdpclient7remoteprogram2-property"></a><span data-ttu-id="9a7cc-112">IMsRdpClient7 :: RemoteProgram2, propriété</span><span class="sxs-lookup"><span data-stu-id="9a7cc-112">IMsRdpClient7::RemoteProgram2 property</span></span>

<span data-ttu-id="9a7cc-113">Récupère un objet qui prend en charge l’interface [**ITSRemoteProgram2**](itsremoteprogram2.md) .</span><span class="sxs-lookup"><span data-stu-id="9a7cc-113">Retrieves an object that supports the [**ITSRemoteProgram2**](itsremoteprogram2.md) interface.</span></span>

<span data-ttu-id="9a7cc-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9a7cc-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7cc-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a7cc-115">Syntax</span></span>


```C++
HRESULT get_RemoteProgram2(
  [out, retval] ITSRemoteProgram2 **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="9a7cc-116">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9a7cc-116">Property value</span></span>

<span data-ttu-id="9a7cc-117">Adresse d’un pointeur d’interface [**ITSRemoteProgram2**](itsremoteprogram2.md) qui reçoit l’objet.</span><span class="sxs-lookup"><span data-stu-id="9a7cc-117">The address of an [**ITSRemoteProgram2**](itsremoteprogram2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7cc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a7cc-118">Requirements</span></span>



| <span data-ttu-id="9a7cc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a7cc-119">Requirement</span></span> | <span data-ttu-id="9a7cc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a7cc-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7cc-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a7cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7cc-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9a7cc-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="9a7cc-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a7cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7cc-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a7cc-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="9a7cc-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9a7cc-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="9a7cc-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a7cc-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9a7cc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9a7cc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a7cc-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a7cc-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9a7cc-129">IID</span><span class="sxs-lookup"><span data-stu-id="9a7cc-129">IID</span></span><br/>                      | <span data-ttu-id="9a7cc-130">IID \_ IMsRdpClient7 est défini en tant que b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="9a7cc-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9a7cc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a7cc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7cc-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9a7cc-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9a7cc-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9a7cc-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9a7cc-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9a7cc-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9a7cc-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="9a7cc-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





