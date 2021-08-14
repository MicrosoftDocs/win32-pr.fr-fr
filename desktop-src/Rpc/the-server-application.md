---
title: Application serveur
description: Affichez la partie application serveur d’un exemple d’appel de procédure distante (RPC). L’exemple provient de l’application « Hello World » dans le kit de développement logiciel (SDK) de plateforme.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c393e16a4c26b39efb95d23a2745f75cbeb984cac466c869046f9775f94c80c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923988"
---
# <a name="the-server-application"></a>Application serveur

L’exemple ci-dessous provient de l’application « Hello World » dans le \\ répertoire RPC Hello du kit de développement logiciel (SDK) de la plateforme. Le côté serveur de l’application distribuée informe le système que ses services sont disponibles. Il attend ensuite les demandes des clients. Le compilateur MIDL doit être utilisé avec l’exemple ci-dessous.

Selon la taille de votre application et vos préférences de codage, vous pouvez choisir d’implémenter des procédures distantes dans un ou plusieurs fichiers distincts. Dans ce didacticiel, le fichier source hellos. c contient la routine principale du serveur. Le fichier Hellop. c contient la procédure distante.

L’Organisation des procédures distantes dans des fichiers distincts présente l’avantage de pouvoir lier les procédures à un programme autonome pour déboguer le code avant qu’il ne soit converti en application distribuée. Une fois les procédures opérationnelles dans le programme autonome, vous pouvez compiler et lier les fichiers sources contenant les procédures distantes avec l’application serveur. Comme pour le fichier source de l’application cliente, le fichier source de l’application serveur doit inclure le fichier d’en-tête Hello. h.

Le serveur appelle les fonctions runtime RPC [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) et [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) pour rendre les informations de liaison disponibles pour le client. Cet exemple de programme transmet le nom du handle d’interface à **RpcServerRegisterIf**. Les autres paramètres ont la valeur **null**. Le serveur appelle ensuite la fonction [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) pour indiquer qu’il attend les demandes des clients.

L’application serveur doit également inclure les deux fonctions de gestion de la mémoire que le stub serveur appelle : l' [**\_ \_ allocation d’utilisateur MIDL**](the-midl-user-allocate-function.md) et l' [**\_ utilisateur MIDL \_ gratuit**](the-midl-user-free-function.md). Ces fonctions allouent et libèrent de la mémoire sur le serveur lorsqu’une procédure distante transmet des paramètres au serveur. Dans cet exemple de programme **, MIDL \_ User \_ allocate** et **MIDL \_ User \_ Free** sont simplement des wrappers pour les fonctions de la bibliothèque C [**malloc**](pointers-and-memory-allocation.md) et **Free**. (Notez que, dans les déclarations anticipées générées par le compilateur MIDL, « MIDL » est en majuscules. Le fichier d’en-tête Rpcndr. h définit les allocations de l’utilisateur MIDL \_ \_ et gratuit de l’utilisateur pour qu’il soit attribué à l’utilisateur MIDL et au MIDL l' \_ \_ allocation utilisateur \_ \_ \_ \_ , respectivement.)


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
 }

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 




