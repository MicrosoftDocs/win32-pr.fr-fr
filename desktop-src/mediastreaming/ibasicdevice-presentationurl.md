---
title: Méthode IBasicDevice PresentationUrl
description: Récupère l’URL de présentation de l’appareil.
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- API de diffusion multimédia en continu de méthode PresentationUrl
- API de diffusion multimédia en continu de méthode PresentationUrl, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode PresentationUrl
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89d10187329692c4f279a94cde004455a182733e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380752"
---
# <a name="ibasicdevicepresentationurl-method"></a><span data-ttu-id="a62a4-106">IBasicDevice ::P méthode resentationUrl</span><span class="sxs-lookup"><span data-stu-id="a62a4-106">IBasicDevice::PresentationUrl method</span></span>

<span data-ttu-id="a62a4-107">Récupère l’URL de présentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a62a4-107">Retrieves the device s presentation URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="a62a4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a62a4-108">Syntax</span></span>


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="a62a4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a62a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a62a4-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a62a4-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a62a4-111">Reçoit un pointeur vers l’URL de présentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a62a4-111">Receives a pointer to the device s presentation URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a62a4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a62a4-112">Return value</span></span>

<span data-ttu-id="a62a4-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a62a4-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a62a4-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a62a4-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a62a4-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a62a4-115">Return code</span></span>                                                                          | <span data-ttu-id="a62a4-116">Description</span><span class="sxs-lookup"><span data-stu-id="a62a4-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a62a4-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a62a4-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a62a4-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a62a4-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a62a4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a62a4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a62a4-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="a62a4-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





