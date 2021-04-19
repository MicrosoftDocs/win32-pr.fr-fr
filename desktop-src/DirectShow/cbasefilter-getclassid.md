---
description: 'La méthode GetClassID récupère l’identificateur de classe du filtre. Cette méthode implémente la méthode IPersist :: GetClassID.'
ms.assetid: c3a8b6ab-b36f-493e-9436-6784e25e2511
title: Méthode CBaseFilter. GetClassID (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02dfe8452da6366454dcc1cfeeed93c379c89bd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524050"
---
# <a name="cbasefiltergetclassid-method"></a><span data-ttu-id="ecb29-104">Méthode CBaseFilter. GetClassID</span><span class="sxs-lookup"><span data-stu-id="ecb29-104">CBaseFilter.GetClassID method</span></span>

<span data-ttu-id="ecb29-105">La `GetClassID` méthode récupère l’identificateur de classe du filtre.</span><span class="sxs-lookup"><span data-stu-id="ecb29-105">The `GetClassID` method retrieves the class identifier of the filter.</span></span> <span data-ttu-id="ecb29-106">Cette méthode implémente la méthode **IPersist :: GetClassID** .</span><span class="sxs-lookup"><span data-stu-id="ecb29-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb29-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecb29-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="ecb29-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecb29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb29-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="ecb29-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="ecb29-110">Pointeur vers une variable qui reçoit l’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="ecb29-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb29-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ecb29-111">Return value</span></span>

<span data-ttu-id="ecb29-112">Retourne le \_ pointeur S ou OK \_ .</span><span class="sxs-lookup"><span data-stu-id="ecb29-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb29-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecb29-113">Requirements</span></span>



| <span data-ttu-id="ecb29-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecb29-114">Requirement</span></span> | <span data-ttu-id="ecb29-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecb29-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb29-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecb29-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ecb29-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecb29-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ecb29-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ecb29-118">Library</span></span><br/> | <dl> <span data-ttu-id="ecb29-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ecb29-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb29-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecb29-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb29-121">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="ecb29-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




