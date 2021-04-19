---
title: IBasicDevice ModelName, méthode
description: Récupère le nom du modèle de l’appareil.
ms.assetid: 8F871E89-97C1-4788-83AB-B7E0D8D6E0B5
keywords:
- API de diffusion multimédia en continu de la méthode ModelName
- Méthode ModelName API de diffusion multimédia en continu, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode ModelName
topic_type:
- apiref
api_name:
- IBasicDevice.ModelName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e486b372b2108bc85153f416032ef6bfbe8a397
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510042"
---
# <a name="ibasicdevicemodelname-method"></a><span data-ttu-id="46273-106">IBasicDevice :: ModelName, méthode</span><span class="sxs-lookup"><span data-stu-id="46273-106">IBasicDevice::ModelName method</span></span>

<span data-ttu-id="46273-107">Récupère le nom du modèle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46273-107">Retrieves the device s model name.</span></span>

## <a name="syntax"></a><span data-ttu-id="46273-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46273-108">Syntax</span></span>


```C++
HRESULT ModelName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="46273-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46273-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46273-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="46273-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46273-111">Reçoit un pointeur vers le nom du modèle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46273-111">Receives a pointer to the device s model name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46273-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46273-112">Return value</span></span>

<span data-ttu-id="46273-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="46273-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="46273-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="46273-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="46273-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="46273-115">Return code</span></span>                                                                          | <span data-ttu-id="46273-116">Description</span><span class="sxs-lookup"><span data-stu-id="46273-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="46273-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="46273-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="46273-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="46273-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="46273-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46273-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46273-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="46273-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





