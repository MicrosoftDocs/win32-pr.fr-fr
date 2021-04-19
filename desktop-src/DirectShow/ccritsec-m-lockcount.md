---
description: Nombre de verrous en attente sur cet objet.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'Membre CCritSec :: m_lockCount (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88098a8ded025a899e2092a96308bd6c54750758
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534772"
---
# <a name="ccritsecm_lockcount-member"></a><span data-ttu-id="0bf8e-103">CCritSec :: m \_ lockCount, membre</span><span class="sxs-lookup"><span data-stu-id="0bf8e-103">CCritSec::m\_lockCount member</span></span>

<span data-ttu-id="0bf8e-104">Nombre de verrous en attente sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="0bf8e-104">Number of outstanding locks on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bf8e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bf8e-105">Syntax</span></span>


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a><span data-ttu-id="0bf8e-106">Notes</span><span class="sxs-lookup"><span data-stu-id="0bf8e-106">Remarks</span></span>

<span data-ttu-id="0bf8e-107">Cette variable membre est définie uniquement dans la version Debug de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="0bf8e-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="0bf8e-108">Les fonctions de [débogage des sections critiques](critical-section-debugging-functions.md) utilisent ce membre.</span><span class="sxs-lookup"><span data-stu-id="0bf8e-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) functions use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf8e-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bf8e-109">Requirements</span></span>



| <span data-ttu-id="0bf8e-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bf8e-110">Requirement</span></span> | <span data-ttu-id="0bf8e-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bf8e-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf8e-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bf8e-112">Header</span></span><br/>  | <dl> <span data-ttu-id="0bf8e-113"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bf8e-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0bf8e-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0bf8e-114">Library</span></span><br/> | <dl> <span data-ttu-id="0bf8e-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0bf8e-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bf8e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bf8e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf8e-117">**CCritSec, classe**</span><span class="sxs-lookup"><span data-stu-id="0bf8e-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




