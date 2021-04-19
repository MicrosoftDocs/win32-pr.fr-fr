---
description: Les variables de condition sont des primitives de synchronisation qui autorisent les threads à attendre qu’une condition particulière se produise. Les variables de condition sont des objets en mode utilisateur qui ne peuvent pas être partagés entre les processus.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Variables de condition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fad7d80c1c5e06fc6e496198cd298b190daba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541888"
---
# <a name="condition-variables"></a><span data-ttu-id="94d62-104">Variables de condition</span><span class="sxs-lookup"><span data-stu-id="94d62-104">Condition Variables</span></span>

<span data-ttu-id="94d62-105">Les variables de condition sont des primitives de synchronisation qui autorisent les threads à attendre qu’une condition particulière se produise.</span><span class="sxs-lookup"><span data-stu-id="94d62-105">Condition variables are synchronization primitives that enable threads to wait until a particular condition occurs.</span></span> <span data-ttu-id="94d62-106">Les variables de condition sont des objets en mode utilisateur qui ne peuvent pas être partagés entre les processus.</span><span class="sxs-lookup"><span data-stu-id="94d62-106">Condition variables are user-mode objects that cannot be shared across processes.</span></span>

<span data-ttu-id="94d62-107">Les variables de condition permettent aux threads de libérer atomiquement un verrou et de passer en état de veille.</span><span class="sxs-lookup"><span data-stu-id="94d62-107">Condition variables enable threads to atomically release a lock and enter the sleeping state.</span></span> <span data-ttu-id="94d62-108">Ils peuvent être utilisés avec des sections critiques ou des verrous SRW (Slim Reader/Writer).</span><span class="sxs-lookup"><span data-stu-id="94d62-108">They can be used with critical sections or slim reader/writer (SRW) locks.</span></span> <span data-ttu-id="94d62-109">Les variables de condition prennent en charge les opérations « réveiller un » ou « mettre en éveil tous les threads en attente ».</span><span class="sxs-lookup"><span data-stu-id="94d62-109">Condition variables support operations that "wake one" or "wake all" waiting threads.</span></span> <span data-ttu-id="94d62-110">Une fois qu’un thread est en éveil, il acquiert à nouveau le verrou libéré lorsque le thread est passé à l’état de veille.</span><span class="sxs-lookup"><span data-stu-id="94d62-110">After a thread is woken, it re-acquires the lock it released when the thread entered the sleeping state.</span></span>

