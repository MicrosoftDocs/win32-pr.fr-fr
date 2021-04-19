---
title: Méthode DeviceController. CachedDevices
description: Récupère une collection de pointeurs d’interface IBasicDevice qui représente la vue mise en cache de tous les appareils DLNA détectables. | Méthode DeviceController. CachedDevices
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- API de diffusion multimédia en continu de méthode CachedDevices
- API de diffusion multimédia en continu de méthode CachedDevices, interface DeviceController
- API de diffusion multimédia en continu de l’interface DeviceController, méthode CachedDevices
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0bb39e03a9788e0c444f682b61d39fc1c65781b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535134"
---
# <a name="devicecontrollercacheddevices-method"></a><span data-ttu-id="fd4e3-107">Méthode DeviceController. CachedDevices</span><span class="sxs-lookup"><span data-stu-id="fd4e3-107">DeviceController.CachedDevices method</span></span>

<span data-ttu-id="fd4e3-108">Récupère une collection de pointeurs d’interface [**IBasicDevice**](ibasicdevice.md) qui représente la vue mise en cache de tous les appareils DLNA détectables.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd4e3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd4e3-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="fd4e3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd4e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd4e3-111">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fd4e3-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd4e3-112">Reçoit une collection énumérable de pointeurs d’interface [**IBasicDevice**](ibasicdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="fd4e3-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd4e3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd4e3-113">Return value</span></span>

<span data-ttu-id="fd4e3-114">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fd4e3-115">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fd4e3-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fd4e3-116">Return code</span></span>                                                                          | <span data-ttu-id="fd4e3-117">Description</span><span class="sxs-lookup"><span data-stu-id="fd4e3-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fd4e3-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fd4e3-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fd4e3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd4e3-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="fd4e3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd4e3-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd4e3-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fd4e3-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span></span>
</dt> </dl>

 

