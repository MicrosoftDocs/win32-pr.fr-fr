---
title: Formats de disque
description: 'IMAPi prend en charge trois formats de système de fichiers : ISO 9660, Joliet et UDF.'
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310085"
---
# <a name="disc-formats"></a><span data-ttu-id="71ac3-103">Formats de disque</span><span class="sxs-lookup"><span data-stu-id="71ac3-103">Disc Formats</span></span>

<span data-ttu-id="71ac3-104">IMAPi prend en charge trois formats de système de fichiers : [ISO 9660](#iso-9660), [Joliet](#joliet)et [UDF](#universal-disk-format-udf).</span><span class="sxs-lookup"><span data-stu-id="71ac3-104">IMAPI supports three file system formats: [ISO 9660](#iso-9660), [Joliet](#joliet), and [UDF](#universal-disk-format-udf).</span></span>

## <a name="iso-9660"></a><span data-ttu-id="71ac3-105">ISO 9660</span><span class="sxs-lookup"><span data-stu-id="71ac3-105">ISO 9660</span></span>

<span data-ttu-id="71ac3-106">Le format ISO 9660 est le système de fichiers standard d’origine pour les disques de données de CD.</span><span class="sxs-lookup"><span data-stu-id="71ac3-106">The ISO 9660 format is the original standard file system for CD data discs.</span></span> <span data-ttu-id="71ac3-107">Le format est reconnu sur plusieurs systèmes d’exploitation, notamment MSDOS, le Mac OS, UNIX et le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="71ac3-107">The format is recognized on several operating systems, including MSDOS, the Mac OS, UNIX, and the Windows operating system.</span></span> <span data-ttu-id="71ac3-108">Le format ISO 9660 est publié par le Organisation internationale de normalisation (ISO).</span><span class="sxs-lookup"><span data-stu-id="71ac3-108">The ISO 9660 format is published by the International Organization for Standardization (ISO).</span></span>

<span data-ttu-id="71ac3-109">Le format commence au secteur 16 avec l’en-tête volume, CD0001 ; le reste de l’en-tête suit.</span><span class="sxs-lookup"><span data-stu-id="71ac3-109">The format begins at sector 16 with the volume header, CD0001; the remainder of the header follows.</span></span> <span data-ttu-id="71ac3-110">D’autres formats dérivés commencent également au secteur 16, mais utilisent une autre chaîne pour l’en-tête du volume.</span><span class="sxs-lookup"><span data-stu-id="71ac3-110">Other derived formats also begin at sector 16, but use another string for the volume header.</span></span> <span data-ttu-id="71ac3-111">Par exemple, les disques High Sierra utilisent la chaîne CD-ROM0001 et le format interactif du CD Compact utilise CD-I0001.</span><span class="sxs-lookup"><span data-stu-id="71ac3-111">For example, High Sierra discs use the string CD-ROM0001 and Compact Disc Interactive format uses CD-I0001.</span></span>

<span data-ttu-id="71ac3-112">L’en-tête pointe vers les zones du disque qui stockent les noms de fichiers au format ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="71ac3-112">The header points to areas of the disc that store the file names in ISO 9660 format.</span></span> <span data-ttu-id="71ac3-113">La Convention d’affectation de noms de fichiers et de répertoires se compose de 8 caractères, un point et 3 caractères supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="71ac3-113">The file and directory naming convention consists of 8 characters, a period, and 3 more characters.</span></span> <span data-ttu-id="71ac3-114">Il s’agit de la même convention d’affectation de noms que celle utilisée par le système d’exploitation MSDOS.</span><span class="sxs-lookup"><span data-stu-id="71ac3-114">This is the same naming convention used by the MSDOS operating system.</span></span>

<span data-ttu-id="71ac3-115">Des en-têtes de système de fichiers supplémentaires, pour les formats tels que Joliet et UDF, peuvent coexister sur un disque sans affecter la lisibilité du format ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="71ac3-115">Additional file system headers, for formats such as Joliet and UDF, can co-exist on a disc without affecting the readability of the ISO 9660 format.</span></span> <span data-ttu-id="71ac3-116">Après les index, un ensemble de fichiers de données occupe le disque. Les index de chaque système de fichiers référencent indépendamment les fichiers de données sur le disque.</span><span class="sxs-lookup"><span data-stu-id="71ac3-116">After the indexes, a set of data files occupy the disc. The indexes for each file system independently reference data files on the disc.</span></span>

<span data-ttu-id="71ac3-117">La spécification ISO 9660 définit trois niveaux de format :</span><span class="sxs-lookup"><span data-stu-id="71ac3-117">The ISO 9660 specification defines three levels of the format:</span></span>

-   <span data-ttu-id="71ac3-118">Le niveau 1 définit des noms de fichiers pour utiliser le format de caractère 8,3.</span><span class="sxs-lookup"><span data-stu-id="71ac3-118">Level 1 defines file names to use the 8.3 character format.</span></span>
-   <span data-ttu-id="71ac3-119">Le niveau 2 autorise des noms de fichiers plus longs, tels qu’ils figurent sur les plateformes DOS 6. xx, MacIntosh et UNIX.</span><span class="sxs-lookup"><span data-stu-id="71ac3-119">Level 2 permits longer file names, as found on DOS 6.xx, MacIntosh, and UNIX platforms.</span></span>
-   <span data-ttu-id="71ac3-120">Le niveau 3 permet d’améliorer les performances de récupération (lecture) des données et des fichiers audio entrelacés.</span><span class="sxs-lookup"><span data-stu-id="71ac3-120">Level 3 allows interleaved data and audio files to improve retrieval (playback) performance.</span></span> <span data-ttu-id="71ac3-121">Ce niveau supprime également la limite de 2 Go de fichiers.</span><span class="sxs-lookup"><span data-stu-id="71ac3-121">This level also removes the 2GB file limit.</span></span> <span data-ttu-id="71ac3-122">Ce niveau n’est **pas** pris en charge par l’API de mastérisation d’image.</span><span class="sxs-lookup"><span data-stu-id="71ac3-122">This level is **not** supported by the Image Mastering API.</span></span>

<span data-ttu-id="71ac3-123">Les disques DVD peuvent également utiliser ISO 9660 ; Toutefois, le système de fichiers UDF est le système de fichiers le plus répandu utilisé avec les supports DVD.</span><span class="sxs-lookup"><span data-stu-id="71ac3-123">DVD discs can also use ISO 9660; however, the UDF file system is the most prevalent file system used with DVD media.</span></span>

## <a name="joliet"></a><span data-ttu-id="71ac3-124">Joliet</span><span class="sxs-lookup"><span data-stu-id="71ac3-124">Joliet</span></span>

<span data-ttu-id="71ac3-125">Le format Joliet est une dérivée de la norme ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="71ac3-125">The Joliet format is a derivative of ISO 9660.</span></span> <span data-ttu-id="71ac3-126">Ce format écrit l’index du système de fichiers Joliet sur l’image disque en plus de l’index du système de fichiers ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="71ac3-126">This format writes the Joliet file system index to the disc image in addition to the ISO 9660 file system index.</span></span>

<span data-ttu-id="71ac3-127">L’index Joliet offre les améliorations suivantes à l’index du système de fichiers :</span><span class="sxs-lookup"><span data-stu-id="71ac3-127">The Joliet index provides the following improvements to the file system index:</span></span>

-   <span data-ttu-id="71ac3-128">Reconnaît les noms de fichiers longs jusqu’à 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="71ac3-128">Recognizes long file names up to 32 characters.</span></span>
-   <span data-ttu-id="71ac3-129">Distingue les lettres majuscules et minuscules dans les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="71ac3-129">Distinguishes between upper and lower case letters in the file names.</span></span>
-   <span data-ttu-id="71ac3-130">Prend en charge les caractères Unicode dans le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="71ac3-130">Supports Unicode characters in the filename.</span></span>

<span data-ttu-id="71ac3-131">L’en-tête de format Joliet commence au secteur 17 du disque.</span><span class="sxs-lookup"><span data-stu-id="71ac3-131">The Joliet format header begins at sector 17 of the disc.</span></span>

<span data-ttu-id="71ac3-132">Étant donné que le format Joliet conserve le système de fichiers ISO 9660 sur un disque, la compatibilité avec les appareils conformes ISO 9660 est conservée.</span><span class="sxs-lookup"><span data-stu-id="71ac3-132">Because the Joliet format preserves the ISO 9660 file system on a disc, compatibility with ISO 9660-compliant devices is retained.</span></span>

## <a name="universal-disk-format-udf"></a><span data-ttu-id="71ac3-133">Format UDF (Universal Disk Format)</span><span class="sxs-lookup"><span data-stu-id="71ac3-133">Universal Disk Format (UDF)</span></span>

<span data-ttu-id="71ac3-134">Le format UDF (Universal Disk Format) est un système de fichiers plus récent développé pour le support optique par l’Association de technologie de stockage optique (OSTA).</span><span class="sxs-lookup"><span data-stu-id="71ac3-134">The Universal Disk Format (UDF) is a newer file system developed for optical media by the Optical Storage Technology Association (OSTA).</span></span> <span data-ttu-id="71ac3-135">UDF est un format portable reconnu par plusieurs systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="71ac3-135">UDF is a portable format that is recognized by several operating systems.</span></span> <span data-ttu-id="71ac3-136">UDF remplace ISO 9660 comme nouveau standard, en particulier avec les supports de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="71ac3-136">UDF is replacing ISO 9660 as the new standard, especially with read/write media.</span></span>

<span data-ttu-id="71ac3-137">Les fonctionnalités UDF sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="71ac3-137">Features of UDF include the following:</span></span>

-   <span data-ttu-id="71ac3-138">Prend en charge une taille maximale de 2 to.</span><span class="sxs-lookup"><span data-stu-id="71ac3-138">Supports media up to 2TB in size.</span></span>
-   <span data-ttu-id="71ac3-139">Prend en charge les disques Flash Media, Iomega REV et CD-MRW.</span><span class="sxs-lookup"><span data-stu-id="71ac3-139">Supports flash media, Iomega REV discs, and CD-MRW discs.</span></span>
-   <span data-ttu-id="71ac3-140">Stocke des fichiers d’une longueur inférieure à 2 Ko dans le bloc d’entrée de fichier.</span><span class="sxs-lookup"><span data-stu-id="71ac3-140">Stores files less than 2 KB in length in the File Entry block.</span></span>
-   <span data-ttu-id="71ac3-141">Prend en charge des fichiers d’une longueur maximale de 2 to avec des noms de fichiers tant que 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="71ac3-141">Supports files up to 2TB with filenames as long as 255 characters.</span></span>
-   <span data-ttu-id="71ac3-142">Prend en charge un ensemble complet d’attributs de fichier adaptés à différents systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="71ac3-142">Supports a rich set of file attributes that suit various operating systems.</span></span>
-   <span data-ttu-id="71ac3-143">Prend en charge un format de pont où les formats ISO 9660, Joliet et UDF résident tous sur le même disque. Cela est utilisé dans les applications vidéo, telles que DVD-Video, DVD + VR et DVD-VR.</span><span class="sxs-lookup"><span data-stu-id="71ac3-143">Supports a bridge format where ISO 9660, Joliet, and UDF formats all reside on the same disc. This is used in video applications, such as DVD-Video, DVD+VR, and DVD-VR.</span></span>
-   <span data-ttu-id="71ac3-144">Prend en charge les flux nommés et les fichiers « en temps réel ».</span><span class="sxs-lookup"><span data-stu-id="71ac3-144">Supports named streams and 'Real-Time' files.</span></span>

 

 




