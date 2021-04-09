---
title: GetMuteOperation. GetResults, méthode
description: Retourne les résultats de l’opération asynchrone démarrée par GetMuteAsync.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- Méthode GetResults API de diffusion multimédia en continu
- Méthode GetResults API de diffusion multimédia en continu, interface GetMuteOperation
- API de diffusion multimédia en continu de l’interface GetMuteOperation, méthode GetResults
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101513"
---
# <a name="getmuteoperationgetresults-method"></a><span data-ttu-id="de63b-106">GetMuteOperation. GetResults, méthode</span><span class="sxs-lookup"><span data-stu-id="de63b-106">GetMuteOperation.GetResults method</span></span>

<span data-ttu-id="de63b-107">Retourne les résultats de l’opération asynchrone démarrée par [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span><span class="sxs-lookup"><span data-stu-id="de63b-107">Returns the results of the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="de63b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de63b-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="de63b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de63b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de63b-110">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="de63b-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="de63b-111">Valeur de silence.</span><span class="sxs-lookup"><span data-stu-id="de63b-111">The mute value.</span></span> <span data-ttu-id="de63b-112">La valeur true indique que l’audio est actuellement en sourdine.</span><span class="sxs-lookup"><span data-stu-id="de63b-112">A value of true indicates that audio is currently muted.</span></span> <span data-ttu-id="de63b-113">La valeur false indique que l’audio n’est pas muet.</span><span class="sxs-lookup"><span data-stu-id="de63b-113">A value of false indicates that audio is not muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de63b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de63b-114">Return value</span></span>

<span data-ttu-id="de63b-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="de63b-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="de63b-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="de63b-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="de63b-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="de63b-117">Return code</span></span>                                                                          | <span data-ttu-id="de63b-118">Description</span><span class="sxs-lookup"><span data-stu-id="de63b-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="de63b-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="de63b-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="de63b-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="de63b-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de63b-121">Notes</span><span class="sxs-lookup"><span data-stu-id="de63b-121">Remarks</span></span>

<span data-ttu-id="de63b-122">La méthode **GetResults** est généralement appelée à partir du gestionnaire d’événements qui a été enregistré en définissant la propriété [**Completed**](getmuteoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="de63b-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getmuteoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="de63b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de63b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de63b-124">**GetMuteOperation**</span><span class="sxs-lookup"><span data-stu-id="de63b-124">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

