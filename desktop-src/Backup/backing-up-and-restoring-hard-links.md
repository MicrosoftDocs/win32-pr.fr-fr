---
title: Sauvegarde et restauration des liens physiques
description: Pour sauvegarder et restaurer des liens physiques, utilisez les fonctions CreateFile, CreateHardLink, FindFirstFileNameW, FindNextFileNameW, BackupRead, GetFileInformationByHandle et BackupWrite, comme indiqué dans les exemples de pseudos suivants.
ms.assetid: 129e9cf4-8ab1-45d2-8e1a-4bc85b9de668
keywords:
- Sauvegarde des liens physiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c72155231295a1eb07b6b565c018b765693c8f46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031663"
---
# <a name="backing-up-and-restoring-hard-links"></a>Sauvegarde et restauration des liens physiques

Pour sauvegarder et restaurer des liens physiques, utilisez les fonctions [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**CreateHardLink**](/windows/desktop/api/winbase/nf-winbase-createhardlinka), [**FindFirstFileNameW**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilenamew), [**FindNextFileNameW**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew), [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread), [**GetFileInformationByHandle**](/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle)et [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) , comme indiqué dans les exemples de pseudos suivants.

## <a name="pseudocode-algorithm-for-backing-up-hard-links"></a>Algorithme de pseudocode pour la sauvegarde des liens physiques

``` syntax
1.  Initialize and empty a list of known links. 
2.  While there are more files to back up 
3.     Read the disk and get the next file. 
4.     Call CreateFile to open the file for read. 
5.     Call GetFileInformationByHandle to get the NumberOfLinks 
          and the FileIndex.
6.     If the NumberOfLinks is greater than 1 
7.        Search the list of known links, looking for the  
             same FileIndex.
8.        If a match is found 
9.           Skip this file; its link exists already on
                your backup media.
10.       Else
11.          Add the full path of the file and the FileIndex
                to the list of links.
12.          Call BackupRead to copy all data to your backup media.
13.          Call FindFirstFileNameW and FindNextFileNameW to 
                enumerate the hard links to the file.
14.          For each hard link
15.             Mark the data as a LINK on your backup media.
16.             Store the full path from the list to your backup media.
17.          Endfor
18.       Endif
19.    Else
20.       Call BackupRead to copy all data to your backup media.
21.    Endif
22. EndWhile
```

## <a name="pseudocode-algorithm-for-restoring-hard-links"></a>Algorithme de pseudocode pour la restauration des liens physiques

``` syntax
1.  While there are more files to restore 
2.     If there are hard links to the file
3.        Call CreateHardLink to recreate the links.
4.     Endif
5.     Call BackupWrite with the data stored on your backup media
6.  EndWhile
```

**Windows Server 2003 et Windows XP :** Les fonctions [**FindFirstFileNameW**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilenamew) et [**FindNextFileNameW**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew) ne sont pas prises en charge. Vous pouvez utiliser à la place la procédure décrite dans l’exemple de pseudo-code suivant.

## <a name="alternate-pseudocode-algorithm-for-backing-up-hard-links"></a>Autre algorithme de pseudo-code pour la sauvegarde des liens physiques

``` syntax
1.  Initialize and empty a list of known links. 
2.  While there are more files to back up 
3.     Read the disk and get the next file. 
4.     Call CreateFile to open the file for read. 
5.     Call GetFileInformationByHandle to get the NumberOfLinks and 
          the FileIndex. 
6.     If the NumberOfLinks is greater than 1 
7.        Search the list of known links looking for 
             the same FileIndex. 
8.           If a match is NOT found 
9.              Add the full path of the file and the FileIndex
                   to the list. 
10.             Call BackupRead to copy all data to 
                   your backup media. 
11.          Else 
12.             Mark the data as a LINK on your backup media 
13.             Store the full path from the list 
                   to your backup media. 
14.          Endif 
15.    Else 
16.       Call BackupRead to copy all data to your 
             backup media. 
17.    Endif 
18. EndWhile
```

 

 