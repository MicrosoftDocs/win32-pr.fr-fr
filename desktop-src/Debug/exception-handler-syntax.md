---
description: Les \_ \_ \_ \_ Mots clés try et except sont utilisés pour construire un gestionnaire d’exceptions basé sur des frames. L’exemple suivant illustre la structure d’un gestionnaire d’exceptions.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Syntaxe de Exception-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eff9e6ca5d16a71b416f79a09f46795592a696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522876"
---
# <a name="exception-handler-syntax"></a><span data-ttu-id="039e4-104">Syntaxe de Exception-Handler</span><span class="sxs-lookup"><span data-stu-id="039e4-104">Exception-Handler Syntax</span></span>

<span data-ttu-id="039e4-105">Les mots clés **\_ \_ try** et **\_ \_ except** sont utilisés pour construire un gestionnaire d’exceptions basé sur des frames.</span><span class="sxs-lookup"><span data-stu-id="039e4-105">The **\_\_try** and **\_\_except** keywords are used to construct a frame-based exception handler.</span></span> <span data-ttu-id="039e4-106">L’exemple suivant illustre la structure d’un gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="039e4-106">The following example shows the structure of an exception handler.</span></span>


```C++
__try 
{
    // guarded body of code 
 
} 
__except (filter-expression) 
{ 
    // exception-handler block 
 
}
```



<span data-ttu-id="039e4-107">Notez que le bloc **\_ \_ try** et le bloc de gestionnaire d’exceptions requièrent des accolades ( {} ).</span><span class="sxs-lookup"><span data-stu-id="039e4-107">Note that the **\_\_try** block and the exception-handler block require braces ({}).</span></span> <span data-ttu-id="039e4-108">L’utilisation d’une instruction **goto** pour accéder au corps d’un bloc **\_ \_ try** ou dans un bloc de gestionnaire d’exceptions n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="039e4-108">Using a **goto** statement to jump into the body of a **\_\_try** block or into an exception-handler block is not permitted.</span></span> <span data-ttu-id="039e4-109">Cette règle s’applique à la fois aux gestionnaires d’exceptions et de terminaison.</span><span class="sxs-lookup"><span data-stu-id="039e4-109">This rule applies to both exception handlers and termination handlers.</span></span>

