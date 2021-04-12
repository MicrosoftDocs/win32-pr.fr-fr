---
title: IBasicDevice SerialNumber, méthode
description: Récupère le numéro de série de l’appareil.
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- Méthode SerialNumber API de diffusion multimédia en continu
- SerialNumber méthode SerialNumber API de diffusion multimédia en continu, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode SerialNumber
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f24fad2e74c3ec2a5b489d8f5dd57265ea6d21bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312487"
---
# <a name="ibasicdeviceserialnumber-method"></a><span data-ttu-id="11fff-106">IBasicDevice :: SerialNumber, méthode</span><span class="sxs-lookup"><span data-stu-id="11fff-106">IBasicDevice::SerialNumber method</span></span>

<span data-ttu-id="11fff-107">Récupère le numéro de série de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11fff-107">Retrieves the device s serial number.</span></span>

## <a name="syntax"></a><span data-ttu-id="11fff-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11fff-108">Syntax</span></span>


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="11fff-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11fff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11fff-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="11fff-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11fff-111">Reçoit un pointeur vers le numéro de série de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="11fff-111">Receives a pointer to the device s serial number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11fff-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11fff-112">Return value</span></span>

<span data-ttu-id="11fff-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="11fff-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="11fff-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="11fff-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="11fff-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="11fff-115">Return code</span></span>                                                                          | <span data-ttu-id="11fff-116">Description</span><span class="sxs-lookup"><span data-stu-id="11fff-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="11fff-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11fff-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="11fff-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="11fff-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="11fff-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11fff-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11fff-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="11fff-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





