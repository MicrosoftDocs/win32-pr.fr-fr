---
description: 'La méthode GetClassID récupère l’identificateur de classe. Cette méthode implémente la méthode IPersist :: GetClassID.'
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Méthode CBaseMediaFilter. GetClassID (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dafacba684711c5c04a155d2609e0bc68450fa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520818"
---
# <a name="cbasemediafiltergetclassid-method"></a><span data-ttu-id="66e07-104">Méthode CBaseMediaFilter. GetClassID</span><span class="sxs-lookup"><span data-stu-id="66e07-104">CBaseMediaFilter.GetClassID method</span></span>

<span data-ttu-id="66e07-105">La `GetClassID` méthode récupère l’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="66e07-105">The `GetClassID` method retrieves the class identifier.</span></span> <span data-ttu-id="66e07-106">Cette méthode implémente la méthode **IPersist :: GetClassID** .</span><span class="sxs-lookup"><span data-stu-id="66e07-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="66e07-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66e07-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="66e07-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66e07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66e07-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="66e07-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="66e07-110">Pointeur vers une variable qui reçoit l’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="66e07-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66e07-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66e07-111">Return value</span></span>

<span data-ttu-id="66e07-112">Retourne le \_ pointeur S ou OK \_ .</span><span class="sxs-lookup"><span data-stu-id="66e07-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e07-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66e07-113">Requirements</span></span>



| <span data-ttu-id="66e07-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66e07-114">Requirement</span></span> | <span data-ttu-id="66e07-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="66e07-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66e07-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="66e07-116">Header</span></span><br/>  | <dl> <span data-ttu-id="66e07-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66e07-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66e07-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="66e07-118">Library</span></span><br/> | <dl> <span data-ttu-id="66e07-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="66e07-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e07-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66e07-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e07-121">**CBaseMediaFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="66e07-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