<span data-ttu-id="039e4-110">Le bloc **\_ \_ try** contient le corps protégé du code protégé par le gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="039e4-110">The **\_\_try** block contains the guarded body of code that the exception handler protects.</span></span> <span data-ttu-id="039e4-111">Une fonction peut avoir n’importe quel nombre de gestionnaires d’exceptions, et ces instructions de gestion des exceptions peuvent être imbriquées dans la même fonction ou dans des fonctions différentes.</span><span class="sxs-lookup"><span data-stu-id="039e4-111">A function can have any number of exception handlers, and these exception-handling statements can be nested within the same function or in different functions.</span></span> <span data-ttu-id="039e4-112">Si une exception se produit dans le bloc **\_ \_ try** , le système prend le contrôle et commence la recherche d’un gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="039e4-112">If an exception occurs within the **\_\_try** block, the system takes control and begins the search for an exception handler.</span></span> <span data-ttu-id="039e4-113">Pour obtenir une description détaillée de cette recherche, consultez [gestion des exceptions](exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="039e4-113">For a detailed description of this search, see [Exception Handling](exception-handling.md).</span></span>

<span data-ttu-id="039e4-114">Le gestionnaire d’exceptions reçoit uniquement les exceptions qui se produisent dans un thread unique.</span><span class="sxs-lookup"><span data-stu-id="039e4-114">The exception handler receives only exceptions that occur within a single thread.</span></span> <span data-ttu-id="039e4-115">Cela signifie que si un bloc **\_ \_ try** contient un appel à la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ou [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , les exceptions qui se produisent dans le nouveau processus ou thread ne sont pas distribuées à ce gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="039e4-115">This means that if a **\_\_try** block contains a call to the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) or [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function, exceptions that occur within the new process or thread are not dispatched to this handler.</span></span>

<span data-ttu-id="039e4-116">Le système évalue l’expression de filtre de chaque gestionnaire d’exceptions protégeant le code dans lequel l’exception s’est produite jusqu’à ce que l’exception soit gérée ou qu’il n’y ait plus de gestionnaires.</span><span class="sxs-lookup"><span data-stu-id="039e4-116">The system evaluates the filter expression of each exception handler guarding the code in which the exception occurred until either the exception is handled or there are no more handlers.</span></span> <span data-ttu-id="039e4-117">Une expression de filtre doit être évaluée comme l’une des trois valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="039e4-117">A filter expression must be evaluated as one of the three following values.</span></span>



| <span data-ttu-id="039e4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="039e4-118">Value</span></span>                              | <span data-ttu-id="039e4-119">Signification</span><span class="sxs-lookup"><span data-stu-id="039e4-119">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="039e4-120">**\_Gestionnaire d’exécution d’exception \_**</span><span class="sxs-lookup"><span data-stu-id="039e4-120">**EXCEPTION\_EXECUTE\_HANDLER**</span></span>    | <span data-ttu-id="039e4-121">Le système transfère le contrôle au gestionnaire d’exceptions, et l’exécution se poursuit dans le frame de pile dans lequel le gestionnaire est trouvé.</span><span class="sxs-lookup"><span data-stu-id="039e4-121">The system transfers control to the exception handler, and execution continues in the stack frame in which the handler is found.</span></span>                                                                                       |
| <span data-ttu-id="039e4-122">**L’EXCEPTION \_ continue la \_ recherche**</span><span class="sxs-lookup"><span data-stu-id="039e4-122">**EXCEPTION\_CONTINUE\_SEARCH**</span></span>    | <span data-ttu-id="039e4-123">Le système continue à rechercher un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="039e4-123">The system continues to search for a handler.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="039e4-124">**\_l’exception continue \_ l’exécution**</span><span class="sxs-lookup"><span data-stu-id="039e4-124">**EXCEPTION\_CONTINUE\_EXECUTION**</span></span> | <span data-ttu-id="039e4-125">Le système arrête la recherche d’un gestionnaire et retourne le contrôle au point auquel l’exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="039e4-125">The system stops its search for a handler and returns control to the point at which the exception occurred.</span></span> <span data-ttu-id="039e4-126">Si l’exception n’est pas continue, cela provoque une exception d’exception non **\_ continuable \_** .</span><span class="sxs-lookup"><span data-stu-id="039e4-126">If the exception is noncontinuable, this results in an **EXCEPTION\_NONCONTINUABLE\_EXCEPTION** exception.</span></span> |



 

<span data-ttu-id="039e4-127">L’expression de filtre est évaluée dans le contexte de la fonction dans laquelle le gestionnaire d’exceptions se trouve, même si l’exception s’est peut-être produite dans une fonction différente.</span><span class="sxs-lookup"><span data-stu-id="039e4-127">The filter expression is evaluated in the context of the function in which the exception handler is located, even though the exception may have occurred in a different function.</span></span> <span data-ttu-id="039e4-128">Cela signifie que l’expression de filtre peut accéder aux variables locales de la fonction.</span><span class="sxs-lookup"><span data-stu-id="039e4-128">This means that the filter expression can access the function's local variables.</span></span> <span data-ttu-id="039e4-129">De même, le bloc de gestionnaire d’exceptions peut accéder aux variables locales de la fonction dans laquelle il se trouve.</span><span class="sxs-lookup"><span data-stu-id="039e4-129">Similarly, the exception-handler block can access the local variables of the function in which it is located.</span></span>

<span data-ttu-id="039e4-130">Pour obtenir d’autres exemples, consultez [utilisation d’un gestionnaire d’exceptions](using-an-exception-handler.md).</span><span class="sxs-lookup"><span data-stu-id="039e4-130">For more examples, see [Using an Exception Handler](using-an-exception-handler.md).</span></span>

<span data-ttu-id="039e4-131">Pour plus d’informations sur les expressions de filtre et les fonctions de filtre, consultez [gestion des exceptions basée sur des frames](frame-based-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="039e4-131">For more information about filter expressions and filter functions, see [Frame-based Exception Handling](frame-based-exception-handling.md).</span></span>

 

 
