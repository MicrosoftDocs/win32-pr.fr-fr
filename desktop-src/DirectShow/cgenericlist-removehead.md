---
description: La méthode RemoveHead supprime le premier élément de la liste.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Méthode CGenericList. RemoveHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da9267d6b3e0c3196b3a9d1e873f222649b66684
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533131"
---
# <a name="cgenericlistremovehead-method"></a><span data-ttu-id="679f0-103">Méthode CGenericList. RemoveHead</span><span class="sxs-lookup"><span data-stu-id="679f0-103">CGenericList.RemoveHead method</span></span>

<span data-ttu-id="679f0-104">La `RemoveHead` méthode supprime le premier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="679f0-104">The `RemoveHead` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="679f0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="679f0-105">Syntax</span></span>


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a><span data-ttu-id="679f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="679f0-106">Parameters</span></span>

<span data-ttu-id="679f0-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="679f0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="679f0-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="679f0-108">Return value</span></span>

<span data-ttu-id="679f0-109">Retourne un pointeur vers un objet de type **Object** (le type de modèle), ou **null** si la liste est vide.</span><span class="sxs-lookup"><span data-stu-id="679f0-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="679f0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="679f0-110">Remarks</span></span>

<span data-ttu-id="679f0-111">Cette méthode supprime le nœud de liste, mais pas l’élément contenu dans le nœud.</span><span class="sxs-lookup"><span data-stu-id="679f0-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="679f0-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="679f0-112">Requirements</span></span>



| <span data-ttu-id="679f0-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="679f0-113">Requirement</span></span> | <span data-ttu-id="679f0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="679f0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="679f0-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="679f0-115">Header</span></span><br/>  | <dl> <span data-ttu-id="679f0-116"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="679f0-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="679f0-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="679f0-117">Library</span></span><br/> | <dl> <span data-ttu-id="679f0-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="679f0-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="679f0-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="679f0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="679f0-120">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="679f0-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




