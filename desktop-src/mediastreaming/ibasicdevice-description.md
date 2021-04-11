---
title: IBasicDevice, méthode de description
description: Récupère une description de l’appareil.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- Méthode de description API de diffusion multimédia en continu
- Méthode de description API de diffusion multimédia en continu, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode de description
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f094246d1424c458e624d4a49358b63a84b9b7d2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030110"
---
# <a name="ibasicdevicedescription-method"></a><span data-ttu-id="6306e-106">IBasicDevice ::D méthode escription</span><span class="sxs-lookup"><span data-stu-id="6306e-106">IBasicDevice::Description method</span></span>

<span data-ttu-id="6306e-107">Récupère une description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6306e-107">Retrieves a description of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6306e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6306e-108">Syntax</span></span>


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="6306e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6306e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6306e-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6306e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6306e-111">Reçoit un pointeur vers la description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6306e-111">Receives a pointer to the description of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6306e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6306e-112">Return value</span></span>

<span data-ttu-id="6306e-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6306e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6306e-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6306e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6306e-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6306e-115">Return code</span></span>                                                                          | <span data-ttu-id="6306e-116">Description</span><span class="sxs-lookup"><span data-stu-id="6306e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6306e-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6306e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6306e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6306e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6306e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6306e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6306e-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="6306e-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





