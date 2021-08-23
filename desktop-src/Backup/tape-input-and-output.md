---
title: Entrée et sortie sur bande
description: Les applications peuvent utiliser plusieurs fonctions pour effectuer des entrées et sorties (e/s) sur un lecteur de bande. Les e/s de bande sont similaires aux e/s effectuées sur un appareil de communication.
ms.assetid: 1862c267-0070-4fe8-bb77-40167913978a
keywords:
- Sauvegarde d’entrée et de sortie sur bande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281eb6104cb71fbd5e7f0b3d9072cefe562ac7b9cc54e05ede53bece8755178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021268"
---
# <a name="tape-input-and-output"></a>Entrée et sortie sur bande

Les applications peuvent utiliser plusieurs fonctions pour effectuer des entrées et sorties (e/s) sur un lecteur de bande. Les e/s de bande sont similaires aux e/s effectuées sur un appareil de communication.

Lors de l’exécution d’e/s sur bande, certains lecteurs de bande stockent les informations du microprogramme de bande dans les premiers blocs sur une bande, généralement à l’aide d’une partie des 100 premiers blocs. Les applications ne doivent pas utiliser ces blocs. Des informations plus spécifiques sur ce sujet sont disponibles auprès des fabricants de systèmes à bandes individuels. En général, une application qui ignore les premiers blocs 100 sur une bande évite les caractéristiques des lecteurs de bande.

Les fonctions [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition) et [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition) récupèrent et déplacent la position actuelle de la bande. La fonction [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark) écrit un nombre spécifié de setmarks, de marques, de marques de courtes et de marques de caractères longs. La fonction [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape) efface tout ou partie d’une bande.

Les fonctions [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) lisent et écrivent des données de fichier depuis et vers la bande. Les données sont lues et écrites dans des blocs complets. Si la taille de bloc de la bande est de 512 octets, toutes les opérations de lecture et d’écriture doivent utiliser des mémoires tampons qui sont des nombres entiers simples de cette taille de bloc : 512, 1024, 1536, 2048, et ainsi de suite. La plupart, voire tous, les lecteurs autorisent uniquement une opération d’écriture après le rembobinage de la bande ou après qu’une opération de lecture a produit un message d’erreur de fin de données.

Pour lire ou écrire des données de fichier vers ou à partir d’une bande en mode bloc de longueur variable, procédez comme suit :

1.  Déterminez si le lecteur de bande prend en charge le mode bloc de longueur variable en appelant la fonction [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) et en vérifiant le \_ \_ \_ bit de bloc de la variable de lecteur de bande du membre **FeaturesLow** de la structure de [**\_ \_ \_ paramètres de lecteur obtenir la bande**](/windows/desktop/api/Winnt/ns-winnt-tape_get_drive_parameters) retournée.
2.  Spécifiez le mode de taille de bloc variable en appelant la fonction [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) , en affectant la valeur zéro au membre **BlockSize** de la structure des [**paramètres de média de jeu de bandes \_ \_ \_**](/windows/desktop/api/Winnt/ns-winnt-tape_set_media_parameters) . Ensuite, utilisez [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) pour lire ou écrire les données du fichier.

Si [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) rencontre une marque de marque, les données jusqu’à la marque sont lues et la fonction échoue. (La fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne un code d’erreur indiquant le type de la marque de texte qui a été rencontrée.) Le système d’exploitation déplace la bande au-delà de la marque de la marque, et une application peut appeler à nouveau **ReadFile** pour continuer la lecture.

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) lisent et écrivent uniquement le flux de données. Les fonctions [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) et [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) lisent et écrivent tous les flux associés à un fichier. Celles-ci incluent les données, les attributs étendus, la sécurité et d’autres flux de données. La sécurité et les flux de données alternatifs s’appliquent uniquement à la partition de système de fichiers NTFS.

La fonction [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek) recherche dans un fichier accédé initialement par [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) ou [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite). Cette fonction permet à une application d’ignorer les informations qui provoquent des erreurs d’accès.

Si une application doit accéder uniquement aux données du fichier, elle doit utiliser [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Ces fonctions peuvent également lire d’autres flux de données si les flux ont été créés à l’aide de la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

Une application de sauvegarde sur bande doit utiliser [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) et [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) pour copier toutes les informations relatives à un fichier. Toutefois, ces fonctions ne lisent ni n’écrivent les caractéristiques des fichiers, telles que les attributs, l’heure de création de fichier, etc. Les applications doivent utiliser les fonctions d’entrée et de sortie de fichier, telles que [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) et [**SetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa), pour récupérer et définir ces valeurs.

 

 