---
title: Méthode IBasicDevice PhysicalAddresses
description: Retourne un vecteur d’adresses physiques.
ms.assetid: 85F48EE3-14A1-46DA-A3C3-F94A8A43CF92
keywords:
- API de diffusion multimédia en continu de méthode PhysicalAddresses
- API de diffusion multimédia en continu de méthode PhysicalAddresses, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode PhysicalAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f1cd87435c78e1f6877d1bb6afd1b38981b05dc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312448"
---
# <a name="ibasicdevicephysicaladdresses-method"></a><span data-ttu-id="66b41-106">IBasicDevice ::P méthode hysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="66b41-106">IBasicDevice::PhysicalAddresses method</span></span>

<span data-ttu-id="66b41-107">Retourne un vecteur d’adresses physiques.</span><span class="sxs-lookup"><span data-stu-id="66b41-107">Returns a vector of physical addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="66b41-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66b41-108">Syntax</span></span>


```C++
HRESULT PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="66b41-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66b41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66b41-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="66b41-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66b41-111">Reçoit une collection énumérable de pointeurs vers des adresses physiques.</span><span class="sxs-lookup"><span data-stu-id="66b41-111">Receives an enumerable collection of pointers to physical addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66b41-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66b41-112">Return value</span></span>

<span data-ttu-id="66b41-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="66b41-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="66b41-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="66b41-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="66b41-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="66b41-115">Return code</span></span>                                                                          | <span data-ttu-id="66b41-116">Description</span><span class="sxs-lookup"><span data-stu-id="66b41-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="66b41-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66b41-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="66b41-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="66b41-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="66b41-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66b41-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66b41-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="66b41-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





