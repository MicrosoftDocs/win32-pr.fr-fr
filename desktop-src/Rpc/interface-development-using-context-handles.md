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
# <a name="interface-development-using-context-handles"></a><span data-ttu-id="42b33-103">Développement d’interface à l’aide de handles de contexte</span><span class="sxs-lookup"><span data-stu-id="42b33-103">Interface Development Using Context Handles</span></span>

<span data-ttu-id="42b33-104">En général, vous créez un handle de contexte en spécifiant l' \[ attribut de [**\_ handle de contexte**](/windows/desktop/Midl/context-handle) \] sur une définition de type dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="42b33-104">Typically, you create a context handle by specifying the \[[**context\_handle**](/windows/desktop/Midl/context-handle)\] attribute on a type definition in the IDL file.</span></span> <span data-ttu-id="42b33-105">La définition de type spécifie également implicitement une routine d’exécution de contexte, que vous devez fournir.</span><span class="sxs-lookup"><span data-stu-id="42b33-105">The type definition also implicitly specifies a context run-down routine, which you must provide.</span></span> <span data-ttu-id="42b33-106">Si la communication entre le client et le serveur est interrompue, le temps d’exécution du serveur appelle cette routine pour effectuer tout nettoyage nécessaire.</span><span class="sxs-lookup"><span data-stu-id="42b33-106">If communication between the client and server breaks down, the server run time invokes this routine to perform any needed cleanup.</span></span> <span data-ttu-id="42b33-107">Pour plus d’informations sur les routines d’exécution de contexte, consultez [routine de fonctionnement du contexte de serveur](server-context-run-down-routine.md).</span><span class="sxs-lookup"><span data-stu-id="42b33-107">For more information on context run-down routines, see [Server Context Run-down Routine](server-context-run-down-routine.md).</span></span>

<span data-ttu-id="42b33-108">Une interface qui utilise un handle de contexte doit avoir un handle de liaison pour la liaison initiale, qui doit avoir lieu avant que le serveur puisse retourner un handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="42b33-108">An interface that uses a context handle must have a binding handle for the initial binding, which has to take place before the server can return a context handle.</span></span> <span data-ttu-id="42b33-109">Vous pouvez utiliser un handle de liaison automatique, implicite ou explicite pour créer la liaison et établir le contexte.</span><span class="sxs-lookup"><span data-stu-id="42b33-109">You can use an automatic, implicit, or explicit binding handle to create the binding and establish the context.</span></span>

<span data-ttu-id="42b33-110">Un handle de contexte doit être du [**type \* void**](/windows/desktop/Midl/void) , ou un type qui est résolu en [**void \***](/windows/desktop/Midl/void).</span><span class="sxs-lookup"><span data-stu-id="42b33-110">A context handle must be of the [**void \***](/windows/desktop/Midl/void) type, or a type that resolves to [**void \***](/windows/desktop/Midl/void).</span></span> <span data-ttu-id="42b33-111">Le programme serveur le convertit en type requis.</span><span class="sxs-lookup"><span data-stu-id="42b33-111">The server program casts it to the required type.</span></span>

> [!Note]  
> <span data-ttu-id="42b33-112">L’utilisation de \[ [**dans**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] pour les paramètres de handle de contexte est déconseillée, sauf pour les routines qui ferment des handles de contexte.</span><span class="sxs-lookup"><span data-stu-id="42b33-112">The use of \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] for context handle parameters is discouraged except for routines that close context handles.</span></span> <span data-ttu-id="42b33-113">Si le contexte gère les paramètres marqués \[ [**dans**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] sont utilisés, ne transmettez pas un descripteur de contexte **null** ou non initialisé du client au serveur.</span><span class="sxs-lookup"><span data-stu-id="42b33-113">If context handles parameters marked \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] are used, do not pass a **NULL** or uninitialized context handle from the client to the server.</span></span> <span data-ttu-id="42b33-114">Un pointeur **null** vers un handle de contexte doit être passé à la place.</span><span class="sxs-lookup"><span data-stu-id="42b33-114">A **NULL** pointer to a context handle should be passed instead.</span></span> <span data-ttu-id="42b33-115">Veuillez noter que les paramètres de handle de contexte marqués \[ [**dans**](/windows/desktop/Midl/in) \] n’acceptent pas les pointeurs **null** .</span><span class="sxs-lookup"><span data-stu-id="42b33-115">Please note, context handle parameters marked \[[**in**](/windows/desktop/Midl/in)\] do not accept **NULL** pointers.</span></span>

 

