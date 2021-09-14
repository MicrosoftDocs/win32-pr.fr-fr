---
title: Indiquer les erreurs par exceptions
description: Pour les programmeurs C traditionnels, les erreurs sont généralement retournées via des valeurs de retour, ou un paramètre < out \ spécial qui retourne le code d’erreur.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fafc97e4d9c9d76b965ab67bcd57f4f33100625
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194171"
---
# <a name="indicate-errors-by-exceptions"></a>Indiquer les erreurs par exceptions

Pour les programmeurs C traditionnels, les erreurs sont généralement retournées via des valeurs de retour, ou un \[ paramètre de sortie spécial \] qui retourne le code d’erreur. Cela amène les interfaces implémentées de la façon suivante :

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

Le problème de cette approche est que les valeurs de retour RPC sont simplement des entiers longs. Ils n’ont aucune signification particulière en tant qu’erreurs (Notez que l' [**État d’erreur \_ \_ t**](/windows/desktop/Midl/error-status-t) n’a pas de sémantique spéciale côté serveur), ce qui a des implications importantes.

Premièrement, RPC n’est pas averti que l’opération a échoué. Il tente de démarshaler tous les \[ arguments in, out \] et \[ out \] . La sémantique d’échec des handles de contexte est également différente. Le paquet renvoyé au client est essentiellement un paquet de réussite, avec le code d’erreur enfoui en profondeur dans le paquet. Cela signifie également que RPC n’utilise pas les informations d’erreur étendues, si bien que le logiciel client ne peut pas déterminer où l’appel a échoué.

L’indication des erreurs dans les routines de serveur RPC en levant des exceptions SEH (Structured Exception Handling) (et non C++) est une approche bien meilleure. Quand une exception SEH est levée, le contrôle passe directement à l’heure d’exécution RPC. Une erreur se produit parfois de manière profonde dans une routine qui ne peut pas être nettoyée correctement et qui doit indiquer une erreur à son appelant. La routine doit retourner une erreur à son appelant, qui à son tour peut retourner une erreur à son appelant, et ainsi de suite. Toutefois, la dernière routine serveur sur la pile doit lever une exception avant de retourner à RPC pour indiquer à RPC qu’une erreur s’est produite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des exceptions](exception-handling.md)
</dt> </dl>

 

 