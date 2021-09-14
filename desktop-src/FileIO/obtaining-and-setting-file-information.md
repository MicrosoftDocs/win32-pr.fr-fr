---
description: Fonctions à utiliser pour récupérer et définir des informations de fichier.
ms.assetid: 3b5fb709-c699-4651-8072-97210c8cf763
title: Obtention et définition des informations de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c6eb6abf2554e1945e0782c667245ea0eaa99be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009891"
---
# <a name="obtaining-and-setting-file-information"></a>Obtention et définition des informations de fichier

Les rubriques suivantes décrivent comment récupérer et définir des informations de fichier.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                             | Description                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Récupération des informations de type de fichier](retrieving-file-type-information.md)<br/>                               | La fonction [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) récupère le type d’un fichier : disque, caractère (tel qu’une console), canal ou inconnu.<br/>                                                                                                                                               |
| [Détermination de la taille d’un fichier](determining-the-size-of-a-file.md)<br/>                                   | La fonction [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) récupère la taille d’un fichier.<br/>                                                                                                                                                                                                      |
| [Recherche d’un ou plusieurs fichiers](searching-for-one-or-more-files.md)<br/>                                 | Une application peut rechercher dans le répertoire actif tous les noms de fichiers qui correspondent à un modèle donné à l’aide des fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)et [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .<br/> |
| [Définition et obtention de l’horodateur d’un fichier](setting-and-getting-the-timestamp-of-a-file.md)<br/>         | Les applications peuvent récupérer et définir la date et l’heure de création, de modification ou de dernier accès d’un fichier à l’aide des fonctions [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) et [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) .<br/>                                                                         |
| [Détermination de la page de codes du jeu de caractères en cours](determining-the-current-character-set-code-page.md)<br/> | La fonction [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) détermine si les fonctions d’e/s de fichier utilisent la page de codes du jeu de caractères ANSI ou OEM.<br/>                                                                                                                               |



 

 

