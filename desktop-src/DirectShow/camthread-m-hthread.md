---
description: Handle du thread.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'Membre CAMThread :: m_hThread (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540693"
---
# <a name="camthreadm_hthread-member"></a><span data-ttu-id="f3c12-103">CAMThread :: m \_ hThread, membre</span><span class="sxs-lookup"><span data-stu-id="f3c12-103">CAMThread::m\_hThread member</span></span>

<span data-ttu-id="f3c12-104">Handle du thread.</span><span class="sxs-lookup"><span data-stu-id="f3c12-104">Handle to the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3c12-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3c12-105">Syntax</span></span>


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a><span data-ttu-id="f3c12-106">Notes</span><span class="sxs-lookup"><span data-stu-id="f3c12-106">Remarks</span></span>

<span data-ttu-id="f3c12-107">Cette variable est initialisée avec la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f3c12-107">This variable is initialized as **NULL**.</span></span> <span data-ttu-id="f3c12-108">La méthode [**CAMThread :: Create**](camthread-create.md) définit cette variable sur le handle de thread.</span><span class="sxs-lookup"><span data-stu-id="f3c12-108">The [**CAMThread::Create**](camthread-create.md) method sets this variable to the thread handle.</span></span> <span data-ttu-id="f3c12-109">Pour déterminer si le thread existe, appelez la méthode [**CAMThread :: ThreadExists**](camthread-threadexists.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c12-109">To determine whether the thread exists, call the [**CAMThread::ThreadExists**](camthread-threadexists.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3c12-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3c12-110">Requirements</span></span>



| <span data-ttu-id="f3c12-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3c12-111">Requirement</span></span> | <span data-ttu-id="f3c12-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3c12-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c12-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3c12-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f3c12-114"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3c12-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f3c12-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f3c12-115">Library</span></span><br/> | <dl> <span data-ttu-id="f3c12-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f3c12-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3c12-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3c12-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c12-118">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="f3c12-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




