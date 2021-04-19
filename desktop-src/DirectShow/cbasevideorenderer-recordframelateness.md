---
description: La méthode RecordFrameLateness enregistre l’heure à laquelle le rendu s’est produit et rassemble des statistiques pour la page de propriétés.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Méthode CBaseVideoRenderer. RecordFrameLateness (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542473"
---
# <a name="cbasevideorendererrecordframelateness-method"></a><span data-ttu-id="2700b-103">Méthode CBaseVideoRenderer. RecordFrameLateness</span><span class="sxs-lookup"><span data-stu-id="2700b-103">CBaseVideoRenderer.RecordFrameLateness method</span></span>

<span data-ttu-id="2700b-104">La `RecordFrameLateness` méthode enregistre le moment où le rendu s’est produit et rassemble des statistiques pour la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2700b-104">The `RecordFrameLateness` method records how timely the rendering occurred and gathers statistics for the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="2700b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2700b-105">Syntax</span></span>


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="2700b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2700b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2700b-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="2700b-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="2700b-108">Valeur indiquant la date de fin de l’échantillon, en unités de temps de référence.</span><span class="sxs-lookup"><span data-stu-id="2700b-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="2700b-109">*trFrame*</span><span class="sxs-lookup"><span data-stu-id="2700b-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="2700b-110">Temps d’intertramage, en unités de temps de référence.</span><span class="sxs-lookup"><span data-stu-id="2700b-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2700b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2700b-111">Return value</span></span>

<span data-ttu-id="2700b-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2700b-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2700b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2700b-113">Requirements</span></span>



| <span data-ttu-id="2700b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2700b-114">Requirement</span></span> | <span data-ttu-id="2700b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2700b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2700b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="2700b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2700b-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2700b-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2700b-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2700b-118">Library</span></span><br/> | <dl> <span data-ttu-id="2700b-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2700b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2700b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2700b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2700b-121">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="2700b-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




