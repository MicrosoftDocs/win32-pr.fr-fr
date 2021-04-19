---
description: Cet opérateur vérifie si une heure de référence est inférieure ou égale à une autre.
ms.assetid: ae7449b7-d319-4e76-892f-0f9ae63ddf94
title: COARefTime. Operator>=, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69b345f42c854e939c21a028827889a03e0ce735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541626"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="39640-103">COARefTime. Operator>=, méthode</span><span class="sxs-lookup"><span data-stu-id="39640-103">COARefTime.operator>= method</span></span>

<span data-ttu-id="39640-104">Cet opérateur vérifie si une heure de référence est inférieure ou égale à une autre.</span><span class="sxs-lookup"><span data-stu-id="39640-104">This operator tests if one reference time is less than or equal to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="39640-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39640-105">Syntax</span></span>


```C++
BOOL operator>=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="39640-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39640-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39640-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="39640-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="39640-108">Référence à l’objet **COARefTime** à comparer.</span><span class="sxs-lookup"><span data-stu-id="39640-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39640-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39640-109">Return value</span></span>

<span data-ttu-id="39640-110">Retourne la **valeur true** si cet objet est inférieur ou égal à *RT*.</span><span class="sxs-lookup"><span data-stu-id="39640-110">Returns **TRUE** if this object is less than or equal to *rt*.</span></span> <span data-ttu-id="39640-111">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="39640-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="39640-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39640-112">Requirements</span></span>



| <span data-ttu-id="39640-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39640-113">Requirement</span></span> | <span data-ttu-id="39640-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="39640-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39640-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="39640-115">Header</span></span><br/>  | <dl> <span data-ttu-id="39640-116"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39640-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="39640-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="39640-117">Library</span></span><br/> | <dl> <span data-ttu-id="39640-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="39640-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39640-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39640-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39640-120">**COARefTime, classe**</span><span class="sxs-lookup"><span data-stu-id="39640-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




