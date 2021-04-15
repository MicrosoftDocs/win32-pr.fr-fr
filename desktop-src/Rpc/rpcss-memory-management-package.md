---
title: Package de gestion de mémoire RpcSs
description: La paire d’allocateur/annulateur par défaut utilisée par les stubs et le moment de l’exécution lors de l’allocation de mémoire pour le compte de l’application est MIDL User aslocate \_ \_ /MIDL \_ User \_ Free.
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463535"
---
# <a name="rpcss-memory-management-package"></a><span data-ttu-id="530d2-103">Package de gestion de mémoire RpcSs</span><span class="sxs-lookup"><span data-stu-id="530d2-103">RpcSs Memory Management Package</span></span>

<span data-ttu-id="530d2-104">La paire d’allocateur/annulateur par défaut utilisée par les stubs et le moment de l’exécution lors de l’allocation de mémoire pour le compte de l’application est **MIDL utilisateur \_ \_ allouez** un / **\_ utilisateur MIDL \_ gratuit** à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="530d2-104">The default allocator/deallocator pair used by the stubs and run time when allocating memory on behalf of the application is **midl\_user\_allocate**/**midl\_user\_free**.</span></span> <span data-ttu-id="530d2-105">Toutefois, vous pouvez choisir le package RpcSs au lieu de la valeur par défaut en utilisant l’attribut ACF **\[ Enable \_ allocate \]**.</span><span class="sxs-lookup"><span data-stu-id="530d2-105">However, you can choose the RpcSs package instead of the default by using the ACF attribute **\[enable\_allocate\]**.</span></span> <span data-ttu-id="530d2-106">Le package RpcSs se compose de fonctions RPC qui commencent par le préfixe **RPCSS** ou **RpcSm**.</span><span class="sxs-lookup"><span data-stu-id="530d2-106">The RpcSs package consists of RPC functions that begin with the prefix **RpcSs** or **RpcSm**.</span></span> <span data-ttu-id="530d2-107">Le package RpcSs n’est pas recommandé pour les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="530d2-107">The RpcSs package is not recommended for Windows applications.</span></span>

> [!Note]  
> <span data-ttu-id="530d2-108">Le package de gestion de la mémoire RPCSS est obsolète.</span><span class="sxs-lookup"><span data-stu-id="530d2-108">The Rpcss Memory Management Package is obsolete.</span></span> <span data-ttu-id="530d2-109">Il est recommandé que [**l' \_ \_ allocation d’utilisateur MIDL**](/windows/desktop/Midl/midl-user-allocate-1) et l' [**\_ utilisateur MIDL \_ gratuit**](/windows/desktop/Midl/midl-user-free-1) soient utilisés à la place.</span><span class="sxs-lookup"><span data-stu-id="530d2-109">It is recommended that [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) are used in its place.</span></span>

 

<span data-ttu-id="530d2-110">En mode **/OSF** , le package RPCSS est activé automatiquement pour les stubs générés par MIDL lorsque des pointeurs complets sont utilisés, lorsque les arguments nécessitent une allocation de mémoire ou à la suite de l’utilisation de l’attribut **\[ Enable \_ allocate \]** .</span><span class="sxs-lookup"><span data-stu-id="530d2-110">In **/osf** mode, the RpcSs package is enabled for MIDL-generated stubs automatically when full pointers are used, when the arguments require memory allocation, or as a result of using the **\[enable\_allocate\]** attribute.</span></span> <span data-ttu-id="530d2-111">Dans le mode par défaut (Microsoft étendu), le package RpcSs est activé uniquement lorsque l’attribut **\[ activer l' \_ allocation \]** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="530d2-111">In the default (Microsoft extended) mode, the RpcSs package is enabled only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="530d2-112">L’attribut **\[ Enable \_ allocate \]** active l’environnement RPCSS par les stubs côté serveur.</span><span class="sxs-lookup"><span data-stu-id="530d2-112">The **\[enable\_allocate\]** attribute enables the RpcSs environment by the server-side stubs.</span></span> <span data-ttu-id="530d2-113">Le côté client est averti de la possibilité que le package RpcSs soit activé.</span><span class="sxs-lookup"><span data-stu-id="530d2-113">The client side becomes alerted to the possibility that the RpcSs package may be enabled.</span></span> <span data-ttu-id="530d2-114">En mode **/OSF** , le côté client n’est pas affecté.</span><span class="sxs-lookup"><span data-stu-id="530d2-114">In **/osf** mode, the client side is not affected.</span></span>

<span data-ttu-id="530d2-115">Lorsque le package RpcSs est activé, l’allocation de mémoire côté serveur s’effectue à l’aide de la paire annulateur et de la paire de gestion de mémoire RpcSs privée.</span><span class="sxs-lookup"><span data-stu-id="530d2-115">When the RpcSs package is enabled, allocation of memory on the server side is accomplished with the private RpcSs memory management allocator and deallocator pair.</span></span> <span data-ttu-id="530d2-116">Vous pouvez allouer de la mémoire à l’aide du même mécanisme en appelant [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (ou [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span><span class="sxs-lookup"><span data-stu-id="530d2-116">You can allocate memory using the same mechanism by calling [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (or [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span></span> <span data-ttu-id="530d2-117">Lors du retour du stub serveur, toute la mémoire allouée par le package RpcSs est automatiquement libérée.</span><span class="sxs-lookup"><span data-stu-id="530d2-117">Upon return from the server stub, all the memory allocated by the RpcSs package is automatically freed.</span></span> <span data-ttu-id="530d2-118">L’exemple suivant montre comment activer le package RpcSs :</span><span class="sxs-lookup"><span data-stu-id="530d2-118">The following example shows how to enable the RpcSs package:</span></span>

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

<span data-ttu-id="530d2-119">Votre application peut libérer explicitement la mémoire en appelant la fonction [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) ou [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) .</span><span class="sxs-lookup"><span data-stu-id="530d2-119">Your application can explicitly free memory by invoking the [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) or [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) function.</span></span> <span data-ttu-id="530d2-120">Notez que ces fonctions ne libèrent pas réellement de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="530d2-120">Note that these functions do not actually free memory.</span></span> <span data-ttu-id="530d2-121">Ils le marquent pour suppression.</span><span class="sxs-lookup"><span data-stu-id="530d2-121">They mark it for deletion.</span></span> <span data-ttu-id="530d2-122">La bibliothèque RPC libère la mémoire lorsque votre programme appelle [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) ou [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span><span class="sxs-lookup"><span data-stu-id="530d2-122">The RPC library releases the memory when your program calls [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) or [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span></span>

<span data-ttu-id="530d2-123">Vous pouvez également activer l’environnement de gestion de la mémoire de votre application en appelant la routine [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) (et vous pouvez la désactiver en appelant la routine [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) ).</span><span class="sxs-lookup"><span data-stu-id="530d2-123">You can also enable the memory management environment for your application by calling the [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) routine (and you can disable it by calling the [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) routine).</span></span> <span data-ttu-id="530d2-124">Une fois activée, le code d’application peut allouer et libérer de la mémoire en appelant des fonctions à partir du package RpcSs.</span><span class="sxs-lookup"><span data-stu-id="530d2-124">Once enabled, application code can allocate and deallocate memory by calling functions from the RpcSs package.</span></span>

 

 