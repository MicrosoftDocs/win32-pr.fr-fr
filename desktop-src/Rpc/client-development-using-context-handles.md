---
title: Développement de clients à l’aide de handles de contexte
description: La seule utilisation d’un programme client pour un handle de contexte consiste à le passer au serveur chaque fois que le client effectue un appel de procédure distante.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c7d2dfca901085c743b25eb233ee2493b893e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507378"
---
# <a name="client-development-using-context-handles"></a><span data-ttu-id="e014d-103">Développement de clients à l’aide de handles de contexte</span><span class="sxs-lookup"><span data-stu-id="e014d-103">Client Development Using Context Handles</span></span>

<span data-ttu-id="e014d-104">La seule utilisation d’un programme client pour un handle de contexte consiste à le passer au serveur chaque fois que le client effectue un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="e014d-104">The only use a client program has for a context handle is to pass it to the server each time the client makes a remote procedure call.</span></span> <span data-ttu-id="e014d-105">L’application cliente n’a pas besoin d’accéder au contenu du descripteur.</span><span class="sxs-lookup"><span data-stu-id="e014d-105">The client application does not need to access the contents of the handle.</span></span> <span data-ttu-id="e014d-106">Il ne doit pas essayer de modifier les données de handle de contexte de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="e014d-106">It should not try to change the context handle data in any way.</span></span> <span data-ttu-id="e014d-107">Les procédures distantes appelées par le client effectuent toutes les opérations nécessaires sur le contexte du serveur.</span><span class="sxs-lookup"><span data-stu-id="e014d-107">The remote procedures that the client invokes perform all necessary operations on the server's context.</span></span>

<span data-ttu-id="e014d-108">Avant de demander un handle de contexte à partir d’un serveur, les clients doivent établir une liaison avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="e014d-108">Prior to requesting a context handle from a server, clients must establish a binding with the server.</span></span> <span data-ttu-id="e014d-109">Le client peut utiliser un handle de liaison automatique, implicite ou explicite.</span><span class="sxs-lookup"><span data-stu-id="e014d-109">The client may use an automatic, implicit, or explicit binding handle.</span></span> <span data-ttu-id="e014d-110">Avec un handle de liaison valide, le client peut appeler une procédure distante sur le serveur qui retourne un handle de contexte ouvert (non **null**) ou passe un par un paramètre **\[ out \]** dans la liste de paramètres de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="e014d-110">With a valid binding handle, the client can call a remote procedure on the server that either returns an opened (non-**NULL**) context handle or passes one through an **\[out\]** parameter in the remote procedure's parameter list.</span></span>

<span data-ttu-id="e014d-111">Les clients peuvent utiliser les descripteurs de contexte ouverts de la manière dont ils ont besoin.</span><span class="sxs-lookup"><span data-stu-id="e014d-111">Clients may use opened context handles in any way they require.</span></span> <span data-ttu-id="e014d-112">Toutefois, ils doivent invalider le descripteur lorsqu’il n’en a plus besoin.</span><span class="sxs-lookup"><span data-stu-id="e014d-112">They should, however, invalidate the handle when they no longer need it.</span></span> <span data-ttu-id="e014d-113">Il existe deux façons de procéder :</span><span class="sxs-lookup"><span data-stu-id="e014d-113">There are two way to do this:</span></span>

-   <span data-ttu-id="e014d-114">Pour appeler une procédure distante offerte par le programme serveur qui libère le contexte et ferme le descripteur de contexte (affecte la **valeur null**).</span><span class="sxs-lookup"><span data-stu-id="e014d-114">To invoke a remote procedure offered by the server program that frees the context and closes the context handle (sets it to **NULL**).</span></span>
-   <span data-ttu-id="e014d-115">Lorsque le serveur est inaccessible, appelez la fonction [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="e014d-115">When the server is unreachable, call the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="e014d-116">La deuxième approche nettoie uniquement l’État côté client et ne nettoie pas l’État côté serveur. elle doit donc être utilisée uniquement lorsque la partition réseau est suspectée et que le client et le serveur effectuent un nettoyage indépendant.</span><span class="sxs-lookup"><span data-stu-id="e014d-116">The second approach only cleans up the client side state, and does not clean up the server-side state, so it should be used only when network partition is suspected, and the client and the server will do an independent cleanup.</span></span> <span data-ttu-id="e014d-117">Le serveur effectue un nettoyage indépendant par le biais de la routine d’exécution, le client le fait à l’aide de la fonction [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="e014d-117">The server performs independent cleanup through the run-down routine, the client does so using the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="e014d-118">Le fragment de code suivant présente un exemple de la façon dont un client peut utiliser un handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="e014d-118">The following code fragment presents an example of how a client might use a context handle.</span></span> <span data-ttu-id="e014d-119">Pour afficher la définition de l’interface utilisée par cet exemple, consultez [développement d’interface à l’aide de handles de contexte](interface-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="e014d-119">To view the definition of the interface that this example uses, see [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span> <span data-ttu-id="e014d-120">Pour l’implémentation de serveur, consultez [développement de serveurs à l’aide de handles de contexte](server-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="e014d-120">For the server implementation, see [Server Development Using Context Handles](server-development-using-context-handles.md).</span></span>

<span data-ttu-id="e014d-121">Dans cet exemple, le client appelle RemoteOpen pour obtenir un handle de contexte qui contient des données valides.</span><span class="sxs-lookup"><span data-stu-id="e014d-121">In this example, the client calls RemoteOpen to obtain a context handle that contains valid data.</span></span> <span data-ttu-id="e014d-122">Le client peut ensuite utiliser le handle de contexte dans les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="e014d-122">The client can then use the context handle in remote procedure calls.</span></span> <span data-ttu-id="e014d-123">Étant donné qu’il n’a plus besoin du handle de liaison, le client peut libérer le handle explicite utilisé pour créer le handle de contexte :</span><span class="sxs-lookup"><span data-stu-id="e014d-123">Because it no longer needs the binding handle, the client can free the explicit handle it used to create the context handle:</span></span>


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



<span data-ttu-id="e014d-124">Dans cet exemple, l’application cliente utilise une procédure appelée RemoteRead pour lire un fichier de données sur le serveur jusqu’à ce qu’il rencontre une fin de fichier.</span><span class="sxs-lookup"><span data-stu-id="e014d-124">The client application in this example uses a procedure called RemoteRead to read a data file on the server until it encounters an end of file.</span></span> <span data-ttu-id="e014d-125">Il ferme ensuite le fichier en appelant RemoteClose.</span><span class="sxs-lookup"><span data-stu-id="e014d-125">It then closes the file by calling RemoteClose.</span></span> <span data-ttu-id="e014d-126">Le descripteur de contexte apparaît en tant que paramètre dans les fonctions RemoteRead et RemoteClose, comme suit :</span><span class="sxs-lookup"><span data-stu-id="e014d-126">The context handle appears as a parameter in the RemoteRead and RemoteClose functions as:</span></span>


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



 

 




