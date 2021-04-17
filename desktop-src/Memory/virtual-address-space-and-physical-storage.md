---
description: La quantité maximale de mémoire physique prise en charge par Microsoft Windows est comprise entre 2 Go et 2 to, en fonction de la version de Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Espace d’adressage virtuel et stockage physique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d36445eb2639cbfc4db2a6e4abaf28b9af87cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528888"
---
# <a name="virtual-address-space-and-physical-storage"></a><span data-ttu-id="6f80f-103">Espace d’adressage virtuel et stockage physique</span><span class="sxs-lookup"><span data-stu-id="6f80f-103">Virtual Address Space and Physical Storage</span></span>

<span data-ttu-id="6f80f-104">La quantité maximale de mémoire physique prise en charge par Microsoft Windows est comprise entre 2 Go et 24 to, en fonction de la version de Windows.</span><span class="sxs-lookup"><span data-stu-id="6f80f-104">The maximum amount of physical memory supported by Microsoft Windows ranges from 2 GB to 24 TB, depending on the version of Windows.</span></span> <span data-ttu-id="6f80f-105">Pour plus d’informations, consultez [limites de mémoire pour les versions de Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="6f80f-105">For more information, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span> <span data-ttu-id="6f80f-106">L’espace d’adressage virtuel de chaque processus peut être plus petit ou plus grand que la mémoire physique totale disponible sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6f80f-106">The virtual address space of each process can be smaller or larger than the total physical memory available on the computer.</span></span> <span data-ttu-id="6f80f-107">Le sous-ensemble de l’espace d’adressage virtuel d’un processus qui réside dans la mémoire physique est appelé la *plage de travail*.</span><span class="sxs-lookup"><span data-stu-id="6f80f-107">The subset of the virtual address space of a process that resides in physical memory is known as the *working set*.</span></span> <span data-ttu-id="6f80f-108">Si les threads d’un processus essaient d’utiliser plus de mémoire physique que ce qui est actuellement disponible, le système pagine le contenu de la mémoire sur le disque.</span><span class="sxs-lookup"><span data-stu-id="6f80f-108">If the threads of a process attempt to use more physical memory than is currently available, the system pages some of the memory contents to disk.</span></span> <span data-ttu-id="6f80f-109">La quantité totale d’espace d’adressage virtuel disponible pour un processus est limitée par la mémoire physique et l’espace libre sur le disque disponible pour le fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="6f80f-109">The total amount of virtual address space available to a process is limited by physical memory and the free space on disk available for the paging file.</span></span>

<span data-ttu-id="6f80f-110">Le stockage physique et l’espace d’adressage virtuel de chaque processus sont organisés en *pages*, en unités de mémoire dont la taille dépend de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="6f80f-110">Physical storage and the virtual address space of each process are organized into *pages*, units of memory, whose size depends on the host computer.</span></span> <span data-ttu-id="6f80f-111">Par exemple, sur les ordinateurs x86, la taille de la page hôte est de 4 kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="6f80f-111">For example, on x86 computers the host page size is 4 kilobytes.</span></span>

<span data-ttu-id="6f80f-112">Pour maximiser sa flexibilité dans la gestion de la mémoire, le système peut déplacer des pages de la mémoire physique vers et à partir d’un fichier d’échange sur le disque.</span><span class="sxs-lookup"><span data-stu-id="6f80f-112">To maximize its flexibility in managing memory, the system can move pages of physical memory to and from a paging file on disk.</span></span> <span data-ttu-id="6f80f-113">Lorsqu’une page est déplacée dans la mémoire physique, le système met à jour les mappages de pages des processus affectés.</span><span class="sxs-lookup"><span data-stu-id="6f80f-113">When a page is moved in physical memory, the system updates the page maps of the affected processes.</span></span> <span data-ttu-id="6f80f-114">Lorsque le système a besoin d’espace en mémoire physique, il déplace les pages les moins récemment utilisées de la mémoire physique vers le fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="6f80f-114">When the system needs space in physical memory, it moves the least recently used pages of physical memory to the paging file.</span></span> <span data-ttu-id="6f80f-115">La manipulation de la mémoire physique par le système est totalement transparente pour les applications, qui fonctionnent uniquement dans leurs espaces d’adressage virtuels.</span><span class="sxs-lookup"><span data-stu-id="6f80f-115">Manipulation of physical memory by the system is completely transparent to applications, which operate only in their virtual address spaces.</span></span>

 

 



