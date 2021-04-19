---
description: La fonction WaitDispatchingMessages attend qu’un objet soit signalé, tout en distribuant les messages de fenêtre.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: WaitDispatchingMessages, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540237"
---
# <a name="waitdispatchingmessages-function"></a><span data-ttu-id="8c261-103">WaitDispatchingMessages fonction)</span><span class="sxs-lookup"><span data-stu-id="8c261-103">WaitDispatchingMessages function</span></span>

<span data-ttu-id="8c261-104">La `WaitDispatchingMessages` fonction attend qu’un objet soit signalé, tout en distribuant les messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8c261-104">The `WaitDispatchingMessages` function waits for an object to be signaled, while dispatching window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c261-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c261-105">Syntax</span></span>


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="8c261-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c261-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c261-107">*hObject*</span><span class="sxs-lookup"><span data-stu-id="8c261-107">*hObject*</span></span> 
</dt> <dd>

<span data-ttu-id="8c261-108">Handle de l’objet à attendre.</span><span class="sxs-lookup"><span data-stu-id="8c261-108">Handle of the object to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="8c261-109">*dwWait*</span><span class="sxs-lookup"><span data-stu-id="8c261-109">*dwWait*</span></span> 
</dt> <dd>

<span data-ttu-id="8c261-110">Intervalle de délai d’attente, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="8c261-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="8c261-111">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8c261-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8c261-112">Handle facultatif vers une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8c261-112">Optional handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="8c261-113">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="8c261-113">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="8c261-114">Message de fenêtre facultatif, en spécifiant un message à distribuer.</span><span class="sxs-lookup"><span data-stu-id="8c261-114">Optional window message, specifying a message to dispatch.</span></span>

</dd> <dt>

<span data-ttu-id="8c261-115">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="8c261-115">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="8c261-116">Handle facultatif d’un événement à attendre.</span><span class="sxs-lookup"><span data-stu-id="8c261-116">Optional handle to an event to wait for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c261-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c261-117">Return value</span></span>

<span data-ttu-id="8c261-118">Retourne la valeur de la fonction **WaitForMultipleObjects** .</span><span class="sxs-lookup"><span data-stu-id="8c261-118">Returns the value from the **WaitForMultipleObjects** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c261-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8c261-119">Remarks</span></span>

<span data-ttu-id="8c261-120">Si un objet possède une fenêtre, il doit distribuer les messages de fenêtre en attente.</span><span class="sxs-lookup"><span data-stu-id="8c261-120">If an object owns a window, it should dispatch window messages while waiting.</span></span> <span data-ttu-id="8c261-121">Cette fonction permet à l’objet d’attendre un événement, un sémaphore ou un autre objet d’exclusion mutuelle lors de la distribution des messages.</span><span class="sxs-lookup"><span data-stu-id="8c261-121">This function enables the object to wait for an event, semaphore, or other mutual exclusion object while dispatching messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c261-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c261-122">Requirements</span></span>



| <span data-ttu-id="8c261-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c261-123">Requirement</span></span> | <span data-ttu-id="8c261-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c261-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c261-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c261-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8c261-126"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c261-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8c261-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c261-127">Library</span></span><br/> | <dl> <span data-ttu-id="8c261-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8c261-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c261-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c261-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c261-130">Fonctions d’assistance diverses</span><span class="sxs-lookup"><span data-stu-id="8c261-130">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




