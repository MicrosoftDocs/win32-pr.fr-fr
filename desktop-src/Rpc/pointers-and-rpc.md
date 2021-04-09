---
title: Pointeurs et RPC
description: Il est très efficace d’utiliser des pointeurs en tant que paramètres de fonction C.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840521"
---
# <a name="pointers-and-rpc"></a><span data-ttu-id="77f21-103">Pointeurs et RPC</span><span class="sxs-lookup"><span data-stu-id="77f21-103">Pointers and RPC</span></span>

<span data-ttu-id="77f21-104">Il est très efficace d’utiliser des pointeurs en tant que paramètres de fonction C.</span><span class="sxs-lookup"><span data-stu-id="77f21-104">It is very efficient to use pointers as C-function parameters.</span></span> <span data-ttu-id="77f21-105">Le pointeur ne coûte que quelques octets et peut être utilisé pour accéder à une grande quantité de mémoire.</span><span class="sxs-lookup"><span data-stu-id="77f21-105">The pointer costs only a few bytes and can be used to access a large amount of memory.</span></span> <span data-ttu-id="77f21-106">Toutefois, dans une application distribuée, les procédures du client et du serveur se trouvent dans des espaces d’adressage différents ; elles peuvent être sur des ordinateurs différents.</span><span class="sxs-lookup"><span data-stu-id="77f21-106">However, in a distributed application, the client and server procedures reside in different address spaces—they can be on different computers.</span></span> <span data-ttu-id="77f21-107">Par conséquent, le client et le serveur n’ont généralement pas accès au même espace mémoire.</span><span class="sxs-lookup"><span data-stu-id="77f21-107">Therefore, the client and the server usually do not have access to the same memory space.</span></span>

<span data-ttu-id="77f21-108">Quand l’un des paramètres de la procédure distante est un pointeur vers un objet, le client doit transmettre une copie de cet objet et de son pointeur au serveur.</span><span class="sxs-lookup"><span data-stu-id="77f21-108">When one of the remote procedure's parameters is a pointer to an object, the client must transmit a copy of that object and its pointer to the server.</span></span> <span data-ttu-id="77f21-109">Si la procédure distante modifie l’objet par le biais de son pointeur, le serveur retourne le pointeur et sa copie modifiée.</span><span class="sxs-lookup"><span data-stu-id="77f21-109">If the remote procedure modifies the object through its pointer, the server returns the pointer and its modified copy.</span></span>

<span data-ttu-id="77f21-110">MIDL offre des attributs de pointeur pour réduire la quantité de surcharge requise et la taille de votre application.</span><span class="sxs-lookup"><span data-stu-id="77f21-110">MIDL offers pointer attributes to minimize the amount of required overhead and the size of your application.</span></span> <span data-ttu-id="77f21-111">Cette section traite de l’objectif et des utilisations des attributs de pointeur MIDL.</span><span class="sxs-lookup"><span data-stu-id="77f21-111">This section discusses the purpose and uses of MIDL pointer attributes.</span></span> <span data-ttu-id="77f21-112">Elle présente également des informations sur la gestion des pointeurs dans les applications RPC.</span><span class="sxs-lookup"><span data-stu-id="77f21-112">It also presents information on pointer handling in RPC applications.</span></span> <span data-ttu-id="77f21-113">Elle est composée des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="77f21-113">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="77f21-114">Genres de pointeurs</span><span class="sxs-lookup"><span data-stu-id="77f21-114">Kinds of Pointers</span></span>](kinds-of-pointers.md)
-   [<span data-ttu-id="77f21-115">Pointeurs et allocation de mémoire</span><span class="sxs-lookup"><span data-stu-id="77f21-115">Pointers and Memory Allocation</span></span>](pointers-and-memory-allocation.md)
-   [<span data-ttu-id="77f21-116">Types de pointeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="77f21-116">Default Pointer Types</span></span>](default-pointer-types.md)
-   [<span data-ttu-id="77f21-117">Héritage de type d’attribut de pointeur</span><span class="sxs-lookup"><span data-stu-id="77f21-117">Pointer-Attribute Type Inheritance</span></span>](pointer-attribute-type-inheritance.md)

 

 




