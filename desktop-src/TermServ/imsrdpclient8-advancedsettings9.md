---
title: IMsRdpClient8 propriété AdvancedSettings9
description: Contient un objet qui prend en charge l’interface IMsRdpClientAdvancedSettings8.
ms.assetid: eb7bf118-15e7-4a11-91b1-e48f18afb436
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AdvancedSettings9
- Services Bureau à distance de la propriété AdvancedSettings9, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété AdvancedSettings9
- Services Bureau à distance de la propriété AdvancedSettings9, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété AdvancedSettings9
- Services Bureau à distance de la propriété AdvancedSettings9, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété AdvancedSettings9
topic_type:
- apiref
api_name:
- IMsRdpClient8.AdvancedSettings9
- IMsRdpClient8.get_AdvancedSettings9
- IMsRdpClient9.AdvancedSettings9
- IMsRdpClient9.get_AdvancedSettings9
- IMsRdpClient10.AdvancedSettings9
- IMsRdpClient10.get_AdvancedSettings9
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fce4c6f07b0c6c798d613e5312b3ae2b258c9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511186"
---
# <a name="imsrdpclient8advancedsettings9-property"></a><span data-ttu-id="ffecf-110">IMsRdpClient8 :: AdvancedSettings9, propriété</span><span class="sxs-lookup"><span data-stu-id="ffecf-110">IMsRdpClient8::AdvancedSettings9 property</span></span>

<span data-ttu-id="ffecf-111">Contient un objet qui prend en charge l’interface [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) .</span><span class="sxs-lookup"><span data-stu-id="ffecf-111">Contains an object that supports the [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface.</span></span>

<span data-ttu-id="ffecf-112">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ffecf-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffecf-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffecf-113">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings9(
  [out, retval] IMsRdpClientAdvancedSettings8 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="ffecf-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ffecf-114">Property value</span></span>

<span data-ttu-id="ffecf-115">Interface [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) qui représente l’objet de paramètres.</span><span class="sxs-lookup"><span data-stu-id="ffecf-115">An [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface that represents the settings object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffecf-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffecf-116">Requirements</span></span>



| <span data-ttu-id="ffecf-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffecf-117">Requirement</span></span> | <span data-ttu-id="ffecf-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffecf-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffecf-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffecf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ffecf-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ffecf-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="ffecf-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffecf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ffecf-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ffecf-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="ffecf-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ffecf-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="ffecf-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffecf-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ffecf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ffecf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffecf-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffecf-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ffecf-127">IID</span><span class="sxs-lookup"><span data-stu-id="ffecf-127">IID</span></span><br/>                      | <span data-ttu-id="ffecf-128">IID \_ IMsRdpClient8 est défini en tant que 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="ffecf-128">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ffecf-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffecf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffecf-130">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ffecf-130">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ffecf-131">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ffecf-131">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ffecf-132">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="ffecf-132">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





