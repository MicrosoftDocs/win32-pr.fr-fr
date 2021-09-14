---
title: Initialisation de la bibliothèque COM
description: Initialisation de la bibliothèque COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094378"
---
# <a name="initializing-the-com-library"></a>Initialisation de la bibliothèque COM

tout programme Windows qui utilise com doit initialiser la bibliothèque com en appelant la fonction [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) . Chaque thread qui utilise une interface COM doit effectuer un appel distinct à cette fonction. **CoInitializeEx** a la signature suivante :


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



Le premier paramètre est réservé et doit avoir la **valeur null**. Le deuxième paramètre spécifie le modèle de thread utilisé par votre programme. COM prend en charge deux *modèles de thread* différents, *thread cloisonné et multithread* . Si vous spécifiez un thread cloisonné, vous effectuez les garanties suivantes :

-   Vous allez accéder à chaque objet COM à partir d’un seul thread. vous ne partagez pas les pointeurs d’interface COM entre plusieurs threads.
-   Le thread aura une boucle de message. (Voir [messages de fenêtre](window-messages.md) dans le module 1.)

Si l’une de ces contraintes n’est pas vraie, utilisez le modèle multithread. Pour spécifier le modèle de thread, définissez l’un des indicateurs suivants dans le paramètre *dwCoInit* .



| Indicateur                          | Description         |
|-------------------------------|---------------------|
| **APARTMENTTHREADED coinit \_** | Thread cloisonné. |
| **coinit \_ multithread**     | Multithread.      |



 

Vous devez définir exactement l’un de ces indicateurs. En règle générale, un thread qui crée une fenêtre doit utiliser l’indicateur **coinit \_ APARTMENTTHREADED** et les autres threads doivent utiliser la **coinit \_ multithread**. Toutefois, certains composants COM requièrent un modèle de thread particulier. La documentation MSDN doit vous indiquer quand c’est le cas.

> [!Note]  
> En fait, même si vous spécifiez un thread cloisonné, il est toujours possible de partager des interfaces entre les threads, à l’aide d’une technique appelée *marshaling*. Le marshaling n’entre pas dans le cadre de ce module. Le point important est qu’avec le thread cloisonné, vous ne devez jamais simplement copier un pointeur d’interface vers un autre thread. Pour plus d’informations sur les modèles de threads COM, consultez [processus, threads et Apartments](/windows/desktop/com/processes--threads--and-apartments).

 

En plus des indicateurs déjà mentionnés, il est judicieux de définir l’indicateur **coinit \_ Disable \_ OLE1DDE** dans le paramètre *dwCoInit* . La définition de cet indicateur évite une surcharge liée à la liaison et à l’incorporation d’objets (OLE) 1,0, une technologie obsolète.

Voici comment initialiser COM pour le thread cloisonné :


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



Le type de retour **HRESULT** contient un code d’erreur ou de réussite. Nous allons examiner la gestion des erreurs COM dans la section suivante.

## <a name="uninitializing-the-com-library"></a>Désinitialisation de la bibliothèque COM

Pour chaque appel réussi à [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), vous devez appeler [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) avant que le thread ne se termine. Cette fonction n’accepte aucun paramètre et n’a pas de valeur de retour.


```C++
CoUninitialize();
```



## <a name="next"></a>Suivant

[Codes d’erreur dans COM](error-codes-in-com.md)

 

 