---
description: Fonctions utilisées dans la gestion des disques.
ms.assetid: 301d3062-29a1-4b44-bbcd-e9d5b7d7823b
title: Fonctions de gestion des disques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677443c58aa8b9a60758d817e31e3804ef25ae66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529379"
---
# <a name="disk-management-functions"></a><span data-ttu-id="776bf-103">Fonctions de gestion des disques</span><span class="sxs-lookup"><span data-stu-id="776bf-103">Disk Management Functions</span></span>

<span data-ttu-id="776bf-104">Les fonctions suivantes sont utilisées dans gestion des disques.</span><span class="sxs-lookup"><span data-stu-id="776bf-104">The following functions are used in disk management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="776bf-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="776bf-105">In this section</span></span>



| <span data-ttu-id="776bf-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="776bf-106">Function</span></span>                                                    | <span data-ttu-id="776bf-107">Description</span><span class="sxs-lookup"><span data-stu-id="776bf-107">Description</span></span>                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="776bf-108">**GetDiskFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="776bf-108">**GetDiskFreeSpace**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)<br/>     | <span data-ttu-id="776bf-109">Récupère des informations sur le disque spécifié, y compris la quantité d’espace libre sur le disque.</span><span class="sxs-lookup"><span data-stu-id="776bf-109">Retrieves information about the specified disk, including the amount of free space on the disk.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="776bf-110">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="776bf-110">**GetDiskFreeSpaceEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)<br/> | <span data-ttu-id="776bf-111">Récupère des informations sur la quantité d’espace disponible sur un volume de disque, qui correspond à la quantité totale d’espace, à la quantité totale d’espace libre et à la quantité totale d’espace libre disponible pour l’utilisateur associé au thread appelant.</span><span class="sxs-lookup"><span data-stu-id="776bf-111">Retrieves information about the amount of space that is available on a disk volume, which is the total amount of space, the total amount of free space, and the total amount of free space available to the user that is associated with the calling thread.</span></span><br/> |



 

<span data-ttu-id="776bf-112">Autres fonctions utilisées dans la gestion des disques.</span><span class="sxs-lookup"><span data-stu-id="776bf-112">Other functions used in disk management.</span></span>



| <span data-ttu-id="776bf-113">Fonction</span><span class="sxs-lookup"><span data-stu-id="776bf-113">Function</span></span>                         | <span data-ttu-id="776bf-114">Description</span><span class="sxs-lookup"><span data-stu-id="776bf-114">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="776bf-115">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="776bf-115">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) | <span data-ttu-id="776bf-116">Crée ou ouvre un fichier ou un périphérique d’e/s.</span><span class="sxs-lookup"><span data-stu-id="776bf-116">Creates or opens a file or I/O device.</span></span> <span data-ttu-id="776bf-117">Les périphériques d’e/s les plus couramment utilisés sont les suivants : fichier, flux de fichier, répertoire, disque physique, volume, mémoire tampon de la console, lecteur de bande, ressource de communication, mailslot et canal.</span><span class="sxs-lookup"><span data-stu-id="776bf-117">The most commonly used I/O devices are as follows: file, file stream, directory, physical disk, volume, console buffer, tape drive, communications resource, mailslot, and pipe.</span></span><br/> |
| [<span data-ttu-id="776bf-118">**DeleteFile**</span><span class="sxs-lookup"><span data-stu-id="776bf-118">**DeleteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) | <span data-ttu-id="776bf-119">Supprime un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="776bf-119">Deletes an existing file.</span></span><br/>                                                                                                                                                                                               |



 

 

 




