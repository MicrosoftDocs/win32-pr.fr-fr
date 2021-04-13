---
title: Méthode IBasicDevice ModelUrl
description: Récupère l’URL du modèle de l’appareil.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- API de diffusion multimédia en continu de méthode ModelUrl
- API de diffusion multimédia en continu de méthode ModelUrl, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode ModelUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f616d1a122f5fe6025c80742df61eb86d41514a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312451"
---
# <a name="ibasicdevicemodelurl-method"></a><span data-ttu-id="7ca60-106">IBasicDevice :: ModelUrl, méthode</span><span class="sxs-lookup"><span data-stu-id="7ca60-106">IBasicDevice::ModelUrl method</span></span>

<span data-ttu-id="7ca60-107">Récupère l’URL du modèle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ca60-107">Retrieves the device s model URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca60-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ca60-108">Syntax</span></span>


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="7ca60-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ca60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca60-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7ca60-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca60-111">Reçoit un pointeur vers l’URL du modèle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ca60-111">Receives a pointer to the device s model URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ca60-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ca60-112">Return value</span></span>

<span data-ttu-id="7ca60-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7ca60-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7ca60-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7ca60-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7ca60-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7ca60-115">Return code</span></span>                                                                          | <span data-ttu-id="7ca60-116">Description</span><span class="sxs-lookup"><span data-stu-id="7ca60-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7ca60-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca60-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7ca60-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ca60-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="7ca60-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ca60-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca60-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="7ca60-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





