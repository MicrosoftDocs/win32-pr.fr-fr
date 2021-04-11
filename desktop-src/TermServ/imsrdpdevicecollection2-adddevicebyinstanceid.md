---
title: Méthode IMsRdpDeviceCollection2 AddDeviceByInstanceId
description: Ajoute un appareil non répertorié au regroupement de périphériques.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddDeviceByInstanceId
- Méthode AddDeviceByInstanceId Services Bureau à distance, interface IMsRdpDeviceCollection2
- Services Bureau à distance de l’interface IMsRdpDeviceCollection2, méthode AddDeviceByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032376"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a><span data-ttu-id="3a32f-106">IMsRdpDeviceCollection2 :: AddDeviceByInstanceId, méthode</span><span class="sxs-lookup"><span data-stu-id="3a32f-106">IMsRdpDeviceCollection2::AddDeviceByInstanceId method</span></span>

<span data-ttu-id="3a32f-107">Ajoute un appareil non répertorié au regroupement de périphériques.</span><span class="sxs-lookup"><span data-stu-id="3a32f-107">Adds an unlisted device to the device collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a32f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a32f-108">Syntax</span></span>


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a><span data-ttu-id="3a32f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a32f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a32f-110">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a32f-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a32f-111">Type : **[ **RedirectDeviceType**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="3a32f-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="3a32f-112">Valeur de l’énumération [**RedirectDeviceType**](redirectdevicetype.md) qui spécifie le type d’appareil ajouté.</span><span class="sxs-lookup"><span data-stu-id="3a32f-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device being added.</span></span>

</dd> <dt>

<span data-ttu-id="3a32f-113">*InstanceID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a32f-113">*InstanceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a32f-114">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3a32f-114">Type: **BSTR**</span></span>

<span data-ttu-id="3a32f-115">Identificateur d’instance de l’appareil à ajouter.</span><span class="sxs-lookup"><span data-stu-id="3a32f-115">The instance identifier of the device to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a32f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a32f-116">Return value</span></span>

<span data-ttu-id="3a32f-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3a32f-117">Type: **HRESULT**</span></span>

<span data-ttu-id="3a32f-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3a32f-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a32f-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a32f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a32f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a32f-120">Requirements</span></span>



| <span data-ttu-id="3a32f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a32f-121">Requirement</span></span> | <span data-ttu-id="3a32f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a32f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a32f-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a32f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3a32f-124">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3a32f-124">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="3a32f-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a32f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3a32f-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3a32f-126">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="3a32f-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3a32f-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a32f-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a32f-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3a32f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3a32f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a32f-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a32f-130"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a32f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a32f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a32f-132">**RedirectDeviceType**</span><span class="sxs-lookup"><span data-stu-id="3a32f-132">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="3a32f-133">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="3a32f-133">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