<span data-ttu-id="42b33-116">Le fragment suivant d’un exemple de définition d’interface montre comment une application distribuée peut utiliser un handle de contexte pour qu’un serveur ouvre et met à jour un fichier de données pour chaque client.</span><span class="sxs-lookup"><span data-stu-id="42b33-116">The following fragment of a sample interface definition shows how a distributed application can use a context handle to have a server open and update a data file for each client.</span></span>

<span data-ttu-id="42b33-117">L’interface doit contenir un appel de procédure distante pour initialiser le handle et lui affecter une valeur non **null** .</span><span class="sxs-lookup"><span data-stu-id="42b33-117">The interface must contain a remote procedure call to initialize the handle and set it to a non-**null** value.</span></span> <span data-ttu-id="42b33-118">Dans cet exemple, la fonction RemoteOpen effectue cette opération.</span><span class="sxs-lookup"><span data-stu-id="42b33-118">In this example, the RemoteOpen function performs this operation.</span></span> <span data-ttu-id="42b33-119">Elle spécifie le handle de contexte avec un \[ [](/windows/desktop/Midl/out-idl) \] attribut directionnel out.</span><span class="sxs-lookup"><span data-stu-id="42b33-119">It specifies the context handle with an \[[**out**](/windows/desktop/Midl/out-idl)\] directional attribute.</span></span> <span data-ttu-id="42b33-120">Vous pouvez également retourner le descripteur de contexte comme valeur de retour de la procédure.</span><span class="sxs-lookup"><span data-stu-id="42b33-120">Alternatively, you could return the context handle as the procedure's return value.</span></span> <span data-ttu-id="42b33-121">Toutefois, dans cet exemple, nous passons le descripteur de contexte par le biais de la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="42b33-121">However in this example, we'll pass the context handle out through the parameter list.</span></span>

<span data-ttu-id="42b33-122">Dans cet exemple, les informations de contexte sont un descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="42b33-122">In this example, the context information is a file handle.</span></span> <span data-ttu-id="42b33-123">Il effectue le suivi de l’emplacement actuel dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="42b33-123">It keeps track of the current location in the file.</span></span> <span data-ttu-id="42b33-124">L’interface empaquette le descripteur de fichier comme handle de contexte et le passe en tant que paramètre aux appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="42b33-124">The interface packages the file handle as a context handle and passes it as a parameter to remote procedure calls.</span></span> <span data-ttu-id="42b33-125">Une structure contient le nom de fichier et le descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="42b33-125">A structure contains the file name and the file handle.</span></span>

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

<span data-ttu-id="42b33-126">La fonction RemoteOpen crée un handle de contexte valide non **null** .</span><span class="sxs-lookup"><span data-stu-id="42b33-126">The RemoteOpen function creates a valid, non-**null** context handle.</span></span> <span data-ttu-id="42b33-127">Il passe le descripteur de contexte au client.</span><span class="sxs-lookup"><span data-stu-id="42b33-127">It passes the context handle to the client.</span></span> <span data-ttu-id="42b33-128">Les appels de procédure distante suivants, tels que RemoteRead, utilisent le handle de contexte en tant que pointeur.</span><span class="sxs-lookup"><span data-stu-id="42b33-128">Subsequent remote procedure calls, such as RemoteRead, use the context handle as an in pointer.</span></span>

<span data-ttu-id="42b33-129">En plus de la procédure distante qui initialise le descripteur de contexte, l’interface doit contenir une procédure qui libère le contexte du serveur et définit le descripteur de contexte sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="42b33-129">In addition to the remote procedure that initializes the context handle, the interface must contain a procedure that frees the server context and sets context handle to **NULL**.</span></span> <span data-ttu-id="42b33-130">Dans l’exemple précédent, la fonction RemoteClose effectue cette opération.</span><span class="sxs-lookup"><span data-stu-id="42b33-130">In the preceding example, the RemoteClose function performs this operation.</span></span>

 

 