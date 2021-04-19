---
title: Méthode MediaRenderer. PauseAsync
description: Ordonne à DMR de suspendre de manière asynchrone la diffusion du contenu actuel. | Méthode MediaRenderer. PauseAsync
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- API de diffusion multimédia en continu de méthode PauseAsync
- API de diffusion multimédia en continu de méthode PauseAsync, interface MediaRenderer
- API de diffusion multimédia en continu de l’interface MediaRenderer, méthode PauseAsync
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbbc55931c7cc7fc5e2e5ec39ba63fe7a064478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531301"
---
# <a name="mediarendererpauseasync-method"></a><span data-ttu-id="ef059-107">Méthode MediaRenderer. PauseAsync</span><span class="sxs-lookup"><span data-stu-id="ef059-107">MediaRenderer.PauseAsync method</span></span>

<span data-ttu-id="ef059-108">Ordonne à DMR de suspendre de manière asynchrone la diffusion du contenu actuel.</span><span class="sxs-lookup"><span data-stu-id="ef059-108">Instructs the DMR asynchronously to pause playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef059-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef059-109">Syntax</span></span>


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="ef059-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef059-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef059-111">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef059-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef059-112">Reçoit une référence à un objet [**PlaybackOperation**](playbackoperation.md) qui est utilisé pour obtenir les résultats de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ef059-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef059-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef059-113">Return value</span></span>

<span data-ttu-id="ef059-114">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ef059-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ef059-115">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ef059-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ef059-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ef059-116">Return code</span></span>                                                                          | <span data-ttu-id="ef059-117">Description</span><span class="sxs-lookup"><span data-stu-id="ef059-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ef059-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef059-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ef059-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef059-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ef059-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef059-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef059-121">**MediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="ef059-121">**MediaRenderer**</span></span>](mediarenderer.md)
</dt> </dl>

 

 





