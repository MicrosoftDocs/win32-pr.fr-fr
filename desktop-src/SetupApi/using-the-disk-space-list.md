---
description: Avant de pouvoir ajouter ou supprimer des opérations de fichier à partir de la liste d’espace disque, vous devez la créer à l’aide de la fonction SetupCreateDiskSpaceList.
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: Utilisation de la liste Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a19f100fd5190472f5f6bfebaf74affe1a789cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533842"
---
# <a name="using-the-disk-space-list"></a><span data-ttu-id="02995-103">Utilisation de la liste Disk-Space</span><span class="sxs-lookup"><span data-stu-id="02995-103">Using the Disk-Space List</span></span>

<span data-ttu-id="02995-104">Avant de pouvoir ajouter ou supprimer des opérations de fichier à partir de la liste d’espace disque, vous devez la créer à l’aide de la fonction [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="02995-104">Before you can add or remove file operations from the disk-space list, you must create it by using the [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) function.</span></span>

<span data-ttu-id="02995-105">Après avoir créé une liste d’espace disque, vous pouvez ajouter des opérations de copie ou de suppression de fichiers individuelles à la liste à l’aide de [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span><span class="sxs-lookup"><span data-stu-id="02995-105">After you create a disk-space list you can add individual file copy or delete operations to the list by using [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span></span> <span data-ttu-id="02995-106">Pour ajouter toutes les opérations de copie ou de suppression de fichiers dans une section INF entière, utilisez la fonction [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) ou [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="02995-106">To add all the file copy or delete operations in an entire INF section, use either the [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) or [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) function.</span></span>

<span data-ttu-id="02995-107">Une fois que vous avez ajouté toutes les opérations d’installation à la liste d’espace disque, vous pouvez l’interroger pour déterminer la quantité d’espace disque nécessaire pour l’installation spécifiée à l’aide de la fonction [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) .</span><span class="sxs-lookup"><span data-stu-id="02995-107">After you add all the installation operations to the disk-space list, you can query it to find out how much disk space is required for the specified installation by using the [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) function.</span></span>

<span data-ttu-id="02995-108">La fonction [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) retourne les spécifications de lecteur pour chaque lecteur cible référencé dans les opérations de fichier sur la liste d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="02995-108">The [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) function returns the drive specifications for each target drive referenced in the file operations on the disk-space list.</span></span> <span data-ttu-id="02995-109">Vous pouvez utiliser ces informations pour comparer par programmation l’espace disponible sur ces lecteurs avec l’espace requis par l’installation.</span><span class="sxs-lookup"><span data-stu-id="02995-109">You can use this information to programmatically compare the available space on these drives with the space required by the installation.</span></span>

<span data-ttu-id="02995-110">Pour supprimer une opération de fichier de la liste d’espace disque, utilisez la fonction [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="02995-110">To remove a file operation from the disk-space list, use the [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) function.</span></span> <span data-ttu-id="02995-111">Pour supprimer toutes les opérations de copie ou de suppression de fichiers à partir d’une section INF entière, utilisez la fonction [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) ou [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="02995-111">To remove all file copy or delete operations from an entire INF section, use the [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) or [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) function.</span></span>

<span data-ttu-id="02995-112">Une fois que la liste d’espace disque n’est plus nécessaire, vous pouvez libérer les ressources qui lui sont allouées en appelant la fonction [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) .</span><span class="sxs-lookup"><span data-stu-id="02995-112">After the disk-space list is no longer required, you can release the resources allocated to it by calling the [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) function.</span></span>

 

 



