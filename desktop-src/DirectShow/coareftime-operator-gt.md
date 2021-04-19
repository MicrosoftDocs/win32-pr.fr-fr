---
description: Cet opérateur vérifie si une heure de référence est supérieure à une autre.
ms.assetid: db281040-9bcf-41fc-95b4-5481ffc5061f
title: COARefTime. Operator>, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c796bd5194c5bdb2dcbe260b803274962f81347
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545955"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="bf72f-103">COARefTime. Operator>, méthode</span><span class="sxs-lookup"><span data-stu-id="bf72f-103">COARefTime.operator> method</span></span>

<span data-ttu-id="bf72f-104">Cet opérateur vérifie si une heure de référence est supérieure à une autre.</span><span class="sxs-lookup"><span data-stu-id="bf72f-104">This operator tests if one reference time is greater than another.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf72f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf72f-105">Syntax</span></span>


```C++
BOOL operator>(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="bf72f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf72f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf72f-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="bf72f-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="bf72f-108">Référence à l’objet **COARefTime** à comparer.</span><span class="sxs-lookup"><span data-stu-id="bf72f-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf72f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf72f-109">Return value</span></span>

<span data-ttu-id="bf72f-110">Retourne la **valeur true** si cet objet est strictement supérieur à *RT*.</span><span class="sxs-lookup"><span data-stu-id="bf72f-110">Returns **TRUE** if this object is strictly greater than *rt*.</span></span> <span data-ttu-id="bf72f-111">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="bf72f-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf72f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf72f-112">Requirements</span></span>



| <span data-ttu-id="bf72f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf72f-113">Requirement</span></span> | <span data-ttu-id="bf72f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf72f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf72f-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf72f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="bf72f-116"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf72f-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf72f-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bf72f-117">Library</span></span><br/> | <dl> <span data-ttu-id="bf72f-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bf72f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf72f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf72f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf72f-120">**COARefTime, classe**</span><span class="sxs-lookup"><span data-stu-id="bf72f-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




