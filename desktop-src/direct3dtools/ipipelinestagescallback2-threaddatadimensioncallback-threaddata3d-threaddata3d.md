---
description: Rappel qui avertit l’hôte du nombre de threads et de groupes du nuanceur de calcul dans la requête associée.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataDimensionCallback\_ThreadData3D\_ThreadData3D
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback2 :: ThreadDataDimensionCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E8765C14-0A55-468D-BCA8-3E28E5476DFB
api_name:
- IPipeLineStagesCallback2.ThreadDataDimensionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a8ee64c863128513563f3ce50dd2bfcdd77714
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392820"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3dspanipipelinestagescallback2threaddatadimensioncallback-method"></a><span data-ttu-id="19c3d-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>IPipeLineStagesCallback2 :: ThreadDataDimensionCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="19c3d-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>IPipeLineStagesCallback2::ThreadDataDimensionCallback method</span></span>

<span data-ttu-id="19c3d-104">Rappel qui avertit l’hôte du nombre de threads et de groupes du nuanceur de calcul dans la requête associée.</span><span class="sxs-lookup"><span data-stu-id="19c3d-104">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c3d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19c3d-105">Syntax</span></span>


```C++
HRESULT ThreadDataDimensionCallback(
   ThreadData3D threadGroupCount,
   ThreadData3D threadGroupSize
);
```

## <a name="parameters"></a><span data-ttu-id="19c3d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19c3d-106">Parameters</span></span>

<span data-ttu-id="19c3d-107">*threadGroupCount* </span><span class="sxs-lookup"><span data-stu-id="19c3d-107">*threadGroupCount* </span></span>  
<span data-ttu-id="19c3d-108">Nombre multidimensionnel de groupes de threads.</span><span class="sxs-lookup"><span data-stu-id="19c3d-108">The multi-dimensional count of thread groups.</span></span>

<span data-ttu-id="19c3d-109">*threadGroupSize* </span><span class="sxs-lookup"><span data-stu-id="19c3d-109">*threadGroupSize* </span></span>  
<span data-ttu-id="19c3d-110">Taille multidimensionnelle de chaque groupe de threads.</span><span class="sxs-lookup"><span data-stu-id="19c3d-110">The multi-dimensional size of each thread group.</span></span>

## <a name="return-value"></a><span data-ttu-id="19c3d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19c3d-111">Return value</span></span>

<span data-ttu-id="19c3d-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="19c3d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19c3d-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19c3d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="19c3d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19c3d-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="19c3d-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="19c3d-115">Header</span></span></p></td><td><span data-ttu-id="19c3d-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="19c3d-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="19c3d-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19c3d-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="19c3d-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="19c3d-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
