---
title: GetVolumeOperation. GetResults, méthode
description: Retourne les résultats de l’opération asynchrone démarrée par GetVolumeAsync.
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- Méthode GetResults API de diffusion multimédia en continu
- Méthode GetResults API de diffusion multimédia en continu, interface GetVolumeOperation
- API de diffusion multimédia en continu de l’interface GetVolumeOperation, méthode GetResults
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 444eaf590e5afc5d4f5185bcd3793698d6fe4535
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509843"
---
# <a name="getvolumeoperationgetresults-method"></a><span data-ttu-id="7f813-106">GetVolumeOperation. GetResults, méthode</span><span class="sxs-lookup"><span data-stu-id="7f813-106">GetVolumeOperation.GetResults method</span></span>

<span data-ttu-id="7f813-107">Retourne les résultats de l’opération asynchrone démarrée par [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span><span class="sxs-lookup"><span data-stu-id="7f813-107">Returns the results of the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f813-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f813-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="7f813-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f813-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f813-110">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7f813-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7f813-111">Volume.</span><span class="sxs-lookup"><span data-stu-id="7f813-111">The volume.</span></span> <span data-ttu-id="7f813-112">Valeur comprise entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="7f813-112">A value between 0 and 100.</span></span> <span data-ttu-id="7f813-113">0 indique un volume minimum et 100 indique un volume maximal.</span><span class="sxs-lookup"><span data-stu-id="7f813-113">0 indicates minimum volume, and 100 indicates maximum volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f813-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f813-114">Return value</span></span>

<span data-ttu-id="7f813-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7f813-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7f813-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7f813-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7f813-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7f813-117">Return code</span></span>                                                                          | <span data-ttu-id="7f813-118">Description</span><span class="sxs-lookup"><span data-stu-id="7f813-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7f813-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7f813-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7f813-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f813-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f813-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7f813-121">Remarks</span></span>

<span data-ttu-id="7f813-122">La méthode **GetResults** est généralement appelée à partir du gestionnaire d’événements qui a été enregistré en définissant la propriété [**Completed**](getvolumeoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="7f813-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getvolumeoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f813-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f813-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f813-124">**GetVolumeOperation**</span><span class="sxs-lookup"><span data-stu-id="7f813-124">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

