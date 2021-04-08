---
title: Indiquer les erreurs par exceptions
description: Pour les programmeurs C traditionnels, les erreurs sont généralement retournées via des valeurs de retour, ou un paramètre < out \ spécial qui retourne le code d’erreur.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fafc97e4d9c9d76b965ab67bcd57f4f33100625
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842533"
---
# <a name="indicate-errors-by-exceptions"></a><span data-ttu-id="27f5b-103">Indiquer les erreurs par exceptions</span><span class="sxs-lookup"><span data-stu-id="27f5b-103">Indicate Errors by Exceptions</span></span>

<span data-ttu-id="27f5b-104">Pour les programmeurs C traditionnels, les erreurs sont généralement retournées via des valeurs de retour, ou un \[ paramètre de sortie spécial \] qui retourne le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="27f5b-104">For traditional C programmers, errors are commonly returned through return values, or a special \[out\] parameter that returns the error code.</span></span> <span data-ttu-id="27f5b-105">Cela amène les interfaces implémentées de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="27f5b-105">This leads to interfaces implemented the following way:</span></span>

``` syntax
long sample(...)
{
    ...
    p = new Cbar(...);
    if (p == NULL)
    {
        // cleanup
        ...
        return ERROR_OUTOFMEMORY;
    }
}
```

<span data-ttu-id="27f5b-106">Le problème de cette approche est que les valeurs de retour RPC sont simplement des entiers longs.</span><span class="sxs-lookup"><span data-stu-id="27f5b-106">The problem with this approach is that RPC return values are simply long integers.</span></span> <span data-ttu-id="27f5b-107">Ils n’ont aucune signification particulière en tant qu’erreurs (Notez que l' [**État d’erreur \_ \_ t**](/windows/desktop/Midl/error-status-t) n’a pas de sémantique spéciale côté serveur), ce qui a des implications importantes.</span><span class="sxs-lookup"><span data-stu-id="27f5b-107">They have no special meaning as errors (note that [**error\_status\_t**](/windows/desktop/Midl/error-status-t) has no special semantics on the server side), which carries important implications.</span></span>

<span data-ttu-id="27f5b-108">Premièrement, RPC n’est pas averti que l’opération a échoué. Il tente de démarshaler tous les \[ arguments in, out \] et \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="27f5b-108">First, RPC is not alerted that the operation failed; it attempts to unmarshal all \[in, out\] and \[out\] arguments.</span></span> <span data-ttu-id="27f5b-109">La sémantique d’échec des handles de contexte est également différente.</span><span class="sxs-lookup"><span data-stu-id="27f5b-109">The failure semantics of context handles are also different.</span></span> <span data-ttu-id="27f5b-110">Le paquet renvoyé au client est essentiellement un paquet de réussite, avec le code d’erreur enfoui en profondeur dans le paquet.</span><span class="sxs-lookup"><span data-stu-id="27f5b-110">The packet returned to the client is essentially a success packet, with the error code buried deep in the packet.</span></span> <span data-ttu-id="27f5b-111">Cela signifie également que RPC n’utilise pas les informations d’erreur étendues, si bien que le logiciel client ne peut pas déterminer où l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="27f5b-111">This also means RPC does not use extended error information, so client software often is unable to discern where the call failed.</span></span>

<span data-ttu-id="27f5b-112">L’indication des erreurs dans les routines de serveur RPC en levant des exceptions SEH (Structured Exception Handling) (et non C++) est une approche bien meilleure.</span><span class="sxs-lookup"><span data-stu-id="27f5b-112">Indicating errors in RPC server routines by throwing Structured Exception Handling (SEH) exceptions (not C++) is a much better approach.</span></span> <span data-ttu-id="27f5b-113">Quand une exception SEH est levée, le contrôle passe directement à l’heure d’exécution RPC.</span><span class="sxs-lookup"><span data-stu-id="27f5b-113">When an SEH exception is thrown, control goes directly to the RPC run time.</span></span> <span data-ttu-id="27f5b-114">Une erreur se produit parfois de manière profonde dans une routine qui ne peut pas être nettoyée correctement et qui doit indiquer une erreur à son appelant.</span><span class="sxs-lookup"><span data-stu-id="27f5b-114">An error sometimes occurs deep in a routine that cannot properly clean up, and it needs to indicate an error to its caller.</span></span> <span data-ttu-id="27f5b-115">La routine doit retourner une erreur à son appelant, qui à son tour peut retourner une erreur à son appelant, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="27f5b-115">The routine should return an error to its caller, which in turn can return an error to its caller and so on.</span></span> <span data-ttu-id="27f5b-116">Toutefois, la dernière routine serveur sur la pile doit lever une exception avant de retourner à RPC pour indiquer à RPC qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="27f5b-116">However, the last server routine on the stack should throw an exception before it returns to RPC to indicate to RPC that an error occurred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27f5b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27f5b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27f5b-118">Gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="27f5b-118">Exception Handling</span></span>](exception-handling.md)
</dt> </dl>

 

 