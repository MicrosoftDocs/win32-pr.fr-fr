---
title: La nouvelle API permet aux applications d’envoyer des indicateurs « supprimer et annuler le mappage » sur des supports de stockage
description: La nouvelle API permet aux applications d’envoyer \ 0034 ; TRIM et DEMAPPAGE \ 0034 ; indications sur les supports de stockage
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "106511518"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a><span data-ttu-id="b33a6-103">La nouvelle API permet aux applications d’envoyer des indicateurs « supprimer et annuler le mappage » sur des supports de stockage</span><span class="sxs-lookup"><span data-stu-id="b33a6-103">New API allows apps to send "TRIM and Unmap" hints to storage media</span></span>

## <a name="platforms"></a><span data-ttu-id="b33a6-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="b33a6-104">Platforms</span></span>

<span data-ttu-id="b33a6-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="b33a6-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="b33a6-106">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b33a6-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="b33a6-107">Description</span><span class="sxs-lookup"><span data-stu-id="b33a6-107">Description</span></span>

<span data-ttu-id="b33a6-108">Les indicateurs de découpage informent le lecteur que certains secteurs qui ont été alloués précédemment ne sont plus nécessaires à l’application et peuvent être purgés.</span><span class="sxs-lookup"><span data-stu-id="b33a6-108">TRIM hints notify the drive that certain sectors that previously were allocated are no longer needed by the app and can be purged.</span></span> <span data-ttu-id="b33a6-109">Cette valeur est généralement utilisée lorsqu’une application effectue des allocations d’espace importantes par le biais d’un fichier, puis gère automatiquement les allocations dans le fichier (par exemple, les fichiers de disque dur virtuel).</span><span class="sxs-lookup"><span data-stu-id="b33a6-109">This is typically used when an app makes large space allocations via a file and then self-manages the allocations to the file (for example, Virtual Hard Disk files).</span></span>

<span data-ttu-id="b33a6-110">**Qu’est-ce que TRIM ?**</span><span class="sxs-lookup"><span data-stu-id="b33a6-110">**What is TRIM?**</span></span>

