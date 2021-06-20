---
title: Application serveur
description: Affichez la partie application serveur d’un exemple d’appel de procédure distante (RPC). L’exemple provient de l’application « Hello World » dans le kit de développement logiciel (SDK) de plateforme.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b8a2bb66fd415a9b8f778134edb4903f88a717
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406062"
---
# <a name="the-server-application"></a><span data-ttu-id="9d14c-104">Application serveur</span><span class="sxs-lookup"><span data-stu-id="9d14c-104">The Server Application</span></span>

<span data-ttu-id="9d14c-105">L’exemple ci-dessous provient de l’application « Hello World » dans le \\ répertoire RPC Hello du kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="9d14c-105">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="9d14c-106">Le côté serveur de l’application distribuée informe le système que ses services sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="9d14c-106">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="9d14c-107">Il attend ensuite les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="9d14c-107">It then waits for client requests.</span></span> <span data-ttu-id="9d14c-108">Le compilateur MIDL doit être utilisé avec l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9d14c-108">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="9d14c-109">Selon la taille de votre application et vos préférences de codage, vous pouvez choisir d’implémenter des procédures distantes dans un ou plusieurs fichiers distincts.</span><span class="sxs-lookup"><span data-stu-id="9d14c-109">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="9d14c-110">Dans ce didacticiel, le fichier source hellos. c contient la routine principale du serveur.</span><span class="sxs-lookup"><span data-stu-id="9d14c-110">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="9d14c-111">Le fichier Hellop. c contient la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="9d14c-111">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="9d14c-112">L’Organisation des procédures distantes dans des fichiers distincts présente l’avantage de pouvoir lier les procédures à un programme autonome pour déboguer le code avant qu’il ne soit converti en application distribuée.</span><span class="sxs-lookup"><span data-stu-id="9d14c-112">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="9d14c-113">Une fois les procédures opérationnelles dans le programme autonome, vous pouvez compiler et lier les fichiers sources contenant les procédures distantes avec l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="9d14c-113">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="9d14c-114">Comme pour le fichier source de l’application cliente, le fichier source de l’application serveur doit inclure le fichier d’en-tête Hello. h.</span><span class="sxs-lookup"><span data-stu-id="9d14c-114">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="9d14c-115">Le serveur appelle les fonctions runtime RPC [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) et [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) pour rendre les informations de liaison disponibles pour le client.</span><span class="sxs-lookup"><span data-stu-id="9d14c-115">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="9d14c-116">Cet exemple de programme transmet le nom du handle d’interface à **RpcServerRegisterIf**.</span><span class="sxs-lookup"><span data-stu-id="9d14c-116">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="9d14c-117">Les autres paramètres ont la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="9d14c-117">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="9d14c-118">Le serveur appelle ensuite la fonction [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) pour indiquer qu’il attend les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="9d14c-118">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="9d14c-119">L’application serveur doit également inclure les deux fonctions de gestion de la mémoire que le stub serveur appelle : l' [**\_ \_ allocation d’utilisateur MIDL**](the-midl-user-allocate-function.md) et l' [**\_ utilisateur MIDL \_ gratuit**](the-midl-user-free-function.md).</span><span class="sxs-lookup"><span data-stu-id="9d14c-119">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="9d14c-120">Ces fonctions allouent et libèrent de la mémoire sur le serveur lorsqu’une procédure distante transmet des paramètres au serveur.</span><span class="sxs-lookup"><span data-stu-id="9d14c-120">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="9d14c-121">Dans cet exemple de programme **, MIDL \_ User \_ allocate** et **MIDL \_ User \_ Free** sont simplement des wrappers pour les fonctions de la bibliothèque C [**malloc**](pointers-and-memory-allocation.md) et **Free**.</span><span class="sxs-lookup"><span data-stu-id="9d14c-121">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="9d14c-122">(Notez que, dans les déclarations anticipées générées par le compilateur MIDL, « MIDL » est en majuscules.</span><span class="sxs-lookup"><span data-stu-id="9d14c-122">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="9d14c-123">Le fichier d’en-tête Rpcndr. h définit les allocations de l’utilisateur MIDL \_ \_ et gratuit de l’utilisateur pour qu’il soit attribué à l’utilisateur MIDL et au MIDL l' \_ \_ allocation utilisateur \_ \_ \_ \_ , respectivement.)</span><span class="sxs-lookup"><span data-stu-id="9d14c-123">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


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



 

 




