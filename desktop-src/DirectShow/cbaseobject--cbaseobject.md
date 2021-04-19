---
description: Méthode de destructeur.
ms.assetid: 3714d030-f0bd-4826-a3c5-fc206bb88561
title: CBaseObject. ~ CBaseObject, destructeur (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.~CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 908f335105fa88f3ed547eed0e92ea50a6f85f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539579"
---
# <a name="cbaseobjectcbaseobject-destructor"></a><span data-ttu-id="82dca-103">CBaseObject. ~ CBaseObject, destructeur</span><span class="sxs-lookup"><span data-stu-id="82dca-103">CBaseObject.~CBaseObject destructor</span></span>

<span data-ttu-id="82dca-104">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="82dca-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="82dca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82dca-105">Syntax</span></span>


```C++
~CBaseObject();
```



## <a name="remarks"></a><span data-ttu-id="82dca-106">Notes</span><span class="sxs-lookup"><span data-stu-id="82dca-106">Remarks</span></span>

<span data-ttu-id="82dca-107">Cette méthode décrémente le nombre d’objets actifs.</span><span class="sxs-lookup"><span data-stu-id="82dca-107">This method decrements the active-object count.</span></span> <span data-ttu-id="82dca-108">(Voir [**CBaseObject :: ObjectsActive**](cbaseobject-objectsactive.md).)</span><span class="sxs-lookup"><span data-stu-id="82dca-108">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="82dca-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82dca-109">Requirements</span></span>



| <span data-ttu-id="82dca-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82dca-110">Requirement</span></span> | <span data-ttu-id="82dca-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="82dca-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82dca-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="82dca-112">Header</span></span><br/>  | <dl> <span data-ttu-id="82dca-113"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82dca-113"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="82dca-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="82dca-114">Library</span></span><br/> | <dl> <span data-ttu-id="82dca-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="82dca-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82dca-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82dca-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82dca-117">**CBaseObject, classe**</span><span class="sxs-lookup"><span data-stu-id="82dca-117">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




