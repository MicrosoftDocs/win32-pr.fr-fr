---
title: IBasicDevice ManufacturerUrl, méthode
description: Récupère l’URL du fabricant de l’appareil.
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- Méthode ManufacturerUrl API de diffusion multimédia en continu
- ManufacturerUrl, méthode, API de diffusion multimédia en continu, interface IBasicDevice
- API streaming de média de l’interface IBasicDevice, méthode ManufacturerUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e41ca83c98507c65ead8d1faf2922ee84b45649
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030176"
---
# <a name="ibasicdevicemanufacturerurl-method"></a><span data-ttu-id="72aa6-106">IBasicDevice :: ManufacturerUrl, méthode</span><span class="sxs-lookup"><span data-stu-id="72aa6-106">IBasicDevice::ManufacturerUrl method</span></span>

<span data-ttu-id="72aa6-107">Récupère l’URL du fabricant de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="72aa6-107">Retrieves the device s manufacturer URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="72aa6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72aa6-108">Syntax</span></span>


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="72aa6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72aa6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72aa6-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="72aa6-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72aa6-111">Reçoit un pointeur vers l’URL du fabricant de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="72aa6-111">Receives a pointer to the device s manufacturer URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72aa6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72aa6-112">Return value</span></span>

<span data-ttu-id="72aa6-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="72aa6-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="72aa6-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="72aa6-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="72aa6-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="72aa6-115">Return code</span></span>                                                                          | <span data-ttu-id="72aa6-116">Description</span><span class="sxs-lookup"><span data-stu-id="72aa6-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="72aa6-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="72aa6-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="72aa6-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="72aa6-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="72aa6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72aa6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72aa6-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="72aa6-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





