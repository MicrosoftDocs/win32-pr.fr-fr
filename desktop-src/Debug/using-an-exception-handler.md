---
description: Les exemples suivants illustrent l’utilisation d’un gestionnaire d’exceptions.
ms.assetid: c3b4e696-9f45-4616-ac6b-07ba29750bb2
title: Utilisation d’un gestionnaire d’exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309f65122c333efa8974087117faa0120e1ac6223d458698dc7f00fe398967e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002419"
---
# <a name="using-an-exception-handler"></a>Utilisation d’un gestionnaire d’exceptions

Les exemples suivants illustrent l’utilisation d’un gestionnaire d’exceptions.

## <a name="example-1"></a>Exemple 1

Le fragment de code suivant utilise la gestion structurée des exceptions pour vérifier si une opération de division sur les entiers 2 32 bits entraîne une erreur de division par zéro. Si cela se produit, la fonction retourne **false**; sinon, elle retourne la **valeur true**.


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



## <a name="example-2"></a>Exemple 2

L’exemple de fonction suivant appelle la fonction [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) et utilise la gestion structurée des exceptions pour rechercher une exception de point d’arrêt. Si un événement se produit, la fonction retourne **false**; sinon, elle retourne la **valeur true**.

L’expression de filtre dans l’exemple utilise la fonction [**GetExceptionCode**](getexceptioncode.md) pour vérifier le type d’exception avant d’exécuter le gestionnaire. Cela permet au système de continuer à rechercher un gestionnaire approprié si un autre type d’exception se produit.

En outre, l’utilisation de l’instruction **Return** dans le bloc **\_ \_ try** d’un gestionnaire d’exceptions diffère de l’utilisation de **Return** dans le bloc **\_ \_ try** d’un gestionnaire d’arrêt, ce qui provoque un arrêt anormal du bloc **\_ \_ try** . Il s’agit d’une utilisation valide de l’instruction return dans un gestionnaire d’exceptions.


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



Retourne uniquement le \_ \_ Gestionnaire d’exécution d’exception à partir d’un filtre d’exception lorsque le type d’exception est attendu et que l’adresse d’erreur est connue. Vous devez autoriser le gestionnaire d’exceptions par défaut à traiter les types d’exception inattendus et les adresses défaillantes.

## <a name="example-3"></a>Exemple 3

L’exemple suivant montre l’interaction des gestionnaires imbriqués. La fonction [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) provoque une exception dans le corps protégé d’un gestionnaire de terminaisons qui se trouve à l’intérieur du corps protégé d’un gestionnaire d’exceptions. L’exception amène le système à évaluer la fonction FilterFunction, dont la valeur de retour provoque à son tour l’appel du gestionnaire d’exceptions. Toutefois, avant l’exécution du bloc de gestionnaire d’exceptions, le bloc **\_ \_ finally** du gestionnaire de terminaisons est exécuté, car le workflow de contrôle a quitté le bloc **\_ \_ try** du gestionnaire de terminaisons.


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



 

 
