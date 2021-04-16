---
title: PlaybackOperation. GetResults, méthode
description: Retourne les résultats d’une opération asynchrone démarrée par l’une des méthodes de lecture MediaRenderer.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- Méthode GetResults API de diffusion multimédia en continu
- Méthode GetResults API de diffusion multimédia en continu, interface PlaybackOperation
- API de diffusion multimédia en continu de l’interface PlaybackOperation, méthode GetResults
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f146876966cc4e003bd88ad295c9938e5240abfe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380547"
---
# <a name="playbackoperationgetresults-method"></a><span data-ttu-id="50c41-106">PlaybackOperation. GetResults, méthode</span><span class="sxs-lookup"><span data-stu-id="50c41-106">PlaybackOperation.GetResults method</span></span>

<span data-ttu-id="50c41-107">Retourne les résultats d’une opération asynchrone démarrée par l’une des méthodes de lecture [**MediaRenderer**](mediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="50c41-107">Returns the results of an asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="50c41-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50c41-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="50c41-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50c41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50c41-110">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="50c41-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="50c41-111">Résultat de l'opération.</span><span class="sxs-lookup"><span data-stu-id="50c41-111">The result of the operation.</span></span> <span data-ttu-id="50c41-112">La valeur 0 indique que l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="50c41-112">A value of 0 indicates that the operation completed.</span></span> <span data-ttu-id="50c41-113">Les autres valeurs sont réservées.</span><span class="sxs-lookup"><span data-stu-id="50c41-113">Other values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50c41-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50c41-114">Return value</span></span>

<span data-ttu-id="50c41-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="50c41-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="50c41-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="50c41-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="50c41-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="50c41-117">Return code</span></span>                                                                          | <span data-ttu-id="50c41-118">Description</span><span class="sxs-lookup"><span data-stu-id="50c41-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="50c41-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="50c41-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="50c41-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="50c41-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="50c41-121">Notes</span><span class="sxs-lookup"><span data-stu-id="50c41-121">Remarks</span></span>

<span data-ttu-id="50c41-122">La méthode **GetResults** est généralement appelée à partir du gestionnaire d’événements qui a été enregistré en définissant la propriété [**Completed**](playbackoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="50c41-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](playbackoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="50c41-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50c41-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c41-124">**PlaybackOperation**</span><span class="sxs-lookup"><span data-stu-id="50c41-124">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 





