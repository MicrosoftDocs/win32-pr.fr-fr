---
title: L'application cliente
description: L’exemple ci-dessous provient de l’application « Hello World » dans le \\ répertoire RPC Hello du kit de développement logiciel (SDK) de la plateforme.
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f97c7c35e00d3f36c645bfad2825dbada5e3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463606"
---
# <a name="the-client-application"></a><span data-ttu-id="c20ad-103">L'application cliente</span><span class="sxs-lookup"><span data-stu-id="c20ad-103">The Client Application</span></span>

<span data-ttu-id="c20ad-104">L’exemple ci-dessous provient de l’application « Hello World » dans le \\ répertoire RPC Hello du kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="c20ad-104">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="c20ad-105">Le fichier source HELLOC. c contient une directive pour inclure le fichier d’en-tête généré par MIDL, Hello. h.</span><span class="sxs-lookup"><span data-stu-id="c20ad-105">The Helloc.c source file contains a directive to include the MIDL-generated header file, Hello.h.</span></span> <span data-ttu-id="c20ad-106">Dans Hello. h, les directives incluent RPC. h et Rpcndr. h, qui contiennent les définitions des routines d’exécution RPC, **HelloProc** et **Shutdown**, ainsi que les types de données utilisés par les applications clientes et serveur.</span><span class="sxs-lookup"><span data-stu-id="c20ad-106">Within Hello.h are directives to include Rpc.h and rpcndr.h, which contain the definitions for the RPC run-time routines, **HelloProc** and **Shutdown**, and data types that the client and server applications use.</span></span> <span data-ttu-id="c20ad-107">Le compilateur MIDL doit être utilisé avec l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c20ad-107">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="c20ad-108">Étant donné que le client gère sa connexion au serveur, l’application cliente appelle des fonctions d’exécution pour établir un handle vers le serveur et pour libérer ce handle une fois les appels de procédure distante terminés.</span><span class="sxs-lookup"><span data-stu-id="c20ad-108">Because the client is managing its connection to the server, the client application calls run-time functions to establish a handle to the server and to release this handle after the remote procedure calls are complete.</span></span> <span data-ttu-id="c20ad-109">La fonction [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combine les composants du handle de liaison dans une représentation sous forme de chaîne de ce handle et alloue de la mémoire pour la liaison de chaîne.</span><span class="sxs-lookup"><span data-stu-id="c20ad-109">The function [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combines the components of the binding handle into a string representation of that handle and allocates memory for the string binding.</span></span> <span data-ttu-id="c20ad-110">La fonction [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) crée un handle de liaison de serveur, **Hello \_ ClientIfHandle**, pour l’application cliente à partir de cette représentation sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="c20ad-110">The function [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) creates a server binding handle, **hello\_ClientIfHandle**, for the client application from that string representation.</span></span>

<span data-ttu-id="c20ad-111">Dans l’appel à [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), les paramètres ne spécifient pas l’UUID, car ce didacticiel suppose qu’il n’existe qu’une seule implémentation de l’interface « Hello ».</span><span class="sxs-lookup"><span data-stu-id="c20ad-111">In the call to [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), the parameters do not specify the UUID because this tutorial assumes there is just one implementation of the interface "hello."</span></span> <span data-ttu-id="c20ad-112">En outre, l’appel ne spécifie pas d’adresse réseau, car l’application utilisera la valeur par défaut, qui est l’ordinateur hôte local.</span><span class="sxs-lookup"><span data-stu-id="c20ad-112">In addition, the call does not specify a network address because the application will use the default, which is the local host machine.</span></span> <span data-ttu-id="c20ad-113">La séquence de protocole est une chaîne de caractères qui représente le transport réseau sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="c20ad-113">The protocol sequence is a character string that represents the underlying network transport.</span></span> <span data-ttu-id="c20ad-114">Le point de terminaison est un nom qui est spécifique à la séquence de protocole.</span><span class="sxs-lookup"><span data-stu-id="c20ad-114">The endpoint is a name which is specific to the protocol sequence.</span></span> <span data-ttu-id="c20ad-115">Cet exemple utilise des canaux nommés pour son transport réseau. la séquence de protocole est donc « ncacn \_ NP ».</span><span class="sxs-lookup"><span data-stu-id="c20ad-115">This example uses named pipes for its network transport, so the protocol sequence is "ncacn\_np".</span></span> <span data-ttu-id="c20ad-116">Le nom du point de terminaison est « \\ pipe \\ Hello ».</span><span class="sxs-lookup"><span data-stu-id="c20ad-116">The endpoint name is "\\pipe\\hello".</span></span>

<span data-ttu-id="c20ad-117">Les appels de procédure distante, **HelloProc** et **Shutdown**, ont lieu dans le gestionnaire d’exceptions RPC, un ensemble de macros qui vous permettent de contrôler les exceptions qui se produisent en dehors du code de l’application.</span><span class="sxs-lookup"><span data-stu-id="c20ad-117">The actual remote procedure calls, **HelloProc** and **Shutdown**, take place within the RPC exception handler—a set of macros that let you control exceptions that occur outside the application code.</span></span> <span data-ttu-id="c20ad-118">Si le module d’exécution RPC signale une exception, le contrôle passe au bloc [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) .</span><span class="sxs-lookup"><span data-stu-id="c20ad-118">If the RPC run-time module reports an exception, control passes to the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) block.</span></span> <span data-ttu-id="c20ad-119">C’est là que vous insérez le code pour effectuer tout nettoyage nécessaire, puis quitter correctement.</span><span class="sxs-lookup"><span data-stu-id="c20ad-119">This is where you would insert code to do any needed cleanup and then exit gracefully.</span></span> <span data-ttu-id="c20ad-120">Cet exemple de programme informe simplement l’utilisateur qu’une exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c20ad-120">This example program simply informs the user that an exception occurred.</span></span> <span data-ttu-id="c20ad-121">Si vous ne souhaitez pas utiliser d’exceptions, vous pouvez utiliser les attributs ACF [ \_ État comm](/windows/desktop/Midl/comm-status) et [ \_ État d’erreur](/windows/desktop/Midl/fault-status) pour signaler des erreurs.</span><span class="sxs-lookup"><span data-stu-id="c20ad-121">If you do not want to use exceptions, you can use the ACF attributes [comm\_status](/windows/desktop/Midl/comm-status) and [fault\_status](/windows/desktop/Midl/fault-status) to report errors.</span></span>

<span data-ttu-id="c20ad-122">Une fois les appels de procédure distante terminés, le client appelle d’abord [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) pour libérer la mémoire qui a été allouée pour la liaison de chaîne.</span><span class="sxs-lookup"><span data-stu-id="c20ad-122">After the remote procedure calls are completed, the client first calls [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) to free the memory that was allocated for the string binding.</span></span> <span data-ttu-id="c20ad-123">Notez qu’une fois que le handle de liaison a été créé, un programme client peut libérer une liaison de chaîne à tout moment.</span><span class="sxs-lookup"><span data-stu-id="c20ad-123">Note that once the binding handle has been created, a client program can free a string binding at any time.</span></span> <span data-ttu-id="c20ad-124">Le client appelle ensuite [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) pour libérer le handle.</span><span class="sxs-lookup"><span data-stu-id="c20ad-124">The client next calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to release the handle.</span></span>


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



 

 