<span data-ttu-id="94d62-111">Notez que l’appelant doit allouer une structure de **\_ variable de condition** et l’initialiser en appelant [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (pour initialiser la structure de manière dynamique) ou affecter la variable de **condition constante \_ \_ init** à la variable de structure (pour initialiser la structure de manière statique).</span><span class="sxs-lookup"><span data-stu-id="94d62-111">Note that the caller must allocate a **CONDITION\_VARIABLE** structure and initialize it by either calling [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (to initialize the structure dynamically) or assign the constant **CONDITION\_VARIABLE\_INIT** to the structure variable (to initialize the structure statically).</span></span>

<span data-ttu-id="94d62-112">**Windows Server 2003 et Windows XP :** Les variables de condition ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="94d62-112">**Windows Server 2003 and Windows XP:** Condition variables are not supported.</span></span>

<span data-ttu-id="94d62-113">Les fonctions de variable conditionnelle sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="94d62-113">The following are the condition variable functions.</span></span>



| <span data-ttu-id="94d62-114">Fonction de variable conditionnelle</span><span class="sxs-lookup"><span data-stu-id="94d62-114">Condition variable function</span></span>                                        | <span data-ttu-id="94d62-115">Description</span><span class="sxs-lookup"><span data-stu-id="94d62-115">Description</span></span>                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94d62-116">**InitializeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="94d62-116">**InitializeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | <span data-ttu-id="94d62-117">Initialise une variable de condition.</span><span class="sxs-lookup"><span data-stu-id="94d62-117">Initializes a condition variable.</span></span>                                                                              |
| [<span data-ttu-id="94d62-118">**SleepConditionVariableCS**</span><span class="sxs-lookup"><span data-stu-id="94d62-118">**SleepConditionVariableCS**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | <span data-ttu-id="94d62-119">Met en veille la variable de condition spécifiée et libère la section critique spécifiée sous la forme d’une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="94d62-119">Sleeps on the specified condition variable and releases the specified critical section as an atomic operation.</span></span> |
| [<span data-ttu-id="94d62-120">**SleepConditionVariableSRW**</span><span class="sxs-lookup"><span data-stu-id="94d62-120">**SleepConditionVariableSRW**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | <span data-ttu-id="94d62-121">Met en veille la variable de condition spécifiée et libère le verrou SRW spécifié sous la forme d’une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="94d62-121">Sleeps on the specified condition variable and releases the specified SRW lock as an atomic operation.</span></span>         |
| [<span data-ttu-id="94d62-122">**WakeAllConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="94d62-122">**WakeAllConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | <span data-ttu-id="94d62-123">Sort tous les threads en attente de la variable de condition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="94d62-123">Wakes all threads waiting on the specified condition variable.</span></span>                                                 |
| [<span data-ttu-id="94d62-124">**WakeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="94d62-124">**WakeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | <span data-ttu-id="94d62-125">Veille un thread unique en attente sur la variable de condition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="94d62-125">Wakes a single thread waiting on the specified condition variable.</span></span>                                             |



 

<span data-ttu-id="94d62-126">Le pseudo-code suivant illustre le modèle d’utilisation classique des variables de condition.</span><span class="sxs-lookup"><span data-stu-id="94d62-126">The following pseudocode demonstrates the typical usage pattern of condition variables.</span></span>

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

<span data-ttu-id="94d62-127">Par exemple, dans une implémentation d’un verrou en lecture/écriture, la `TestPredicate` fonction vérifie que la requête de verrou en cours est compatible avec les propriétaires existants.</span><span class="sxs-lookup"><span data-stu-id="94d62-127">For example, in an implementation of a reader/writer lock, the `TestPredicate` function would verify that the current lock request is compatible with the existing owners.</span></span> <span data-ttu-id="94d62-128">Si c’est le cas, acquérir le verrou ; Sinon, veille.</span><span class="sxs-lookup"><span data-stu-id="94d62-128">If it is, acquire the lock; otherwise, sleep.</span></span> <span data-ttu-id="94d62-129">Pour obtenir un exemple plus détaillé, consultez [utilisation de variables de condition](using-condition-variables.md).</span><span class="sxs-lookup"><span data-stu-id="94d62-129">For a more detailed example, see [Using Condition Variables](using-condition-variables.md).</span></span>

<span data-ttu-id="94d62-130">Les variables de condition sont soumises à des réveils paraparasites (ceux qui ne sont pas associés à une éveil explicite) et des réveils volés (un autre thread gère pour s’exécuter avant le thread réveill).</span><span class="sxs-lookup"><span data-stu-id="94d62-130">Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread).</span></span> <span data-ttu-id="94d62-131">Par conséquent, vous devez revérifier un prédicat (généralement dans une boucle **while** ) après le retour d’une opération Sleep.</span><span class="sxs-lookup"><span data-stu-id="94d62-131">Therefore, you should recheck a predicate (typically in a **while** loop) after a sleep operation returns.</span></span>

<span data-ttu-id="94d62-132">Vous pouvez réveiller d’autres threads à l’aide de [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) ou [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) , à l’intérieur ou à l’extérieur du verrou associé à la variable de condition.</span><span class="sxs-lookup"><span data-stu-id="94d62-132">You can wake other threads using [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) or [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) either inside or outside the lock associated with the condition variable.</span></span> <span data-ttu-id="94d62-133">Il est généralement préférable de libérer le verrou avant de sortir d’autres threads afin de réduire le nombre de changements de contexte.</span><span class="sxs-lookup"><span data-stu-id="94d62-133">It is usually better to release the lock before waking other threads to reduce the number of context switches.</span></span>

<span data-ttu-id="94d62-134">Il est souvent pratique d’utiliser plusieurs variables de condition avec le même verrou.</span><span class="sxs-lookup"><span data-stu-id="94d62-134">It is often convenient to use more than one condition variable with the same lock.</span></span> <span data-ttu-id="94d62-135">Par exemple, une implémentation d’un verrou en lecture/écriture peut utiliser une seule section critique, mais des variables de condition distinctes pour les lecteurs et les enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="94d62-135">For example, an implementation of a reader/writer lock might use a single critical section but separate condition variables for readers and writers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94d62-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94d62-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94d62-137">Utilisation de variables de condition</span><span class="sxs-lookup"><span data-stu-id="94d62-137">Using Condition Variables</span></span>](using-condition-variables.md)
</dt> </dl>

 

 
