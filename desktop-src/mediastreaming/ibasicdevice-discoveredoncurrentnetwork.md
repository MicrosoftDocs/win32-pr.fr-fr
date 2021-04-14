---
title: Méthode IBasicDevice DiscoveredOnCurrentNetwork
description: Récupère une valeur qui indique si l’appareil se trouve sur le réseau actuel.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- API de diffusion multimédia en continu de méthode DiscoveredOnCurrentNetwork
- API de diffusion multimédia en continu de méthode DiscoveredOnCurrentNetwork, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode DiscoveredOnCurrentNetwork
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e79a012413b3b3d78a9c4617f01ca6cc01cf7e1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380680"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a><span data-ttu-id="56ed9-106">IBasicDevice ::D méthode iscoveredOnCurrentNetwork</span><span class="sxs-lookup"><span data-stu-id="56ed9-106">IBasicDevice::DiscoveredOnCurrentNetwork method</span></span>

<span data-ttu-id="56ed9-107">Récupère une valeur qui indique si l’appareil se trouve sur le réseau actuel.</span><span class="sxs-lookup"><span data-stu-id="56ed9-107">Retrieves a value that indicates if the device is on the current network.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ed9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56ed9-108">Syntax</span></span>


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="56ed9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56ed9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56ed9-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="56ed9-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56ed9-111">Reçoit un pointeur vers une valeur booléenne qui est **true** si l’appareil se trouve sur le réseau actuel.</span><span class="sxs-lookup"><span data-stu-id="56ed9-111">Receives a pointer to a boolean value that is **True** if the device is on the current network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56ed9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56ed9-112">Return value</span></span>

<span data-ttu-id="56ed9-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="56ed9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="56ed9-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="56ed9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="56ed9-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="56ed9-115">Return code</span></span>                                                                          | <span data-ttu-id="56ed9-116">Description</span><span class="sxs-lookup"><span data-stu-id="56ed9-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="56ed9-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="56ed9-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="56ed9-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="56ed9-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="56ed9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56ed9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ed9-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="56ed9-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





