---
description: Objet de section critique qui protège l’état du filtre. La méthode d’assistance CSource ::p StateLock retourne un pointeur vers cette variable membre.
ms.assetid: faaf5fea-54bc-4856-9bca-3ed420c491e4
title: 'Membre CSource :: m_cStateLock (source. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85ff046b7e1f7a0ccfcc41f630785a3e8404e256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522780"
---
# <a name="csourcem_cstatelock-member"></a><span data-ttu-id="b997b-104">CSource :: m \_ cStateLock, membre</span><span class="sxs-lookup"><span data-stu-id="b997b-104">CSource::m\_cStateLock member</span></span>

<span data-ttu-id="b997b-105">Objet de section critique qui protège l’état du filtre.</span><span class="sxs-lookup"><span data-stu-id="b997b-105">Critical section object that protects the filter state.</span></span> <span data-ttu-id="b997b-106">La méthode d’assistance [**CSource ::P statelock**](csource--pstatelock.md) retourne un pointeur vers cette variable membre.</span><span class="sxs-lookup"><span data-stu-id="b997b-106">The [**CSource::pStateLock**](csource--pstatelock.md) helper method returns a pointer to this member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b997b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b997b-107">Syntax</span></span>


```C++
CCritSec m_cStateLock;
```



## <a name="requirements"></a><span data-ttu-id="b997b-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b997b-108">Requirements</span></span>



| <span data-ttu-id="b997b-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b997b-109">Requirement</span></span> | <span data-ttu-id="b997b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b997b-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b997b-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="b997b-111">Header</span></span><br/>  | <dl> <span data-ttu-id="b997b-112"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b997b-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b997b-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b997b-113">Library</span></span><br/> | <dl> <span data-ttu-id="b997b-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b997b-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b997b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b997b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b997b-116">**CSource, classe**</span><span class="sxs-lookup"><span data-stu-id="b997b-116">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




