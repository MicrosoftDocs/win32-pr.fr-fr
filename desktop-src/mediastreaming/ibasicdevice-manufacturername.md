---
title: Méthode IBasicDevice ManufacturerName
description: Récupère le nom du fabricant de l’appareil.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- API de diffusion multimédia en continu de méthode ManufacturerName
- API de diffusion multimédia en continu de méthode ManufacturerName, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode ManufacturerName
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 698b4b6c202ed157737b20296976a282c7f97ba3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106509228"
---
# <a name="ibasicdevicemanufacturername-method"></a><span data-ttu-id="c9936-106">IBasicDevice :: ManufacturerName, méthode</span><span class="sxs-lookup"><span data-stu-id="c9936-106">IBasicDevice::ManufacturerName method</span></span>

<span data-ttu-id="c9936-107">Récupère le nom du fabricant de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9936-107">Retrieves the device s manufacturer name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9936-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9936-108">Syntax</span></span>


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="c9936-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9936-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9936-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9936-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9936-111">Reçoit un pointeur vers le nom du fabricant de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9936-111">Receives a pointer to the device s manufacturer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9936-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9936-112">Return value</span></span>

<span data-ttu-id="c9936-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c9936-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c9936-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c9936-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c9936-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c9936-115">Return code</span></span>                                                                          | <span data-ttu-id="c9936-116">Description</span><span class="sxs-lookup"><span data-stu-id="c9936-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c9936-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9936-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c9936-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9936-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c9936-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9936-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9936-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="c9936-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





