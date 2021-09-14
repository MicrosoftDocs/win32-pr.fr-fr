---
description: Montre comment les fonctions de sauvegarde des services de certificats peuvent être utilisées pour restaurer et récupérer une base de données de services de certificats et ses fichiers associés.
ms.assetid: f4914f45-629d-4f24-8328-d7f27e8a0062
title: Restauration des services de certificats à partir d’une sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f5adf46d802194909397a3b70483b3cf43bb409
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416363"
---
# <a name="restoring-certificate-services-from-backup"></a>Restauration des services de certificats à partir d’une sauvegarde

Le scénario suivant montre comment les fonctions de sauvegarde des services de certificats peuvent être utilisées pour restaurer et récupérer une base de données de services de certificats et ses fichiers associés. Le processus de restauration implique l’écriture des fichiers contenus dans un jeu de sauvegarde sur disque. Vous pouvez restaurer plusieurs jeux de sauvegarde (une sauvegarde complète plus zéro, une ou plusieurs sauvegardes incrémentielles), mais toutes les restaurations doivent être terminées avant de commencer le processus de récupération. Le processus de récupération implique la relecture des fichiers journaux par les services de certificats pour garantir la cohérence des fichiers journaux et de base de données, garantissant ainsi l’intégrité de la base de données. Le scénario illustre les appels de fonction permettant de restaurer les jeux de sauvegarde et d’informer les services de certificats des paramètres de récupération.

Une sauvegarde complète existante de la base de données des services de certificats doit exister avant d’implémenter ce scénario.

1.  Chargez la bibliothèque Certadm.dll en mémoire (en appelant [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Récupérez l’adresse de chacune des fonctions nécessaires dans Certadm.dll (par le biais de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Utilisez ces adresses lors de l’appel des fonctions dans les étapes restantes.
3.  Appelez [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) pour déterminer si les services de certificats sont en ligne. Si les services de certificats sont en cours d’exécution, arrêtez-le avant de continuer. Les services de certificats ne doivent pas être en ligne pour que les opérations de restauration aboutissent.
4.  Appelez [**CertSrvRestorePrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew) pour démarrer une session de restauration. Le descripteur de contexte de sauvegarde des services de certificats qui en résulte sera utilisé par plusieurs autres fonctions.
5.  Déterminez le chemin d’accès à l’emplacement de la base de données. Pendant un scénario de sauvegarde, cette valeur aurait été disponible à partir d’un appel à [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw); Cette valeur doit avoir été stockée dans le cadre de la sauvegarde.
6.  Créez un mappage de restauration spécifiant le nom de la base de données restaurée. Une structure de table de restauration de base de données de services de certificats (CSEDB \_ RSTMAPW) est utilisée pour spécifier un mappage de restauration. Définissez le \_ membre **pwszDatabaseName** du RSTMAPW CSEDB et le \_ membre **RSTMAPW** CSEDB pwszNewDatabaseName sur l’emplacement de la base de données déterminé à l’étape 5. Si, éventuellement, la base de données restaurée doit avoir un nom différent de celui de la base de données de sauvegarde, définissez le \_ membre **pwszNewDatabaseName** du RSTMAPW CSEDB sur le nouveau nom de la base de données.
7.  Si vous souhaitez vous assurer que les modifications apportées à la base de données après la sauvegarde ne sont pas réappliquées à la fin de la restauration de la base de données (dans le cadre de la récupération de la base de données lors du prochain démarrage des services de certificats), supprimez les fichiers de la base de données active et des répertoires des journaux du serveur cible
8.  Copiez les fichiers contenus dans la sauvegarde complète dans les répertoires de la base de données active et du journal du serveur cible.
9.  Appelez [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw) pour inscrire une opération de restauration pour la sauvegarde complète. **CertSrvRestoreRegister** utilise le mappage de restauration spécifié à l’étape 6. **CertSrvRestoreRegister** spécifie également l’emplacement de la base de données de sauvegarde et des journaux. L’appel de **CertSrvRestoreRegister** force les services de certificats à tenter d’effectuer une opération de restauration lors du prochain démarrage. Il empêche également les services de certificats de traiter les demandes de certificats jusqu’à ce que la restauration soit terminée.
10. Appelez [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete), ce qui a pour effet de terminer l’activité d’inscription démarrée à l’étape 8. Notez que l’inscription d’une opération de restauration est une instruction qui doit être suivie par les services de certificats lorsqu’elle est démarrée. la récupération réelle aura lieu uniquement après le démarrage des services de certificats.
11. Pour chaque sauvegarde incrémentielle à restaurer, copiez les fichiers contenus dans la sauvegarde incrémentielle dans le répertoire des journaux actifs du serveur cible, puis appelez [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw), suivi d’un appel à [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete). L’inscription des sauvegardes incrémentielles pour la restauration peut se produire dans n’importe quel ordre, mais seul l’ensemble des fichiers pour une sauvegarde incrémentielle doit être copié sur le serveur avant chaque appel à **CertSrvRestoreRegister**.
12. Copiez les fichiers dynamiques des services de certificats sur le serveur cible. Les fichiers dynamiques auraient été identifiés lors de la sauvegarde lors de l’appel de [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) . Il peut être nécessaire d’arrêter le service de publication World Wide Web pour autoriser le remplacement des fichiers dynamiques.
13. Appelez [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend) pour mettre fin à la session de restauration.
14. Démarrez l’application des services de certificats manuellement (ou attendez le prochain redémarrage pour qu’elle démarre automatiquement). Lorsque les services de certificats démarrent, il détermine si une opération de restauration a été inscrite ; Si une opération de restauration a été enregistrée, les services de certificats commencent la récupération. Les services de certificats ne traitent pas les demandes de certificat tant que l’opération de récupération n’est pas terminée.

> [!Note]  
> Une fois la récupération terminée, il est important d’effectuer une nouvelle sauvegarde complète de la base de données des services de certificats. Cela est nécessaire pour tronquer les fichiers journaux restaurés et établir un jeu de sauvegarde de base pour les restaurations ultérieures. Les sauvegardes effectuées après une restauration ne peuvent pas être mélangées à des sauvegardes (complètes ou incrémentielles) effectuées avant la restauration. autrement dit, après la restauration d’une base de données de services de certificats et l’avancement de l’état suivant, vous ne pouvez pas utiliser les sauvegardes de prérestauration pour restaurer la base de données à l’état suivant.

 

 

 
