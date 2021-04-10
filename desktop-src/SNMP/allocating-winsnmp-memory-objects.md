---
title: Allocation d’objets de mémoire WinSNMP
description: Les descripteurs, les handles de ressource et les chaînes de style C sont les trois types d’objets de mémoire dans l’environnement de programmation WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028536"
---
# <a name="allocating-winsnmp-memory-objects"></a><span data-ttu-id="1e92a-103">Allocation d’objets de mémoire WinSNMP</span><span class="sxs-lookup"><span data-stu-id="1e92a-103">Allocating WinSNMP Memory Objects</span></span>

<span data-ttu-id="1e92a-104">Les descripteurs, les handles de ressource et les chaînes de style C sont les trois types d’objets de mémoire dans l’environnement de programmation WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="1e92a-104">Descriptors, resource handles and C-style strings are the three types of memory objects in the WinSNMP programming environment.</span></span>

<span data-ttu-id="1e92a-105">Le type d’objet détermine si l’implémentation de l’WinSNMP de Microsoft ou l’application WinSNMP alloue et libère la mémoire pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="1e92a-105">The type of object determines whether the Microsoft WinSNMP implementation or the WinSNMP application allocates and deallocates the memory for the object.</span></span> <span data-ttu-id="1e92a-106">Cela réduit l’allocation inutile de l’espace de la mémoire tampon temporaire et la copie inutile des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="1e92a-106">This reduces unnecessary allocation of temporary buffer space and unnecessary copying of buffers.</span></span>

<span data-ttu-id="1e92a-107">Le tableau suivant résume l’allocation et la désallocation des ressources pour les objets mémoire WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="1e92a-107">The following table summarizes the allocation and deallocation of resources for WinSNMP memory objects.</span></span>



| <span data-ttu-id="1e92a-108">Type d’objet</span><span class="sxs-lookup"><span data-stu-id="1e92a-108">Object type</span></span>                                                                   | <span data-ttu-id="1e92a-109">Description</span><span class="sxs-lookup"><span data-stu-id="1e92a-109">Description</span></span>                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e92a-110">descripteur [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)</span><span class="sxs-lookup"><span data-stu-id="1e92a-110">[**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor</span></span> | <span data-ttu-id="1e92a-111">Si l’application WinSNMP alloue de la mémoire, elle doit libérer la mémoire avec un appel à une fonction appropriée.</span><span class="sxs-lookup"><span data-stu-id="1e92a-111">If the WinSNMP application allocates the memory, it must deallocate the memory with a call to an appropriate function.</span></span> <span data-ttu-id="1e92a-112">Si l’implémentation alloue la mémoire, l’application doit appeler la fonction [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1e92a-112">If the implementation allocates the memory, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to deallocate the memory.</span></span> |
| <span data-ttu-id="1e92a-113">[**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) , structure</span><span class="sxs-lookup"><span data-stu-id="1e92a-113">[**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure</span></span>                                    | <span data-ttu-id="1e92a-114">Si le membre de **valeur** est un descripteur [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , l’application doit s’exécuter comme indiqué ci-dessus pour les descripteurs.</span><span class="sxs-lookup"><span data-stu-id="1e92a-114">If the **value** member is an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor, the application must proceed as indicated above for descriptors.</span></span>                                                                                                     |
| <span data-ttu-id="1e92a-115">Handle de ressource</span><span class="sxs-lookup"><span data-stu-id="1e92a-115">Resource handle</span></span>                                                               | <span data-ttu-id="1e92a-116">L’implémentation alloue, gère et libère la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1e92a-116">The implementation allocates, manages, and frees the memory.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="1e92a-117">Chaîne de style C</span><span class="sxs-lookup"><span data-stu-id="1e92a-117">C-style string</span></span>                                                                | <span data-ttu-id="1e92a-118">L’application WinSNMP doit gérer et libérer la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="1e92a-118">The WinSNMP application must manage and free the memory it allocates.</span></span>                                                                                                                                                                                                                |



 

<span data-ttu-id="1e92a-119">Pour plus d’informations, consultez [libération de descripteurs WinSNMP](freeing-winsnmp-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="1e92a-119">For more information, see [Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md).</span></span>

 

 




