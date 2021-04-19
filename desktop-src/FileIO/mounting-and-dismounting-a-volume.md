---
description: La création d’un dossier monté est un processus en deux étapes.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Création de dossiers montés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540906"
---
# <a name="creating-mounted-folders"></a><span data-ttu-id="5c9fb-103">Création de dossiers montés</span><span class="sxs-lookup"><span data-stu-id="5c9fb-103">Creating Mounted Folders</span></span>

<span data-ttu-id="5c9fb-104">La création d’un dossier monté est un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-104">Creating a mounted folder is a two-step process.</span></span> <span data-ttu-id="5c9fb-105">Tout d’abord, appelez [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) avec le point de montage (lettre de lecteur, chemin d’accès du GUID du volume ou dossier monté) du volume à affecter au dossier monté.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-105">First, call [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) with the mount point (drive letter, volume GUID path, or mounted folder) of the volume to be assigned to the mounted folder.</span></span> <span data-ttu-id="5c9fb-106">Utilisez ensuite la fonction [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) pour associer le chemin d’accès du GUID du volume retourné au répertoire souhaité sur un autre volume.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-106">Then use the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function to associate the returned volume GUID path with the desired directory on another volume.</span></span> <span data-ttu-id="5c9fb-107">Pour obtenir un exemple de code, consultez [création d’un dossier monté](mounting-a-volume-at-a-mount-point.md).</span><span class="sxs-lookup"><span data-stu-id="5c9fb-107">For example code, see [Creating a Mounted Folder](mounting-a-volume-at-a-mount-point.md).</span></span>

<span data-ttu-id="5c9fb-108">Votre application peut désigner n’importe quel répertoire vide sur un volume autre que la racine comme dossier monté.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-108">Your application can designate any empty directory on a volume other than the root as a mounted folder.</span></span> <span data-ttu-id="5c9fb-109">Lorsque vous appelez la fonction [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , ce répertoire devient le dossier monté.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-109">When you call the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, that directory becomes the mounted folder.</span></span> <span data-ttu-id="5c9fb-110">Vous pouvez attribuer le même volume à plusieurs dossiers montés.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-110">You can assign the same volume to multiple mounted folders.</span></span>

<span data-ttu-id="5c9fb-111">Une fois le dossier monté établi, il est géré automatiquement par le redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-111">After the mounted folder has been established, it is maintained through computer restarts automatically.</span></span>

<span data-ttu-id="5c9fb-112">En cas de défaillance d’un volume, tous les volumes qui ont été affectés aux dossiers montés sur ce volume ne sont plus accessibles via ces dossiers montés.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-112">If a volume fails, any volumes that have been assigned to mounted folders on that volume can no longer be accessed through those mounted folders.</span></span> <span data-ttu-id="5c9fb-113">Supposons, par exemple, que vous ayez deux volumes, C : et D :, et que D : soit associé au dossier monté C : monté \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="5c9fb-113">For example, suppose you have two volumes, C: and D:, and that D: is associated with the mounted folder C:\\MountD\\.</span></span> <span data-ttu-id="5c9fb-114">Si le volume C : échoue, le volume D : n’est plus accessible via le chemin d’accès C : \\ monté \\ .</span><span class="sxs-lookup"><span data-stu-id="5c9fb-114">If volume C: fails, volume D: can no longer be accessed through the path C:\\MountD\\.</span></span>

<span data-ttu-id="5c9fb-115">Seuls les volumes de système de fichiers NTFS peuvent avoir des dossiers montés, mais les volumes cibles pour les dossiers montés peuvent être des volumes non NTFS.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-115">Only NTFS file system volumes can have mounted folders, but the target volumes for the mounted folders can be non-NTFS volumes.</span></span>

<span data-ttu-id="5c9fb-116">Les dossiers montés sont implémentés à l’aide de points d’analyse et sont soumis à leurs restrictions.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-116">Mounted folders are implemented by using reparse points and are subject to their restrictions.</span></span> <span data-ttu-id="5c9fb-117">Pour plus d’informations, consultez [points d’analyse](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="5c9fb-117">For more information, see [Reparse Points](reparse-points.md).</span></span> <span data-ttu-id="5c9fb-118">Il n’est pas nécessaire de manipuler des points d’analyse pour utiliser des dossiers montés. les fonctions telles que [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) gèrent tous les détails du point d’analyse pour vous.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-118">It is not necessary to manipulate reparse points to use mounted folders; functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) handle all the reparse point details for you.</span></span>

<span data-ttu-id="5c9fb-119">Étant donné que les dossiers montés sont des répertoires, vous pouvez les renommer, les supprimer, les déplacer et les manipuler, comme vous le feriez pour d’autres annuaires.</span><span class="sxs-lookup"><span data-stu-id="5c9fb-119">Because mounted folders are directories, you can rename, remove, move, and otherwise manipulate them, as you would other directories.</span></span>

<span data-ttu-id="5c9fb-120">(Remarque : la documentation TechNet utilise le terme *lecteurs montés* pour faire référence aux *dossiers montés*.)</span><span class="sxs-lookup"><span data-stu-id="5c9fb-120">(Note: The TechNet documentation uses the term *mounted drives* to refer to *mounted folders*.)</span></span>

 

 



