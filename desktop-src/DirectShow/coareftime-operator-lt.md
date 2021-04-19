---
description: Cet opérateur vérifie si une heure de référence est inférieure à une autre.
ms.assetid: 709fb861-a836-4a20-8c93-c0e8ab79f377
title: COARefTime. Operator<, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c61403b959f8b5ee19e9ba0d9cd0ab4db54c124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543846"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="ea4b6-103">COARefTime. Operator<, méthode</span><span class="sxs-lookup"><span data-stu-id="ea4b6-103">COARefTime.operator< method</span></span>

<span data-ttu-id="ea4b6-104">Cet opérateur vérifie si une heure de référence est inférieure à une autre.</span><span class="sxs-lookup"><span data-stu-id="ea4b6-104">This operator tests if one reference time is less than another.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4b6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea4b6-105">Syntax</span></span>


```C++
BOOL operator<(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="ea4b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea4b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea4b6-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="ea4b6-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4b6-108">Référence à l’objet **COARefTime** à comparer.</span><span class="sxs-lookup"><span data-stu-id="ea4b6-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea4b6-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea4b6-109">Return value</span></span>

<span data-ttu-id="ea4b6-110">Retourne la **valeur true** si cet objet est strictement inférieur à *RT*.</span><span class="sxs-lookup"><span data-stu-id="ea4b6-110">Returns **TRUE** if this object is strictly less than *rt*.</span></span> <span data-ttu-id="ea4b6-111">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="ea4b6-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea4b6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea4b6-112">Requirements</span></span>



| <span data-ttu-id="ea4b6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea4b6-113">Requirement</span></span> | <span data-ttu-id="ea4b6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea4b6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4b6-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea4b6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ea4b6-116"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea4b6-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ea4b6-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea4b6-117">Library</span></span><br/> | <dl> <span data-ttu-id="ea4b6-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ea4b6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4b6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea4b6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4b6-120">**COARefTime, classe**</span><span class="sxs-lookup"><span data-stu-id="ea4b6-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




