---
title: RPC_BINDING_HANDLE (rpcdce. h)
description: Le \_ type de données handle de liaison RPC déclare un handle de liaison contenant les informations que la bibliothèque Runtime RPC utilise pour accéder aux informations de liaison.
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743789"
---
# <a name="rpc_binding_handle"></a><span data-ttu-id="a9b80-104">\_handle de liaison RPC \_</span><span class="sxs-lookup"><span data-stu-id="a9b80-104">RPC\_BINDING\_HANDLE</span></span>

<span data-ttu-id="a9b80-105">Le type de données **\_ handle de liaison RPC** déclare un handle de liaison contenant les informations que la bibliothèque Runtime RPC utilise pour accéder aux informations de liaison.</span><span class="sxs-lookup"><span data-stu-id="a9b80-105">The **RPC\_BINDING HANDLE** data type declares a binding handle containing information that the RPC run-time library uses to access binding information.</span></span>


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="a9b80-106">Notes</span><span class="sxs-lookup"><span data-stu-id="a9b80-106">Remarks</span></span>

<span data-ttu-id="a9b80-107">La bibliothèque Runtime utilise des informations de liaison pour établir une relation client-serveur qui autorise l’exécution d’appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="a9b80-107">The run-time library uses binding information to establish a client-server relationship that allows the execution of remote procedure calls.</span></span> <span data-ttu-id="a9b80-108">En fonction du contexte dans lequel un handle de liaison est créé, il est considéré comme un handle de liaison de serveur ou un handle de liaison client.</span><span class="sxs-lookup"><span data-stu-id="a9b80-108">Based on the context in which a binding handle is created, it is considered a server-binding handle or a client-binding handle.</span></span>

<span data-ttu-id="a9b80-109">Un handle de liaison de serveur contient les informations nécessaires à un client pour établir une relation avec un serveur spécifique.</span><span class="sxs-lookup"><span data-stu-id="a9b80-109">A server-binding handle contains the information necessary for a client to establish a relationship with a specific server.</span></span> <span data-ttu-id="a9b80-110">Un nombre quelconque de routines runtime de l’API RPC retournent un handle de liaison de serveur qui peut être utilisé pour effectuer un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="a9b80-110">Any number of RPC API run-time routines return a server-binding handle that can be used for making a remote procedure call.</span></span>

<span data-ttu-id="a9b80-111">Un handle de liaison client ne peut pas être utilisé pour effectuer un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="a9b80-111">A client-binding handle cannot be used to make a remote procedure call.</span></span> <span data-ttu-id="a9b80-112">La bibliothèque Runtime RPC crée et fournit un handle de liaison client à une procédure de serveur appelé (également appelée routine de gestionnaire de serveur) en tant que paramètre de \_ handle de liaison RPC \_ .</span><span class="sxs-lookup"><span data-stu-id="a9b80-112">The RPC run-time library creates and provides a client-binding handle to a called-server procedure (also called a server-manager routine) as the RPC\_BINDING\_HANDLE parameter.</span></span> <span data-ttu-id="a9b80-113">Le handle de liaison client contient des informations sur le client appelant.</span><span class="sxs-lookup"><span data-stu-id="a9b80-113">The client-binding handle contains information about the calling client.</span></span>

<span data-ttu-id="a9b80-114">Les fonctions \*\* \* RpcBinding\* _ _*et \* RpcNsBinding*_ retournent le code \_ d’état RPC \_ \_ de type incorrect \_ de \_ liaison quand une application fournit le type de handle de liaison incorrect.</span><span class="sxs-lookup"><span data-stu-id="a9b80-114">The **RpcBinding\** _ and _*RpcNsBinding\*\*_ functions return the status code RPC\_S\_WRONG\_KIND\_OF\_BINDING when an application provides the incorrect binding-handle type.</span></span>

