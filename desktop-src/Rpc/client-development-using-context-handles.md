---
title: Développement de clients à l’aide de handles de contexte
description: La seule utilisation d’un programme client pour un handle de contexte consiste à le passer au serveur chaque fois que le client effectue un appel de procédure distante.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ff599bebdf042bc2021d53538cff1c0203d2de875bdc52c50a72675b73a47f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931840"
---
# <a name="client-development-using-context-handles"></a>Développement de clients à l’aide de handles de contexte

La seule utilisation d’un programme client pour un handle de contexte consiste à le passer au serveur chaque fois que le client effectue un appel de procédure distante. L’application cliente n’a pas besoin d’accéder au contenu du descripteur. Il ne doit pas essayer de modifier les données de handle de contexte de quelque manière que ce soit. Les procédures distantes appelées par le client effectuent toutes les opérations nécessaires sur le contexte du serveur.

Avant de demander un handle de contexte à partir d’un serveur, les clients doivent établir une liaison avec le serveur. Le client peut utiliser un handle de liaison automatique, implicite ou explicite. Avec un handle de liaison valide, le client peut appeler une procédure distante sur le serveur qui retourne un handle de contexte ouvert (non **null**) ou passe un par un paramètre **\[ out \]** dans la liste de paramètres de la procédure distante.

Les clients peuvent utiliser les descripteurs de contexte ouverts de la manière dont ils ont besoin. Toutefois, ils doivent invalider le descripteur lorsqu’il n’en a plus besoin. Il existe deux façons de procéder :

-   Pour appeler une procédure distante offerte par le programme serveur qui libère le contexte et ferme le descripteur de contexte (affecte la **valeur null**).
-   Lorsque le serveur est inaccessible, appelez la fonction [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .

La deuxième approche nettoie uniquement l’État côté client et ne nettoie pas l’État côté serveur. elle doit donc être utilisée uniquement lorsque la partition réseau est suspectée et que le client et le serveur effectuent un nettoyage indépendant. Le serveur effectue un nettoyage indépendant par le biais de la routine d’exécution, le client le fait à l’aide de la fonction [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .

Le fragment de code suivant présente un exemple de la façon dont un client peut utiliser un handle de contexte. Pour afficher la définition de l’interface utilisée par cet exemple, consultez [développement d’interface à l’aide de handles de contexte](interface-development-using-context-handles.md). Pour l’implémentation de serveur, consultez [développement de serveurs à l’aide de handles de contexte](server-development-using-context-handles.md).

Dans cet exemple, le client appelle RemoteOpen pour obtenir un handle de contexte qui contient des données valides. Le client peut ensuite utiliser le handle de contexte dans les appels de procédure distante. Étant donné qu’il n’a plus besoin du handle de liaison, le client peut libérer le handle explicite utilisé pour créer le handle de contexte :


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



Dans cet exemple, l’application cliente utilise une procédure appelée RemoteRead pour lire un fichier de données sur le serveur jusqu’à ce qu’il rencontre une fin de fichier. Il ferme ensuite le fichier en appelant RemoteClose. Le descripteur de contexte apparaît en tant que paramètre dans les fonctions RemoteRead et RemoteClose, comme suit :


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




