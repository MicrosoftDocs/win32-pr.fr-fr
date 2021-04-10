---
title: Méthode IBasicDevice CanWakeDevices
description: Récupère une valeur qui indique si l’appareil peut sortir de veille.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- API de diffusion multimédia en continu de méthode CanWakeDevices
- API de diffusion multimédia en continu de méthode CanWakeDevices, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode CanWakeDevices
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030304"
---
# <a name="ibasicdevicecanwakedevices-method"></a><span data-ttu-id="4ca3a-106">IBasicDevice :: CanWakeDevices, méthode</span><span class="sxs-lookup"><span data-stu-id="4ca3a-106">IBasicDevice::CanWakeDevices method</span></span>

<span data-ttu-id="4ca3a-107">Récupère une valeur qui indique si l’appareil peut sortir de veille.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-107">Retrieves a value that indicates if the device can wake.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca3a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ca3a-108">Syntax</span></span>


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="4ca3a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ca3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ca3a-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4ca3a-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca3a-111">Reçoit un pointeur vers une valeur booléenne qui est **true** si l’appareil peut sortir de veille.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-111">Receives a pointer to a boolean value that is **True** if the device can wake.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ca3a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ca3a-112">Return value</span></span>

<span data-ttu-id="4ca3a-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4ca3a-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4ca3a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4ca3a-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4ca3a-115">Return code</span></span>                                                                          | <span data-ttu-id="4ca3a-116">Description</span><span class="sxs-lookup"><span data-stu-id="4ca3a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4ca3a-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4ca3a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4ca3a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4ca3a-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4ca3a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ca3a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca3a-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="4ca3a-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





