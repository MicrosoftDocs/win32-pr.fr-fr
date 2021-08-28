---
title: L'application cliente
description: Affichez la partie application cliente d’un exemple d’appel de procédure distante (RPC). L’exemple ci-dessous provient de l’application « Hello World » dans le kit de développement logiciel (SDK) de plateforme.
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570e883d908a12a053052945675e8819c3dbdcc8bb6a30fba787f1f62c49e9e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924548"
---
# <a name="the-client-application"></a>L'application cliente

L’exemple ci-dessous provient de l’application « Hello World » dans le \\ répertoire RPC Hello du kit de développement logiciel (SDK) de la plateforme. Le fichier source HELLOC. c contient une directive pour inclure le fichier d’en-tête généré par MIDL, Hello. h. Dans Hello. h, les directives incluent RPC. h et Rpcndr. h, qui contiennent les définitions des routines d’exécution RPC, **HelloProc** et **Shutdown**, ainsi que les types de données utilisés par les applications clientes et serveur. Le compilateur MIDL doit être utilisé avec l’exemple ci-dessous.

Étant donné que le client gère sa connexion au serveur, l’application cliente appelle des fonctions d’exécution pour établir un handle vers le serveur et pour libérer ce handle une fois les appels de procédure distante terminés. La fonction [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combine les composants du handle de liaison dans une représentation sous forme de chaîne de ce handle et alloue de la mémoire pour la liaison de chaîne. La fonction [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) crée un handle de liaison de serveur, **Hello \_ ClientIfHandle**, pour l’application cliente à partir de cette représentation sous forme de chaîne.

Dans l’appel à [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), les paramètres ne spécifient pas l’UUID, car ce didacticiel suppose qu’il n’existe qu’une seule implémentation de l’interface « Hello ». En outre, l’appel ne spécifie pas d’adresse réseau, car l’application utilisera la valeur par défaut, qui est l’ordinateur hôte local. La séquence de protocole est une chaîne de caractères qui représente le transport réseau sous-jacent. Le point de terminaison est un nom qui est spécifique à la séquence de protocole. Cet exemple utilise des canaux nommés pour son transport réseau. la séquence de protocole est donc « ncacn \_ NP ». Le nom du point de terminaison est « \\ pipe \\ Hello ».

Les appels de procédure distante, **HelloProc** et **Shutdown**, ont lieu dans le gestionnaire d’exceptions RPC, un ensemble de macros qui vous permettent de contrôler les exceptions qui se produisent en dehors du code de l’application. Si le module d’exécution RPC signale une exception, le contrôle passe au bloc [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) . C’est là que vous insérez le code pour effectuer tout nettoyage nécessaire, puis quitter correctement. Cet exemple de programme informe simplement l’utilisateur qu’une exception s’est produite. Si vous ne souhaitez pas utiliser d’exceptions, vous pouvez utiliser les attributs ACF [ \_ État comm](/windows/desktop/Midl/comm-status) et [ \_ État d’erreur](/windows/desktop/Midl/fault-status) pour signaler des erreurs.

Une fois les appels de procédure distante terminés, le client appelle d’abord [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) pour libérer la mémoire qui a été allouée pour la liaison de chaîne. Notez qu’une fois que le handle de liaison a été créé, un programme client peut libérer une liaison de chaîne à tout moment. Le client appelle ensuite [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) pour libérer le handle.


```C++
/* file: helloc.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h" 
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszUuid             = NULL;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszNetworkAddress   = NULL;
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned char * pszOptions          = NULL;
    unsigned char * pszStringBinding    = NULL;
    unsigned char * pszString           = "hello, world";
    unsigned long ulCode;
 
    status = RpcStringBindingCompose(pszUuid,
                                     pszProtocolSequence,
                                     pszNetworkAddress,
                                     pszEndpoint,
                                     pszOptions,
                                     &pszStringBinding);
    if (status) exit(status);

    status = RpcBindingFromStringBinding(pszStringBinding, &hello_ClientIfHandle);
 
    if (status) exit(status);
 
    RpcTryExcept  
    {
        HelloProc(pszString);
        Shutdown();
    }
    RpcExcept(1) 
    {
        ulCode = RpcExceptionCode();
        printf("Runtime reported exception 0x%lx = %ld\n", ulCode, ulCode);
    }
    RpcEndExcept
 
    status = RpcStringFree(&pszStringBinding); 
 
    if (status) exit(status);
 
    status = RpcBindingFree(&hello_IfHandle);
 
    if (status) exit(status);

    exit(0);
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



 

 