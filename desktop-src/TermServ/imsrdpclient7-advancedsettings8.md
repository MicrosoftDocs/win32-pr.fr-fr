---
title: IMsRdpClient7 propriété AdvancedSettings8
description: Récupère un objet qui prend en charge l’interface IMsRdpClientAdvancedSettings7.
ms.assetid: e3bb3b74-52db-4ec2-999c-9d12c24f65be
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AdvancedSettings8
- Services Bureau à distance de la propriété AdvancedSettings8, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété AdvancedSettings8
- Services Bureau à distance de la propriété AdvancedSettings8, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété AdvancedSettings8
- Services Bureau à distance de la propriété AdvancedSettings8, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété AdvancedSettings8
- Services Bureau à distance de la propriété AdvancedSettings8, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété AdvancedSettings8
topic_type:
- apiref
api_name:
- IMsRdpClient7.AdvancedSettings8
- IMsRdpClient7.get_AdvancedSettings8
- IMsRdpClient8.AdvancedSettings8
- IMsRdpClient8.get_AdvancedSettings8
- IMsRdpClient9.AdvancedSettings8
- IMsRdpClient9.get_AdvancedSettings8
- IMsRdpClient10.AdvancedSettings8
- IMsRdpClient10.get_AdvancedSettings8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 887306216682ba1555739a4258b8337694fabe0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103089"
---
# <a name="imsrdpclient7advancedsettings8-property"></a><span data-ttu-id="ea834-112">IMsRdpClient7 :: AdvancedSettings8, propriété</span><span class="sxs-lookup"><span data-stu-id="ea834-112">IMsRdpClient7::AdvancedSettings8 property</span></span>

<span data-ttu-id="ea834-113">Récupère un objet qui prend en charge l’interface [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .</span><span class="sxs-lookup"><span data-stu-id="ea834-113">Retrieves an object that supports the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface.</span></span>

<span data-ttu-id="ea834-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ea834-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea834-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea834-115">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings8(
  [out, retval] IMsRdpClientAdvancedSettings7 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="ea834-116">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ea834-116">Property value</span></span>

<span data-ttu-id="ea834-117">Adresse d’un pointeur d’interface [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) qui reçoit l’objet.</span><span class="sxs-lookup"><span data-stu-id="ea834-117">The address of an [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea834-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea834-118">Requirements</span></span>



| <span data-ttu-id="ea834-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea834-119">Requirement</span></span> | <span data-ttu-id="ea834-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea834-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea834-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea834-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea834-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ea834-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="ea834-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea834-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea834-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ea834-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="ea834-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ea834-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea834-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea834-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ea834-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ea834-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea834-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea834-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ea834-129">IID</span><span class="sxs-lookup"><span data-stu-id="ea834-129">IID</span></span><br/>                      | <span data-ttu-id="ea834-130">IID \_ IMsRdpClient7 est défini en tant que b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="ea834-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ea834-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea834-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea834-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ea834-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ea834-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ea834-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ea834-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ea834-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ea834-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="ea834-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





