---
description: L’opérateur assigne une nouvelle heure de référence et utilise le paramètre « RT [ref] ».
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: COARefTime. Operator = méthode (Ctlutil. h)-RT [ref], paramètre
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106544410"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a><span data-ttu-id="96ec5-103">COARefTime. Operator = méthode (Ctlutil. h)-RT [ref], paramètre</span><span class="sxs-lookup"><span data-stu-id="96ec5-103">COARefTime.operator= method (Ctlutil.h) - rt [ref] parameter</span></span>

<span data-ttu-id="96ec5-104">Cet opérateur affecte une nouvelle heure de référence.</span><span class="sxs-lookup"><span data-stu-id="96ec5-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ec5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96ec5-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a><span data-ttu-id="96ec5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96ec5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ec5-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="96ec5-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="96ec5-108">Référence à une valeur de [**\_ temps de référence**](reference-time.md) qui spécifie la nouvelle durée de référence en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="96ec5-108">Reference to a [**REFERENCE\_TIME**](reference-time.md) value that specifies the new reference time in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ec5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96ec5-109">Return value</span></span>

<span data-ttu-id="96ec5-110">Retourne une référence à l’objet.</span><span class="sxs-lookup"><span data-stu-id="96ec5-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="96ec5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96ec5-111">Requirements</span></span>

| <span data-ttu-id="96ec5-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96ec5-112">Requirement</span></span>                    | <span data-ttu-id="96ec5-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="96ec5-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96ec5-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="96ec5-114">Header</span></span>  | <span data-ttu-id="96ec5-115">Ctlutil. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="96ec5-115">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="96ec5-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="96ec5-116">Library</span></span> | <span data-ttu-id="96ec5-117">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="96ec5-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="96ec5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96ec5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ec5-119">**COARefTime, classe**</span><span class="sxs-lookup"><span data-stu-id="96ec5-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




