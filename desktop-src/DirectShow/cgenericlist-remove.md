---
description: La méthode Remove supprime l’élément à la position spécifiée.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: CGenericList. Remove, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530331"
---
# <a name="cgenericlistremove-method"></a><span data-ttu-id="4775a-103">CGenericList. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="4775a-103">CGenericList.Remove method</span></span>

<span data-ttu-id="4775a-104">La `Remove` méthode supprime l’élément à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4775a-104">The `Remove` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="4775a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4775a-105">Syntax</span></span>


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="4775a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4775a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4775a-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="4775a-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="4775a-108">Valeur de POSITION indiquant l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="4775a-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4775a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4775a-109">Return value</span></span>

<span data-ttu-id="4775a-110">Retourne un pointeur vers un objet de type **Object** (le type de modèle).</span><span class="sxs-lookup"><span data-stu-id="4775a-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="4775a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4775a-111">Remarks</span></span>

<span data-ttu-id="4775a-112">Cette méthode supprime le nœud de la liste, mais ne supprime pas l’élément contenu dans ce nœud.</span><span class="sxs-lookup"><span data-stu-id="4775a-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="4775a-113">Si *pos* a la **valeur null**, la méthode retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4775a-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4775a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4775a-114">Requirements</span></span>



| <span data-ttu-id="4775a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4775a-115">Requirement</span></span> | <span data-ttu-id="4775a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4775a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4775a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="4775a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4775a-118"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4775a-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4775a-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4775a-119">Library</span></span><br/> | <dl> <span data-ttu-id="4775a-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4775a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4775a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4775a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4775a-122">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="4775a-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




