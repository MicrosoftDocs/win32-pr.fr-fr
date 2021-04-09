---
title: Méthode IMediaRendererActionInformation IsStopAvailable
description: Récupère une valeur qui indique si DMR accepte actuellement la méthode StopAsync.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- API de diffusion multimédia en continu de méthode IsStopAvailable
- API de diffusion multimédia en continu de méthode IsStopAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsStopAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e0a031bafc9a755dfec2498f4e2a52cdd9ef5b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101581"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a><span data-ttu-id="5da80-106">IMediaRendererActionInformation :: IsStopAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="5da80-106">IMediaRendererActionInformation::IsStopAvailable method</span></span>

<span data-ttu-id="5da80-107">Récupère une valeur qui indique si DMR accepte actuellement la méthode [**StopAsync**](imediarenderer-stopasync.md) .</span><span class="sxs-lookup"><span data-stu-id="5da80-107">Retrieves a value that indicates whether the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da80-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5da80-108">Syntax</span></span>


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="5da80-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5da80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5da80-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5da80-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5da80-111">Valeur booléenne qui est **true** si DMR accepte actuellement la méthode [**StopAsync**](imediarenderer-stopasync.md) et **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="5da80-111">A boolean value that is **True** if the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5da80-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5da80-112">Return value</span></span>

<span data-ttu-id="5da80-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5da80-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5da80-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5da80-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5da80-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5da80-115">Return code</span></span>                                                                          | <span data-ttu-id="5da80-116">Description</span><span class="sxs-lookup"><span data-stu-id="5da80-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5da80-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5da80-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5da80-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="5da80-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5da80-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5da80-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da80-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="5da80-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

