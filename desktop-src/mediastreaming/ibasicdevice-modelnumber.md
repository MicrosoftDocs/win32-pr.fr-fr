---
title: Méthode IBasicDevice ModelNumber
description: Récupère le numéro de modèle de l’appareil.
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- API de diffusion multimédia en continu de méthode ModelNumber
- API de diffusion multimédia en continu de méthode ModelNumber, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode ModelNumber
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8034e67e5f3c552f0af83678d75e33881f1318f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841218"
---
# <a name="ibasicdevicemodelnumber-method"></a><span data-ttu-id="1485e-106">IBasicDevice :: ModelNumber, méthode</span><span class="sxs-lookup"><span data-stu-id="1485e-106">IBasicDevice::ModelNumber method</span></span>

<span data-ttu-id="1485e-107">Récupère le numéro de modèle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1485e-107">Retrieves the device s model number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1485e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1485e-108">Syntax</span></span>


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="1485e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1485e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1485e-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1485e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1485e-111">Reçoit un pointeur vers le numéro de modèle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1485e-111">Receives a pointer to the device s model number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1485e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1485e-112">Return value</span></span>

<span data-ttu-id="1485e-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1485e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1485e-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1485e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1485e-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1485e-115">Return code</span></span>                                                                          | <span data-ttu-id="1485e-116">Description</span><span class="sxs-lookup"><span data-stu-id="1485e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1485e-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1485e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1485e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1485e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1485e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1485e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1485e-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="1485e-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





