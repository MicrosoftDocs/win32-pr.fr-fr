---
title: Méthode IMsRdpDeviceCollection2 RedirectNow
description: Force la redirection ou la suppression des appareils qui ont été sélectionnés ou désélectionnés dans la collection.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RedirectNow
- Méthode RedirectNow Services Bureau à distance, interface IMsRdpDeviceCollection2
- Services Bureau à distance de l’interface IMsRdpDeviceCollection2, méthode RedirectNow
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941681"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a><span data-ttu-id="f44a5-106">IMsRdpDeviceCollection2 :: RedirectNow, méthode</span><span class="sxs-lookup"><span data-stu-id="f44a5-106">IMsRdpDeviceCollection2::RedirectNow method</span></span>

<span data-ttu-id="f44a5-107">Force la redirection ou la suppression des appareils qui ont été sélectionnés ou désélectionnés dans la collection.</span><span class="sxs-lookup"><span data-stu-id="f44a5-107">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f44a5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f44a5-108">Syntax</span></span>


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a><span data-ttu-id="f44a5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f44a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f44a5-110">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f44a5-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44a5-111">Type : **[ **RedirectDeviceType**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="f44a5-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="f44a5-112">Valeur de l’énumération [**RedirectDeviceType**](redirectdevicetype.md) qui spécifie le type de périphérique à rediriger.</span><span class="sxs-lookup"><span data-stu-id="f44a5-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device to be redirected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f44a5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f44a5-113">Return value</span></span>

<span data-ttu-id="f44a5-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f44a5-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f44a5-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f44a5-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f44a5-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f44a5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f44a5-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f44a5-117">Requirements</span></span>



| <span data-ttu-id="f44a5-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f44a5-118">Requirement</span></span> | <span data-ttu-id="f44a5-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f44a5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f44a5-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f44a5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f44a5-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f44a5-121">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="f44a5-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f44a5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f44a5-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f44a5-123">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="f44a5-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f44a5-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="f44a5-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f44a5-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f44a5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f44a5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f44a5-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f44a5-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f44a5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f44a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f44a5-129">**RedirectDeviceType**</span><span class="sxs-lookup"><span data-stu-id="f44a5-129">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="f44a5-130">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="f44a5-130">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





