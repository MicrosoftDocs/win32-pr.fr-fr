---
description: Cet opérateur divise une heure de référence par une valeur.
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: COARefTime. Operator/Method (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e1e4d7b7adb881ac11988a2d2c46946ff6cddcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537776"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="11120-103">COARefTime. Operator/méthode</span><span class="sxs-lookup"><span data-stu-id="11120-103">COARefTime.operator/ method</span></span>

<span data-ttu-id="11120-104">Cet opérateur divise une heure de référence par une valeur.</span><span class="sxs-lookup"><span data-stu-id="11120-104">This operator divides a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="11120-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11120-105">Syntax</span></span>


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="11120-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11120-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11120-107">*l*</span><span class="sxs-lookup"><span data-stu-id="11120-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="11120-108">Division.</span><span class="sxs-lookup"><span data-stu-id="11120-108">Divisor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11120-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11120-109">Return value</span></span>

<span data-ttu-id="11120-110">Retourne un nouvel objet **COARefTime** égal au quotient de cet objet et **l**.</span><span class="sxs-lookup"><span data-stu-id="11120-110">Returns a new **COARefTime** object equal to the quotient of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="11120-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11120-111">Requirements</span></span>



| <span data-ttu-id="11120-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11120-112">Requirement</span></span> | <span data-ttu-id="11120-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="11120-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11120-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="11120-114">Header</span></span><br/>  | <dl> <span data-ttu-id="11120-115"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11120-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="11120-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="11120-116">Library</span></span><br/> | <dl> <span data-ttu-id="11120-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="11120-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11120-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11120-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11120-119">**COARefTime, classe**</span><span class="sxs-lookup"><span data-stu-id="11120-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




