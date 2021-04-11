---
description: Gérer les répertoires avec la table d’entrée de répertoire, les handles de répertoire, les points d’analyse.
title: Systèmes de fichiers locaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755157"
---
# <a name="local-file-systems"></a><span data-ttu-id="b7c09-103">Systèmes de fichiers locaux</span><span class="sxs-lookup"><span data-stu-id="b7c09-103">Local File Systems</span></span>

<span data-ttu-id="b7c09-104">Un *système de fichiers* permet aux applications de stocker et de récupérer des fichiers sur les périphériques de stockage.</span><span class="sxs-lookup"><span data-stu-id="b7c09-104">A *file system* enables applications to store and retrieve files on storage devices.</span></span> <span data-ttu-id="b7c09-105">Les fichiers sont placés dans une structure hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="b7c09-105">Files are placed in a hierarchical structure.</span></span> <span data-ttu-id="b7c09-106">Le système de fichiers spécifie les conventions d’affectation de noms des fichiers et le format de spécification du chemin d’accès à un fichier dans l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="b7c09-106">The file system specifies naming conventions for files and the format for specifying the path to a file in the tree structure.</span></span>

<span data-ttu-id="b7c09-107">Chaque système de fichiers se compose d’un ou de plusieurs pilotes et bibliothèques de liens dynamiques qui définissent les formats de données et les fonctionnalités du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b7c09-107">Each file system consists of one or more drivers and dynamic-link libraries that define the data formats and features of the file system.</span></span> <span data-ttu-id="b7c09-108">Les systèmes de fichiers peuvent exister sur différents types de périphériques de stockage, y compris les disques durs, les juke-boxes, les disques optiques amovibles, les unités de sauvegarde sur bande et les cartes mémoire.</span><span class="sxs-lookup"><span data-stu-id="b7c09-108">File systems can exist on many different types of storage devices, including hard disks, jukeboxes, removable optical disks, tape back-up units, and memory cards.</span></span>

<span data-ttu-id="b7c09-109">Tous les systèmes de fichiers pris en charge par Windows disposent des composants de stockage suivants :</span><span class="sxs-lookup"><span data-stu-id="b7c09-109">All file systems supported by Windows have the following storage components:</span></span>

-   <span data-ttu-id="b7c09-110">Volumes.</span><span class="sxs-lookup"><span data-stu-id="b7c09-110">Volumes.</span></span> <span data-ttu-id="b7c09-111">Un *volume* est un ensemble de répertoires et de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b7c09-111">A *volume* is a collection of directories and files.</span></span>
-   <span data-ttu-id="b7c09-112">Répertoires.</span><span class="sxs-lookup"><span data-stu-id="b7c09-112">Directories.</span></span> <span data-ttu-id="b7c09-113">Un *répertoire* est une collection hiérarchique de répertoires et de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b7c09-113">A *directory* is a hierarchical collection of directories and files.</span></span>
-   <span data-ttu-id="b7c09-114">Fichiers.</span><span class="sxs-lookup"><span data-stu-id="b7c09-114">Files.</span></span> <span data-ttu-id="b7c09-115">Un *fichier* est un regroupement logique de données associées.</span><span class="sxs-lookup"><span data-stu-id="b7c09-115">A *file* is a logical grouping of related data.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b7c09-116">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b7c09-116">In this section</span></span>



| <span data-ttu-id="b7c09-117">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b7c09-117">Topic</span></span>                                                                | <span data-ttu-id="b7c09-118">Description</span><span class="sxs-lookup"><span data-stu-id="b7c09-118">Description</span></span>                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7c09-119">Gestion de répertoires</span><span class="sxs-lookup"><span data-stu-id="b7c09-119">Directory Management</span></span>](directory-management.md)<br/>          | <span data-ttu-id="b7c09-120">Un *répertoire* est une collection hiérarchique de répertoires et de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b7c09-120">A *directory* is a hierarchical collection of directories and files.</span></span> <span data-ttu-id="b7c09-121">La seule contrainte sur le nombre de fichiers pouvant être contenus dans un répertoire unique est la taille physique du disque sur lequel se trouve le répertoire.</span><span class="sxs-lookup"><span data-stu-id="b7c09-121">The only constraint on the number of files that can be contained in a single directory is the physical size of the disk on which the directory is located.</span></span><br/> |
| [<span data-ttu-id="b7c09-122">Gestion des disques</span><span class="sxs-lookup"><span data-stu-id="b7c09-122">Disk Management</span></span>](disk-management.md)<br/>                    | <span data-ttu-id="b7c09-123">Un *disque dur* est un disque rigide à l’intérieur d’un ordinateur qui stocke et fournit un accès relativement rapide à de grandes quantités de données.</span><span class="sxs-lookup"><span data-stu-id="b7c09-123">A *hard disk* is a rigid disk inside a computer that stores and provides relatively quick access to large amounts of data.</span></span> <span data-ttu-id="b7c09-124">C’est le type de stockage le plus souvent utilisé avec Windows.</span><span class="sxs-lookup"><span data-stu-id="b7c09-124">It is the type of storage most often used with Windows.</span></span> <span data-ttu-id="b7c09-125">Le système prend également en charge les supports amovibles.</span><span class="sxs-lookup"><span data-stu-id="b7c09-125">The system also supports removable media.</span></span><br/>    |
| [<span data-ttu-id="b7c09-126">Gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="b7c09-126">File Management</span></span>](file-management.md)<br/>                    | <span data-ttu-id="b7c09-127">Un *objet fichier* fournit une représentation d’une ressource (un appareil physique ou une ressource située sur un appareil physique) qui peut être gérée par le système d’e/s.</span><span class="sxs-lookup"><span data-stu-id="b7c09-127">A *file object* provides a representation of a resource (either a physical device or a resource located on a physical device) that can be managed by the I/O system.</span></span><br/>                                                            |
| [<span data-ttu-id="b7c09-128">NTFS transactionnel (TxF)</span><span class="sxs-lookup"><span data-stu-id="b7c09-128">Transactional NTFS (TxF)</span></span>](transactional-ntfs-portal.md)<br/> | <span data-ttu-id="b7c09-129">Le NTFS transactionnel (TxF) autorise l’exécution d’opérations de fichiers sur un volume de système de fichiers NTFS dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="b7c09-129">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="b7c09-130">Gestion des volumes</span><span class="sxs-lookup"><span data-stu-id="b7c09-130">Volume Management</span></span>](volume-management.md)<br/>                | <span data-ttu-id="b7c09-131">Le niveau le plus élevé de l’organisation dans le système de fichiers est le *volume*.</span><span class="sxs-lookup"><span data-stu-id="b7c09-131">The highest level of organization in the file system is the *volume*.</span></span> <span data-ttu-id="b7c09-132">Un système de fichiers réside sur un volume.</span><span class="sxs-lookup"><span data-stu-id="b7c09-132">A file system resides on a volume.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="b7c09-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7c09-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b7c09-134">[Informations techniques de référence sur FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b7c09-134">[FAT Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="b7c09-135">[Technologies de systèmes de fichiers](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b7c09-135">[File Systems Technologies](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="b7c09-136">[Référence technique NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b7c09-136">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

