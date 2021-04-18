---
description: Chaque fois qu’un processus crée ou ouvre un objet d’annuaire, il reçoit un descripteur de l’objet.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Handles de répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526974"
---
# <a name="directory-handles"></a>Handles de répertoire

Chaque fois qu’un processus crée ou ouvre un objet d’annuaire, il reçoit un descripteur de l’objet.

Pour obtenir un descripteur d’un répertoire existant, appelez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec l’indicateur de **fichier \_ indicateurs de \_ \_ sémantique de sauvegarde** .

Vous pouvez transmettre un handle de répertoire aux fonctions suivantes.



| Fonction                                                         | Description                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)                              | Sauvegardez un fichier ou un répertoire, y compris les informations de sécurité.<br/>                                                                                      |
| [**BackupSeek**](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | Effectue une recherche vers l’avant dans un flux de données accédé initialement à l’aide de la fonction [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) ou [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) .<br/> |
| [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | Restaurez un fichier ou un répertoire qui a été sauvegardé à l’aide de [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).<br/>                                                             |
| [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | Récupère des informations de fichier pour le fichier spécifié.<br/>                                                                                                    |
| [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | Récupère la taille du fichier spécifié, en octets.<br/>                                                                                                   |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Récupère la date et l’heure de création, du dernier accès et de la dernière modification d’un fichier ou d’un répertoire.<br/>                                                   |
| [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | Récupère le type de fichier du fichier spécifié.<br/>                                                                                                        |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | Récupère des informations qui décrivent les modifications dans le répertoire spécifié.<br/>                                                                      |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Définit la date et l’heure de création du fichier ou du répertoire spécifié, du dernier accès ou de la dernière modification.<br/>                                             |



 

 

