---
title: Méthode IBasicDevice RemoteStreamingUrls
description: Retourne un vecteur d’URL de diffusion en continu à distance.
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- API de diffusion multimédia en continu de méthode RemoteStreamingUrls
- API de diffusion multimédia en continu de méthode RemoteStreamingUrls, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode RemoteStreamingUrls
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdc4bd363096e7b808a51cfbddb764daabe03a55
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380753"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a><span data-ttu-id="6aeed-106">IBasicDevice :: RemoteStreamingUrls, méthode</span><span class="sxs-lookup"><span data-stu-id="6aeed-106">IBasicDevice::RemoteStreamingUrls method</span></span>

<span data-ttu-id="6aeed-107">Retourne un vecteur d’URL de diffusion en continu à distance.</span><span class="sxs-lookup"><span data-stu-id="6aeed-107">Returns a vector of remote streaming URLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aeed-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6aeed-108">Syntax</span></span>


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="6aeed-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6aeed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aeed-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6aeed-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aeed-111">Reçoit une collection énumérable de pointeurs vers des URL de diffusion en continu distantes.</span><span class="sxs-lookup"><span data-stu-id="6aeed-111">Receives an enumerable collection of pointers to remote streaming URLs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aeed-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6aeed-112">Return value</span></span>

<span data-ttu-id="6aeed-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6aeed-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6aeed-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6aeed-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6aeed-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6aeed-115">Return code</span></span>                                                                          | <span data-ttu-id="6aeed-116">Description</span><span class="sxs-lookup"><span data-stu-id="6aeed-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6aeed-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6aeed-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6aeed-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6aeed-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6aeed-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6aeed-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aeed-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="6aeed-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





