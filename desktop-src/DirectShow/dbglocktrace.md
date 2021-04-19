---
description: Active ou désactive la journalisation du débogage d’une section critique donnée.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: DbgLockTrace, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525452"
---
# <a name="dbglocktrace-function"></a><span data-ttu-id="b4416-103">DbgLockTrace fonction)</span><span class="sxs-lookup"><span data-stu-id="b4416-103">DbgLockTrace function</span></span>

<span data-ttu-id="b4416-104">Active ou désactive la journalisation du débogage d’une section critique donnée.</span><span class="sxs-lookup"><span data-stu-id="b4416-104">Enables or disables debug logging of a given critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4416-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4416-105">Syntax</span></span>


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a><span data-ttu-id="b4416-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4416-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4416-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="b4416-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="b4416-108">Pointeur vers une section critique [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="b4416-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> <dt>

<span data-ttu-id="b4416-109">*fTrace*</span><span class="sxs-lookup"><span data-stu-id="b4416-109">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="b4416-110">Valeur spécifiant si la journalisation est activée.</span><span class="sxs-lookup"><span data-stu-id="b4416-110">Value specifying whether logging is enabled.</span></span> <span data-ttu-id="b4416-111">Utilisez **true** pour activer la journalisation ou **false** pour la désactiver.</span><span class="sxs-lookup"><span data-stu-id="b4416-111">Use **TRUE** to enable logging or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4416-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4416-112">Return value</span></span>

<span data-ttu-id="b4416-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b4416-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4416-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b4416-114">Remarks</span></span>

<span data-ttu-id="b4416-115">Utilisez cette fonction pour tracer une section critique spécifique.</span><span class="sxs-lookup"><span data-stu-id="b4416-115">Use this function to trace a specific critical section.</span></span> <span data-ttu-id="b4416-116">Par défaut, la journalisation du débogage des sections critiques est désactivée, en raison du grand nombre de sections critiques.</span><span class="sxs-lookup"><span data-stu-id="b4416-116">By default, debug logging of critical sections is disabled, because of the large number of critical sections.</span></span>

<span data-ttu-id="b4416-117">Pour suivre une section critique, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b4416-117">To trace a critical section, perform the following steps:</span></span>

1.  <span data-ttu-id="b4416-118">Définissez DEBUG ou \_ Debug avant d’inclure les en-têtes DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b4416-118">Define DEBUG or \_DEBUG before you include the DirectShow headers.</span></span>
2.  <span data-ttu-id="b4416-119">Activez la journalisation du débogage pour les sections critiques en appelant [**DbgSetModuleLevel**](dbgsetmodulelevel.md) avec l’indicateur de verrouillage du journal \_ .</span><span class="sxs-lookup"><span data-stu-id="b4416-119">Enable debug logging for critical sections, by calling [**DbgSetModuleLevel**](dbgsetmodulelevel.md) with the LOG\_LOCKING flag.</span></span>
3.  <span data-ttu-id="b4416-120">Appelez **DbgLockTrace** sur la section critique que vous souhaitez tracer.</span><span class="sxs-lookup"><span data-stu-id="b4416-120">Call **DbgLockTrace** on the critical section you want to trace.</span></span>

<span data-ttu-id="b4416-121">Dans les versions commerciales, la fonction **DbgLockTrace** n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="b4416-121">In retail builds, the **DbgLockTrace** function has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="b4416-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="b4416-122">Examples</span></span>

<span data-ttu-id="b4416-123">L’exemple de code suivant montre comment suivre une section critique.</span><span class="sxs-lookup"><span data-stu-id="b4416-123">The following code example shows how to trace a critical section.</span></span>


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
```



## <a name="requirements"></a><span data-ttu-id="b4416-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4416-124">Requirements</span></span>



| <span data-ttu-id="b4416-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4416-125">Requirement</span></span> | <span data-ttu-id="b4416-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4416-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4416-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4416-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b4416-128"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4416-128"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b4416-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4416-129">Library</span></span><br/> | <dl> <span data-ttu-id="b4416-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b4416-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4416-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4416-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4416-132">Fonctions de débogage des sections critiques</span><span class="sxs-lookup"><span data-stu-id="b4416-132">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




