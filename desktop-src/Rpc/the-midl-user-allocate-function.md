---
title: Fonction midl_user_allocate
description: La \_ \_ fonction Allocate de l’utilisateur MIDL est une procédure qui doit être fournie par les développeurs d’applications RPC.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102005"
---
# <a name="the-midl_user_allocate-function"></a><span data-ttu-id="48205-103">La fonction d’allocation de l' \_ utilisateur MIDL \_</span><span class="sxs-lookup"><span data-stu-id="48205-103">The midl\_user\_allocate Function</span></span>

<span data-ttu-id="48205-104">La **fonction \_ \_ allocate de l’utilisateur MIDL** est une procédure qui doit être fournie par les développeurs d’applications RPC.</span><span class="sxs-lookup"><span data-stu-id="48205-104">The **midl\_user\_allocate** function is a procedure that must be supplied by developers of RPC applications.</span></span> <span data-ttu-id="48205-105">Elle alloue de la mémoire pour les stubs RPC et les routines de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="48205-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="48205-106">La fonction d' **\_ \_ allocation de votre utilisateur MIDL** doit correspondre au prototype suivant :</span><span class="sxs-lookup"><span data-stu-id="48205-106">Your **midl\_user\_allocate** function must match the following prototype:</span></span>

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

<span data-ttu-id="48205-107">Le paramètre *cBytes* spécifie le nombre d’octets à allouer.</span><span class="sxs-lookup"><span data-stu-id="48205-107">The *cBytes* parameter specifies the number of bytes to allocate.</span></span> <span data-ttu-id="48205-108">Les applications clientes et les applications serveur doivent implémenter la fonction d' **\_ \_ allocation utilisateur MIDL** , sauf si vous compilez en mode de compatibilité OSF (/OSF).</span><span class="sxs-lookup"><span data-stu-id="48205-108">Both client applications and server applications must implement the **midl\_user\_allocate** function unless you are compiling in OSF-compatibility (/osf) mode.</span></span> <span data-ttu-id="48205-109">Les applications et les stubs générés appellent l' **\_ \_ allocation** directe ou indirecte de l’utilisateur MIDL pour gérer les objets alloués.</span><span class="sxs-lookup"><span data-stu-id="48205-109">Applications and generated stubs call **midl\_user\_allocate** directly or indirectly to manage allocated objects.</span></span> <span data-ttu-id="48205-110">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="48205-110">For example:</span></span>

-   <span data-ttu-id="48205-111">Les applications clientes et serveur appellent **MIDL \_ User \_ allocate** pour allouer de la mémoire pour l’application, par exemple lors de la création d’un nœud dans une arborescence ou une liste liée.</span><span class="sxs-lookup"><span data-stu-id="48205-111">The client and server applications call **midl\_user\_allocate** to allocate memory for the application, such as when creating a new node in a tree or linked list.</span></span>
-   <span data-ttu-id="48205-112">Le stub serveur appelle **l' \_ \_ allocation d’utilisateur MIDL** lors du démarshaling de données dans l’espace d’adressage du serveur.</span><span class="sxs-lookup"><span data-stu-id="48205-112">The server stub calls **midl\_user\_allocate** when unmarshaling data into the server address space.</span></span>
-   <span data-ttu-id="48205-113">Le stub client appelle **l' \_ \_ allocation d’utilisateur MIDL** lors du démarshaling de données à partir du serveur qui est référencé par un \[ pointeur de sortie \] .</span><span class="sxs-lookup"><span data-stu-id="48205-113">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an \[out\] pointer.</span></span> <span data-ttu-id="48205-114">Notez que pour \[ les \] \[ pointeurs in, out \] et \[ unique \] , le stub client appelle **l' \_ \_ allocation de l’utilisateur MIDL** uniquement si la \[ \] valeur de pointeur unique était null en entrée et que les modifications apportées à une valeur non null au cours de l’appel.</span><span class="sxs-lookup"><span data-stu-id="48205-114">Note that for \[in\], \[out\], and \[unique\] pointers, the client stub calls **midl\_user\_allocate** only if the \[unique\] pointer value was null on input and changes to a non-null value during the call.</span></span> <span data-ttu-id="48205-115">Si le \[ \] pointeur unique n’était pas null en entrée, le stub client écrit les données associées dans la mémoire existante.</span><span class="sxs-lookup"><span data-stu-id="48205-115">If the \[unique\] pointer was non-null on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="48205-116">Si **l' \_ \_ allocation d’utilisateur MIDL** échoue pour allouer de la mémoire, elle doit retourner un pointeur null.</span><span class="sxs-lookup"><span data-stu-id="48205-116">If **midl\_user\_allocate** fails to allocate memory, it should return a null pointer.</span></span>

<span data-ttu-id="48205-117">La fonction d' **\_ \_ allocation de l’utilisateur MIDL** doit retourner un pointeur aligné sur 8 octets.</span><span class="sxs-lookup"><span data-stu-id="48205-117">The **midl\_user\_allocate** function should return an 8-byte aligned pointer.</span></span>

<span data-ttu-id="48205-118">Par exemple, les exemples de programmes fournis avec le kit de développement logiciel (SDK) de la plateforme implémentent **MIDL \_ User \_ allocate** en termes de la fonction C [**malloc**](pointers-and-memory-allocation.md):</span><span class="sxs-lookup"><span data-stu-id="48205-118">For example, the sample programs provided with the Platform Software Development Kit (SDK) implement **midl\_user\_allocate** in terms of the C function [**malloc**](pointers-and-memory-allocation.md):</span></span>


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> <span data-ttu-id="48205-119">Si le package RpcSs est activé (par exemple, à la suite de l’utilisation de l' \[ attribut [**Enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] ), utilisez [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) pour allouer de la mémoire côté serveur.</span><span class="sxs-lookup"><span data-stu-id="48205-119">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) to allocate memory on the server side.</span></span> <span data-ttu-id="48205-120">Pour plus d’informations sur \[ **Enable \_ allocate** \] , consultez [référence MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="48205-120">For additional information on \[**enable\_allocate**\], see [MIDL Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 

 