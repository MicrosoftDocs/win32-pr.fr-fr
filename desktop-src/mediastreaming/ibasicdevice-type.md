---
title: Méthode de type IBasicDevice
description: Récupère une valeur d’énumération indiquant le type d’appareil de l’appareil DLNA.
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- Méthode de type Media Streaming API
- Méthode de type Media Streaming API, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode de type
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a69f0671c82363ff61179c0120b3db8f6e755de9
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383228"
---
# <a name="ibasicdevicetype-method"></a><span data-ttu-id="a535e-106">IBasicDevice :: type, méthode</span><span class="sxs-lookup"><span data-stu-id="a535e-106">IBasicDevice::Type method</span></span>

<span data-ttu-id="a535e-107">Récupère une valeur d’énumération indiquant le type d’appareil de l’appareil DLNA.</span><span class="sxs-lookup"><span data-stu-id="a535e-107">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a535e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a535e-108">Syntax</span></span>


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a><span data-ttu-id="a535e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a535e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a535e-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a535e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a535e-111">Reçoit un pointeur vers une valeur [**DeviceTypes**](devicetypes.md) .</span><span class="sxs-lookup"><span data-stu-id="a535e-111">Receives a pointer to a [**DeviceTypes**](devicetypes.md) value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a535e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a535e-112">Return value</span></span>

<span data-ttu-id="a535e-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a535e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a535e-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a535e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a535e-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a535e-115">Return code</span></span>                                                                          | <span data-ttu-id="a535e-116">Description</span><span class="sxs-lookup"><span data-stu-id="a535e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a535e-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a535e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a535e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a535e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a535e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a535e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a535e-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="a535e-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





