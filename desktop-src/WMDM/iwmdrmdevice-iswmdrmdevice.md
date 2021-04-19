---
title: Méthode IWMDRMDevice IsWMDRMDevice
description: La méthode IsWMDRMDevice détermine si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Méthode IsWMDRMDevice Gestionnaire de périphériques Windows Media
- Méthode IsWMDRMDevice Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode IsWMDRMDevice
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523585"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a><span data-ttu-id="1bf88-106">IWMDRMDevice :: IsWMDRMDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="1bf88-106">IWMDRMDevice::IsWMDRMDevice method</span></span>

<span data-ttu-id="1bf88-107">La méthode **IsWMDRMDevice** détermine si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="1bf88-107">The **IsWMDRMDevice** method determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf88-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bf88-108">Syntax</span></span>


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a><span data-ttu-id="1bf88-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bf88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bf88-110">*pdwVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1bf88-110">*pdwVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bf88-111">Version de Windows Media DRM 10 pour les appareils mobiles, qui a la valeur 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="1bf88-111">Version of Windows Media DRM 10 for Portable Devices, which has value of 0x00010000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bf88-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1bf88-112">Return value</span></span>

<span data-ttu-id="1bf88-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1bf88-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1bf88-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1bf88-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1bf88-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1bf88-115">Return code</span></span>                                                                          | <span data-ttu-id="1bf88-116">Description</span><span class="sxs-lookup"><span data-stu-id="1bf88-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1bf88-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1bf88-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1bf88-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1bf88-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1bf88-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bf88-119">Requirements</span></span>



| <span data-ttu-id="1bf88-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bf88-120">Requirement</span></span> | <span data-ttu-id="1bf88-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bf88-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf88-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1bf88-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1bf88-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1bf88-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="1bf88-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1bf88-124">Library</span></span><br/> | <dl> <span data-ttu-id="1bf88-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bf88-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bf88-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bf88-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf88-127">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="1bf88-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





