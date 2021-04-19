---
description: Les \_ \_ \_ \_ Mots clés try et finally sont utilisés pour construire un gestionnaire de terminaisons. L’exemple suivant illustre la structure d’un gestionnaire de terminaisons.
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Syntaxe de Termination-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbf2656636490738a292c274a3e3184a34c0f94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515358"
---
# <a name="termination-handler-syntax"></a><span data-ttu-id="966a8-104">Syntaxe de Termination-Handler</span><span class="sxs-lookup"><span data-stu-id="966a8-104">Termination-Handler Syntax</span></span>

<span data-ttu-id="966a8-105">Les mots clés **\_ \_ try** et **\_ \_ finally** sont utilisés pour construire un gestionnaire de terminaisons.</span><span class="sxs-lookup"><span data-stu-id="966a8-105">The **\_\_try** and **\_\_finally** keywords are used to construct a termination handler.</span></span> <span data-ttu-id="966a8-106">L’exemple suivant illustre la structure d’un gestionnaire de terminaisons.</span><span class="sxs-lookup"><span data-stu-id="966a8-106">The following example shows the structure of a termination handler.</span></span>


```C++
__try 
{ 
    // guarded body of code 
 
} 
__finally 
{ 
    // __finally block 
 
}
```



<span data-ttu-id="966a8-107">Pour obtenir des exemples, consultez [utilisation d’un gestionnaire de terminaisons](using-a-termination-handler.md).</span><span class="sxs-lookup"><span data-stu-id="966a8-107">For examples, see [Using a Termination Handler](using-a-termination-handler.md).</span></span>

<span data-ttu-id="966a8-108">Comme avec le gestionnaire d’exceptions, le bloc **\_ \_ try** et le bloc **\_ \_ finally** requièrent des accolades ( {} ), et l’utilisation d’une instruction **goto** pour accéder à l’un ou l’autre bloc n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="966a8-108">As with the exception handler, both the **\_\_try** block and the **\_\_finally** block require braces ({}), and using a **goto** statement to jump into either block is not permitted.</span></span>

<span data-ttu-id="966a8-109">Le bloc **\_ \_ try** contient le corps de code gardé protégé par le gestionnaire de terminaisons.</span><span class="sxs-lookup"><span data-stu-id="966a8-109">The **\_\_try** block contains the guarded body of code that is protected by the termination handler.</span></span> <span data-ttu-id="966a8-110">Une fonction peut avoir un nombre quelconque de gestionnaires de terminaisons, et ces blocs de gestion des arrêts peuvent être imbriqués dans la même fonction ou dans des fonctions différentes.</span><span class="sxs-lookup"><span data-stu-id="966a8-110">A function can have any number of termination handlers, and these termination-handling blocks can be nested within the same function or in different functions.</span></span>

<span data-ttu-id="966a8-111">Le bloc **\_ \_ finally** est exécuté chaque fois que le workflow de contrôle quitte le bloc **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="966a8-111">The **\_\_finally** block is executed whenever the flow of control leaves the **\_\_try** block.</span></span> <span data-ttu-id="966a8-112">Toutefois, le bloc **\_ \_ finally** n’est pas exécuté si vous appelez l’une des fonctions suivantes dans le bloc **\_ \_ try** : [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)ou **Abort**.</span><span class="sxs-lookup"><span data-stu-id="966a8-112">However, the **\_\_finally** block is not executed if you call any of the following functions within the **\_\_try** block: [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), or **abort**.</span></span>

<span data-ttu-id="966a8-113">Le bloc **\_ \_ finally** est exécuté dans le contexte de la fonction dans laquelle se trouve le gestionnaire de terminaisons.</span><span class="sxs-lookup"><span data-stu-id="966a8-113">The **\_\_finally** block is executed in the context of the function in which the termination handler is located.</span></span> <span data-ttu-id="966a8-114">Cela signifie que le bloc **\_ \_ finally** peut accéder aux variables locales de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="966a8-114">This means that the **\_\_finally** block can access that function's local variables.</span></span> <span data-ttu-id="966a8-115">L’exécution du bloc **\_ \_ finally** peut se terminer de l’une des manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="966a8-115">Execution of the **\_\_finally** block can terminate by any of the following means.</span></span>

-   <span data-ttu-id="966a8-116">Exécution de la dernière instruction dans le bloc et continuation à l’instruction suivante</span><span class="sxs-lookup"><span data-stu-id="966a8-116">Execution of the last statement in the block and continuation to the next instruction</span></span>
-   <span data-ttu-id="966a8-117">Utilisation d’une instruction de contrôle (**Return**, **break**, **continue** ou **goto**)</span><span class="sxs-lookup"><span data-stu-id="966a8-117">Use of a control statement (**return**, **break**, **continue**, or **goto**)</span></span>
-   <span data-ttu-id="966a8-118">Utilisation de **longjmp** ou d’un saut vers un gestionnaire d’exceptions</span><span class="sxs-lookup"><span data-stu-id="966a8-118">Use of **longjmp** or a jump to an exception handler</span></span>

