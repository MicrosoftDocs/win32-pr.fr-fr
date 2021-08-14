---
description: Comment vous pouvez utiliser les fonctions de sauvegarde des services de certificats pour sauvegarder une base de données de services de certificats et ses fichiers associés.
ms.assetid: f5c9c9f9-5211-4151-b8e0-3351d462c71b
title: Sauvegarde des services de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeeb0881d517de538971d7eafb835ec48f3f33328e3a026b450e6719bfb23ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773085"
---
# <a name="backing-up-certificate-services"></a>Sauvegarde des services de certificats

Vous trouverez ci-dessous un scénario illustrant l’utilisation des fonctions de sauvegarde des services de certificats pour sauvegarder une base de données de services de certificats et ses fichiers associés.

1.  Chargez la bibliothèque Certadm.dll en mémoire (en appelant [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Récupérez l’adresse de chacune des fonctions nécessaires dans Certadm.dll (par le biais de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Utilisez ces adresses lors de l’appel des fonctions dans les étapes restantes.
3.  Appelez [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) pour déterminer si les services de certificats sont en ligne. Les services de certificats doivent être en ligne pour que les opérations de sauvegarde soient réussies.
4.  Appelez [**CertSrvBackupPrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew) pour démarrer une session de sauvegarde. Le descripteur de contexte de sauvegarde des services de certificats qui en résulte sera utilisé par la plupart des autres fonctions de sauvegarde.
5.  Appelez [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) pour déterminer le mappage de restauration. La table de restauration contient les chemins d’accès à utiliser lors de la restauration de la sauvegarde. Enregistrez les informations récupérées par **CertSrvRestoreGetDatabaseLocations** dans un emplacement spécifique à l’application.
6.  Appelez [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) pour déterminer les noms des fichiers de base de données à sauvegarder. Pour chacun de ces fichiers, exécutez les étapes 7 à 9.
7.  Appelez [**CertSrvBackupOpenFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew) pour ouvrir le fichier à sauvegarder.
8.  Appelez [**CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread) pour lire une partie des octets du fichier, puis appelez une routine propre à l’application pour stocker les octets sur un support de sauvegarde. Répétez cette étape jusqu’à ce que tous les octets du fichier soient sauvegardés.
9.  Appelez [**CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose) pour fermer le fichier.
10. Appelez [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) pour déterminer les noms des fichiers journaux à sauvegarder. Pour chacun de ces fichiers, exécutez les étapes 7 à 9.
11. Appelez [**CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs) pour tronquer les fichiers journaux qui ont été sauvegardés aux étapes 6 et 10. Cette étape est facultative. Toutefois, appelez **CertSrvBackupTruncateLogs** uniquement si tous les fichiers retournés par [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) et [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) ont été sauvegardés (sinon, l’opération de restauration échoue). Pour plus d’informations, consultez la page de référence de **CertSrvBackupTruncateLogs** .
12. Appelez [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) pour déterminer les noms des fichiers non-de base de données à sauvegarder. Ces fichiers sont identifiés uniquement par la fonction et doivent être sauvegardés par d’autres moyens.
13. Sauvegardez les fichiers dynamiques identifiés à l’étape 12, à l’aide de routines distinctes de Certadm.dll.
14. Appelez [**CertSrvBackupEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend) pour mettre fin à la session de sauvegarde.
15. Appelez [**CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree) en fonction des besoins pour libérer les tampons alloués par certaines fonctions de sauvegarde des services de certificats. Les appels à [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw), [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)et [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) allouez des tampons qui peuvent être libérés par un appel à **CertSrvBackupFree**.
16. Libérez les ressources Certadm.dll en appelant [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary).

Pour plus d’informations sur les privilèges requis pour sauvegarder la base de données des services de certificats et les fichiers associés, consultez [définition des privilèges de sauvegarde et de restauration](setting-the-backup-and-restore-privileges.md).

 

 
