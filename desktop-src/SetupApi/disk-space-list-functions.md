---
description: Les fonctions suivantes sont utilisées avec la liste d’espace disque.
ms.assetid: 18693b2d-6b0f-4f9c-b3cf-e50c36e2f2e1
title: Disk-Space les fonctions de liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f520cc7a3ddcd0b12b27bd11768a95231a8ed4b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319582"
---
# <a name="disk-space-list-functions"></a>Disk-Space les fonctions de liste

Les fonctions suivantes sont utilisées avec la liste d’espace disque.



| Fonction                                                                                         | Description                                                                                                                          |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupAdjustDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)                                     | Ajuste la quantité d’espace nécessaire pour un lecteur spécifié.                                                                          |
| [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)                                     | Crée une liste d’espace disque et lui alloue des ressources.                                                                             |
| [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)                                   | Détruit une liste d’espace disque, en libérant les ressources qui lui sont allouées.                                                                   |
| [**SetupDuplicateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)                               | Duplique une liste d’espace disque en tant que nouvelle liste indépendante d’espace disque.                                                                   |
| [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)                       | Remplit une mémoire tampon avec les spécifications de lecteur pour tous les lecteurs répertoriés dans la liste espace disque.                                       |
| [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)                         | Retourne la quantité totale d’espace disque nécessaire pour effectuer les opérations de fichier sur un lecteur particulier répertorié dans la liste espace disque. |
| [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)                                       | Ajoute une opération de copie ou de suppression de fichier à la liste d’espace disque.                                                                         |
| [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)                         | Ajoute toutes les opérations de fichiers dans une section **copier** les fichiers ou **supprimer des fichiers** d’un fichier INF à une liste d’espace disque.                    |
| [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)           | Ajoute toutes les opérations de fichiers dans une section d' **installation** d’un fichier INF à la liste d’espace disque.                                        |
| [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)                             | Supprime une opération de copie ou de suppression de fichier d’une liste d’espace disque.                                                                      |
| [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)               | Supprime toutes les opérations de fichiers dans une section **copier** les fichiers ou **supprimer des fichiers** d’un fichier INF à partir d’une liste d’espace disque.               |
| [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) | Supprime toutes les opérations de fichier dans la section d' **installation** d’un fichier INF à partir de la liste d’espace disque.                                  |



 

 

 