<span data-ttu-id="b33a6-111">Les disques SSD (Solid State Drives) sont généralement des appareils avec effacement de blocs basés sur la mémoire flash ; Cela signifie que lorsque les données sont écrites dans le SSD, elles ne peuvent pas être remplacées et doivent être écrites ailleurs jusqu’à ce que le bloc puisse être récupéré par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="b33a6-111">Solid state drives (SSDs) are typically flash memory based block-erased devices; this means that when data is written to the SSD, it cannot be over-written in place and must be written elsewhere until the block can be garbage collected.</span></span> <span data-ttu-id="b33a6-112">Étant donné que le SSD n’a pas de mécanisme interne pour déterminer que certains blocs sont supprimés et que d’autres sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b33a6-112">Since the SSD has no internal mechanism for determining that certain blocks are removed and others are needed.</span></span> <span data-ttu-id="b33a6-113">La seule fois où le SSD peut marquer un « impropre » de secteur est lorsqu’il est trop écrit.</span><span class="sxs-lookup"><span data-stu-id="b33a6-113">The only time the SSD can mark a sector ‘dirty’ is when it is over-written.</span></span> <span data-ttu-id="b33a6-114">Dans d’autres cas, par exemple lors de la suppression d’un fichier, le disque SSD conserve ces secteurs, car la suppression est effectuée en tant que modification de table de fichiers maîtres (MFT) uniquement, et non en tant qu’opération à tous les secteurs du fichier.</span><span class="sxs-lookup"><span data-stu-id="b33a6-114">In other cases, such as when a file is deleted, the SSD retains these sectors because the deletion is performed as a master file table (MFT) change only, and not as an operation to all the sectors of the file.</span></span> <span data-ttu-id="b33a6-115">Dans Windows 7, nous avons introduit une méthode standard de communication avec les disques SSD à propos des secteurs qui ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b33a6-115">In Windows 7, we introduced a standard way of communicating with SSDs about sectors that are not needed any more.</span></span> <span data-ttu-id="b33a6-116">Cette commande est définie dans la [spécification T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) comme commande Trim ; NTFS envoie la commande TRIM pour certaines opérations Inline normales, telles que « DeleteFile ».</span><span class="sxs-lookup"><span data-stu-id="b33a6-116">This command is defined in the [T13 specification](https://www.t13.org/Standards/Default.aspx?DocumentType=3) as the TRIM command; NTFS sends the TRIM command for some normal inline operations such as “deletefile.”</span></span>

<span data-ttu-id="b33a6-117">**Autres utilisations du découpage dans le monde du stockage**</span><span class="sxs-lookup"><span data-stu-id="b33a6-117">**Other uses of TRIM in the storage world**</span></span>

<span data-ttu-id="b33a6-118">Comme les disques SSD, les réseaux de zone de stockage (San) et les nouvelles mises en œuvre de l’espace logiciel de la fonctionnalité Windows 8 consomment les indicateurs de commande TRIM pour gérer leurs espaces dans les environnements alloués dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="b33a6-118">Like SSDs, storage area networks (SANs) and the new Windows 8 feature Software Spaces implementations consume TRIM command hints to manage their spaces in thinly provisioned environments.</span></span> <span data-ttu-id="b33a6-119">Les espaces San et logiciels allouent des régions de stockage dans des tailles supérieures à celles des secteurs ou des clusters (n’importe où entre 1 Mo et 1 Go).</span><span class="sxs-lookup"><span data-stu-id="b33a6-119">SANs and Software Spaces allocate regions of storage in sizes that are greater than sectors or clusters (anywhere from 1MB to 1GB).</span></span> <span data-ttu-id="b33a6-120">Lorsqu’ils reçoivent des indicateurs de découpage pour la taille d’allocation (ou supérieur à la taille d’allocation), le SAN/SSD peut désallouer une région pour libérer de l’espace pour d’autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="b33a6-120">When they receive TRIM hints for its allocation size (or greater than the allocation size), the SAN/SSD can de-allocate a region to free up the space for other files.</span></span> <span data-ttu-id="b33a6-121">Ils transmettent généralement tous les indicateurs de découpage au média sous-jacent (SSD ou HDD) afin qu’ils puissent consommer l’espace libéré comme il convient.</span><span class="sxs-lookup"><span data-stu-id="b33a6-121">They typically pass through all TRIM hints to the underlying media (SSD or HDD) so that they can consume the freed up space as appropriate.</span></span> <span data-ttu-id="b33a6-122">Elles ne déplacent généralement pas les données dans les régions de désallocation, ni n’effectuent le suivi des zones de découpage dans les zones désallouées (lorsque la région est vide).</span><span class="sxs-lookup"><span data-stu-id="b33a6-122">They do not typically move data around to de-allocate regions, nor do they keep track of TRIM areas to de-allocated regions (when the region is empty).</span></span>

<span data-ttu-id="b33a6-123">Les réseaux San alloués dynamiquement utilisent les indicateurs de découpage qui leur sont transmis pour réduire l’encombrement de stockage physique global, réduisant ainsi les coûts.</span><span class="sxs-lookup"><span data-stu-id="b33a6-123">Thinly provisioned SANs use the TRIM hints that are passed to them to help reduce the overall physical storage footprint, hence reducing cost.</span></span> <span data-ttu-id="b33a6-124">La [spécification SCSI de T10](https://www.t10.org) définit la commande’Annuler' (semblable à la commande Trim). ici, la commande s’applique à tous les types de stockage, y compris les disques durs, les disques SSD et d’autres.</span><span class="sxs-lookup"><span data-stu-id="b33a6-124">The [T10 SCSI specification](https://www.t10.org) defines the ‘Unmap’ command (similar to the TRIM command); here the command is applicable to all kinds of storage including HDDs, SSDs, and others.</span></span> <span data-ttu-id="b33a6-125">La commande de mappage permet de supprimer des blocs physiques de l’allocation du SAN.</span><span class="sxs-lookup"><span data-stu-id="b33a6-125">The UnMap command helps to remove physical blocks from the SAN’s allocation.</span></span>

## <a name="how-to-use-the-new-api"></a><span data-ttu-id="b33a6-126">Utilisation de la nouvelle API</span><span class="sxs-lookup"><span data-stu-id="b33a6-126">How to use the new API</span></span>


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



<span data-ttu-id="b33a6-127">Le découpage de fichier est passé via la mémoire tampon si possible ou de manière asynchrone (sans mise en mémoire tampon) au découpage de commande du DSM IOCTL d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b33a6-127">File TRIM is passed via the buffer if possible or asynchronously (non-buffered) to the Device IOCTL DSM command TRIM.</span></span> <span data-ttu-id="b33a6-128">Elle est mappée à la commande TRIM pour les périphériques ATA et à la commande de mappage pour les périphériques SCSI.</span><span class="sxs-lookup"><span data-stu-id="b33a6-128">This is mapped to the TRIM command for ATA devices and UnMap command for SCSI devices.</span></span> <span data-ttu-id="b33a6-129">Le code d’ajustement de fichier envoie les régions un par un, comme spécifié par les étendues ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b33a6-129">The file TRIM code sends the regions one-by-one as specified by the extents above.</span></span>

<span data-ttu-id="b33a6-130">Le découpage de fichier n’attend pas les retours de l’appareil, car les commandes TRIM et DEMAPPAGE sont définies comme indicateurs sur le support de stockage sous-jacent et les codes de retour ne sont pas attendus.</span><span class="sxs-lookup"><span data-stu-id="b33a6-130">File TRIM does not wait for returns from the device, because the TRIM and Unmap commands are defined as hints to the underlying storage media and return codes are not expected.</span></span>

<span data-ttu-id="b33a6-131">**Flux de travail de bout en bout :**</span><span class="sxs-lookup"><span data-stu-id="b33a6-131">**End-to-end workflow:**</span></span>

1.  <span data-ttu-id="b33a6-132">Découper le fichier d’appel</span><span class="sxs-lookup"><span data-stu-id="b33a6-132">Call File Trim</span></span>
    1.  <span data-ttu-id="b33a6-133">L’ajustement de fichier examine les entrées pour rechercher les erreurs</span><span class="sxs-lookup"><span data-stu-id="b33a6-133">File TRIM examines inputs for errors</span></span>
    2.  <span data-ttu-id="b33a6-134">La suppression de fichier fractionne les étendues dans les régions LCN</span><span class="sxs-lookup"><span data-stu-id="b33a6-134">File TRIM breaks up the extents into LCN regions</span></span>
    3.  <span data-ttu-id="b33a6-135">La suppression des fichiers est arrondie à la taille des régions mal alignées qui sont passées à la suppression</span><span class="sxs-lookup"><span data-stu-id="b33a6-135">File TRIM rounds up and down for mis-aligned regions that are passed into TRIM</span></span>
    4.  <span data-ttu-id="b33a6-136">La suppression de fichiers purge les entrées du cache qui se rapportent aux zones de suppression.</span><span class="sxs-lookup"><span data-stu-id="b33a6-136">File TRIM purges entries in the cache that relate to the TRIM areas</span></span>
    5.  <span data-ttu-id="b33a6-137">La suppression de fichier passe le \_ DSM ioctl (Trim) par région</span><span class="sxs-lookup"><span data-stu-id="b33a6-137">File TRIM passes IOCTL\_DSM (Trim) per region</span></span>
2.  <span data-ttu-id="b33a6-138">La suppression du fichier renvoie ou des erreurs</span><span class="sxs-lookup"><span data-stu-id="b33a6-138">File TRIM returns or errors</span></span>
    1.  <span data-ttu-id="b33a6-139">La vérification des erreurs est effectuée au niveau de la validité de l’entrée</span><span class="sxs-lookup"><span data-stu-id="b33a6-139">Error checking is done on input validity</span></span>
    2.  <span data-ttu-id="b33a6-140">Si seules certaines étendues sont valides, une erreur est retournée pour l’appel complet de l’API</span><span class="sxs-lookup"><span data-stu-id="b33a6-140">If only some of the extents are valid, one error is returned for the complete API call</span></span>

<span data-ttu-id="b33a6-141">**Cas d’utilisation**</span><span class="sxs-lookup"><span data-stu-id="b33a6-141">**Use cases**</span></span>

<span data-ttu-id="b33a6-142">**Disque dur virtuel (VHD) de consommateur monté sur un disque SSD :**</span><span class="sxs-lookup"><span data-stu-id="b33a6-142">**Consumer virtual hard disk (VHD) mounted on an SSD:**</span></span>

<span data-ttu-id="b33a6-143">Le disque dur virtuel est initialement monté sur le média non utilisé « Clean ».</span><span class="sxs-lookup"><span data-stu-id="b33a6-143">The VHD is initially mounted on ‘clean’ unused media.</span></span> <span data-ttu-id="b33a6-144">Au fur et à mesure que le disque dur virtuel est utilisé, le disque dur virtuel consomme des parties du support de stockage pour les fichiers, etc. Lorsqu’il supprime des fichiers du support de stockage, ces fichiers ne sont pas supprimés du disque SSD puisque le VHD complet est stocké sous la forme d’un fichier sur le disque SSD.</span><span class="sxs-lookup"><span data-stu-id="b33a6-144">As the VHD is used, the VHD consumes parts of the storage media for files, etc. When it deletes files in the storage media, these files are not removed from the SSD since the complete VHD is stored as one file on the SSD.</span></span> <span data-ttu-id="b33a6-145">L’environnement Hyper-V appelle la suppression de fichiers pour toutes les régions qui sont supprimées lorsque Delete-File se produit dans l’environnement VHD.</span><span class="sxs-lookup"><span data-stu-id="b33a6-145">The Hyper-V environment calls File TRIM for all regions that are deleted when delete-file occurs in the VHD environment.</span></span> <span data-ttu-id="b33a6-146">Les \_ suppressions de fichiers sont traduites dans le SSD pour permettre l’optimisation des performances des disques SSD.</span><span class="sxs-lookup"><span data-stu-id="b33a6-146">The File\_TRIMs are translated to the SSD so that the SSD performance can be optimized.</span></span>

<span data-ttu-id="b33a6-147">**VHD de consommateur monté sur un réseau SAN alloué dynamiquement :**</span><span class="sxs-lookup"><span data-stu-id="b33a6-147">**Consumer VHD mounted on a thinly provisioned SAN:**</span></span>

<span data-ttu-id="b33a6-148">Le disque dur virtuel est initialement monté sur une plaque minimale d’un environnement dynamiquement approvisionné.</span><span class="sxs-lookup"><span data-stu-id="b33a6-148">The VHD is initially mounted on one minimum slab of a thinly provisioned environment.</span></span> <span data-ttu-id="b33a6-149">Au fur et à mesure que les fichiers sont stockés dans le disque dur virtuel, l’encombrement de stockage du disque dur virtuel augmente en multiples de tablettes.</span><span class="sxs-lookup"><span data-stu-id="b33a6-149">As files are stored in the VHD, the storage footprint of the VHD grows in multiples of slabs.</span></span> <span data-ttu-id="b33a6-150">Lorsque des fichiers sont supprimés du disque dur virtuel, Hyper-V appelle la \_ Suppression de fichiers sur le réseau San sous-jacent alloué dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="b33a6-150">When files are removed in the VHD, the Hyper-V calls File\_TRIM to the underlying thinly provisioned SAN.</span></span> <span data-ttu-id="b33a6-151">Si les SUPPRESSIONs sont supérieures à la granularité de la dalle, le réseau SAN peut maintenant supprimer une dalle et, par conséquent, réduire l’encombrement du disque dur virtuel sur ce réseau SAN.</span><span class="sxs-lookup"><span data-stu-id="b33a6-151">If the TRIMs are bigger than the SLAB granularity, the SAN can now remove a SLAB and hence reduce the footprint of the VHD on that SAN.</span></span>

<span data-ttu-id="b33a6-152">Si le disque dur virtuel réside sur un serveur Windows 8, l’optimiseur de stockage enverra également des découpages pour réduire l’encombrement des dalles du disque dur virtuel à partir du disque dur virtuel monté.</span><span class="sxs-lookup"><span data-stu-id="b33a6-152">If the VHD is resident on a Windows 8 based server, the Storage Optimizer will also send TRIMs to reduce the slab footprint of the VHD from within the mounted VHD.</span></span>

## <a name="tests"></a><span data-ttu-id="b33a6-153">Tests</span><span class="sxs-lookup"><span data-stu-id="b33a6-153">Tests</span></span>

<span data-ttu-id="b33a6-154">Il n’existe pas d’API comparables dans les versions antérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b33a6-154">There are no comparable APIs in earlier operating system releases.</span></span> <span data-ttu-id="b33a6-155">L’API elle-même ne doit pas avoir d’impact sur les performances. Toutefois, le support de stockage (s’il est implémenté correctement) peut présenter de meilleures performances en écriture.</span><span class="sxs-lookup"><span data-stu-id="b33a6-155">There should be no performance impact from the actual API itself, though the storage media (if implemented correctly) can show better write performance.</span></span> <span data-ttu-id="b33a6-156">L’API doit être utilisée très attentivement ; seules les extensions qui ne sont plus nécessaires doivent être transmises, car celles-ci sont définitivement supprimées du support de stockage.</span><span class="sxs-lookup"><span data-stu-id="b33a6-156">The API should be used very carefully; only extents that are no longer needed should be passed down as those extents will be permanently removed from the storage media.</span></span>

## <a name="resources"></a><span data-ttu-id="b33a6-157">Ressources</span><span class="sxs-lookup"><span data-stu-id="b33a6-157">Resources</span></span>

-   [<span data-ttu-id="b33a6-158">Spécification T13</span><span class="sxs-lookup"><span data-stu-id="b33a6-158">T13 specification</span></span>](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [<span data-ttu-id="b33a6-159">Spécification SCSI de T10</span><span class="sxs-lookup"><span data-stu-id="b33a6-159">T10 SCSI specification</span></span>](https://www.t10.org/)

 

 




