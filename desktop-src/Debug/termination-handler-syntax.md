---
description: Les \_ \_ \_ \_ Mots clés try et finally sont utilisés pour construire un gestionnaire de terminaisons. L’exemple suivant illustre la structure d’un gestionnaire de terminaisons.
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Syntaxe de Termination-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3a6322bbcf86f56a75c62eaba03d50827edcd71a57addf48ef3777c7687796
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984459"
---
# <a name="termination-handler-syntax"></a>Syntaxe de Termination-Handler

Les mots clés **\_ \_ try** et **\_ \_ finally** sont utilisés pour construire un gestionnaire de terminaisons. L’exemple suivant illustre la structure d’un gestionnaire de terminaisons.


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



Pour obtenir des exemples, consultez [utilisation d’un gestionnaire de terminaisons](using-a-termination-handler.md).

Comme avec le gestionnaire d’exceptions, le bloc **\_ \_ try** et le bloc **\_ \_ finally** requièrent des accolades ( {} ), et l’utilisation d’une instruction **goto** pour accéder à l’un ou l’autre bloc n’est pas autorisée.

Le bloc **\_ \_ try** contient le corps de code gardé protégé par le gestionnaire de terminaisons. Une fonction peut avoir un nombre quelconque de gestionnaires de terminaisons, et ces blocs de gestion des arrêts peuvent être imbriqués dans la même fonction ou dans des fonctions différentes.

Le bloc **\_ \_ finally** est exécuté chaque fois que le workflow de contrôle quitte le bloc **\_ \_ try** . Toutefois, le bloc **\_ \_ finally** n’est pas exécuté si vous appelez l’une des fonctions suivantes dans le bloc **\_ \_ try** : [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)ou **Abort**.

Le bloc **\_ \_ finally** est exécuté dans le contexte de la fonction dans laquelle se trouve le gestionnaire de terminaisons. Cela signifie que le bloc **\_ \_ finally** peut accéder aux variables locales de cette fonction. L’exécution du bloc **\_ \_ finally** peut se terminer de l’une des manières suivantes.

-   Exécution de la dernière instruction dans le bloc et continuation à l’instruction suivante
-   Utilisation d’une instruction de contrôle (**Return**, **break**, **continue** ou **goto**)
-   Utilisation de **longjmp** ou d’un saut vers un gestionnaire d’exceptions

Si l’exécution du bloc **\_ \_ try** se termine en raison d’une exception qui appelle le bloc de gestion des exceptions d’un gestionnaire d’exceptions basé sur des frames, le bloc **\_ \_ finally** est exécuté avant l’exécution du bloc de gestion des exceptions. De même, un appel à la fonction de la bibliothèque Runtime C **longjmp** à partir du bloc **\_ \_ try** provoque l’exécution du bloc **\_ \_ finally** avant la reprise de l’exécution à la cible de l’opération **longjmp** . Si l’exécution de bloc **\_ \_ try** se termine en raison d’une instruction de contrôle (**Return**, **break**, **continue** ou **goto**), le bloc **\_ \_ finally** est exécuté.

La fonction [**AbnormalTermination**](abnormaltermination.md) peut être utilisée dans le bloc **\_ \_ finally** pour déterminer si le bloc **\_ \_ try** s’est arrêté séquentiellement, c’est-à-dire s’il a atteint l’accolade fermante (}). Le fait de quitter le bloc **\_ \_ try** en raison d’un appel à **longjmp**, d’un saut à un gestionnaire d’exceptions, ou d’une instruction **Return**, **break**, **continue** ou **goto** , est considéré comme un arrêt anormal. Notez que l’échec de l’arrêt séquentiel fait que le système recherche dans tous les frames de pile dans l’ordre inverse pour déterminer si des gestionnaires de terminaison doivent être appelés. Cela peut entraîner une dégradation des performances en raison de l’exécution de centaines d’instructions.

Pour éviter l’arrêt anormal du gestionnaire de terminaisons, l’exécution doit se poursuivre jusqu’à la fin du bloc. Vous pouvez également exécuter l’instruction **\_ \_ Leave** . L’instruction **\_ \_ Leave** autorise l’arrêt immédiat du bloc **\_ \_ try** sans entraîner un arrêt anormal et une baisse des performances. Consultez la documentation de votre compilateur pour déterminer si l’instruction **\_ \_ Leave** est prise en charge.

Si l’exécution du bloc **\_ \_ finally** se termine en raison de l’instruction de contrôle de **retour** , elle équivaut à une instruction **goto** à l’accolade fermante dans la fonction englobante. Par conséquent, la fonction englobante retourne.

 

 
