---
title: Application serveur
description: L’exemple ci-dessous provient de l’application « Hello World » dans le \\ répertoire RPC Hello du kit de développement logiciel (SDK) de la plateforme.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6f13e2c8fecdcff820c62f3076dd2a8edd1a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840081"
---
# <a name="the-server-application"></a><span data-ttu-id="79a0a-103">Application serveur</span><span class="sxs-lookup"><span data-stu-id="79a0a-103">The Server Application</span></span>

<span data-ttu-id="79a0a-104">L’exemple ci-dessous provient de l’application « Hello World » dans le \\ répertoire RPC Hello du kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="79a0a-104">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="79a0a-105">Le côté serveur de l’application distribuée informe le système que ses services sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="79a0a-105">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="79a0a-106">Il attend ensuite les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="79a0a-106">It then waits for client requests.</span></span> <span data-ttu-id="79a0a-107">Le compilateur MIDL doit être utilisé avec l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="79a0a-107">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="79a0a-108">Selon la taille de votre application et vos préférences de codage, vous pouvez choisir d’implémenter des procédures distantes dans un ou plusieurs fichiers distincts.</span><span class="sxs-lookup"><span data-stu-id="79a0a-108">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="79a0a-109">Dans ce didacticiel, le fichier source hellos. c contient la routine principale du serveur.</span><span class="sxs-lookup"><span data-stu-id="79a0a-109">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="79a0a-110">Le fichier Hellop. c contient la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="79a0a-110">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="79a0a-111">L’Organisation des procédures distantes dans des fichiers distincts présente l’avantage de pouvoir lier les procédures à un programme autonome pour déboguer le code avant qu’il ne soit converti en application distribuée.</span><span class="sxs-lookup"><span data-stu-id="79a0a-111">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="79a0a-112">Une fois les procédures opérationnelles dans le programme autonome, vous pouvez compiler et lier les fichiers sources contenant les procédures distantes avec l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="79a0a-112">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="79a0a-113">Comme pour le fichier source de l’application cliente, le fichier source de l’application serveur doit inclure le fichier d’en-tête Hello. h.</span><span class="sxs-lookup"><span data-stu-id="79a0a-113">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="79a0a-114">Le serveur appelle les fonctions runtime RPC [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) et [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) pour rendre les informations de liaison disponibles pour le client.</span><span class="sxs-lookup"><span data-stu-id="79a0a-114">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="79a0a-115">Cet exemple de programme transmet le nom du handle d’interface à **RpcServerRegisterIf**.</span><span class="sxs-lookup"><span data-stu-id="79a0a-115">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="79a0a-116">Les autres paramètres ont la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="79a0a-116">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="79a0a-117">Le serveur appelle ensuite la fonction [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) pour indiquer qu’il attend les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="79a0a-117">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="79a0a-118">L’application serveur doit également inclure les deux fonctions de gestion de la mémoire que le stub serveur appelle : l' [**\_ \_ allocation d’utilisateur MIDL**](the-midl-user-allocate-function.md) et l' [**\_ utilisateur MIDL \_ gratuit**](the-midl-user-free-function.md).</span><span class="sxs-lookup"><span data-stu-id="79a0a-118">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="79a0a-119">Ces fonctions allouent et libèrent de la mémoire sur le serveur lorsqu’une procédure distante transmet des paramètres au serveur.</span><span class="sxs-lookup"><span data-stu-id="79a0a-119">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="79a0a-120">Dans cet exemple de programme **, MIDL \_ User \_ allocate** et **MIDL \_ User \_ Free** sont simplement des wrappers pour les fonctions de la bibliothèque C [**malloc**](pointers-and-memory-allocation.md) et **Free**.</span><span class="sxs-lookup"><span data-stu-id="79a0a-120">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="79a0a-121">(Notez que, dans les déclarations anticipées générées par le compilateur MIDL, « MIDL » est en majuscules.</span><span class="sxs-lookup"><span data-stu-id="79a0a-121">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="79a0a-122">Le fichier d’en-tête Rpcndr. h définit les allocations de l’utilisateur MIDL \_ \_ et gratuit de l’utilisateur pour qu’il soit attribué à l’utilisateur MIDL et au MIDL l' \_ \_ allocation utilisateur \_ \_ \_ \_ , respectivement.)</span><span class="sxs-lookup"><span data-stu-id="79a0a-122">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


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



 

 




