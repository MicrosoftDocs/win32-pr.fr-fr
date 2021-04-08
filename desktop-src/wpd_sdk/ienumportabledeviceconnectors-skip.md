---
description: Ignore le nombre spécifié d’appareils dans la séquence d’énumération.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'IEnumPortableDeviceConnectors :: Skip, méthode (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: c00daecccd12beee8e9e741c2906e47484fa6da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034870"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a><span data-ttu-id="f9f28-103">IEnumPortableDeviceConnectors :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="f9f28-103">IEnumPortableDeviceConnectors::Skip method</span></span>

<span data-ttu-id="f9f28-104">La méthode **Skip** ignore le nombre spécifié d’appareils dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="f9f28-104">The **Skip** method skips the specified number of devices in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9f28-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9f28-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a><span data-ttu-id="f9f28-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9f28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9f28-107">*cConnectors* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9f28-107">*cConnectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9f28-108">Nombre d’appareils à ignorer.</span><span class="sxs-lookup"><span data-stu-id="f9f28-108">The number of devices to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9f28-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9f28-109">Return value</span></span>

<span data-ttu-id="f9f28-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f9f28-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f9f28-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f9f28-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f9f28-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f9f28-112">Return code</span></span>                                                                             | <span data-ttu-id="f9f28-113">Description</span><span class="sxs-lookup"><span data-stu-id="f9f28-113">Description</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9f28-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f28-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="f9f28-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9f28-115">The method succeeded.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="f9f28-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f9f28-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="f9f28-117">Impossible d’ignorer le nombre d’appareils spécifié.</span><span class="sxs-lookup"><span data-stu-id="f9f28-117">The specified number of devices could not be skipped.</span></span> <span data-ttu-id="f9f28-118">Cause possible : le paramètre *cConnectors* spécifie plus d’appareils que le nombre réel dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="f9f28-118">One possible cause: The *cConnectors* parameter specifies more devices than actually remain in the enumeration sequence.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f9f28-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9f28-119">Requirements</span></span>



| <span data-ttu-id="f9f28-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9f28-120">Requirement</span></span> | <span data-ttu-id="f9f28-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9f28-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f28-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9f28-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f9f28-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9f28-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="f9f28-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9f28-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f9f28-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9f28-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                   |
| <span data-ttu-id="f9f28-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9f28-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9f28-127"><dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9f28-127"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="f9f28-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="f9f28-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9f28-129"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9f28-129"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="f9f28-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f9f28-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9f28-131"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9f28-131"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="f9f28-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9f28-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f28-133">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="f9f28-133">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




