---
description: La \_ variable de membre m bModifiesData indique si le filtre modifie les exemples de données qui sont reçus. La valeur est définie dans le constructeur CTransInPlaceFilter, mais prend par défaut la valeur TRUE.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Membre CTransInPlaceFilter :: m_bModifiesData (Transip. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5bc0d630fd0eda6e9915f8c11f5b15d21b725ce8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530315"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a><span data-ttu-id="c8850-104">CTransInPlaceFilter :: m \_ bModifiesData, membre</span><span class="sxs-lookup"><span data-stu-id="c8850-104">CTransInPlaceFilter::m\_bModifiesData member</span></span>

<span data-ttu-id="c8850-105">La `m_bModifiesData` variable membre indique si le filtre modifie les exemples de données qui sont reçus.</span><span class="sxs-lookup"><span data-stu-id="c8850-105">The `m_bModifiesData` member variable indicates whether the filter modifies the sample data that is receives.</span></span> <span data-ttu-id="c8850-106">La valeur est définie dans le constructeur **CTransInPlaceFilter** , mais prend par défaut la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="c8850-106">The value is set in the **CTransInPlaceFilter** constructor, but defaults to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8850-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8850-107">Syntax</span></span>


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a><span data-ttu-id="c8850-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c8850-108">Remarks</span></span>

<span data-ttu-id="c8850-109">Cette variable affecte la manière dont le filtre négocie l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="c8850-109">This variable affects how the filter negotiates the allocator.</span></span> <span data-ttu-id="c8850-110">Si la valeur est **true**, le filtre ne peut pas utiliser d’allocateur en lecture seule pour les deux connexions de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="c8850-110">If the value is **TRUE**, the filter cannot use a read-only allocator for both pin connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8850-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8850-111">Requirements</span></span>



| <span data-ttu-id="c8850-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8850-112">Requirement</span></span> | <span data-ttu-id="c8850-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8850-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8850-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8850-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c8850-115"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8850-115"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c8850-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c8850-116">Library</span></span><br/> | <dl> <span data-ttu-id="c8850-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c8850-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8850-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8850-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8850-119">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="c8850-119">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




