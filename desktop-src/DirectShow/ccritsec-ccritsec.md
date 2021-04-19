---
description: Méthode de constructeur.
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Constructeur CCritSec. CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6baeadace7c1f8d8d3ad5dee1ff5c9dace1c6907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541545"
---
# <a name="ccritsecccritsec-constructor"></a><span data-ttu-id="4dec2-103">Constructeur CCritSec. CCritSec</span><span class="sxs-lookup"><span data-stu-id="4dec2-103">CCritSec.CCritSec constructor</span></span>

<span data-ttu-id="4dec2-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="4dec2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dec2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4dec2-105">Syntax</span></span>


```C++
CCritSec();
```



## <a name="parameters"></a><span data-ttu-id="4dec2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4dec2-106">Parameters</span></span>

<span data-ttu-id="4dec2-107">Ce constructeur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4dec2-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dec2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="4dec2-108">Remarks</span></span>

<span data-ttu-id="4dec2-109">Cette méthode appelle la fonction [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) pour initialiser la section critique.</span><span class="sxs-lookup"><span data-stu-id="4dec2-109">This method calls the [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) function to initialize the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dec2-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4dec2-110">Requirements</span></span>



| <span data-ttu-id="4dec2-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4dec2-111">Requirement</span></span> | <span data-ttu-id="4dec2-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4dec2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dec2-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="4dec2-113">Header</span></span><br/>  | <dl> <span data-ttu-id="4dec2-114"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4dec2-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4dec2-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4dec2-115">Library</span></span><br/> | <dl> <span data-ttu-id="4dec2-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4dec2-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dec2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4dec2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dec2-118">**CCritSec, classe**</span><span class="sxs-lookup"><span data-stu-id="4dec2-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

