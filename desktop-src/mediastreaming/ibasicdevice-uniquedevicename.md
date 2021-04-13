---
title: Méthode IBasicDevice UniqueDeviceName
description: Récupère le nom d’appareil unique de l’appareil (UDN).
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- API de diffusion multimédia en continu de méthode UniqueDeviceName
- API de diffusion multimédia en continu de méthode UniqueDeviceName, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode UniqueDeviceName
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b3103640fd49880dc5ae5ca881618ac1091de62
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380740"
---
# <a name="ibasicdeviceuniquedevicename-method"></a><span data-ttu-id="ef629-106">IBasicDevice :: UniqueDeviceName, méthode</span><span class="sxs-lookup"><span data-stu-id="ef629-106">IBasicDevice::UniqueDeviceName method</span></span>

<span data-ttu-id="ef629-107">Récupère le nom d’appareil unique de l’appareil (UDN).</span><span class="sxs-lookup"><span data-stu-id="ef629-107">Retrieves the device s unique device name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef629-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef629-108">Syntax</span></span>


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="ef629-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef629-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef629-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef629-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef629-111">Reçoit un pointeur vers le modèle de périphérique s UDN.</span><span class="sxs-lookup"><span data-stu-id="ef629-111">Receives a pointer to the device s model UDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef629-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef629-112">Return value</span></span>

<span data-ttu-id="ef629-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ef629-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ef629-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ef629-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ef629-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ef629-115">Return code</span></span>                                                                          | <span data-ttu-id="ef629-116">Description</span><span class="sxs-lookup"><span data-stu-id="ef629-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ef629-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef629-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ef629-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef629-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ef629-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef629-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef629-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="ef629-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





