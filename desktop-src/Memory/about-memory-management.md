---
description: Chaque processus sur Microsoft Windows 32 bits possède son propre espace d’adressage virtuel qui permet d’adresser jusqu’à 4 gigaoctets de mémoire.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: À propos de la gestion de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519307"
---
# <a name="about-memory-management"></a><span data-ttu-id="4ad24-103">À propos de la gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="4ad24-103">About Memory Management</span></span>

<span data-ttu-id="4ad24-104">Chaque processus sur Microsoft Windows 32 bits possède son propre espace d’adressage virtuel qui permet d’adresser jusqu’à 4 gigaoctets de mémoire.</span><span class="sxs-lookup"><span data-stu-id="4ad24-104">Each process on 32-bit Microsoft Windows has its own virtual address space that enables addressing up to 4 gigabytes of memory.</span></span> <span data-ttu-id="4ad24-105">Chaque processus sur Windows 64 bits a un espace d’adressage virtuel de 8 téraoctets.</span><span class="sxs-lookup"><span data-stu-id="4ad24-105">Each process on 64-bit Windows has a virtual address space of 8 terabytes.</span></span> <span data-ttu-id="4ad24-106">Tous les threads d’un processus peuvent accéder à son espace d’adressage virtuel.</span><span class="sxs-lookup"><span data-stu-id="4ad24-106">All threads of a process can access its virtual address space.</span></span> <span data-ttu-id="4ad24-107">Toutefois, les threads ne peuvent pas accéder à la mémoire qui appartient à un autre processus, ce qui empêche la corruption d’un processus par un autre processus.</span><span class="sxs-lookup"><span data-stu-id="4ad24-107">However, threads cannot access memory that belongs to another process, which protects a process from being corrupted by another process.</span></span>

<span data-ttu-id="4ad24-108">Pour plus d’informations sur l’espace d’adressage virtuel et les fonctions de gestion de la mémoire, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="4ad24-108">For information on the virtual address space and the memory management functions, see the following topics.</span></span>

-   [<span data-ttu-id="4ad24-109">Espace d’adressage virtuel</span><span class="sxs-lookup"><span data-stu-id="4ad24-109">Virtual Address Space</span></span>](virtual-address-space.md)
-   [<span data-ttu-id="4ad24-110">Pools de mémoire</span><span class="sxs-lookup"><span data-stu-id="4ad24-110">Memory Pools</span></span>](memory-pools.md)
-   [<span data-ttu-id="4ad24-111">Informations sur les performances de la mémoire</span><span class="sxs-lookup"><span data-stu-id="4ad24-111">Memory Performance Information</span></span>](memory-performance-information.md)
-   [<span data-ttu-id="4ad24-112">Fonctions de mémoire virtuelle</span><span class="sxs-lookup"><span data-stu-id="4ad24-112">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
-   [<span data-ttu-id="4ad24-113">Fonctions de tas</span><span class="sxs-lookup"><span data-stu-id="4ad24-113">Heap Functions</span></span>](heap-functions.md)
-   [<span data-ttu-id="4ad24-114">Mappage de fichiers</span><span class="sxs-lookup"><span data-stu-id="4ad24-114">File Mapping</span></span>](file-mapping.md)
-   [<span data-ttu-id="4ad24-115">Prise en charge de mémoire importante</span><span class="sxs-lookup"><span data-stu-id="4ad24-115">Large Memory Support</span></span>](large-memory-support.md)
-   [<span data-ttu-id="4ad24-116">Fonctions globales et locales</span><span class="sxs-lookup"><span data-stu-id="4ad24-116">Global and Local Functions</span></span>](global-and-local-functions.md)
-   [<span data-ttu-id="4ad24-117">Fonctions de la bibliothèque C standard</span><span class="sxs-lookup"><span data-stu-id="4ad24-117">Standard C Library Functions</span></span>](standard-c-library-functions.md)
-   [<span data-ttu-id="4ad24-118">Comparaison des méthodes d’allocation de mémoire</span><span class="sxs-lookup"><span data-stu-id="4ad24-118">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)

 

 



