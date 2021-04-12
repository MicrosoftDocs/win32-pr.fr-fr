---
title: IMsRdpClient7 propriété SecuredSettings3
description: Récupère un objet qui prend en charge l’interface IMsRdpClientSecuredSettings2.
ms.assetid: 500ce7ed-bd86-434c-baf8-f30dd667dca3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SecuredSettings3
- Services Bureau à distance de la propriété SecuredSettings3, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété SecuredSettings3
- Services Bureau à distance de la propriété SecuredSettings3, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété SecuredSettings3
- Services Bureau à distance de la propriété SecuredSettings3, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété SecuredSettings3
- Services Bureau à distance de la propriété SecuredSettings3, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété SecuredSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.SecuredSettings3
- IMsRdpClient7.get_SecuredSettings3
- IMsRdpClient8.SecuredSettings3
- IMsRdpClient8.get_SecuredSettings3
- IMsRdpClient9.SecuredSettings3
- IMsRdpClient9.get_SecuredSettings3
- IMsRdpClient10.SecuredSettings3
- IMsRdpClient10.get_SecuredSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 219e3373a6ecb2f5b963a82800f4415f7de64534
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384191"
---
# <a name="imsrdpclient7securedsettings3-property"></a><span data-ttu-id="14250-112">IMsRdpClient7 :: SecuredSettings3, propriété</span><span class="sxs-lookup"><span data-stu-id="14250-112">IMsRdpClient7::SecuredSettings3 property</span></span>

<span data-ttu-id="14250-113">Récupère un objet qui prend en charge l’interface [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="14250-113">Retrieves an object that supports the [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface.</span></span>

<span data-ttu-id="14250-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="14250-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="14250-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14250-115">Syntax</span></span>


```C++
HRESULT get_SecuredSettings3(
  [out] IMsRdpClientSecuredSettings2 **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="14250-116">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="14250-116">Property value</span></span>

<span data-ttu-id="14250-117">Adresse d’un pointeur d’interface [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) qui reçoit l’objet.</span><span class="sxs-lookup"><span data-stu-id="14250-117">The address of an [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="14250-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14250-118">Requirements</span></span>



| <span data-ttu-id="14250-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14250-119">Requirement</span></span> | <span data-ttu-id="14250-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="14250-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14250-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14250-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14250-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="14250-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="14250-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14250-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14250-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14250-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="14250-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="14250-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="14250-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14250-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="14250-127">DLL</span><span class="sxs-lookup"><span data-stu-id="14250-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14250-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14250-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="14250-129">IID</span><span class="sxs-lookup"><span data-stu-id="14250-129">IID</span></span><br/>                      | <span data-ttu-id="14250-130">IID \_ IMsRdpClient7 est défini en tant que b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="14250-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="14250-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14250-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14250-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="14250-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="14250-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="14250-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="14250-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="14250-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="14250-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="14250-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





