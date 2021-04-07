---
title: Méthode IMediaRendererFactory CreateMediaRendererAsync
description: Crée de façon asynchrone une nouvelle instance d’un objet qui implémente l’interface IMediaRenderer à l’aide du nom de périphérique unique spécifié (UDN).
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- API de diffusion multimédia en continu de méthode CreateMediaRendererAsync
- API de diffusion multimédia en continu de méthode CreateMediaRendererAsync, interface IMediaRendererFactory
- API de diffusion multimédia en continu de l’interface IMediaRendererFactory, méthode CreateMediaRendererAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725884"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a><span data-ttu-id="7f1f8-106">IMediaRendererFactory :: CreateMediaRendererAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="7f1f8-106">IMediaRendererFactory::CreateMediaRendererAsync method</span></span>

<span data-ttu-id="7f1f8-107">Crée de façon asynchrone une nouvelle instance d’un objet qui implémente l’interface [**IMediaRenderer**](imediarenderer.md) à l’aide du nom de périphérique unique spécifié (UDN).</span><span class="sxs-lookup"><span data-stu-id="7f1f8-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified Unique Device Name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f1f8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f1f8-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="7f1f8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f1f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f1f8-110">*deviceIdentifier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f1f8-110">*deviceIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f1f8-111">HSTRING contenant un UDN qui identifie l’appareil DMR DLNA pour lequel une instance de [**IMediaRenderer**](imediarenderer.md) sera créée.</span><span class="sxs-lookup"><span data-stu-id="7f1f8-111">An HSTRING containing a UDN that identifies the DLNA DMR device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="7f1f8-112">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7f1f8-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7f1f8-113">Reçoit une référence à un objet [**CreateMediaRendererOperation**](createmediarendereroperation.md) qui est utilisé pour obtenir les résultats de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7f1f8-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f1f8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f1f8-114">Return value</span></span>

<span data-ttu-id="7f1f8-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7f1f8-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7f1f8-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7f1f8-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7f1f8-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7f1f8-117">Return code</span></span>                                                                          | <span data-ttu-id="7f1f8-118">Description</span><span class="sxs-lookup"><span data-stu-id="7f1f8-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7f1f8-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7f1f8-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7f1f8-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f1f8-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="7f1f8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f1f8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f1f8-122">**IMediaRendererFactory**</span><span class="sxs-lookup"><span data-stu-id="7f1f8-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

