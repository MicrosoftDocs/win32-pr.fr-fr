---
description: La méthode obtenir récupère l’élément à la position spécifiée.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: CGenericList. obten, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537550"
---
# <a name="cgenericlistget-method"></a><span data-ttu-id="cb34d-103">CGenericList. obten, méthode</span><span class="sxs-lookup"><span data-stu-id="cb34d-103">CGenericList.Get method</span></span>

<span data-ttu-id="cb34d-104">La `Get` méthode récupère l’élément à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cb34d-104">The `Get` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb34d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb34d-105">Syntax</span></span>


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="cb34d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb34d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb34d-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="cb34d-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="cb34d-108">Indicateur de position de l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="cb34d-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb34d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb34d-109">Return value</span></span>

<span data-ttu-id="cb34d-110">Retourne un pointeur vers un objet de type **Object** (le type de modèle).</span><span class="sxs-lookup"><span data-stu-id="cb34d-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb34d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cb34d-111">Remarks</span></span>

<span data-ttu-id="cb34d-112">Si *pos* a la **valeur null**, la méthode retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cb34d-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb34d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb34d-113">Requirements</span></span>



| <span data-ttu-id="cb34d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb34d-114">Requirement</span></span> | <span data-ttu-id="cb34d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb34d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb34d-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb34d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cb34d-117"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb34d-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cb34d-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb34d-118">Library</span></span><br/> | <dl> <span data-ttu-id="cb34d-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cb34d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb34d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb34d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb34d-121">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="cb34d-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




