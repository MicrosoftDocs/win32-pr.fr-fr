---
title: Méthode IMediaRenderer PauseAsync
description: Ordonne à DMR de suspendre de manière asynchrone la diffusion du contenu actuel. | Méthode IMediaRenderer PauseAsync
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- API de diffusion multimédia en continu de méthode PauseAsync
- API de diffusion multimédia en continu de méthode PauseAsync, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode PauseAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8713fa4b2fe46a694024c2873cd50a0ec89ce898
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538305"
---
# <a name="imediarendererpauseasync-method"></a><span data-ttu-id="e91c4-107">IMediaRenderer ::P méthode auseAsync</span><span class="sxs-lookup"><span data-stu-id="e91c4-107">IMediaRenderer::PauseAsync method</span></span>

<span data-ttu-id="e91c4-108">Ordonne à DMR de suspendre de manière asynchrone la diffusion du contenu actuel.</span><span class="sxs-lookup"><span data-stu-id="e91c4-108">Instructs the DMR asynchronously to pause playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="e91c4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e91c4-109">Syntax</span></span>


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="e91c4-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e91c4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e91c4-111">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e91c4-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e91c4-112">Reçoit une référence à un objet [**PlaybackOperation**](playbackoperation.md) qui est utilisé pour obtenir les résultats de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e91c4-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e91c4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e91c4-113">Return value</span></span>

<span data-ttu-id="e91c4-114">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e91c4-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e91c4-115">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e91c4-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e91c4-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e91c4-116">Return code</span></span>                                                                          | <span data-ttu-id="e91c4-117">Description</span><span class="sxs-lookup"><span data-stu-id="e91c4-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e91c4-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e91c4-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e91c4-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e91c4-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e91c4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e91c4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e91c4-121">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="e91c4-121">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





