---
description: L' \_ opérateur de temps de référence () convertit l’objet en un type de données de temps de référence \_ .
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: CRefTime. Operator REFERENCE_TIME, méthode (reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538120"
---
# <a name="creftimeoperator-reference_time-method"></a><span data-ttu-id="0ea2b-103">CRefTime. Operator Time, méthode de référence \_</span><span class="sxs-lookup"><span data-stu-id="0ea2b-103">CRefTime.operator REFERENCE\_TIME method</span></span>

<span data-ttu-id="0ea2b-104">L' `REFERENCE_TIME()` opérateur convertit l’objet en un type de données de [**\_ temps de référence**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="0ea2b-104">The `REFERENCE_TIME()` operator casts the object to a [**REFERENCE\_TIME**](reference-time.md) data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ea2b-105">Syntax</span></span>


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a><span data-ttu-id="0ea2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ea2b-106">Parameters</span></span>

<span data-ttu-id="0ea2b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0ea2b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ea2b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ea2b-108">Return value</span></span>

<span data-ttu-id="0ea2b-109">Retourne la valeur de [**CRefTime :: m \_ Time**](creftime-m-time.md).</span><span class="sxs-lookup"><span data-stu-id="0ea2b-109">Returns the value of [**CRefTime::m\_time**](creftime-m-time.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ea2b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0ea2b-110">Remarks</span></span>

<span data-ttu-id="0ea2b-111">L’exemple suivant montre comment utiliser cet opérateur de conversion :</span><span class="sxs-lookup"><span data-stu-id="0ea2b-111">The following example shows how to use this cast operator:</span></span>


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a><span data-ttu-id="0ea2b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ea2b-112">Requirements</span></span>



| <span data-ttu-id="0ea2b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ea2b-113">Requirement</span></span> | <span data-ttu-id="0ea2b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ea2b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea2b-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ea2b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="0ea2b-116"><dt>Reftime. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ea2b-116"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ea2b-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0ea2b-117">Library</span></span><br/> | <dl> <span data-ttu-id="0ea2b-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0ea2b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




