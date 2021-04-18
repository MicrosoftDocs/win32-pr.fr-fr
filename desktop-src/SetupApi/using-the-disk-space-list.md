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
# <a name="using-the-disk-space-list"></a>Utilisation de la liste Disk-Space

Avant de pouvoir ajouter ou supprimer des opérations de fichier à partir de la liste d’espace disque, vous devez la créer à l’aide de la fonction [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) .

Après avoir créé une liste d’espace disque, vous pouvez ajouter des opérations de copie ou de suppression de fichiers individuelles à la liste à l’aide de [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista). Pour ajouter toutes les opérations de copie ou de suppression de fichiers dans une section INF entière, utilisez la fonction [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) ou [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) .

Une fois que vous avez ajouté toutes les opérations d’installation à la liste d’espace disque, vous pouvez l’interroger pour déterminer la quantité d’espace disque nécessaire pour l’installation spécifiée à l’aide de la fonction [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) .

La fonction [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) retourne les spécifications de lecteur pour chaque lecteur cible référencé dans les opérations de fichier sur la liste d’espace disque. Vous pouvez utiliser ces informations pour comparer par programmation l’espace disponible sur ces lecteurs avec l’espace requis par l’installation.

Pour supprimer une opération de fichier de la liste d’espace disque, utilisez la fonction [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) . Pour supprimer toutes les opérations de copie ou de suppression de fichiers à partir d’une section INF entière, utilisez la fonction [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) ou [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) .

Une fois que la liste d’espace disque n’est plus nécessaire, vous pouvez libérer les ressources qui lui sont allouées en appelant la fonction [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) .

 

 



