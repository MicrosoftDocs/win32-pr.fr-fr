---
description: Cet opérateur soustrait une heure de référence d’une autre et définit cet objet sur le résultat.
ms.assetid: 573b6f6b-7634-4e78-872c-f869b59a75e2
title: COARefTime. Operator-=, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29afc98da01351f63df45997b8cc338e17a1234c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543247"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="f2429-103">COARefTime. Operator-= méthode</span><span class="sxs-lookup"><span data-stu-id="f2429-103">COARefTime.operator-= method</span></span>

<span data-ttu-id="f2429-104">Cet opérateur soustrait une heure de référence d’une autre et définit cet objet sur le résultat.</span><span class="sxs-lookup"><span data-stu-id="f2429-104">This operator subtracts one reference time from another, and sets this object to the result.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2429-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2429-105">Syntax</span></span>


```C++
COARefTime& operator-=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="f2429-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2429-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2429-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="f2429-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f2429-108">Référence à l’objet **COARefTime** à soustraire.</span><span class="sxs-lookup"><span data-stu-id="f2429-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2429-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2429-109">Return value</span></span>

<span data-ttu-id="f2429-110">Retourne une référence à l’objet.</span><span class="sxs-lookup"><span data-stu-id="f2429-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2429-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2429-111">Requirements</span></span>



| <span data-ttu-id="f2429-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2429-112">Requirement</span></span> | <span data-ttu-id="f2429-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2429-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2429-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2429-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f2429-115"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2429-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2429-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f2429-116">Library</span></span><br/> | <dl> <span data-ttu-id="f2429-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f2429-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2429-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2429-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2429-119">**COARefTime, classe**</span><span class="sxs-lookup"><span data-stu-id="f2429-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




