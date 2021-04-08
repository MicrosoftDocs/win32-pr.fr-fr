---
title: Mise à disposition du serveur sur le réseau
description: Pour qu’une application serveur puisse accepter des appels de procédure distante, elle doit être disponible sur le réseau.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- Appel de procédure distante RPC, tâches, mise à disposition du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029418"
---
# <a name="making-the-server-available-on-the-network"></a><span data-ttu-id="c2eb9-104">Mise à disposition du serveur sur le réseau</span><span class="sxs-lookup"><span data-stu-id="c2eb9-104">Making the Server Available on the Network</span></span>

<span data-ttu-id="c2eb9-105">Pour qu’une application serveur puisse accepter des appels de procédure distante, elle doit être disponible sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-105">Before a server application can accept remote procedure calls, it must be available on the network.</span></span> <span data-ttu-id="c2eb9-106">Pour ce faire, le serveur indique à la durée d’exécution RPC qu’il est disposé à accepter des appels sur une ou plusieurs séquences de protocole.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-106">To do this, the server indicates to the RPC Run time that it is willing to accept calls on one or more protocol sequences.</span></span> <span data-ttu-id="c2eb9-107">Le choix des séquences de protocole prises en charge par une application serveur est une décision importante. différentes séquences de protocole ont des fonctionnalités très différentes.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-107">Choosing the protocol sequences a server application supports is an important decision; different protocol sequences have very different capabilities.</span></span> <span data-ttu-id="c2eb9-108">Les serveurs qui attendent que les appels soient reçus localement doivent utiliser **Ncalrpc**.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-108">Servers that expect calls to be received locally should use **ncalrpc**.</span></span> <span data-ttu-id="c2eb9-109">Les serveurs qui acceptent les appels distants doivent utiliser **ncacn \_ IP \_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-109">Servers that accept remote calls should use **ncacn\_ip\_tcp**.</span></span> <span data-ttu-id="c2eb9-110">Les serveurs ne doivent pas vérifier que la séquence de protocole sur laquelle ils reçoivent des appels est la séquence de protocole sur laquelle ils s’attendent à recevoir des appels.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-110">Servers should not verify that the protocol sequence on which they receive calls is the protocol sequence on which they expect to receive calls.</span></span> <span data-ttu-id="c2eb9-111">Pour plus d’informations, consultez se méfier des autres points de terminaison RPC s’exécutant dans le même processus dans les meilleures pratiques de programmation RPC.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-111">See Be Wary of Other RPC Endpoints Running in the Same Process in Best RPC Programming Practices for more information.</span></span>

<span data-ttu-id="c2eb9-112">L’exemple suivant utilise **le \_ \_ protocole TCP IP ncacn**.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-112">The following example uses **ncacn\_ip\_tcp**.</span></span>

<span data-ttu-id="c2eb9-113">La plupart des programmes serveur utilisent toutes les séquences de protocole disponibles sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-113">Most server programs use all protocol sequences available on the network.</span></span> <span data-ttu-id="c2eb9-114">Pour ce faire, ils appellent la fonction [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) , comme indiqué dans le fragment de code suivant :</span><span class="sxs-lookup"><span data-stu-id="c2eb9-114">To do this, they invoke the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function, as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



<span data-ttu-id="c2eb9-115">Le premier paramètre de la fonction [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) est la séquence de protocole.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-115">The first parameter to the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function is the protocol sequence.</span></span> <span data-ttu-id="c2eb9-116">Le deuxième paramètre dépend de la séquence de protocole.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-116">The second parameter is dependent on the protocol sequence.</span></span> <span data-ttu-id="c2eb9-117">Comme illustré dans le fragment de code, la plupart des programmes serveur définissent ce paramètre sur **RPC \_ C \_ PROTSEQ Max, demandes \_ \_ \_ par défaut**.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-117">As illustrated in the code fragment, most server programs set this parameter to **RPC\_C\_PROTSEQ\_MAX\_REQS\_DEFAULT**.</span></span> <span data-ttu-id="c2eb9-118">Cette valeur définit la bibliothèque RPC pour utiliser la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-118">This value sets the RPC library to use the default value.</span></span> <span data-ttu-id="c2eb9-119">Le troisième paramètre est un descripteur de sécurité et ne doit pas être utilisé dans les applications.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-119">The third parameter is a security descriptor and should not be used in applications.</span></span> <span data-ttu-id="c2eb9-120">Pour plus d’informations, consultez [**sécurité**](security.md).</span><span class="sxs-lookup"><span data-stu-id="c2eb9-120">For more information, see [**Security**](security.md).</span></span>

<span data-ttu-id="c2eb9-121">Vous pouvez également utiliser les fonctions [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)ou [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) .</span><span class="sxs-lookup"><span data-stu-id="c2eb9-121">You can also use the [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep), or [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) functions.</span></span>

<span data-ttu-id="c2eb9-122">Une fois qu’une application serveur a sélectionné au moins une séquence de protocole, les serveurs qui utilisent des points de terminaison dynamiques doivent créer des informations de liaison pour chaque séquence de protocole qu’elle utilise.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-122">After a server application selects at least one protocol sequence, servers that use dynamic endpoints must create binding information for each protocol sequence it uses.</span></span> <span data-ttu-id="c2eb9-123">Le serveur stocke les informations de liaison dans un vecteur de liaison qu’il peut ensuite exporter vers le service mappeur de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-123">The server stores the binding information in a binding vector that it can then export to the endpoint mapper service.</span></span>

<span data-ttu-id="c2eb9-124">Utilisez la fonction [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) pour obtenir un vecteur de liaison pour l’application serveur, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c2eb9-124">Use the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function to obtain a binding vector for the server application, as shown in the following example:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



<span data-ttu-id="c2eb9-125">Le seul paramètre passé à la fonction [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) est un pointeur vers un pointeur vers une structure de [**\_ \_ vecteurs de liaison RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) .</span><span class="sxs-lookup"><span data-stu-id="c2eb9-125">The only parameter passed to the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function is a pointer to a pointer to an [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) structure.</span></span> <span data-ttu-id="c2eb9-126">La bibliothèque Runtime RPC alloue dynamiquement un tableau de vecteurs de liaison et stocke l’adresse du tableau dans la variable de paramètre (dans ce cas, **rpcBindingVector**).</span><span class="sxs-lookup"><span data-stu-id="c2eb9-126">The RPC run-time library dynamically allocates an array of binding vectors and stores the address of the array in the parameter variable (in this case, **rpcBindingVector**).</span></span> <span data-ttu-id="c2eb9-127">Chaque application serveur est chargée de libérer ce vecteur de liaison à l’aide de la fonction [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) une fois qu’il a fini de l’utiliser (par exemple, après l’avoir passé aux fonctions appropriées).</span><span class="sxs-lookup"><span data-stu-id="c2eb9-127">Each server application is responsible for freeing this binding vector using the [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) function once it has finished using it (for example, after it has passed it to the appropriate functions).</span></span>

 

 




