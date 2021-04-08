---
title: IBasicDevice FriendlyName, méthode
description: Récupère le nom convivial de l’appareil.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- Méthode FriendlyName API de diffusion multimédia en continu
- Méthode FriendlyName API de diffusion multimédia en continu, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode FriendlyName
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec2b2edfa3a98dfdbbdd1d236acb6e1f1433f141
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678577"
---
# <a name="ibasicdevicefriendlyname-method"></a><span data-ttu-id="6f25c-106">IBasicDevice :: FriendlyName, méthode</span><span class="sxs-lookup"><span data-stu-id="6f25c-106">IBasicDevice::FriendlyName method</span></span>

<span data-ttu-id="6f25c-107">Récupère le nom convivial de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f25c-107">Retrieves the device s friendly name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f25c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f25c-108">Syntax</span></span>


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="6f25c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f25c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f25c-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6f25c-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f25c-111">Reçoit un pointeur vers le nom convivial de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6f25c-111">Receives a pointer to the device s friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f25c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f25c-112">Return value</span></span>

<span data-ttu-id="6f25c-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6f25c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6f25c-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6f25c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6f25c-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6f25c-115">Return code</span></span>                                                                          | <span data-ttu-id="6f25c-116">Description</span><span class="sxs-lookup"><span data-stu-id="6f25c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6f25c-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6f25c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6f25c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6f25c-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6f25c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f25c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f25c-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="6f25c-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





