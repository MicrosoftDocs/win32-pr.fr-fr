---
description: La méthode RemoveTail supprime le dernier élément de la liste.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Méthode CGenericList. RemoveTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7b98187c663f643acdce28b4f12ebc37b1d4c25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543826"
---
# <a name="cgenericlistremovetail-method"></a><span data-ttu-id="65f5b-103">Méthode CGenericList. RemoveTail</span><span class="sxs-lookup"><span data-stu-id="65f5b-103">CGenericList.RemoveTail method</span></span>

<span data-ttu-id="65f5b-104">La `RemoveTail` méthode supprime le dernier élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="65f5b-104">The `RemoveTail` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f5b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65f5b-105">Syntax</span></span>


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a><span data-ttu-id="65f5b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65f5b-106">Parameters</span></span>

<span data-ttu-id="65f5b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="65f5b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65f5b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65f5b-108">Return value</span></span>

<span data-ttu-id="65f5b-109">Retourne un pointeur vers un objet de type **Object** (le type de modèle), ou **null** si la liste est vide.</span><span class="sxs-lookup"><span data-stu-id="65f5b-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="65f5b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="65f5b-110">Remarks</span></span>

<span data-ttu-id="65f5b-111">Cette méthode supprime le nœud de liste, mais pas l’élément contenu dans le nœud.</span><span class="sxs-lookup"><span data-stu-id="65f5b-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="65f5b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65f5b-112">Requirements</span></span>



| <span data-ttu-id="65f5b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65f5b-113">Requirement</span></span> | <span data-ttu-id="65f5b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="65f5b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f5b-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="65f5b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="65f5b-116"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65f5b-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="65f5b-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65f5b-117">Library</span></span><br/> | <dl> <span data-ttu-id="65f5b-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="65f5b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65f5b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65f5b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f5b-120">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="65f5b-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




