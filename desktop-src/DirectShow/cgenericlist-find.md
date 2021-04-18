---
description: La méthode Find récupère la première position qui contient l’élément spécifié.
ms.assetid: 8e2a3e5d-96e6-4f40-8e2a-4dc8c21088cd
title: CGenericList. Find, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Find
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a21f16e25d8a2ebba4494a850bc456a7b579f2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526753"
---
# <a name="cgenericlistfind-method"></a><span data-ttu-id="8c651-103">CGenericList. Find, méthode</span><span class="sxs-lookup"><span data-stu-id="8c651-103">CGenericList.Find method</span></span>

<span data-ttu-id="8c651-104">La `Find` méthode récupère la première position qui contient l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="8c651-104">The `Find` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c651-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c651-105">Syntax</span></span>


```C++
POSITION Find(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="8c651-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c651-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c651-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="8c651-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="8c651-108">Pointeur vers un objet de type **Object** (type de modèle).</span><span class="sxs-lookup"><span data-stu-id="8c651-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c651-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c651-109">Return value</span></span>

<span data-ttu-id="8c651-110">Retourne une valeur de POSITION, ou **null** si l’élément n’est pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="8c651-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c651-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c651-111">Requirements</span></span>



| <span data-ttu-id="8c651-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c651-112">Requirement</span></span> | <span data-ttu-id="8c651-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c651-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c651-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c651-114">Header</span></span><br/>  | <dl> <span data-ttu-id="8c651-115"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c651-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8c651-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c651-116">Library</span></span><br/> | <dl> <span data-ttu-id="8c651-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8c651-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c651-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c651-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c651-119">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="8c651-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




