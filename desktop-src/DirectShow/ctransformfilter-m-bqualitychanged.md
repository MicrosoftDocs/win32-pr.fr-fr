---
description: Indicateur qui signale si la qualité a changé.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Membre CTransformFilter :: m_bQualityChanged (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540004"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a><span data-ttu-id="6f284-103">CTransformFilter :: m \_ bQualityChanged, membre</span><span class="sxs-lookup"><span data-stu-id="6f284-103">CTransformFilter::m\_bQualityChanged member</span></span>

<span data-ttu-id="6f284-104">Indicateur qui signale si la qualité a changé.</span><span class="sxs-lookup"><span data-stu-id="6f284-104">Flag that indicates whether the quality has changed.</span></span> <span data-ttu-id="6f284-105">La première fois que le filtre supprime un échantillon, il envoie un événement de modification de la [**\_ qualité \_ ce**](ec-quality-change.md) au gestionnaire du graphique de filtre et définit cet indicateur sur **true**.</span><span class="sxs-lookup"><span data-stu-id="6f284-105">The first time that the filter drops a sample, it sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager and sets this flag to **TRUE**.</span></span> <span data-ttu-id="6f284-106">Il ne renvoie pas cet événement tant que le filtre n’est pas arrêté et redémarré, même s’il continue à supprimer des échantillons entre-temps.</span><span class="sxs-lookup"><span data-stu-id="6f284-106">It does not send this event again until the filter stops and restarts, even if it continues to drop samples in the meantime.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f284-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f284-107">Syntax</span></span>


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a><span data-ttu-id="6f284-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f284-108">Requirements</span></span>



| <span data-ttu-id="6f284-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f284-109">Requirement</span></span> | <span data-ttu-id="6f284-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f284-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f284-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f284-111">Header</span></span><br/>  | <dl> <span data-ttu-id="6f284-112"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f284-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6f284-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6f284-113">Library</span></span><br/> | <dl> <span data-ttu-id="6f284-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6f284-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f284-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f284-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f284-116">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="6f284-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




