---
description: Pointeur vers une \_ structure de filtre AMOVIESETUP.
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: 'CFactoryTemplate :: m_pAMovieSetup_Filter, membre (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAMovieSetup_Filter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 087612acf99a41966ccd98d3b41d2b83255a86f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541389"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a><span data-ttu-id="58d00-103">CFactoryTemplate :: m \_ pAMovieSetup, \_ membre de filtre</span><span class="sxs-lookup"><span data-stu-id="58d00-103">CFactoryTemplate::m\_pAMovieSetup\_Filter member</span></span>

<span data-ttu-id="58d00-104">Pointeur vers une structure de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="58d00-104">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="58d00-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58d00-105">Syntax</span></span>


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a><span data-ttu-id="58d00-106">Notes</span><span class="sxs-lookup"><span data-stu-id="58d00-106">Remarks</span></span>

<span data-ttu-id="58d00-107">Utilisez cette structure pour procéder à l’inscription automatique d’un filtre.</span><span class="sxs-lookup"><span data-stu-id="58d00-107">Use this structure to make a filter self-registering.</span></span> <span data-ttu-id="58d00-108">Si votre composant n’est pas un filtre, cette variable membre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="58d00-108">If your component is not a filter, this member variable can be **NULL**.</span></span> <span data-ttu-id="58d00-109">Pour plus d’informations, consultez Comment inscrire des filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="58d00-109">For more information, see How to Register DirectShow Filters.</span></span>

## <a name="requirements"></a><span data-ttu-id="58d00-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58d00-110">Requirements</span></span>



| <span data-ttu-id="58d00-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58d00-111">Requirement</span></span> | <span data-ttu-id="58d00-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="58d00-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58d00-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="58d00-113">Header</span></span><br/>  | <dl> <span data-ttu-id="58d00-114"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58d00-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="58d00-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="58d00-115">Library</span></span><br/> | <dl> <span data-ttu-id="58d00-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="58d00-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58d00-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58d00-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d00-118">**CFactoryTemplate, classe**</span><span class="sxs-lookup"><span data-stu-id="58d00-118">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




