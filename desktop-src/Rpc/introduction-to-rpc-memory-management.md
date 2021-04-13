---
title: Présentation de la gestion de la mémoire RPC
description: Présentation de la gestion de la mémoire de l’appel de procédure distante (RPC).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316062"
---
# <a name="introduction-to-rpc-memory-management"></a><span data-ttu-id="f387d-103">Présentation de la gestion de la mémoire RPC</span><span class="sxs-lookup"><span data-stu-id="f387d-103">Introduction to RPC Memory Management</span></span>

<span data-ttu-id="f387d-104">Dans le contexte de RPC, la gestion de la mémoire implique les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f387d-104">In the context of RPC, memory management involves:</span></span>

-   <span data-ttu-id="f387d-105">Allocation et libération de la mémoire nécessaire pour simuler un espace d’adressage conceptuel unique entre le client et le serveur dans les différents espaces d’adressage des threads du client et du serveur.</span><span class="sxs-lookup"><span data-stu-id="f387d-105">Allocating and deallocating the memory needed to simulate a single conceptual address space between the client and the server in the different address spaces of the client and server's threads.</span></span>
-   <span data-ttu-id="f387d-106">Détermination du composant logiciel responsable de la gestion de la mémoire : l’application ou le stub généré par MIDL.</span><span class="sxs-lookup"><span data-stu-id="f387d-106">Determining which software component is responsible for managing memory — the application or the MIDL-generated stub.</span></span>
-   <span data-ttu-id="f387d-107">Sélection des attributs MIDL qui affectent la gestion de la mémoire : attributs directionnels, attributs du pointeur, attributs du tableau et \[ [ \_ nombre d’octets](/windows/desktop/Midl/byte-count)des attributs ACF \] , \[ [allocation](/windows/desktop/Midl/allocate) \] et activation de l' \[ [ \_ allocation](/windows/desktop/Midl/enable-allocate) \] .</span><span class="sxs-lookup"><span data-stu-id="f387d-107">Selecting MIDL attributes that affect memory management: directional attributes, pointer attributes, array attributes, and the ACF attributes \[ [byte\_count](/windows/desktop/Midl/byte-count)\], \[ [allocate](/windows/desktop/Midl/allocate)\], and \[ [enable\_allocate](/windows/desktop/Midl/enable-allocate)\].</span></span>

<span data-ttu-id="f387d-108">Lorsqu’un programme appelle une fonction ou une procédure dans son espace d’adressage, la gestion de la mémoire est plus simple que dans une application distribuée.</span><span class="sxs-lookup"><span data-stu-id="f387d-108">When a program calls a function or procedure in its address space, memory management is more straightforward than in a distributed application.</span></span> <span data-ttu-id="f387d-109">Pour illustrer cela, le diagramme suivant illustre une arborescence binaire.</span><span class="sxs-lookup"><span data-stu-id="f387d-109">To illustrate, the following diagram depicts a binary tree.</span></span> <span data-ttu-id="f387d-110">Pour passer cette structure de données à une procédure dans son espace d’adressage, un programme passe simplement un pointeur vers la racine de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="f387d-110">To pass this data structure to a procedure in its address space, a program simply passes a pointer to the root of the tree.</span></span>

![arborescence binaire, avec des pointeurs vers des données de structure hébergées à la racine de l’arborescence](images/bintree.png)

<span data-ttu-id="f387d-112">Les applications RPC client/serveur partagent des données entre deux espaces mémoire différents.</span><span class="sxs-lookup"><span data-stu-id="f387d-112">Client/server RPC applications share data across two different memory spaces.</span></span> <span data-ttu-id="f387d-113">Ces espaces mémoire peuvent se trouver ou non sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f387d-113">These memory spaces may or may not be on the same computer.</span></span> <span data-ttu-id="f387d-114">Dans les deux cas, le client et le serveur n’ont pas d’accès direct à l’espace mémoire de l’autre.</span><span class="sxs-lookup"><span data-stu-id="f387d-114">Either way, the client and server have no direct access to each other's memory space.</span></span> <span data-ttu-id="f387d-115">RPC dépend de la capacité à simuler l’espace d’adressage du programme client dans l’espace d’adressage du programme serveur.</span><span class="sxs-lookup"><span data-stu-id="f387d-115">RPC depends on the ability to simulate the client program's address space in the server program's address space.</span></span> <span data-ttu-id="f387d-116">Elle doit également retourner les données, y compris les données nouvelles et modifiées, du serveur à la mémoire du client.</span><span class="sxs-lookup"><span data-stu-id="f387d-116">It must also return data, including new and changed data, from the server to the client memory.</span></span>

<span data-ttu-id="f387d-117">Dans les cas tels que l’arborescence binaire représentée dans le diagramme précédent, il n’est pas suffisant de passer un pointeur vers le nœud racine à une procédure distante.</span><span class="sxs-lookup"><span data-stu-id="f387d-117">In cases such as the binary tree depicted in the preceding diagram, it is not sufficient to pass a pointer to the root node to a remote procedure.</span></span> <span data-ttu-id="f387d-118">Soit le programme, soit les stubs doivent transmettre l’intégralité de l’arborescence à l’espace d’adressage du serveur pour que la procédure distante fonctionne sur celle-ci.</span><span class="sxs-lookup"><span data-stu-id="f387d-118">Either the program or the stubs must pass the entire tree to the server's address space for the remote procedure to operate on it.</span></span>

 

 