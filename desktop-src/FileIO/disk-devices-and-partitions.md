---
description: Décrit un disque dur, le partitionnement et l’enregistrement de démarrage principal.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Périphériques de disque et partitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570276"
---
# <a name="disk-devices-and-partitions"></a><span data-ttu-id="7d090-103">Périphériques de disque et partitions</span><span class="sxs-lookup"><span data-stu-id="7d090-103">Disk Devices and Partitions</span></span>

<span data-ttu-id="7d090-104">Un disque dur se compose d’un ensemble de plateaux empilés, dont les données sont stockées de façon électromagnétique dans des cercles concentriques ou des *pistes*.</span><span class="sxs-lookup"><span data-stu-id="7d090-104">A hard disk consists of a set of stacked platters, each of which has data stored electromagnetically in concentric circles, or *tracks*.</span></span> <span data-ttu-id="7d090-105">Chaque plateau a deux têtes, une à chaque côté du plateau, qui lit ou écrit des données à mesure que le disque tourne.</span><span class="sxs-lookup"><span data-stu-id="7d090-105">Each platter has two heads, one on each side of the platter, that reads or writes data as the disk spins.</span></span> <span data-ttu-id="7d090-106">Un *lecteur de disque dur* contrôle la position, la lecture et l’écriture du disque dur.</span><span class="sxs-lookup"><span data-stu-id="7d090-106">A *hard disk drive* controls the positioning, reading, and writing of the hard disk.</span></span> <span data-ttu-id="7d090-107">Notez que les têtes de tous les plateaux sont positionnés en tant qu’unité.</span><span class="sxs-lookup"><span data-stu-id="7d090-107">Note that the heads of all platters are positioned as a unit.</span></span>

<span data-ttu-id="7d090-108">La plus petite unité adressable d’une piste est un *secteur*.</span><span class="sxs-lookup"><span data-stu-id="7d090-108">The smallest addressable unit of a track is a *sector*.</span></span> <span data-ttu-id="7d090-109">Un *cylindre* est défini comme l’ensemble des pistes qui s’affichent au même emplacement sur chaque plateau.</span><span class="sxs-lookup"><span data-stu-id="7d090-109">A *cylinder* is defined as the set of tracks that appear in the same location on each platter.</span></span> <span data-ttu-id="7d090-110">Par exemple, le schéma suivant montre un disque dur avec quatre plateaux.</span><span class="sxs-lookup"><span data-stu-id="7d090-110">For example, the following diagram shows a hard disk with four platters.</span></span> <span data-ttu-id="7d090-111">Le cylindre X comprend huit pistes (piste X de chaque côté de chaque plateau).</span><span class="sxs-lookup"><span data-stu-id="7d090-111">Cylinder X consists of eight tracks (track X from each side of each platter).</span></span>

![disque dur, y compris les pistes, les secteurs et les plateaux](images/diskdevice.png)

<span data-ttu-id="7d090-113">Un disque dur peut contenir une ou plusieurs régions logiques appelées *partitions*.</span><span class="sxs-lookup"><span data-stu-id="7d090-113">A hard disk can contain one or more logical regions called *partitions*.</span></span> <span data-ttu-id="7d090-114">Les partitions sont créées lorsque l’utilisateur met en forme un disque dur en tant que *disque de base*.</span><span class="sxs-lookup"><span data-stu-id="7d090-114">Partitions are created when the user formats a hard disk as a *basic disk*.</span></span> <span data-ttu-id="7d090-115">Windows prend également en charge les *disques dynamiques*, qui ne sont pas abordés dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="7d090-115">Windows also supports *dynamic disks*, which are not discussed in this topic.</span></span> <span data-ttu-id="7d090-116">Pour plus d’informations sur les disques de base et les disques dynamiques, consultez [disques de base et dynamiques](basic-and-dynamic-disks.md).</span><span class="sxs-lookup"><span data-stu-id="7d090-116">For more information about basic disks and dynamic disks, see [Basic and Dynamic Disks](basic-and-dynamic-disks.md).</span></span>

<span data-ttu-id="7d090-117">La création de plusieurs partitions sur un disque permet l’apparition de disques durs distincts.</span><span class="sxs-lookup"><span data-stu-id="7d090-117">The creation of multiple partitions on a disk allows the appearance of having separate hard drives.</span></span> <span data-ttu-id="7d090-118">Par exemple, un système avec un disque dur doté d’une partition contient un seul volume, désigné par le système en tant que lecteur C. Un système doté d’un disque dur avec deux partitions contient généralement les lecteurs C et D. Le fait de disposer de plusieurs partitions sur un disque dur peut faciliter la gestion du système, par exemple pour organiser des fichiers ou pour prendre en charge plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7d090-118">For example, a system with one hard disk that has one partition contains a single volume, designated by the system as drive C. A system with a hard disk with two partitions typically contains drives C and D. Having multiple partitions on a hard disk can make it easier to manage the system, for example to organize files or to support multiple users.</span></span>

<span data-ttu-id="7d090-119">Le premier secteur physique sur un disque de base contient une structure de données connue sous le nom d’enregistrement de démarrage principal (MBR).</span><span class="sxs-lookup"><span data-stu-id="7d090-119">The first physical sector on a basic disk contains a data structure known as the Master Boot Record (MBR).</span></span> <span data-ttu-id="7d090-120">Le MBR contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7d090-120">The MBR contains the following:</span></span>

-   <span data-ttu-id="7d090-121">Un programme de démarrage (taille maximale de 442 octets)</span><span class="sxs-lookup"><span data-stu-id="7d090-121">A boot program (up to 442 bytes in size)</span></span>
-   <span data-ttu-id="7d090-122">Une signature de disque (nombre unique de 4 octets)</span><span class="sxs-lookup"><span data-stu-id="7d090-122">A disk signature (a unique 4-byte number)</span></span>
-   <span data-ttu-id="7d090-123">Une table de partition (jusqu’à quatre entrées);</span><span class="sxs-lookup"><span data-stu-id="7d090-123">A partition table (up to four entries)</span></span>
-   <span data-ttu-id="7d090-124">Marqueur de fin de MBR (Always 0x55AA)</span><span class="sxs-lookup"><span data-stu-id="7d090-124">An end-of-MBR marker (always 0x55AA)</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d090-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7d090-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d090-126">À propos de la gestion des volumes</span><span class="sxs-lookup"><span data-stu-id="7d090-126">About Volume Management</span></span>](about-volume-management.md)
</dt> <dt>

[<span data-ttu-id="7d090-127">Disques de base et dynamiques</span><span class="sxs-lookup"><span data-stu-id="7d090-127">Basic and Dynamic Disks</span></span>](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