<span data-ttu-id="a9b80-115">Une application peut partager un handle de liaison unique entre plusieurs threads d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a9b80-115">An application can share a single binding handle across multiple threads of execution.</span></span> <span data-ttu-id="a9b80-116">La bibliothèque Runtime RPC gère les appels de procédure distante simultanés qui utilisent un seul handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="a9b80-116">The RPC run-time library manages concurrent remote procedure calls that use a single binding handle.</span></span> <span data-ttu-id="a9b80-117">Toutefois, l’application est responsable de la liaison du contrôle d’accès concurrentiel pour les opérations qui modifient un handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="a9b80-117">However, the application is responsible for binding handle concurrency control for operations that modify a binding handle.</span></span> <span data-ttu-id="a9b80-118">Ces opérations incluent les routines suivantes :</span><span class="sxs-lookup"><span data-stu-id="a9b80-118">These operations include the following routines:</span></span>

-   [<span data-ttu-id="a9b80-119">_ *RpcBindingFree*\*</span><span class="sxs-lookup"><span data-stu-id="a9b80-119">_ *RpcBindingFree*\*</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [<span data-ttu-id="a9b80-120">**RpcBindingReset**</span><span class="sxs-lookup"><span data-stu-id="a9b80-120">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [<span data-ttu-id="a9b80-121">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="a9b80-121">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [<span data-ttu-id="a9b80-122">**RpcBindingSetObject**</span><span class="sxs-lookup"><span data-stu-id="a9b80-122">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

<span data-ttu-id="a9b80-123">Par exemple, si une application partage un handle de liaison entre deux threads d’exécution et réinitialise le point de terminaison de handle de liaison dans l’un des threads en appelant [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="a9b80-123">For example, if an application shares a binding handle across two threads of execution and resets the binding-handle endpoint in one of the threads by calling [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), the results are undefined.</span></span> <span data-ttu-id="a9b80-124">Le handle de liaison sur l’autre thread peut également être réinitialisé, ou l’opération peut échouer ou le processus peut se bloquer.</span><span class="sxs-lookup"><span data-stu-id="a9b80-124">The binding handle on the other thread may also be reset, or the operation may fail, or the process may crash.</span></span> <span data-ttu-id="a9b80-125">Une erreur courante consiste à libérer un handle de liaison lorsqu’un appel sur celui-ci est en cours ; Cela entraîne généralement un blocage du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="a9b80-125">A common error is freeing a binding handle while a call on it is in progress; this usually crashes the calling process.</span></span>

<span data-ttu-id="a9b80-126">Si vous ne souhaitez pas la concurrence, vous pouvez concevoir une application pour créer une copie d’une poignée de liaison en appelant [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span><span class="sxs-lookup"><span data-stu-id="a9b80-126">If you do not want concurrency, you can design an application to create a copy of a binding handle by calling [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span></span> <span data-ttu-id="a9b80-127">Dans ce cas, une opération vers le premier handle de liaison n’a aucun effet sur le second handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="a9b80-127">In this case, an operation to the first binding handle has no effect on the second binding handle.</span></span>

<span data-ttu-id="a9b80-128">Les routines qui requièrent un handle de liaison en tant que paramètre affichent un type de données de **\_ \_ handle de liaison RPC**.</span><span class="sxs-lookup"><span data-stu-id="a9b80-128">Routines requiring a binding handle as a parameter show a data type of **RPC\_BINDING\_HANDLE**.</span></span> <span data-ttu-id="a9b80-129">Les paramètres de handle de liaison sont passés par valeur.</span><span class="sxs-lookup"><span data-stu-id="a9b80-129">Binding-handle parameters are passed by value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b80-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9b80-130">Requirements</span></span>



| <span data-ttu-id="a9b80-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9b80-131">Requirement</span></span> | <span data-ttu-id="a9b80-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9b80-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b80-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9b80-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b80-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9b80-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a9b80-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9b80-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b80-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9b80-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a9b80-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9b80-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9b80-138"><dt>Rpcdce. h (inclure RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9b80-138"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