<span data-ttu-id="966a8-119">Si l’exécution du bloc **\_ \_ try** se termine en raison d’une exception qui appelle le bloc de gestion des exceptions d’un gestionnaire d’exceptions basé sur des frames, le bloc **\_ \_ finally** est exécuté avant l’exécution du bloc de gestion des exceptions.</span><span class="sxs-lookup"><span data-stu-id="966a8-119">If execution of the **\_\_try** block terminates because of an exception that invokes the exception-handling block of a frame-based exception handler, the **\_\_finally** block is executed before the exception-handling block is executed.</span></span> <span data-ttu-id="966a8-120">De même, un appel à la fonction de la bibliothèque Runtime C **longjmp** à partir du bloc **\_ \_ try** provoque l’exécution du bloc **\_ \_ finally** avant la reprise de l’exécution à la cible de l’opération **longjmp** .</span><span class="sxs-lookup"><span data-stu-id="966a8-120">Similarly, a call to the **longjmp** C run-time library function from the **\_\_try** block causes execution of the **\_\_finally** block before execution resumes at the target of the **longjmp** operation.</span></span> <span data-ttu-id="966a8-121">Si l’exécution de bloc **\_ \_ try** se termine en raison d’une instruction de contrôle (**Return**, **break**, **continue** ou **goto**), le bloc **\_ \_ finally** est exécuté.</span><span class="sxs-lookup"><span data-stu-id="966a8-121">If **\_\_try** block execution terminates due to a control statement (**return**, **break**, **continue**, or **goto**), the **\_\_finally** block is executed.</span></span>

<span data-ttu-id="966a8-122">La fonction [**AbnormalTermination**](abnormaltermination.md) peut être utilisée dans le bloc **\_ \_ finally** pour déterminer si le bloc **\_ \_ try** s’est arrêté séquentiellement, c’est-à-dire s’il a atteint l’accolade fermante (}).</span><span class="sxs-lookup"><span data-stu-id="966a8-122">The [**AbnormalTermination**](abnormaltermination.md) function can be used within the **\_\_finally** block to determine whether the **\_\_try** block terminated sequentially — that is, whether it reached the closing brace (}).</span></span> <span data-ttu-id="966a8-123">Le fait de quitter le bloc **\_ \_ try** en raison d’un appel à **longjmp**, d’un saut à un gestionnaire d’exceptions, ou d’une instruction **Return**, **break**, **continue** ou **goto** , est considéré comme un arrêt anormal.</span><span class="sxs-lookup"><span data-stu-id="966a8-123">Leaving the **\_\_try** block because of a call to **longjmp**, a jump to an exception handler, or a **return**, **break**, **continue**, or **goto** statement, is considered an abnormal termination.</span></span> <span data-ttu-id="966a8-124">Notez que l’échec de l’arrêt séquentiel fait que le système recherche dans tous les frames de pile dans l’ordre inverse pour déterminer si des gestionnaires de terminaison doivent être appelés.</span><span class="sxs-lookup"><span data-stu-id="966a8-124">Note that failure to terminate sequentially causes the system to search through all stack frames in reverse order to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="966a8-125">Cela peut entraîner une dégradation des performances en raison de l’exécution de centaines d’instructions.</span><span class="sxs-lookup"><span data-stu-id="966a8-125">This can result in performance degradation due to the execution of hundreds of instructions.</span></span>

<span data-ttu-id="966a8-126">Pour éviter l’arrêt anormal du gestionnaire de terminaisons, l’exécution doit se poursuivre jusqu’à la fin du bloc.</span><span class="sxs-lookup"><span data-stu-id="966a8-126">To avoid abnormal termination of the termination handler, execution should continue to the end of the block.</span></span> <span data-ttu-id="966a8-127">Vous pouvez également exécuter l’instruction **\_ \_ Leave** .</span><span class="sxs-lookup"><span data-stu-id="966a8-127">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="966a8-128">L’instruction **\_ \_ Leave** autorise l’arrêt immédiat du bloc **\_ \_ try** sans entraîner un arrêt anormal et une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="966a8-128">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="966a8-129">Consultez la documentation de votre compilateur pour déterminer si l’instruction **\_ \_ Leave** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="966a8-129">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

<span data-ttu-id="966a8-130">Si l’exécution du bloc **\_ \_ finally** se termine en raison de l’instruction de contrôle de **retour** , elle équivaut à une instruction **goto** à l’accolade fermante dans la fonction englobante.</span><span class="sxs-lookup"><span data-stu-id="966a8-130">If execution of the **\_\_finally** block terminates because of the **return** control statement, it is equivalent to a **goto** to the closing brace in the enclosing function.</span></span> <span data-ttu-id="966a8-131">Par conséquent, la fonction englobante retourne.</span><span class="sxs-lookup"><span data-stu-id="966a8-131">Therefore, the enclosing function will return.</span></span>

 

 
