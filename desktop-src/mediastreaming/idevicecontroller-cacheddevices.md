---
title: Méthode IDeviceController CachedDevices
description: Récupère une collection de pointeurs d’interface IBasicDevice qui représente la vue mise en cache de tous les appareils DLNA détectables. | Méthode IDeviceController CachedDevices
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- API de diffusion multimédia en continu de méthode CachedDevices
- API de diffusion multimédia en continu de méthode CachedDevices, interface IDeviceController
- API de diffusion multimédia en continu de l’interface IDeviceController, méthode CachedDevices
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953768"
---
# <a name="idevicecontrollercacheddevices-method"></a><span data-ttu-id="aa203-107">IDeviceController :: CachedDevices, méthode</span><span class="sxs-lookup"><span data-stu-id="aa203-107">IDeviceController::CachedDevices method</span></span>

<span data-ttu-id="aa203-108">Récupère une collection de pointeurs d’interface [**IBasicDevice**](ibasicdevice.md) qui représente la vue mise en cache de tous les appareils DLNA détectables.</span><span class="sxs-lookup"><span data-stu-id="aa203-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa203-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa203-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="aa203-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa203-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa203-111">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="aa203-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa203-112">Reçoit une collection énumérable de pointeurs d’interface [**IBasicDevice**](ibasicdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="aa203-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa203-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aa203-113">Return value</span></span>

<span data-ttu-id="aa203-114">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="aa203-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="aa203-115">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="aa203-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="aa203-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="aa203-116">Return code</span></span>                                                                          | <span data-ttu-id="aa203-117">Description</span><span class="sxs-lookup"><span data-stu-id="aa203-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="aa203-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aa203-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="aa203-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa203-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="aa203-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa203-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa203-121">**IDeviceController**</span><span class="sxs-lookup"><span data-stu-id="aa203-121">**IDeviceController**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

