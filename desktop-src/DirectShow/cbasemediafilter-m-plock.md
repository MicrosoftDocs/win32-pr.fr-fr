---
description: Pointeur vers une section critique.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'Membre CBaseMediaFilter :: m_pLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531002"
---
# <a name="cbasemediafilterm_plock-member"></a><span data-ttu-id="b709f-103">CBaseMediaFilter :: m \_ pLock, membre</span><span class="sxs-lookup"><span data-stu-id="b709f-103">CBaseMediaFilter::m\_pLock member</span></span>

<span data-ttu-id="b709f-104">Pointeur vers une section critique.</span><span class="sxs-lookup"><span data-stu-id="b709f-104">Pointer to a critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="b709f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b709f-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="b709f-106">Notes</span><span class="sxs-lookup"><span data-stu-id="b709f-106">Remarks</span></span>

<span data-ttu-id="b709f-107">La section critique est conservée lors des transitions d’État ([**CBaseMediaFilter :: Run**](cbasemediafilter-run.md), [**CBaseMediaFilter ::P ause**](cbasemediafilter-pause.md), [**CBaseMediaFilter :: Stop**](cbasemediafilter-stop.md)), lors de l’accès à l’horloge de référence ([**CBaseMediaFilter :: SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter :: GetSyncSource**](cbasemediafilter-getsyncsource.md)) et dans la méthode [**CBaseMediaFilter :: IsActive**](cbasemediafilter-isactive.md) .</span><span class="sxs-lookup"><span data-stu-id="b709f-107">The critical section is held during state transitions ([**CBaseMediaFilter::Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md), [**CBaseMediaFilter::Stop**](cbasemediafilter-stop.md)), when accessing the reference clock ([**CBaseMediaFilter::SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter::GetSyncSource**](cbasemediafilter-getsyncsource.md)), and in the [**CBaseMediaFilter::IsActive**](cbasemediafilter-isactive.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b709f-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b709f-108">Requirements</span></span>



| <span data-ttu-id="b709f-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b709f-109">Requirement</span></span> | <span data-ttu-id="b709f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b709f-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b709f-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="b709f-111">Header</span></span><br/>  | <dl> <span data-ttu-id="b709f-112"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b709f-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b709f-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b709f-113">Library</span></span><br/> | <dl> <span data-ttu-id="b709f-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b709f-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b709f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b709f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b709f-116">**CBaseMediaFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="b709f-116">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




