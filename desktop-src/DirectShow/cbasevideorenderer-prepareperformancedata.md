---
description: La méthode PreparePerformanceData définit les \_ valeurs m trLate et m \_ trFrame du frame actuel.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Méthode CBaseVideoRenderer. PreparePerformanceData (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528645"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a><span data-ttu-id="f0451-103">Méthode CBaseVideoRenderer. PreparePerformanceData</span><span class="sxs-lookup"><span data-stu-id="f0451-103">CBaseVideoRenderer.PreparePerformanceData method</span></span>

<span data-ttu-id="f0451-104">La `PreparePerformanceData` méthode définit les valeurs **m \_ trLate** et **m \_ trFrame** du frame actuel.</span><span class="sxs-lookup"><span data-stu-id="f0451-104">The `PreparePerformanceData` method sets the **m\_trLate** and **m\_trFrame** values of the current frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0451-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0451-105">Syntax</span></span>


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="f0451-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0451-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0451-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="f0451-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="f0451-108">Valeur indiquant la date de fin de l’échantillon, en unités de temps de référence.</span><span class="sxs-lookup"><span data-stu-id="f0451-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="f0451-109">*trFrame*</span><span class="sxs-lookup"><span data-stu-id="f0451-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="f0451-110">Temps d’intertramage, en unités de temps de référence.</span><span class="sxs-lookup"><span data-stu-id="f0451-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0451-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0451-111">Return value</span></span>

<span data-ttu-id="f0451-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f0451-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0451-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f0451-113">Remarks</span></span>

<span data-ttu-id="f0451-114">Cette fonction membre définit **m \_ trLate** à la valeur de *trLate* et **m \_ trFrame** à la valeur de *trFrame*.</span><span class="sxs-lookup"><span data-stu-id="f0451-114">This member function sets **m\_trLate** to the value of *trLate* and **m\_trFrame** to the value of *trFrame*.</span></span>

<span data-ttu-id="f0451-115">Lorsque la fonction membre [**CBaseVideoRenderer :: RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) est appelée à partir de [**CBaseVideoRenderer :: OnRenderStart**](cbasevideorenderer-onrenderstart.md) ou [**CBaseVideoRenderer :: OnDirectRender**](cbasevideorenderer-ondirectrender.md), elle passe les valeurs de **m \_ trLate** et **m \_ trFrame** pour la mise à jour des statistiques.</span><span class="sxs-lookup"><span data-stu-id="f0451-115">When the [**CBaseVideoRenderer::RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) member function is called from either [**CBaseVideoRenderer::OnRenderStart**](cbasevideorenderer-onrenderstart.md) or [**CBaseVideoRenderer::OnDirectRender**](cbasevideorenderer-ondirectrender.md), it passes the values of **m\_trLate** and **m\_trFrame** for it to update the statistics.</span></span> <span data-ttu-id="f0451-116">`PreparePerformanceData` est appelé à partir de [**CBaseVideoRenderer :: OnWaitEnd**](cbasevideorenderer-onwaitend.md) pour définir ces valeurs de membre de données.</span><span class="sxs-lookup"><span data-stu-id="f0451-116">`PreparePerformanceData` is called from [**CBaseVideoRenderer::OnWaitEnd**](cbasevideorenderer-onwaitend.md) to set these data member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0451-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0451-117">Requirements</span></span>



| <span data-ttu-id="f0451-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0451-118">Requirement</span></span> | <span data-ttu-id="f0451-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0451-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0451-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0451-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f0451-121"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0451-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f0451-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0451-122">Library</span></span><br/> | <dl> <span data-ttu-id="f0451-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f0451-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0451-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0451-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0451-125">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="f0451-125">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




