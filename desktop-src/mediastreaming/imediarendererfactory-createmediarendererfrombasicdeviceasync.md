---
title: Méthode IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync
description: Crée de façon asynchrone une nouvelle instance d’un objet qui implémente l’interface IMediaRenderer à l’aide de l’interface IBasicDevice spécifiée.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- API de diffusion multimédia en continu de méthode CreateMediaRendererFromBasicDeviceAsync
- API de diffusion multimédia en continu de méthode CreateMediaRendererFromBasicDeviceAsync, interface IMediaRendererFactory
- API de diffusion multimédia en continu de l’interface IMediaRendererFactory, méthode CreateMediaRendererFromBasicDeviceAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4ee614cca9a03ca203ecde9203e019fab38ab4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031141"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a><span data-ttu-id="e5f0e-106">IMediaRendererFactory :: CreateMediaRendererFromBasicDeviceAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="e5f0e-106">IMediaRendererFactory::CreateMediaRendererFromBasicDeviceAsync method</span></span>

<span data-ttu-id="e5f0e-107">Crée de façon asynchrone une nouvelle instance d’un objet qui implémente l’interface [**IMediaRenderer**](imediarenderer.md) à l’aide de l’interface [**IBasicDevice**](ibasicdevice.md) spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e5f0e-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified [**IBasicDevice**](ibasicdevice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5f0e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5f0e-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="e5f0e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5f0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5f0e-110">*basicDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5f0e-110">*basicDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f0e-111">Pointeur vers une interface [**IBasicDevice**](ibasicdevice.md) représentant l’appareil pour lequel une instance de [**IMediaRenderer**](imediarenderer.md) sera créée.</span><span class="sxs-lookup"><span data-stu-id="e5f0e-111">A pointer to an [**IBasicDevice**](ibasicdevice.md) interface representing the device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="e5f0e-112">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e5f0e-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f0e-113">Reçoit une référence à un objet [**CreateMediaRendererOperation**](createmediarendereroperation.md) qui est utilisé pour obtenir les résultats de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e5f0e-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5f0e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5f0e-114">Return value</span></span>

<span data-ttu-id="e5f0e-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e5f0e-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e5f0e-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e5f0e-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e5f0e-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e5f0e-117">Return code</span></span>                                                                          | <span data-ttu-id="e5f0e-118">Description</span><span class="sxs-lookup"><span data-stu-id="e5f0e-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e5f0e-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e5f0e-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e5f0e-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5f0e-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e5f0e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5f0e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5f0e-122">**IMediaRendererFactory**</span><span class="sxs-lookup"><span data-stu-id="e5f0e-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

