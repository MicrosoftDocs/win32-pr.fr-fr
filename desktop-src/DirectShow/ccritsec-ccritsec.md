---
description: Méthode constructeur CCritSec. CCritSec.
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
ms.openlocfilehash: de2b852ffc9a12622a4560ae834a3347b1e07552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119797"
---
# <a name="ccritsecccritsec-constructor"></a><span data-ttu-id="a3970-103">Constructeur CCritSec. CCritSec</span><span class="sxs-lookup"><span data-stu-id="a3970-103">CCritSec.CCritSec constructor</span></span>

<span data-ttu-id="a3970-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="a3970-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3970-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3970-105">Syntax</span></span>


```C++
CCritSec();
```



## <a name="parameters"></a><span data-ttu-id="a3970-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3970-106">Parameters</span></span>

<span data-ttu-id="a3970-107">Ce constructeur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a3970-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3970-108">Notes </span><span class="sxs-lookup"><span data-stu-id="a3970-108">Remarks</span></span>

<span data-ttu-id="a3970-109">Cette méthode appelle la fonction [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) pour initialiser la section critique.</span><span class="sxs-lookup"><span data-stu-id="a3970-109">This method calls the [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) function to initialize the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3970-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3970-110">Requirements</span></span>



| <span data-ttu-id="a3970-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3970-111">Requirement</span></span> | <span data-ttu-id="a3970-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3970-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3970-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3970-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a3970-114"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3970-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a3970-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a3970-115">Library</span></span><br/> | <dl> <span data-ttu-id="a3970-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a3970-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3970-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3970-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3970-118">**CCritSec, classe**</span><span class="sxs-lookup"><span data-stu-id="a3970-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

