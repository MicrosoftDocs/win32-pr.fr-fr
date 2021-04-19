---
description: Cet opérateur soustrait une heure de référence d’une autre.
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: COARefTime. Operator-Method (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e51ee8aaed69830a498d1d22cebdc3927987f045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535973"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="af52b-103">COARefTime. Operator-méthode</span><span class="sxs-lookup"><span data-stu-id="af52b-103">COARefTime.operator- method</span></span>

<span data-ttu-id="af52b-104">Cet opérateur soustrait une heure de référence d’une autre.</span><span class="sxs-lookup"><span data-stu-id="af52b-104">This operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="af52b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af52b-105">Syntax</span></span>


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="af52b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af52b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af52b-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="af52b-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="af52b-108">Référence à l’objet **COARefTime** à soustraire.</span><span class="sxs-lookup"><span data-stu-id="af52b-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af52b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af52b-109">Return value</span></span>

<span data-ttu-id="af52b-110">Retourne un nouvel objet **COARefTime** égal à la différence entre les temps de référence.</span><span class="sxs-lookup"><span data-stu-id="af52b-110">Returns a new **COARefTime** object equal to the difference of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="af52b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af52b-111">Requirements</span></span>



| <span data-ttu-id="af52b-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af52b-112">Requirement</span></span> | <span data-ttu-id="af52b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="af52b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af52b-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="af52b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="af52b-115"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af52b-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="af52b-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af52b-116">Library</span></span><br/> | <dl> <span data-ttu-id="af52b-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="af52b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af52b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af52b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af52b-119">**COARefTime, classe**</span><span class="sxs-lookup"><span data-stu-id="af52b-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




