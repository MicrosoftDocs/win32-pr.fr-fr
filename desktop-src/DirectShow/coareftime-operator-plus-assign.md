---
description: Cet opérateur ajoute deux heures de référence et définit cet objet sur le résultat.
ms.assetid: 6d29014b-0e31-497e-8326-e3fefc022227
title: COARefTime. Operator + =, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a03d9e98c3c2f2ca09c3f90f2cb0867d976e02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521631"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="86bf3-103">COARefTime. Operator + =, méthode</span><span class="sxs-lookup"><span data-stu-id="86bf3-103">COARefTime.operator+= method</span></span>

<span data-ttu-id="86bf3-104">Cet opérateur ajoute deux heures de référence et définit cet objet sur le résultat.</span><span class="sxs-lookup"><span data-stu-id="86bf3-104">This operator adds two reference times, and sets this object to the result.</span></span>

## <a name="syntax"></a><span data-ttu-id="86bf3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86bf3-105">Syntax</span></span>


```C++
COARefTime& operator+=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="86bf3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86bf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86bf3-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="86bf3-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="86bf3-108">Référence à l’objet **COARefTime** à ajouter.</span><span class="sxs-lookup"><span data-stu-id="86bf3-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86bf3-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86bf3-109">Return value</span></span>

<span data-ttu-id="86bf3-110">Retourne une référence à l’objet.</span><span class="sxs-lookup"><span data-stu-id="86bf3-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="86bf3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86bf3-111">Requirements</span></span>



| <span data-ttu-id="86bf3-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86bf3-112">Requirement</span></span> | <span data-ttu-id="86bf3-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="86bf3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86bf3-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="86bf3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="86bf3-115"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86bf3-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="86bf3-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86bf3-116">Library</span></span><br/> | <dl> <span data-ttu-id="86bf3-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="86bf3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86bf3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86bf3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86bf3-119">**COARefTime, classe**</span><span class="sxs-lookup"><span data-stu-id="86bf3-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




