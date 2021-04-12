---
description: Les fonctions de chiffrement brutes permettent de sauvegarder des fichiers chiffrés.
ms.assetid: 00f9b00e-305d-4554-8b43-7061228c92c3
title: Sauvegarde et restauration de fichiers chiffrés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbc5d1babbbbb92cef9e78f9a0dade702fd63d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034147"
---
# <a name="backup-and-restore-of-encrypted-files"></a>Sauvegarde et restauration de fichiers chiffrés

Le système de fichiers EFS (EFS) filtre l’ouverture d’un fichier chiffré de telle sorte que l’application qui a ouvert le fichier ait accès aux informations non chiffrées, à condition qu’il dispose des informations d’identification appropriées pour accéder au fichier et obtenir la clé nécessaire pour déchiffrer le fichier. Les opérations de lecture ultérieures sur ce fichier produiront du texte non chiffré. Cela est très souhaitable pour un accès standard aux fichiers chiffrés, et assure la transparence du chiffrement et du déchiffrement des fichiers. Toutefois, elle entrave la sauvegarde des fichiers chiffrés, car si la sauvegarde est tentée avec les appels d’e/s de fichier standard tels que [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)et [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), les fichiers sauvegardés seront la version en texte brut.

Les fonctions de chiffrement brutes sont fournies pour résoudre ce problème. Les applications de sauvegarde sont un utilisateur principal prévu pour ces fonctions. Les fonctions de chiffrement brutes diffèrent des autres fonctions de système de fichiers dans le sens où les fonctions d’ouverture, de lecture et d’écriture autorisent l’accès aux flux de données chiffrées brutes et autorisent également la lecture/écriture du flux de $EFS. Par conséquent, l’appelant des fonctions de chiffrement brutes n’a pas besoin d’accéder aux clés de chiffrement qui déchiffrent le fichier. Les API de chiffrement brut suivantes peuvent être utilisées avec les applications de sauvegarde et de restauration : 

| API de chiffrement brut                                     | Description                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)   | Ouvrir un fichier chiffré avec accès aux données au format chiffré. Si l’appelant n’a pas accès à la clé du fichier, l’appelant a besoin de [SeBackupPrivilege](/windows/desktop/SecAuthZ/authorization-constants) pour exporter des fichiers chiffrés ou SeRestorePrivilege pour importer des fichiers chiffrés. |
| [**CloseEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-closeencryptedfileraw) | Fermer un fichier chiffré ouvert avec [ **OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)                                                                                                                                                                                      |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)   | Lire un fichier chiffré en laissant ses données dans un format chiffré                                                                                                                                                                                                                   |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw) | Écrire un fichier chiffré en laissant ses données dans un format chiffré                                                                                                                                                                                                                  |
| [**ImportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_import_func)               | Rappel défini par l’application à utiliser avec [ **WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw)                                                                                                                                                                              |
| [**ExportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_export_func)               | Rappel défini par l’application à utiliser avec [ **ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)                                                                                                                                                                                |



 

 

 
