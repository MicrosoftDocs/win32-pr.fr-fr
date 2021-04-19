---
description: L’opérateur = assigne une nouvelle heure de référence. Cette méthode utilise le paramètre *ll* .
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: CRefTime. Operator =, méthode (reftime. h)-ll paramètre
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106537939"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a><span data-ttu-id="b3123-104">CRefTime. Operator =, méthode (reftime. h)-ll paramètre</span><span class="sxs-lookup"><span data-stu-id="b3123-104">CRefTime.operator= method (Reftime.h) - ll parameter</span></span>

<span data-ttu-id="b3123-105">L’opérateur = assigne une nouvelle heure de référence.</span><span class="sxs-lookup"><span data-stu-id="b3123-105">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3123-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3123-106">Syntax</span></span>


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a><span data-ttu-id="b3123-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3123-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3123-108">*ll*</span><span class="sxs-lookup"><span data-stu-id="b3123-108">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="b3123-109">Nouvelle heure de référence, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="b3123-109">New reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3123-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3123-110">Return value</span></span>

<span data-ttu-id="b3123-111">Retourne une référence à l’objet.</span><span class="sxs-lookup"><span data-stu-id="b3123-111">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3123-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3123-112">Requirements</span></span>



| <span data-ttu-id="b3123-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3123-113">Requirement</span></span> | <span data-ttu-id="b3123-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3123-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3123-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3123-115">Header</span></span>  | <span data-ttu-id="b3123-116">Reftime. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="b3123-116">Reftime.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="b3123-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3123-117">Library</span></span> | <span data-ttu-id="b3123-118">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="b3123-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




