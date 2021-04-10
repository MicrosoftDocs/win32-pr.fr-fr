---
title: Sauvegarde d’un serveur de Active Directory
description: Une sauvegarde Active Directory Server vous oblige à sauvegarder la base de données et les journaux des transactions. Cette rubrique fournit une procédure pas à pas décrivant comment une application de sauvegarde sauvegarde le service d’annuaire Active Directory.
ms.assetid: 250b2f40-6d43-4aa5-a588-b0cd4839828d
ms.tgt_platform: multiple
keywords:
- sauvegarde Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5affde952ee543afe1bb9b794cce074a74382aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028511"
---
# <a name="backing-up-an-active-directory-server"></a>Sauvegarde d’un serveur de Active Directory

Une sauvegarde Active Directory Server vous oblige à sauvegarder la base de données et les journaux des transactions. Cette rubrique fournit une procédure pas à pas décrivant comment une application de sauvegarde sauvegarde le service d’annuaire Active Directory.

L’appelant de ces fonctions de sauvegarde doit avoir le privilège de **\_ \_ nom de sauvegarde se** . Vous pouvez utiliser la fonction [**DsSetAuthIdentity**](dssetauthidentity.md) pour définir le contexte de sécurité sous lequel les fonctions de sauvegarde/restauration d’annuaire sont appelées.

**Pour sauvegarder un serveur Active Directory, procédez comme suit :**

1.  Appelez la fonction [**DsIsNTDSOnline**](dsisntdsonline.md) pour déterminer si Active Directory Domain Services sont en cours d’exécution.
2.  Si Active Directory Domain Services sont en cours d’exécution, appelez la fonction [**DsBackupPrepare**](dsbackupprepare.md) pour initialiser un handle de contexte de sauvegarde. Si Active Directory Domain Services ne sont pas en cours d’exécution, il ne peut pas être sauvegardé et l’application de sauvegarde doit faire échouer l’opération de sauvegarde.
3.  Appelez la fonction [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) pour obtenir la liste des fichiers à sauvegarder. Pour libérer la mémoire retournée par cette fonction, appelez la fonction [**DsBackupFree**](dsbackupfree.md) .
4.  Pour chaque nom de la liste de fichiers retournée, appelez la fonction [**DsBackupOpenFile**](dsbackupopenfile.md) suivie d’appels répétés à la fonction [**DsBackupRead**](dsbackupread.md) jusqu’à ce que l’intégralité du fichier ait été lue. Une fois la lecture du fichier terminée, appelez la fonction [**DsBackupClose**](dsbackupclose.md) pour la fermer.
5.  Une fois tous les fichiers de base de données sauvegardés, appelez la fonction [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) pour obtenir la liste des journaux des transactions. Cette liste est gérée de la même façon que la liste des fichiers de base de données.
6.  Une fois que vous avez fini de sauvegarder le journal des transactions, appelez la fonction [**DsBackupTruncateLogs**](dsbackuptruncatelogs.md) pour supprimer tous les journaux de transactions validés qui ont été sauvegardés.
7.  Enregistrez le contenu du jeton d’expiration fourni par la fonction [**DsBackupPrepare**](dsbackupprepare.md) . Il peut être enregistré dans un fichier ou dans une autre mémoire persistante. Ce jeton doit être passé à la fonction [**DsRestorePrepare**](dsrestoreprepare.md) pour lancer une opération de restauration.
8.  Libérez la mémoire pour le jeton d’expiration en passant le pointeur de jeton à la fonction [**DsBackupFree**](dsbackupfree.md) .
9.  Enfin, appelez la fonction [**DsBackupEnd**](dsbackupend.md) pour libérer toutes les ressources associées au descripteur de contexte de sauvegarde.

 

 




