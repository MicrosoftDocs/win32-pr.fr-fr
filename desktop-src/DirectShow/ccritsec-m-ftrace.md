---
description: Valeur booléenne qui spécifie s’il faut tracer ce verrou.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Membre CCritSec :: m_fTrace (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541734"
---
# <a name="ccritsecm_ftrace-member"></a><span data-ttu-id="21fb6-103">CCritSec :: m \_ fTrace, membre</span><span class="sxs-lookup"><span data-stu-id="21fb6-103">CCritSec::m\_fTrace member</span></span>

<span data-ttu-id="21fb6-104">Valeur booléenne qui spécifie s’il faut tracer ce verrou.</span><span class="sxs-lookup"><span data-stu-id="21fb6-104">Boolean value that specifies whether to trace this lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="21fb6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21fb6-105">Syntax</span></span>


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a><span data-ttu-id="21fb6-106">Notes</span><span class="sxs-lookup"><span data-stu-id="21fb6-106">Remarks</span></span>

<span data-ttu-id="21fb6-107">Cette variable membre est définie uniquement dans la version Debug de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="21fb6-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="21fb6-108">Si la valeur est **true**, une trace de l’état du verrou est écrite dans le journal de débogage.</span><span class="sxs-lookup"><span data-stu-id="21fb6-108">If the value is **TRUE**, a trace of the lock state is written to the debug log.</span></span> <span data-ttu-id="21fb6-109">(La journalisation du débogage des sections critiques doit être active.) Pour plus d’informations, consultez [**DbgLockTrace**](dbglocktrace.md).</span><span class="sxs-lookup"><span data-stu-id="21fb6-109">(Debug logging for critical sections must be active.) For more information, see [**DbgLockTrace**](dbglocktrace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21fb6-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21fb6-110">Requirements</span></span>



| <span data-ttu-id="21fb6-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21fb6-111">Requirement</span></span> | <span data-ttu-id="21fb6-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="21fb6-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21fb6-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="21fb6-113">Header</span></span><br/>  | <dl> <span data-ttu-id="21fb6-114"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21fb6-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="21fb6-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="21fb6-115">Library</span></span><br/> | <dl> <span data-ttu-id="21fb6-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="21fb6-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21fb6-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21fb6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21fb6-118">**CCritSec, classe**</span><span class="sxs-lookup"><span data-stu-id="21fb6-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




