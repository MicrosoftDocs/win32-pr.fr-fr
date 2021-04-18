---
description: Les exemples suivants illustrent l’utilisation d’un gestionnaire d’exceptions.
ms.assetid: c3b4e696-9f45-4616-ac6b-07ba29750bb2
title: Utilisation d’un gestionnaire d’exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dbe7ec23ddd5372cecfe85ae8348092d91cfff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515934"
---
# <a name="using-an-exception-handler"></a><span data-ttu-id="ebcae-103">Utilisation d’un gestionnaire d’exceptions</span><span class="sxs-lookup"><span data-stu-id="ebcae-103">Using an Exception Handler</span></span>

<span data-ttu-id="ebcae-104">Les exemples suivants illustrent l’utilisation d’un gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="ebcae-104">The following examples demonstrate the use of an exception handler.</span></span>

## <a name="example-1"></a><span data-ttu-id="ebcae-105">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="ebcae-105">Example 1</span></span>

<span data-ttu-id="ebcae-106">Le fragment de code suivant utilise la gestion structurée des exceptions pour vérifier si une opération de division sur les entiers 2 32 bits entraîne une erreur de division par zéro.</span><span class="sxs-lookup"><span data-stu-id="ebcae-106">The following code fragment uses structured exception handling to check whether a division operation on two 32-bit integers will result in an division-by-zero error.</span></span> <span data-ttu-id="ebcae-107">Si cela se produit, la fonction retourne **false**; sinon, elle retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="ebcae-107">If this occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>


```C++
BOOL SafeDiv(INT32 dividend, INT32 divisor, INT32 *pResult)
{
    __try 
    { 
        *pResult = dividend / divisor; 
    } 
    __except(GetExceptionCode() == EXCEPTION_INT_DIVIDE_BY_ZERO ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
    { 
        return FALSE;
    }
    return TRUE;
} 
```



## <a name="example-2"></a><span data-ttu-id="ebcae-108">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="ebcae-108">Example 2</span></span>

<span data-ttu-id="ebcae-109">L’exemple de fonction suivant appelle la fonction [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) et utilise la gestion structurée des exceptions pour rechercher une exception de point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ebcae-109">The following example function calls the [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function and uses structured exception handling to check for a breakpoint exception.</span></span> <span data-ttu-id="ebcae-110">Si un événement se produit, la fonction retourne **false**; sinon, elle retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="ebcae-110">If one occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>

<span data-ttu-id="ebcae-111">L’expression de filtre dans l’exemple utilise la fonction [**GetExceptionCode**](getexceptioncode.md) pour vérifier le type d’exception avant d’exécuter le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="ebcae-111">The filter expression in the example uses the [**GetExceptionCode**](getexceptioncode.md) function to check the exception type before executing the handler.</span></span> <span data-ttu-id="ebcae-112">Cela permet au système de continuer à rechercher un gestionnaire approprié si un autre type d’exception se produit.</span><span class="sxs-lookup"><span data-stu-id="ebcae-112">This enables the system to continue its search for an appropriate handler if some other type of exception occurs.</span></span>

<span data-ttu-id="ebcae-113">En outre, l’utilisation de l’instruction **Return** dans le bloc **\_ \_ try** d’un gestionnaire d’exceptions diffère de l’utilisation de **Return** dans le bloc **\_ \_ try** d’un gestionnaire d’arrêt, ce qui provoque un arrêt anormal du bloc **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="ebcae-113">Also, use of the **return** statement in the **\_\_try** block of an exception handler differs from the use of **return** in the **\_\_try** block of a termination handler, which causes an abnormal termination of the **\_\_try** block.</span></span> <span data-ttu-id="ebcae-114">Il s’agit d’une utilisation valide de l’instruction return dans un gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="ebcae-114">This is an valid use of the return statement in an exception handler.</span></span>


```C++
BOOL CheckForDebugger()
{
    __try 
    {
        DebugBreak();
    }
    __except(GetExceptionCode() == EXCEPTION_BREAKPOINT ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH) 
    {
        // No debugger is attached, so return FALSE 
        // and continue.
        return FALSE;
    }
    return TRUE;
}
```



<span data-ttu-id="ebcae-115">Retourne uniquement le \_ \_ Gestionnaire d’exécution d’exception à partir d’un filtre d’exception lorsque le type d’exception est attendu et que l’adresse d’erreur est connue.</span><span class="sxs-lookup"><span data-stu-id="ebcae-115">Only return EXCEPTION\_EXECUTE\_HANDLER from an exception filter when the exception type is expected and the faulting address is known.</span></span> <span data-ttu-id="ebcae-116">Vous devez autoriser le gestionnaire d’exceptions par défaut à traiter les types d’exception inattendus et les adresses défaillantes.</span><span class="sxs-lookup"><span data-stu-id="ebcae-116">You should allow the default exception handler to process unexpected exception types and faulting addresses.</span></span>

## <a name="example-3"></a><span data-ttu-id="ebcae-117">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="ebcae-117">Example 3</span></span>

<span data-ttu-id="ebcae-118">L’exemple suivant montre l’interaction des gestionnaires imbriqués.</span><span class="sxs-lookup"><span data-stu-id="ebcae-118">The following example shows the interaction of nested handlers.</span></span> <span data-ttu-id="ebcae-119">La fonction [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) provoque une exception dans le corps protégé d’un gestionnaire de terminaisons qui se trouve à l’intérieur du corps protégé d’un gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="ebcae-119">The [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) function causes an exception in the guarded body of a termination handler that is inside the guarded body of an exception handler.</span></span> <span data-ttu-id="ebcae-120">L’exception amène le système à évaluer la fonction FilterFunction, dont la valeur de retour provoque à son tour l’appel du gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="ebcae-120">The exception causes the system to evaluate the FilterFunction function, whose return value in turn causes the exception handler to be invoked.</span></span> <span data-ttu-id="ebcae-121">Toutefois, avant l’exécution du bloc de gestionnaire d’exceptions, le bloc **\_ \_ finally** du gestionnaire de terminaisons est exécuté, car le workflow de contrôle a quitté le bloc **\_ \_ try** du gestionnaire de terminaisons.</span><span class="sxs-lookup"><span data-stu-id="ebcae-121">However, before the exception-handler block is executed, the **\_\_finally** block of the termination handler is executed because the flow of control has left the **\_\_try** block of the termination handler.</span></span>


```C++
DWORD FilterFunction() 
{ 
    printf("1 ");                     // printed first 
    return EXCEPTION_EXECUTE_HANDLER; 
} 
 
VOID main(VOID) 
{ 
    __try 
    { 
        __try 
        { 
            RaiseException( 
                1,                    // exception code 
                0,                    // continuable exception 
                0, NULL);             // no arguments 
        } 
        __finally 
        { 
            printf("2 ");             // this is printed second 
        } 
    } 
    __except ( FilterFunction() ) 
    { 
        printf("3\n");                // this is printed last 
    } 
}
```



 

 
