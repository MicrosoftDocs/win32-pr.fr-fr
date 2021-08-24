---
title: Fonctions de sauvegarde
description: Les fonctions suivantes sont utilisées avec la sauvegarde sur bande.
ms.assetid: 8c5f92f7-4918-475c-bc86-2b02291488d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2164958d7261c4c22caf1ac5124f524eca2f7ed355b082bede59d66a2e6fe697
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529609"
---
# <a name="backup-functions"></a>Fonctions de sauvegarde

Les fonctions suivantes sont utilisées avec la [sauvegarde sur bande](tape-backup.md).



| Fonction                                           | Description                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread)                   | Lit les données associées à un fichier ou un répertoire spécifié dans une mémoire tampon.                                |
| [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek)                   | Recherche vers l’avant dans un flux de données.                                                                        |
| [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)                 | Écrit un flux de données à partir d’une mémoire tampon dans un fichier ou un répertoire spécifié.                                |
| [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) | Reformate une bande.                                                                                      |
| [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape)                     | Efface tout ou partie d’une bande.                                                                          |
| [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)     | Récupère des informations qui décrivent la bande ou le lecteur de bande.                                       |
| [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition)         | Récupère l’adresse actuelle de la bande.                                                             |
| [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)             | Détermine si le périphérique à bandes est prêt à traiter les commandes de bande.                                  |
| [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape)                 | Prépare l’accès à la bande ou sa suppression.                                                           |
| [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)     | Spécifie la taille de bloc d’une bande ou configure le périphérique à bandes.                                      |
| [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition)         | Définit la position de la bande sur l’appareil spécifié.                                                        |
| [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark)             | Écrit un nombre spécifié de marques, de setmarks, de marques de sauvegarde courtes ou de longs marques sur un périphérique à bandes. |



 

Les fonctions suivantes sont fournies pour l’utilisation du [stockage d’instance unique et de la sauvegarde SIS](single-instance-store-and-sis-backup.md).



| Fonction                                                          | Description                                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**SisCreateBackupStructure**](siscreatebackupstructure.md)      | Crée la structure de sauvegarde SIS spécifiée en fonction des informations fournies.                      |
| [**SisCreateRestoreStructure**](siscreaterestorestructure.md)    | Crée la structure de restauration SIS spécifiée en fonction des informations fournies.                     |
| [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)    | Retourne des informations décrivant les fichiers du magasin commun vers lesquels pointe le lien SIS spécifié.            |
| [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)          | Libère la mémoire allouée par les fonctions d’API SIS.                                                       |
| [**SisFreeBackupStructure**](sisfreebackupstructure.md)          | Libère la structure de sauvegarde SIS spécifiée.                                                          |
| [**SisFreeRestoreStructure**](sisfreerestorestructure.md)        | Libère la structure de restauration SIS spécifiée.                                                         |
| [**SisRestoredCommon StoreFile**](sisrestoredcommonstorefile.md) | Signale à l’architecture SIS qu’un fichier de magasin commun a été écrit.                         |
| [**SisRestoredLink**](sisrestoredlink.md)                        | Retourne les noms du ou des fichiers du magasin commun vers lesquels pointe le lien SIS restauré spécifié. |



 

Les fonctions suivantes sont fournies pour l’utilisation de la [sauvegarde et de la restauration de fichiers chiffrés](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).



| Fonction                                                | Description                                                                                |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CloseEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw) | Fermez un fichier chiffré ouvert avec [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa). |
| [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)   | Ouvrir un fichier chiffré avec accès aux données au format chiffré.                            |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw)   | Lit un fichier chiffré en laissant ses données dans un format chiffré.                               |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw) | Écrire un fichier chiffré qui laisse ses données dans un format chiffré.                              |



 

 

 