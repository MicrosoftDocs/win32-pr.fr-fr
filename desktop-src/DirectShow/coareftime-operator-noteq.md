---
description: Cet opérateur teste l’inégalité entre deux heures de référence.
ms.assetid: c081fff2-d85e-409a-8902-4b2aa2c1fc78
title: COARefTime. Operator ! =, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e93934d7b31715422f2cc091e606b681a57e7f61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526775"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="23afb-103">COARefTime. Operator ! =, méthode</span><span class="sxs-lookup"><span data-stu-id="23afb-103">COARefTime.operator!= method</span></span>

<span data-ttu-id="23afb-104">Cet opérateur teste l’inégalité entre deux heures de référence.</span><span class="sxs-lookup"><span data-stu-id="23afb-104">This operator tests for inequality between two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="23afb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23afb-105">Syntax</span></span>


```C++
BOOL operator!=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="23afb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23afb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23afb-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="23afb-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="23afb-108">Référence à l’objet **COARefTime** à comparer.</span><span class="sxs-lookup"><span data-stu-id="23afb-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23afb-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23afb-109">Return value</span></span>

<span data-ttu-id="23afb-110">Retourne la **valeur true** si les deux objets ne sont pas égaux.</span><span class="sxs-lookup"><span data-stu-id="23afb-110">Returns **TRUE** if the two objects are not equal.</span></span> <span data-ttu-id="23afb-111">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="23afb-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="23afb-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23afb-112">Requirements</span></span>



| <span data-ttu-id="23afb-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23afb-113">Requirement</span></span> | <span data-ttu-id="23afb-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="23afb-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23afb-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="23afb-115">Header</span></span><br/>  | <dl> <span data-ttu-id="23afb-116"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23afb-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="23afb-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="23afb-117">Library</span></span><br/> | <dl> <span data-ttu-id="23afb-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="23afb-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23afb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23afb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23afb-120">**COARefTime, classe**</span><span class="sxs-lookup"><span data-stu-id="23afb-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




