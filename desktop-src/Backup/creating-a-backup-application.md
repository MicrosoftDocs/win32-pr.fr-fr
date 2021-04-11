---
title: Création d’une application de sauvegarde
description: Pour effectuer une entrée ou une sortie sur une bande, une application de sauvegarde doit d’abord obtenir un descripteur du périphérique à bandes. L’exemple de code suivant montre comment utiliser la fonction CreateFile pour ouvrir un périphérique à bandes.
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- Sauvegarde des applications de sauvegarde
- création d’une sauvegarde d’applications de sauvegarde
- sauvegarde de sauvegarde, création d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77409a0c74ee61e333b92dad8b22d9c68ed92eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031610"
---
# <a name="creating-a-backup-application"></a>Création d’une application de sauvegarde

Pour effectuer une entrée ou une sortie sur une bande, une application de sauvegarde doit d’abord obtenir un descripteur du périphérique à bandes. L’exemple de code suivant montre comment utiliser la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir un périphérique à bandes.


```C++
HANDLE hTape;   // handle to tape device
 
hTape = CreateFile(TEXT("\\\\.\\TAPE0"),         // tape dev to open
                   GENERIC_READ | GENERIC_WRITE, // read/write access
                   0,                            // not used
                   0,                            // not used
                   OPEN_EXISTING,                // req for tape devs
                   0,                            // not used
                   NULL);                        // not used
```



Pour sauvegarder une arborescence de répertoires sur une bande, une application doit utiliser les fonctions [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) et [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) pour parcourir l’arborescence de répertoires. Chaque fois qu’un fichier est trouvé, l’application doit obtenir les attributs de fichier à l’aide de la fonction [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) .

S’il existe des liens physiques, une application doit déterminer le nombre de liens et enregistrer l’identificateur unique du fichier dans une table pour les comparaisons ultérieures. La première fois qu’un fichier est trouvé, l’application doit utiliser [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir le fichier, et la fonction [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) pour commencer la sauvegarde. Elle peut ensuite utiliser la fonction [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) à plusieurs reprises pour transférer toutes les informations contenues dans la mémoire tampon utilisée par **BackupRead** à la bande. La deuxième fois qu’un fichier est trouvé (vérifié par rapport à la table des identificateurs de fichier en présence de liens physiques), l’application peut écrire les informations générales sur le fichier sur la bande, suivies d’un flux qui a un identificateur qui est un **\_ lien de sauvegarde**.

Lors de la restauration de fichiers à partir d’une bande sur un disque, une application doit utiliser les fonctions [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)et [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) . Pour chaque fichier sur une bande, l’application doit utiliser **CreateFile** pour créer un nouveau fichier sur le disque, et **BackupWrite** pour commencer la restauration du fichier. L’application doit ensuite utiliser **ReadFile** à plusieurs reprises jusqu’à ce que toutes les informations du fichier soient lues à partir de la bande dans la mémoire tampon remplie par **BackupWrite**.

Si l’un des flux de la mémoire tampon [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) a un identificateur de flux de **\_ lien de sauvegarde** , l’application doit établir un lien physique. Si les données nécessaires pour établir le lien n’existent pas, **BackupWrite** échoue. L’application peut utiliser un catalogue préexistant pour rechercher et restaurer les données d’origine, ou elle peut informer l’utilisateur que les données de fichier à restaurer se trouvent dans un emplacement différent.

 

 