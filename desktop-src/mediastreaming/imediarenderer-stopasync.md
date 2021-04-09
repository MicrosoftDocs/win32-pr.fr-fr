---
title: Méthode IMediaRenderer StopAsync
description: Fait en sorte que le DMR de manière asynchrone arrête la diffusion du contenu actuel. | Méthode IMediaRenderer StopAsync
ms.assetid: B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0
keywords:
- API de diffusion multimédia en continu de méthode StopAsync
- API de diffusion multimédia en continu de méthode StopAsync, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode StopAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5f73d534fdd786038a242614a981f4915d92c13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870010"
---
# <a name="imediarendererstopasync-method"></a><span data-ttu-id="2e181-107">IMediaRenderer :: StopAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="2e181-107">IMediaRenderer::StopAsync method</span></span>

<span data-ttu-id="2e181-108">Fait en sorte que le DMR de manière asynchrone arrête la diffusion du contenu actuel.</span><span class="sxs-lookup"><span data-stu-id="2e181-108">Instructs the DMR asynchronously to stop playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e181-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e181-109">Syntax</span></span>


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="2e181-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e181-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e181-111">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2e181-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e181-112">Reçoit une référence à un objet [**PlaybackOperation**](playbackoperation.md) qui est utilisé pour obtenir les résultats de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2e181-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e181-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e181-113">Return value</span></span>

<span data-ttu-id="2e181-114">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2e181-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2e181-115">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2e181-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2e181-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2e181-116">Return code</span></span>                                                                          | <span data-ttu-id="2e181-117">Description</span><span class="sxs-lookup"><span data-stu-id="2e181-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2e181-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2e181-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2e181-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="2e181-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="2e181-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e181-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e181-121">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="2e181-121">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





