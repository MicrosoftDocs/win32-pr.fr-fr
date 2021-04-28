---
description: CCritSec. ~ CCritSec, destructeur, méthode de destructeur.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: CCritSec. ~ CCritSec, destructeur (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f282bfe6ea6bca8cb8553572c18cfbc85db6c77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095807"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="1286b-103">CCritSec. ~ CCritSec, destructeur</span><span class="sxs-lookup"><span data-stu-id="1286b-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="1286b-104">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="1286b-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1286b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1286b-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="1286b-106">Notes </span><span class="sxs-lookup"><span data-stu-id="1286b-106">Remarks</span></span>

<span data-ttu-id="1286b-107">Cette méthode appelle la fonction [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) pour supprimer la section critique.</span><span class="sxs-lookup"><span data-stu-id="1286b-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="1286b-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1286b-108">Requirements</span></span>



| <span data-ttu-id="1286b-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1286b-109">Requirement</span></span> | <span data-ttu-id="1286b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="1286b-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1286b-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="1286b-111">Header</span></span><br/>  | <dl> <span data-ttu-id="1286b-112"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1286b-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1286b-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1286b-113">Library</span></span><br/> | <dl> <span data-ttu-id="1286b-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1286b-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1286b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1286b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1286b-116">**CCritSec, classe**</span><span class="sxs-lookup"><span data-stu-id="1286b-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

