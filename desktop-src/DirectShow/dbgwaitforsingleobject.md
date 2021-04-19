---
description: Attend qu’un objet soit signalé.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: DbgWaitForSingleObject, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521762"
---
# <a name="dbgwaitforsingleobject-function"></a><span data-ttu-id="2075a-103">DbgWaitForSingleObject fonction)</span><span class="sxs-lookup"><span data-stu-id="2075a-103">DbgWaitForSingleObject function</span></span>

<span data-ttu-id="2075a-104">Attend qu’un objet soit signalé.</span><span class="sxs-lookup"><span data-stu-id="2075a-104">Waits for an object to become signaled.</span></span>

<span data-ttu-id="2075a-105">Dans une version Debug, cette fonction déclenche une assertion si l’intervalle de délai d’attente expire avant que l’objet soit signalé.</span><span class="sxs-lookup"><span data-stu-id="2075a-105">In a debug build, this function triggers an assert if the time-out interval expires before the object is signaled.</span></span> <span data-ttu-id="2075a-106">Pour définir l’intervalle de délai d’attente, appelez la fonction [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="2075a-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="2075a-107">Dans une version commerciale, cette fonction est équivalente à la fonction **WaitForSingleObject** avec un intervalle de délai d’attente infini.</span><span class="sxs-lookup"><span data-stu-id="2075a-107">In a retail build, this function is equivalent to the **WaitForSingleObject** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="2075a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2075a-108">Syntax</span></span>


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a><span data-ttu-id="2075a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2075a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2075a-110">*h*</span><span class="sxs-lookup"><span data-stu-id="2075a-110">*h*</span></span> 
</dt> <dd>

<span data-ttu-id="2075a-111">Handle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2075a-111">Handle to the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2075a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2075a-112">Requirements</span></span>



| <span data-ttu-id="2075a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2075a-113">Requirement</span></span> | <span data-ttu-id="2075a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2075a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2075a-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="2075a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2075a-116"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2075a-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2075a-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2075a-117">Library</span></span><br/> | <dl> <span data-ttu-id="2075a-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2075a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2075a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2075a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2075a-120">Fonctions de débogage d’attente</span><span class="sxs-lookup"><span data-stu-id="2075a-120">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




