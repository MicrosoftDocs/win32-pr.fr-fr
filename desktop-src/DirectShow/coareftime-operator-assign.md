---
description: Cet opérateur affecte une nouvelle heure de référence.
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: COARefTime. Operator =, méthode (Ctlutil. h)
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
ms.openlocfilehash: 3f5a051cea555975fd8606c3693d4b7d63cb9ce4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528899"
---
# <a name="coareftimeoperator-method-ctlutilh"></a><span data-ttu-id="d81c6-103">COARefTime. Operator =, méthode (Ctlutil. h)</span><span class="sxs-lookup"><span data-stu-id="d81c6-103">COARefTime.operator= method (Ctlutil.h)</span></span>

<span data-ttu-id="d81c6-104">Cet opérateur affecte une nouvelle heure de référence.</span><span class="sxs-lookup"><span data-stu-id="d81c6-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="d81c6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d81c6-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a><span data-ttu-id="d81c6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d81c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d81c6-107">*services Bureau à distance* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="d81c6-107">*rd* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d81c6-108">Référence à une valeur **double** qui spécifie la nouvelle durée de référence en secondes.</span><span class="sxs-lookup"><span data-stu-id="d81c6-108">Reference to a **double** value that specifies the new reference time in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d81c6-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d81c6-109">Return value</span></span>

<span data-ttu-id="d81c6-110">Retourne une référence à l’objet.</span><span class="sxs-lookup"><span data-stu-id="d81c6-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d81c6-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d81c6-111">Requirements</span></span>



| <span data-ttu-id="d81c6-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d81c6-112">Requirement</span></span> | <span data-ttu-id="d81c6-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d81c6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81c6-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="d81c6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d81c6-115"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d81c6-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d81c6-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d81c6-116">Library</span></span><br/> | <dl> <span data-ttu-id="d81c6-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d81c6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d81c6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d81c6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d81c6-119">**COARefTime, classe**</span><span class="sxs-lookup"><span data-stu-id="d81c6-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




