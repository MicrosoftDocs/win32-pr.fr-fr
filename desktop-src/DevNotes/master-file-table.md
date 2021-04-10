---
description: La table de fichiers maîtres (MFT) stocke les informations requises pour récupérer des fichiers à partir d’une partition NTFS.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Table de fichiers maîtres (remarques pour les développeurs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950415"
---
# <a name="master-file-table"></a><span data-ttu-id="2ea49-103">Table de fichiers maîtres</span><span class="sxs-lookup"><span data-stu-id="2ea49-103">Master File Table</span></span>

<span data-ttu-id="2ea49-104">\[Ce document s’applique uniquement à la version 3 des volumes NTFS.\]</span><span class="sxs-lookup"><span data-stu-id="2ea49-104">\[This document applies only to version 3 of NTFS volumes.\]</span></span>

<span data-ttu-id="2ea49-105">La table de fichiers maîtres (MFT) stocke les informations requises pour récupérer des fichiers à partir d’une partition NTFS.</span><span class="sxs-lookup"><span data-stu-id="2ea49-105">The master file table (MFT) stores the information required to retrieve files from an NTFS partition.</span></span>

<span data-ttu-id="2ea49-106">Un fichier peut avoir un ou plusieurs enregistrements MFT et peut contenir un ou plusieurs attributs.</span><span class="sxs-lookup"><span data-stu-id="2ea49-106">A file may have one or more MFT records, and can contain one or more attributes.</span></span> <span data-ttu-id="2ea49-107">Dans NTFS, une référence de fichier correspond à la référence de segment MFT de l’enregistrement de fichier de base.</span><span class="sxs-lookup"><span data-stu-id="2ea49-107">In NTFS, a file reference is the MFT segment reference of the base file record.</span></span> <span data-ttu-id="2ea49-108">Pour plus d’informations, [**consultez \_ \_ référence des segments MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2ea49-108">For more information, see [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

<span data-ttu-id="2ea49-109">La table MFT contient des segments d’enregistrement de fichier ; les 16 premiers sont réservés aux fichiers spéciaux, tels que les suivants :</span><span class="sxs-lookup"><span data-stu-id="2ea49-109">The MFT contains file record segments; the first 16 of these are reserved for special files, such as the following:</span></span>

-   <span data-ttu-id="2ea49-110">0 : MFT ($Mft)</span><span class="sxs-lookup"><span data-stu-id="2ea49-110">0: MFT ($Mft)</span></span>
-   <span data-ttu-id="2ea49-111">5 : répertoire racine ( \\ )</span><span class="sxs-lookup"><span data-stu-id="2ea49-111">5: root directory (\\)</span></span>
-   <span data-ttu-id="2ea49-112">6 : fichier d’allocation de cluster de volumes ($Bitmap)</span><span class="sxs-lookup"><span data-stu-id="2ea49-112">6: volume cluster allocation file ($Bitmap)</span></span>
-   <span data-ttu-id="2ea49-113">8 : fichier de cluster incorrect ($BadClus)</span><span class="sxs-lookup"><span data-stu-id="2ea49-113">8: bad-cluster file ($BadClus)</span></span>

<span data-ttu-id="2ea49-114">Chaque segment d’enregistrement de fichier commence par un en-tête de segment d’enregistrement de fichier.</span><span class="sxs-lookup"><span data-stu-id="2ea49-114">Each file record segment starts with a file record segment header.</span></span> <span data-ttu-id="2ea49-115">Pour plus d’informations, consultez l' [**\_ \_ \_ en-tête de segment d’enregistrement de fichier**](file-record-segment-header.md).</span><span class="sxs-lookup"><span data-stu-id="2ea49-115">For more information, see [**FILE\_RECORD\_SEGMENT\_HEADER**](file-record-segment-header.md).</span></span> <span data-ttu-id="2ea49-116">Chaque segment d’enregistrement de fichier est suivi d’un ou plusieurs attributs.</span><span class="sxs-lookup"><span data-stu-id="2ea49-116">Each file record segment is followed by one or more attributes.</span></span> <span data-ttu-id="2ea49-117">Chaque attribut commence par un en-tête d’enregistrement d’attribut.</span><span class="sxs-lookup"><span data-stu-id="2ea49-117">Each attribute starts with an attribute record header.</span></span> <span data-ttu-id="2ea49-118">Pour plus d’informations, consultez l' [**\_ \_ en-tête d’enregistrement d’attribut**](attribute-record-header.md).</span><span class="sxs-lookup"><span data-stu-id="2ea49-118">For more information, see [**ATTRIBUTE\_RECORD\_HEADER**](attribute-record-header.md).</span></span> <span data-ttu-id="2ea49-119">L’enregistrement d’attribut comprend le type d’attribut (par exemple $DATA ou $BITMAP), un nom facultatif et la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="2ea49-119">The attribute record includes the attribute type (such as $DATA or $BITMAP), an optional name, and the attribute value.</span></span> <span data-ttu-id="2ea49-120">Le flux de données utilisateur est un attribut, comme tous les flux.</span><span class="sxs-lookup"><span data-stu-id="2ea49-120">The user data stream is an attribute, as are all streams.</span></span> <span data-ttu-id="2ea49-121">La liste d’attributs se termine par 0xFFFFFFFF ($END).</span><span class="sxs-lookup"><span data-stu-id="2ea49-121">The attribute list is terminated with 0xFFFFFFFF ($END).</span></span>

<span data-ttu-id="2ea49-122">Voici quelques exemples d’attributs.</span><span class="sxs-lookup"><span data-stu-id="2ea49-122">The following are some example attributes.</span></span>

-   <span data-ttu-id="2ea49-123">Le fichier $Mft contient un attribut $DATA sans nom qui correspond à la séquence des segments d’enregistrement MFT, dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="2ea49-123">The $Mft file contains an unnamed $DATA attribute that is the sequence of MFT record segments, in order.</span></span>
-   <span data-ttu-id="2ea49-124">Le fichier $Mft contient un attribut $BITMAP sans nom qui indique les enregistrements MFT en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="2ea49-124">The $Mft file contains an unnamed $BITMAP attribute that indicates which MFT records are in use.</span></span>
-   <span data-ttu-id="2ea49-125">Le fichier $Bitmap contient un attribut $DATA sans nom qui indique quels clusters sont en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="2ea49-125">The $Bitmap file contains an unnamed $DATA attribute that indicates which clusters are in use.</span></span>
-   <span data-ttu-id="2ea49-126">Le fichier $BadClus contient un attribut $DATA nommé $BAD qui contient une entrée qui correspond à chaque cluster incorrect.</span><span class="sxs-lookup"><span data-stu-id="2ea49-126">The $BadClus file contains a $DATA attribute named $BAD that contains an entry that corresponds to each bad cluster.</span></span>

<span data-ttu-id="2ea49-127">Lorsqu’il n’y a plus d’espace pour le stockage des attributs dans le segment d’enregistrement de fichier, des segments d’enregistrement de fichier supplémentaires sont alloués et insérés dans le premier segment d’enregistrement de fichier (ou de base) dans un attribut appelé liste d’attributs.</span><span class="sxs-lookup"><span data-stu-id="2ea49-127">When there is no more space for storing attributes in the file record segment, additional file record segments are allocated and inserted in the first (or base) file record segment in an attribute called the attribute list.</span></span> <span data-ttu-id="2ea49-128">La liste d’attributs indique où chaque attribut associé au fichier est trouvé.</span><span class="sxs-lookup"><span data-stu-id="2ea49-128">The attribute list indicates where each attribute associated with the file can be found.</span></span> <span data-ttu-id="2ea49-129">Cela comprend tous les attributs de l’enregistrement de fichier de base, à l’exception de la liste d’attributs elle-même.</span><span class="sxs-lookup"><span data-stu-id="2ea49-129">This includes all attributes in the base file record, except for the attribute list itself.</span></span> <span data-ttu-id="2ea49-130">Pour plus d’informations, [**consultez \_ \_ entrée de liste d’attributs**](attribute-list-entry.md).</span><span class="sxs-lookup"><span data-stu-id="2ea49-130">For more information, see [**ATTRIBUTE\_LIST\_ENTRY**](attribute-list-entry.md).</span></span>

<span data-ttu-id="2ea49-131">Les structures associées à la table MFT sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ea49-131">Structures related to the MFT include the following:</span></span>

-   [<span data-ttu-id="2ea49-132">**\_entrée de liste d’attributs \_**</span><span class="sxs-lookup"><span data-stu-id="2ea49-132">**ATTRIBUTE\_LIST\_ENTRY**</span></span>](attribute-list-entry.md)
-   [<span data-ttu-id="2ea49-133">**\_ \_ en-tête d’enregistrement d’attribut**</span><span class="sxs-lookup"><span data-stu-id="2ea49-133">**ATTRIBUTE\_RECORD\_HEADER**</span></span>](attribute-record-header.md)
-   [<span data-ttu-id="2ea49-134">**nom du fichier \_**</span><span class="sxs-lookup"><span data-stu-id="2ea49-134">**FILE\_NAME**</span></span>](file-name.md)
-   [<span data-ttu-id="2ea49-135">**\_ \_ en-tête de segment d’enregistrement de fichier \_**</span><span class="sxs-lookup"><span data-stu-id="2ea49-135">**FILE\_RECORD\_SEGMENT\_HEADER**</span></span>](file-record-segment-header.md)
-   [<span data-ttu-id="2ea49-136">**\_Référence du segment MFT \_**</span><span class="sxs-lookup"><span data-stu-id="2ea49-136">**MFT\_SEGMENT\_REFERENCE**</span></span>](mft-segment-reference.md)
-   [<span data-ttu-id="2ea49-137">**\_ \_ en-tête multisecteur**</span><span class="sxs-lookup"><span data-stu-id="2ea49-137">**MULTI\_SECTOR\_HEADER**</span></span>](multi-sector-header.md)
-   [<span data-ttu-id="2ea49-138">**\_informations standard**</span><span class="sxs-lookup"><span data-stu-id="2ea49-138">**STANDARD\_INFORMATION**</span></span>](standard-information.md)

## <a name="related-topics"></a><span data-ttu-id="2ea49-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ea49-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2ea49-140">[Référence technique NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2ea49-140">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

 
