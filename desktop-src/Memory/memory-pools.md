---
description: 'Le gestionnaire de mémoire crée les pools de mémoire suivants utilisés par le système pour allouer de la mémoire : pool non paginé et pool paginé.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Pools de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60987b43347e55d8ee2d01672dbb8173ffc8dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532316"
---
# <a name="memory-pools"></a><span data-ttu-id="899ea-103">Pools de mémoire</span><span class="sxs-lookup"><span data-stu-id="899ea-103">Memory Pools</span></span>

<span data-ttu-id="899ea-104">Le gestionnaire de mémoire crée les pools de mémoire suivants utilisés par le système pour allouer de la mémoire : pool non paginé et pool paginé.</span><span class="sxs-lookup"><span data-stu-id="899ea-104">The memory manager creates the following memory pools that the system uses to allocate memory: nonpaged pool and paged pool.</span></span> <span data-ttu-id="899ea-105">Les deux pools de mémoire sont situés dans la région de l’espace d’adressage réservée pour le système et mappés à l’espace d’adressage virtuel de chaque processus.</span><span class="sxs-lookup"><span data-stu-id="899ea-105">Both memory pools are located in the region of the address space that is reserved for the system and mapped into the virtual address space of each process.</span></span> <span data-ttu-id="899ea-106">Le pool non paginé se compose d’adresses mémoire virtuelles qui sont garanties de résider dans la mémoire physique tant que les objets de noyau correspondants sont alloués.</span><span class="sxs-lookup"><span data-stu-id="899ea-106">The nonpaged pool consists of virtual memory addresses that are guaranteed to reside in physical memory as long as the corresponding kernel objects are allocated.</span></span> <span data-ttu-id="899ea-107">La réserve paginée se compose d’une mémoire virtuelle qui peut être paginée et déverrouillée du système.</span><span class="sxs-lookup"><span data-stu-id="899ea-107">The paged pool consists of virtual memory that can be paged in and out of the system.</span></span> <span data-ttu-id="899ea-108">Pour améliorer les performances, les systèmes avec un seul processeur ont trois pools paginés et les systèmes multiprocesseurs ont cinq pools paginés.</span><span class="sxs-lookup"><span data-stu-id="899ea-108">To improve performance, systems with a single processor have three paged pools, and multiprocessor systems have five paged pools.</span></span>

<span data-ttu-id="899ea-109">Les descripteurs des [objets de noyau](../sysinfo/kernel-objects.md) sont stockés dans la réserve paginée, donc le nombre de handles que vous pouvez créer est basé sur la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="899ea-109">The handles for [kernel objects](../sysinfo/kernel-objects.md) are stored in the paged pool, so the number of handles you can create is based on available memory.</span></span>

<span data-ttu-id="899ea-110">Le système enregistre les limites et les valeurs actuelles de la réserve non paginée, de la réserve paginée et de l’utilisation du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="899ea-110">The system records the limits and current values for its nonpaged pool, paged pool, and page file usage.</span></span> <span data-ttu-id="899ea-111">Pour plus d’informations, consultez [informations sur les performances](memory-performance-information.md)de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="899ea-111">For more information, see [Memory Performance Information](memory-performance-information.md).</span></span>

 

 
