---
title: Développement d’interface à l’aide de handles de contexte
description: En général, vous créez un handle de contexte en spécifiant l’attribut \ Context \_ handle \ sur une définition de type dans le fichier IDL.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8474d533b27ba1543a9d522dfa4478d306b33cf2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729309"
---
# <a name="interface-development-using-context-handles"></a>Développement d’interface à l’aide de handles de contexte

En général, vous créez un handle de contexte en spécifiant l' \[ attribut de [**\_ handle de contexte**](/windows/desktop/Midl/context-handle) \] sur une définition de type dans le fichier IDL. La définition de type spécifie également implicitement une routine d’exécution de contexte, que vous devez fournir. Si la communication entre le client et le serveur est interrompue, le temps d’exécution du serveur appelle cette routine pour effectuer tout nettoyage nécessaire. Pour plus d’informations sur les routines d’exécution de contexte, consultez [routine de fonctionnement du contexte de serveur](server-context-run-down-routine.md).

Une interface qui utilise un handle de contexte doit avoir un handle de liaison pour la liaison initiale, qui doit avoir lieu avant que le serveur puisse retourner un handle de contexte. Vous pouvez utiliser un handle de liaison automatique, implicite ou explicite pour créer la liaison et établir le contexte.

Un handle de contexte doit être du [**type \* void**](/windows/desktop/Midl/void) , ou un type qui est résolu en [**void \***](/windows/desktop/Midl/void). Le programme serveur le convertit en type requis.

> [!Note]  
> L’utilisation de \[ [**dans**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] pour les paramètres de handle de contexte est déconseillée, sauf pour les routines qui ferment des handles de contexte. Si le contexte gère les paramètres marqués \[ [**dans**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] sont utilisés, ne transmettez pas un descripteur de contexte **null** ou non initialisé du client au serveur. Un pointeur **null** vers un handle de contexte doit être passé à la place. Veuillez noter que les paramètres de handle de contexte marqués \[ [**dans**](/windows/desktop/Midl/in) \] n’acceptent pas les pointeurs **null** .

 

Le fragment suivant d’un exemple de définition d’interface montre comment une application distribuée peut utiliser un handle de contexte pour qu’un serveur ouvre et met à jour un fichier de données pour chaque client.

L’interface doit contenir un appel de procédure distante pour initialiser le handle et lui affecter une valeur non **null** . Dans cet exemple, la fonction RemoteOpen effectue cette opération. Elle spécifie le handle de contexte avec un \[ [](/windows/desktop/Midl/out-idl) \] attribut directionnel out. Vous pouvez également retourner le descripteur de contexte comme valeur de retour de la procédure. Toutefois, dans cet exemple, nous passons le descripteur de contexte par le biais de la liste de paramètres.

Dans cet exemple, les informations de contexte sont un descripteur de fichier. Il effectue le suivi de l’emplacement actuel dans le fichier. L’interface empaquette le descripteur de fichier comme handle de contexte et le passe en tant que paramètre aux appels de procédure distante. Une structure contient le nom de fichier et le descripteur de fichier.

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

La fonction RemoteOpen crée un handle de contexte valide non **null** . Il passe le descripteur de contexte au client. Les appels de procédure distante suivants, tels que RemoteRead, utilisent le handle de contexte en tant que pointeur.

En plus de la procédure distante qui initialise le descripteur de contexte, l’interface doit contenir une procédure qui libère le contexte du serveur et définit le descripteur de contexte sur la **valeur null**. Dans l’exemple précédent, la fonction RemoteClose effectue cette opération.

 

 