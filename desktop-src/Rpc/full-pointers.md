---
title: Pointeurs complets
description: Contrairement aux pointeurs uniques, les pointeurs complets prennent en charge l’alias.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941095"
---
# <a name="full-pointers"></a><span data-ttu-id="683d0-103">Pointeurs complets</span><span class="sxs-lookup"><span data-stu-id="683d0-103">Full Pointers</span></span>

<span data-ttu-id="683d0-104">Contrairement aux pointeurs [uniques](unique-pointers.md) , les pointeurs complets prennent en charge l’alias.</span><span class="sxs-lookup"><span data-stu-id="683d0-104">Unlike [unique](unique-pointers.md) pointers, full pointers support aliasing.</span></span> <span data-ttu-id="683d0-105">Cela signifie que plusieurs pointeurs peuvent faire référence aux mêmes données, comme illustré dans la figure suivante :</span><span class="sxs-lookup"><span data-stu-id="683d0-105">This means that multiple pointers can refer to the same data, as shown in the following figure:</span></span>

![deux pointeurs référençant les mêmes données](images/prog-a02.png)

<span data-ttu-id="683d0-107">Un pointeur complet présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="683d0-107">A full pointer has the following characteristics:</span></span>

-   <span data-ttu-id="683d0-108">Elle peut avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="683d0-108">It can have the value null.</span></span>
-   <span data-ttu-id="683d0-109">Elle peut passer de null à non null pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="683d0-109">It can change from null to non-null during the call.</span></span> <span data-ttu-id="683d0-110">Lorsque la valeur devient non null, le stub client alloue la nouvelle mémoire allouée lors du retour.</span><span class="sxs-lookup"><span data-stu-id="683d0-110">When the value changes to non-null, the client stub allocates new memory allocated on return.</span></span> <span data-ttu-id="683d0-111">Le programme client doit libérer cette mémoire avant qu’elle ne se termine.</span><span class="sxs-lookup"><span data-stu-id="683d0-111">The client program should free this memory before it terminates.</span></span>
-   <span data-ttu-id="683d0-112">Elle peut passer d’une valeur non null à une valeur null pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="683d0-112">It can change from non-null to null during the call.</span></span> <span data-ttu-id="683d0-113">Lorsque la valeur est remplacée par null, l’application est responsable de la libération de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="683d0-113">When the value changes to null, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="683d0-114">La valeur peut passer d’une valeur non null à une autre.</span><span class="sxs-lookup"><span data-stu-id="683d0-114">The value can change from one non-null value to another.</span></span>
-   <span data-ttu-id="683d0-115">Le stockage vers lequel pointe un pointeur complet est accessible par un autre pointeur ou nom dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="683d0-115">The storage that a full pointer points to may be accessed by another pointer or name in the operation.</span></span>
-   <span data-ttu-id="683d0-116">Les données de retour sont écrites dans le stockage existant si le pointeur n’a pas la valeur null.</span><span class="sxs-lookup"><span data-stu-id="683d0-116">Return data is written into existing storage if the pointer does not have the value null.</span></span>

<span data-ttu-id="683d0-117">Utilisez l' \[ attribut [**ptr**](/windows/desktop/Midl/ptr) \] pour spécifier un pointeur complet, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="683d0-117">Use the \[ [**ptr**](/windows/desktop/Midl/ptr) \] attribute to specify a full pointer, as shown in the following example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

<span data-ttu-id="683d0-118">Dans cet exemple, les paramètres *ptrName1* et *ptrName2* sont définis comme des pointeurs complets vers une chaîne.</span><span class="sxs-lookup"><span data-stu-id="683d0-118">In this example the parameters *ptrName1* and *ptrName2* are defined as full pointers to a string.</span></span> <span data-ttu-id="683d0-119">Il est possible que les deux pointeurs pointent vers la même adresse mémoire contenant une seule chaîne.</span><span class="sxs-lookup"><span data-stu-id="683d0-119">It is possible for both pointers to point to the same memory address containing a single string.</span></span>

<span data-ttu-id="683d0-120">\[**pointeur** \] est requis pour fournir la prise en charge des alias.</span><span class="sxs-lookup"><span data-stu-id="683d0-120">\[**ptr**\] is required when providing aliasing support.</span></span> <span data-ttu-id="683d0-121">Toutefois, étant donné qu’elle nécessite le plus grand traitement de tous les pointeurs disponibles dans RPC, elle n’est pas recommandée pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="683d0-121">However, since it requires the most processing of all the pointers available in RPC, it is not recommended for most applications.</span></span>

 

 