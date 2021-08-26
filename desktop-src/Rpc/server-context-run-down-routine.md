---
title: Routine d’exécution du contexte de serveur
description: Si la communication s’arrête alors que le serveur gère le contexte pour le compte du client, une routine de nettoyage peut être nécessaire pour nettoyer l’état géré par le serveur pour le compte d’un client donné.
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3bab4477555e5a304627d026c7471874af50daceb9fe3e4484928c290a55d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035489"
---
# <a name="server-context-run-down-routine"></a>Routine d’exécution du contexte de serveur

Si la communication s’arrête alors que le serveur gère le contexte pour le compte du client, une routine de nettoyage peut être nécessaire pour nettoyer l’état géré par le serveur pour le compte d’un client donné. Cette routine de nettoyage est appelée « *routine d’exécution de contexte »*. Lorsqu’une connexion est interrompue, le stub serveur et la bibliothèque Runtime appellent cette routine sur chaque handle de contexte ouvert par le client.

La routine d’exécution de contexte est obligatoire, et est déclarée implicitement et nommée, lorsque vous appliquez l' \[ attribut de **\_ handle de contexte** \] à une définition de type. Le serveur n’appellera pas la routine d’exécution de contexte si l' \[ attribut de **\_ handle de contexte** \] était appliqué directement à un paramètre.

La syntaxe de la routine d’exécution de contexte est la suivante :

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

Notez que le nom du type détermine le nom de la routine d’exécution du contexte.

Le fragment de code qui suit présente un exemple de routine d’exécution de contexte. qui appelle la procédure RemoteClose utilisée dans l’exemple dans le [développement d’interface à l’aide de handles de contexte](interface-development-using-context-handles.md), le [développement serveur à l’aide de handles de contexte](server-development-using-context-handles.md)et le [développement client à l’aide de handles de contexte](client-development-using-context-handles.md). Cette procédure ferme le descripteur de fichier, libère la mémoire associée au fichier et assigne la **valeur null** au handle de contexte. L’attribution de la **valeur null** est le résultat de l’appel de la fonction RemoteClose et n’est pas nécessaire dans un scénario d’exécution. L’heure d’exécution RPC nettoie son état, que le handle de contexte ait la valeur **null** ou non.

``` syntax
//file: cxhndp.c (fragment of file containing remote procedures)
//The rundown routine is associated with the context handle type.  
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown(
    PCONTEXT_HANDLE_TYPE phContext)
{
    printf("Client died with an open file, closing it..\n");
    RemoteClose(&phContext);
    assert(phContext == 0);
}
```

 

 




