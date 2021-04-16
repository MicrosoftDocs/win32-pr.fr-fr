---
title: Fonction midl_user_free
description: La \_ fonction gratuite de l’utilisateur MIDL \_ doit être fournie par les développeurs RPC.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713ed05173b709780b6496f233051fa3adddff8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382684"
---
# <a name="the-midl_user_free-function"></a><span data-ttu-id="3feeb-103">Fonction d' \_ utilisateur \_ gratuit MIDL</span><span class="sxs-lookup"><span data-stu-id="3feeb-103">The midl\_user\_free Function</span></span>

<span data-ttu-id="3feeb-104">La **fonction \_ \_ gratuite de l’utilisateur MIDL** doit être fournie par les développeurs RPC.</span><span class="sxs-lookup"><span data-stu-id="3feeb-104">The **midl\_user\_free** function must be supplied by RPC developers.</span></span> <span data-ttu-id="3feeb-105">Elle alloue de la mémoire pour les stubs RPC et les routines de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3feeb-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="3feeb-106">Votre fonction d' **\_ utilisateur \_ gratuit MIDL** doit correspondre au prototype suivant :</span><span class="sxs-lookup"><span data-stu-id="3feeb-106">Your **midl\_user\_free** function must match the following prototype:</span></span>

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

<span data-ttu-id="3feeb-107">Le paramètre *pbuffer* spécifie un pointeur vers la mémoire qui doit être libérée.</span><span class="sxs-lookup"><span data-stu-id="3feeb-107">The *pBuffer* parameter specifies a pointer to the memory that is to be freed.</span></span> <span data-ttu-id="3feeb-108">L’application cliente et l’application serveur doivent implémenter la fonction **\_ utilisateur \_ MIDL MIDL** , sauf si vous compilez en mode de compatibilité OSF ([**/OSF**](/windows/desktop/Midl/-osf)).</span><span class="sxs-lookup"><span data-stu-id="3feeb-108">Both client application and server application must implement the **midl\_user\_free** function unless you are compiling in OSF-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="3feeb-109">La **fonction \_ \_ gratuite de l’utilisateur MIDL** doit pouvoir libérer tout le stockage alloué par l’allocation de l' [**\_ utilisateur \_ MIDL**](the-midl-user-allocate-function.md).</span><span class="sxs-lookup"><span data-stu-id="3feeb-109">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](the-midl-user-allocate-function.md).</span></span>

<span data-ttu-id="3feeb-110">Les applications et les stubs appellent **MIDL \_ \_ sans utilisateur** lors du traitement des objets alloués :</span><span class="sxs-lookup"><span data-stu-id="3feeb-110">Applications and stubs call **midl\_user\_free** when dealing with allocated objects:</span></span>

-   <span data-ttu-id="3feeb-111">L’application serveur doit appeler **l' \_ utilisateur MIDL \_ gratuit** pour libérer de la mémoire allouée par l’application, par exemple lors de la suppression d’un nœud de données alloué dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="3feeb-111">The server application should call **midl\_user\_free** to free memory allocated by the application, such as when deleting a dynamically allocated node of data.</span></span>
-   <span data-ttu-id="3feeb-112">Le stub serveur appelle **l' \_ utilisateur MIDL \_ gratuit** pour libérer de la mémoire sur le serveur après avoir marshalé tous les \[ \] arguments out, les arguments out, les \[ \] \[ \] arguments out et la valeur de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="3feeb-112">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all \[out\] arguments, \[in\],\[out\] arguments, and the function return value.</span></span>

<span data-ttu-id="3feeb-113">Par exemple, l’exemple de programme Windows RPC qui affiche « Hello, World » implémente l' **\_ utilisateur MIDL \_ gratuit** en termes de fonction C Free :</span><span class="sxs-lookup"><span data-stu-id="3feeb-113">For example, the RPC Windows sample program that displays "Hello, world" implements **midl\_user\_free** in terms of the C function free:</span></span>


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> <span data-ttu-id="3feeb-114">Si le package RpcSs est activé (par exemple, à la suite de l’utilisation de l' \[ attribut [**Enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] ), votre programme serveur doit utiliser [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="3feeb-114">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), your server program should use [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) to free memory.</span></span> <span data-ttu-id="3feeb-115">Pour plus d’informations, consultez package de gestion de la [mémoire RPCSS](rpcss-memory-management-package.md).</span><span class="sxs-lookup"><span data-stu-id="3feeb-115">For more information, see [RpcSs Memory Management Package](rpcss-memory-management-package.md).</span></span>

 

 

 