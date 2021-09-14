---
description: Les \_ \_ \_ \_ Mots clés try et except sont utilisés pour construire un gestionnaire d’exceptions basé sur des frames. L’exemple suivant illustre la structure d’un gestionnaire d’exceptions.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Syntaxe de Exception-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eff9e6ca5d16a71b416f79a09f46795592a696
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114606"
---
# <a name="exception-handler-syntax"></a>Syntaxe de Exception-Handler

Les mots clés **\_ \_ try** et **\_ \_ except** sont utilisés pour construire un gestionnaire d’exceptions basé sur des frames. L’exemple suivant illustre la structure d’un gestionnaire d’exceptions.


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



Notez que le bloc **\_ \_ try** et le bloc de gestionnaire d’exceptions requièrent des accolades ( {} ). L’utilisation d’une instruction **goto** pour accéder au corps d’un bloc **\_ \_ try** ou dans un bloc de gestionnaire d’exceptions n’est pas autorisée. Cette règle s’applique à la fois aux gestionnaires d’exceptions et de terminaison.

Le bloc **\_ \_ try** contient le corps protégé du code protégé par le gestionnaire d’exceptions. Une fonction peut avoir n’importe quel nombre de gestionnaires d’exceptions, et ces instructions de gestion des exceptions peuvent être imbriquées dans la même fonction ou dans des fonctions différentes. Si une exception se produit dans le bloc **\_ \_ try** , le système prend le contrôle et commence la recherche d’un gestionnaire d’exceptions. Pour obtenir une description détaillée de cette recherche, consultez [gestion des exceptions](exception-handling.md).

Le gestionnaire d’exceptions reçoit uniquement les exceptions qui se produisent dans un thread unique. Cela signifie que si un bloc **\_ \_ try** contient un appel à la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ou [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , les exceptions qui se produisent dans le nouveau processus ou thread ne sont pas distribuées à ce gestionnaire.

Le système évalue l’expression de filtre de chaque gestionnaire d’exceptions protégeant le code dans lequel l’exception s’est produite jusqu’à ce que l’exception soit gérée ou qu’il n’y ait plus de gestionnaires. Une expression de filtre doit être évaluée comme l’une des trois valeurs suivantes.



| Valeur                              | Signification                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_Gestionnaire d’exécution d’exception \_**    | Le système transfère le contrôle au gestionnaire d’exceptions, et l’exécution se poursuit dans le frame de pile dans lequel le gestionnaire est trouvé.                                                                                       |
| **L’EXCEPTION \_ continue la \_ recherche**    | Le système continue à rechercher un gestionnaire.                                                                                                                                                                          |
| **\_l’exception continue \_ l’exécution** | Le système arrête la recherche d’un gestionnaire et retourne le contrôle au point auquel l’exception s’est produite. Si l’exception n’est pas continue, cela provoque une exception d’exception non **\_ continuable \_** . |



 

L’expression de filtre est évaluée dans le contexte de la fonction dans laquelle le gestionnaire d’exceptions se trouve, même si l’exception s’est peut-être produite dans une fonction différente. Cela signifie que l’expression de filtre peut accéder aux variables locales de la fonction. De même, le bloc de gestionnaire d’exceptions peut accéder aux variables locales de la fonction dans laquelle il se trouve.

Pour obtenir d’autres exemples, consultez [utilisation d’un gestionnaire d’exceptions](using-an-exception-handler.md).

Pour plus d’informations sur les expressions de filtre et les fonctions de filtre, consultez [gestion des exceptions basée sur des frames](frame-based-exception-handling.md).

 

 
