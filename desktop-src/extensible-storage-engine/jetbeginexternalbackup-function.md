---
description: 'En savoir plus sur : fonction JetBeginExternalBackup'
title: JetBeginExternalBackup fonction)
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfa3380a1e6efe3001580aab72aeeb6ad1ef203b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986073"
---
# <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup fonction)

La fonction **JetBeginExternalBackup** lance une sauvegarde externe alors que le moteur et la base de données sont en ligne et actifs. **JetBeginExternalBackup** est le premier d’une série de fonctions qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).

Une sauvegarde externe peut être utilisée pour implémenter des sauvegardes complètes, incrémentielles ou différentielles.

La sauvegarde sera approximative, car la sauvegarde sera cohérente à un point unique dans le temps dans l’historique des transactions, mais le contrôle du point exact dans le temps n’est pas possible.

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*grbit*

Groupe de bits qui spécifient zéro, une ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Cet indicateur est déconseillé. L’utilisation de ce bit entraîne le retour de JET_errInvalidgrbit.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Crée une sauvegarde incrémentielle par opposition à une sauvegarde complète. Cela signifie que seuls les fichiers journaux depuis la dernière sauvegarde complète ou incrémentielle sont sauvegardés.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Réservé pour un usage futur. défini pour Windows XP.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Si une sauvegarde externe ou de capture instantanée est déjà en cours, cette erreur est retournée, jusqu’à ce que <strong>JetBeginExternalBackup</strong> (ou l’une des variantes de celle-ci) soit appelé. ESE n’autorise qu’une seule sauvegarde en ligne à la fois.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>L’instance ou le moteur de base de données est en mode de récupération ou d’arrêt ou d’arrêt.</p> | 
| <p>JET_errCheckpointCorrupt</p> | <p>Sur une sauvegarde complète, le fichier de point de contrôle n’a pas pu être lu ou le fichier n’a pas pu être vérifié.</p> | 
| <p>JET_errCheckpointFileNotFound</p> | <p>Dans le cas d’une sauvegarde complète, le fichier de point de contrôle est introuvable.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong> cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errInvalidBackup</p> | <p>L’enregistrement circulaire est activé et le type de sauvegarde spécifié est JET_bitBackupIncremental. Pour plus d’informations sur la façon de contrôler la journalisation circulaire ou non circulaire, consultez <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> dans les <strong>Erreurs du journal des transactions</strong> .</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Un ou plusieurs des membres <em>Grbit</em> ne sont pas valides.</p> | 
| <p>JET_errLoggingDisabled</p> | <p>La récupération ou la journalisation est désactivée. Vous ne pouvez pas effectuer une sauvegarde en ligne si la journalisation est désactivée. Pour plus d’informations sur la journalisation et la récupération, consultez <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</p> | 
| <p>JET_errLogWriteFail</p> | <p>Le moteur a cessé d’écrire sur le lecteur de journal, en raison d’erreurs d’e/s disque complètes ou d’e/s disque.</p> | 
| <p>JET_errMissingFullBackup</p> | <p>La sauvegarde incrémentielle a été spécifiée (avec JET_bitBackupIncremental) et jamais une sauvegarde complète de l’une des bases de données attachées pour le jeu de journalisation.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L’opération a échoué, car la mémoire peut être allouée pour être terminée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>l’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (Windows mode de compatibilité 2000), où une seule instance est prise en charge lorsqu’il existe déjà plusieurs instances.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p> | 



Si la fonction est réussie, une sauvegarde externe est lancée et le moteur d’état de sauvegarde est initialisé. Les API suivantes peuvent maintenant être appelées pour terminer la séquence de sauvegarde externe et diffuser ou lire le fichier de base de données, le fichier de correctif de base de données (si pris en charge) et le fichier journal. Un événement peut être enregistré au début d’une sauvegarde externe.

Si la fonction échoue, la session de sauvegarde ne sera pas initiée. Si une autre session de sauvegarde est en cours, elle ne sera pas annulée.

#### <a name="remarks"></a>Remarques

Le processus de sauvegarde externe (tel qu’il a été démarré par **JetBeginExternalBackup**) est conçu pour permettre une sauvegarde en ligne de transactions approximatives de la totalité de l’instance sur un appareil cible en tant que flux. La sauvegarde contient tous les fichiers de base de données qui sont attachés à l’instance à l’aide de [JetAttachDatabase](./jetattachdatabase-function.md) (pour une sauvegarde complète), suivis des fichiers correctifs de base de données associés (si pris en charge), et enfin des fichiers journaux des transactions qui ont été générés pendant le processus de sauvegarde. Le résultat final est un ensemble de fichiers qui peuvent être restaurés à partir du flux, éventuellement combinés avec des fichiers de base de données et des fichiers journaux existants, et enfin récupérés dans un état cohérent.

L’ordre général des opérations pour une sauvegarde complète est constitué des appels suivants. Tout d’abord, **JetBeginExternalBackup** est appelé pour démarrer le processus de sauvegarde. Ensuite, [JetGetAttachInfo](./jetgetattachinfo-function.md) est appelé pour récupérer la liste des bases de données qui sont attachées à l’instance qui doit être sauvegardée. Pour chacune de ces bases de données, [JetOpenFile](./jetopenfile-function.md) est appelé, suivi d’un certain nombre d’appels [JetReadFile](./jetreadfile-function.md) , puis d’un appel à [JetCloseFile](./jetclosefile-function.md). Ensuite, [JetGetLogInfo](./jetgetloginfo-function.md) est appelé pour obtenir la liste des fichiers journaux et des correctifs de base de données à sauvegarder. Pour chacun de ces fichiers, une autre séquence d’appels [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md)et [JetCloseFile](./jetclosefile-function.md) est effectuée. Ensuite, tous les fichiers journaux de transactions non souhaités sont supprimés à l’aide de [JetTruncateLog](./jettruncatelog-function.md). Enfin, la sauvegarde est terminée par un appel à [JetEndExternalBackup](./jetendexternalbackup-function.md).

Il est également possible de modifier cet ensemble d’étapes pour effectuer une sauvegarde incrémentielle de l’instance. Une sauvegarde incrémentielle énumère et sauvegarde les fichiers journaux. Les sauvegardes incrémentielles sont possibles uniquement si l’enregistrement circulaire n’est pas activé.

Il est également possible de modifier cet ensemble d’étapes pour permettre l’exécution de sauvegardes différentielles ultérieures de l’instance. Pour effectuer une sauvegarde différentielle, n’appelez pas [JetTruncateLog](./jettruncatelog-function.md) dans la sauvegarde complète ou incrémentielle précédente. Si vous n’appelez pas [JetTruncateLog](./jettruncatelog-function.md), vous autorisez les sauvegardes suivantes à être différentielles en ce qui concerne la dernière sauvegarde complète ou incrémentielle. Les sauvegardes différentielles ne sont possibles que si l’enregistrement circulaire n’est pas activé.

Le fichier de correctif de base de données est un fichier auxiliaire spécial qui est utilisé pour stocker les images de page de base de données dans certaines circonstances pendant la sauvegarde. Ce fichier doit être présent dans le même emplacement que la base de données qui lui est associée au cours d’une opération de restauration. ce fichier est utilisé uniquement dans Windows 2000. par conséquent, toute application écrite pour fonctionner sur Windows 2000 et d’autres versions doit prendre en charge les fichiers correctifs de base de données, le cas échéant, mais elle ne doit pas non plus échouer si elles ne sont pas présentes.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
