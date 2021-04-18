---
description: Utilise la fonction Microsoft Win32 SetThreadPriority pour définir la priorité du thread sur une nouvelle valeur.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: CMsgThread. SetThreadPriority, méthode (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540087"
---
# <a name="cmsgthreadsetthreadpriority-method"></a><span data-ttu-id="d4472-103">CMsgThread. SetThreadPriority, méthode</span><span class="sxs-lookup"><span data-stu-id="d4472-103">CMsgThread.SetThreadPriority method</span></span>

<span data-ttu-id="d4472-104">Utilise la fonction Microsoft Win32 **SetThreadPriority** pour définir la priorité du thread sur une nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="d4472-104">Uses the Microsoft Win32 **SetThreadPriority** function to set the priority of the thread to a new value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4472-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4472-105">Syntax</span></span>


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a><span data-ttu-id="d4472-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4472-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4472-107">*nPriority*</span><span class="sxs-lookup"><span data-stu-id="d4472-107">*nPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="d4472-108">Priorité du thread.</span><span class="sxs-lookup"><span data-stu-id="d4472-108">Priority of the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4472-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4472-109">Return value</span></span>

<span data-ttu-id="d4472-110">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d4472-110">Returns one of the following values.</span></span>



| <span data-ttu-id="d4472-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d4472-111">Return code</span></span>                                                                              | <span data-ttu-id="d4472-112">Description</span><span class="sxs-lookup"><span data-stu-id="d4472-112">Description</span></span>                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d4472-113"><dt>VRAI \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="d4472-114">La priorité a été correctement définie.</span><span class="sxs-lookup"><span data-stu-id="d4472-114">Priority was successfully set.</span></span><br/> |
| <dl> <span data-ttu-id="d4472-115"><dt>FALSe \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="d4472-116">La priorité n’a pas été définie.</span><span class="sxs-lookup"><span data-stu-id="d4472-116">Priority was not set.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="d4472-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d4472-117">Remarks</span></span>

<span data-ttu-id="d4472-118">Le client et le thread de travail peuvent appeler cette fonction membre.</span><span class="sxs-lookup"><span data-stu-id="d4472-118">The client and the worker thread can call this member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4472-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4472-119">Requirements</span></span>



| <span data-ttu-id="d4472-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4472-120">Requirement</span></span> | <span data-ttu-id="d4472-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4472-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4472-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4472-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d4472-123"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-123"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4472-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4472-124">Library</span></span><br/> | <dl> <span data-ttu-id="d4472-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4472-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4472-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4472-127">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="d4472-127">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




