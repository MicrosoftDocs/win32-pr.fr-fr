---
title: Pointeurs de référence
description: Les pointeurs de référence sont les pointeurs les plus simples et nécessitent le moins de traitement par le stub client.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031740"
---
# <a name="reference-pointers"></a><span data-ttu-id="93320-103">Pointeurs de référence</span><span class="sxs-lookup"><span data-stu-id="93320-103">Reference Pointers</span></span>

<span data-ttu-id="93320-104">Les pointeurs de référence sont les pointeurs les plus simples et nécessitent le moins de traitement par le stub client.</span><span class="sxs-lookup"><span data-stu-id="93320-104">Reference pointers are the simplest pointers and require the least amount of processing by the client stub.</span></span> <span data-ttu-id="93320-105">Lorsqu’un programme client passe un pointeur de référence à une procédure distante, le pointeur de référence contient toujours l’adresse d’un bloc de mémoire valide.</span><span class="sxs-lookup"><span data-stu-id="93320-105">When a client program passes a reference pointer to a remote procedure, the reference pointer always contains the address of a valid block of memory.</span></span> <span data-ttu-id="93320-106">Elle pointe toujours vers le même bloc de mémoire lorsque la procédure distante se termine.</span><span class="sxs-lookup"><span data-stu-id="93320-106">It will still be pointing to the same memory block when the remote procedure completes.</span></span> <span data-ttu-id="93320-107">Ces pointeurs sont principalement utilisés pour implémenter la sémantique de référence et pour autoriser les \[ paramètres [**out**](/windows/desktop/Midl/out-idl) \] en C.</span><span class="sxs-lookup"><span data-stu-id="93320-107">These pointers are mainly used to implement reference semantics, and to allow for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters in C.</span></span>

<span data-ttu-id="93320-108">Dans l’exemple suivant, la valeur du pointeur ne change pas pendant l’appel, bien que le contenu des données à l’adresse indiquée par le pointeur puisse changer.</span><span class="sxs-lookup"><span data-stu-id="93320-108">In the following example, the value of the pointer does not change during the call, although the contents of the data at the address indicated by the pointer can change.</span></span>

![modification des données à une adresse de pointeur de référence statique](images/prog-a07.png)

<span data-ttu-id="93320-110">Un pointeur de référence présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="93320-110">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="93320-111">Il pointe toujours vers un stockage valide et n’a jamais la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="93320-111">It always points to valid storage and never has the value **NULL**.</span></span>
-   <span data-ttu-id="93320-112">Il ne change jamais pendant un appel et pointe toujours vers le même stockage avant et après l’appel.</span><span class="sxs-lookup"><span data-stu-id="93320-112">It never changes during a call and always points to the same storage before and after the call.</span></span>
-   <span data-ttu-id="93320-113">Les données retournées par la procédure distante sont écrites dans le stockage existant.</span><span class="sxs-lookup"><span data-stu-id="93320-113">Data returned from the remote procedure is written into the existing storage.</span></span>
-   <span data-ttu-id="93320-114">Le stockage désigné par un pointeur de référence n’est pas accessible par un autre pointeur ou tout autre nom dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="93320-114">The storage pointed to by a reference pointer cannot be accessed by any other pointer or any other name in the function.</span></span>

<span data-ttu-id="93320-115">Utilisez l' \[ [](/windows/desktop/Midl/ref) \] attribut ref pour spécifier des pointeurs de référence dans les définitions d’interface, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="93320-115">Use the \[[**ref**](/windows/desktop/Midl/ref)\] attribute to specify reference pointers in interface definitions, as shown in the following example.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

<span data-ttu-id="93320-116">Cet exemple définit le paramètre *pChar* comme un pointeur vers un caractère unique, et non un tableau de caractères.</span><span class="sxs-lookup"><span data-stu-id="93320-116">This example defines the parameter *pChar* as a pointer to a single character, not an array of characters.</span></span> <span data-ttu-id="93320-117">Il s’agit d’un paramètre de \[ **sortie** \] et d’un pointeur de référence qui pointe vers la mémoire que la routine de serveur RemoteFn remplira avec des données.</span><span class="sxs-lookup"><span data-stu-id="93320-117">It is an \[**out**\] parameter and a reference pointer that points to memory that the server routine RemoteFn will fill with data.</span></span>

 

 