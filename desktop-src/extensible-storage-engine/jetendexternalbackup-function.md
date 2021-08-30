---
description: 'En savoir plus sur : fonction JetEndExternalBackup'
title: Fonction JetEndExternalBackup
TOCTitle: JetEndExternalBackup Function
ms:assetid: 058f903b-14b7-44b3-9ec7-7c05c9ec6363
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269176(v=EXCHG.10)
ms:contentKeyID: 32765479
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 31137035dcaa6ee339d018eafe32e53afc513dfe
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474515"
---
# <a name="jetendexternalbackup-function"></a>Fonction JetEndExternalBackup


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetendexternalbackup-function"></a>Fonction JetEndExternalBackup

La fonction **JetEndExternalBackup** met fin à une session de sauvegarde externe. Cette fonction est le dernier élément d’API d’une série d’éléments d’API qui doivent être appelés pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).

```cpp
    JET_ERR JET_API JetEndExternalBackup(void);
```

### <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p><strong>Windows XP :</strong> cette valeur de retour est introduite dans Windows XP</p><p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui nécessite l’accès à toutes les données pour protéger l’intégrité de ces données.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errNoBackup</p> | <p>L’opération a échoué, car aucune sauvegarde externe n’est en cours.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p><strong>Windows Server 2003 :</strong> cette valeur de retour est introduite dans Windows Server 2003.</p><p>L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p> | 
| <p>errBackupAbortByCaller</p> | <p><strong>Windows XP :</strong> cette valeur de retour est introduite dans Windows XP.</p><p>L’appelant a interrompu une sauvegarde au milieu de la séquence de sauvegarde sans signaler l’intention avec <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. cette erreur est le résultat d’un bogue dans le client de sauvegarde de Windows Server 2003 et versions ultérieures. sur Windows XP, cette erreur est retournée pour un arrêt intentionnel de la séquence de sauvegarde externe.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>l’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (Windows mode de compatibilité 2000) quand une seule instance est prise en charge, alors que plusieurs instances existent déjà.</p> | 



Si cette fonction réussit, la sauvegarde externe était un succès. Success indique que tous les fichiers (par exemple, les bases de données et les journaux) qui sont appropriés pour le type de sauvegarde (spécifié dans [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) ont été récupérés à partir du moteur de sauvegarde. Les fichiers sauvegardés peuvent être récupérés avec la récupération matérielle ([JetExternalRestore](./jetexternalrestore-function.md)).

Si cette fonction échoue, la sauvegarde externe se termine généralement. L’échec signifie que la sauvegarde n’est pas valide en raison d’une erreur de client ou d’utilisation de l’application. Il est important de vérifier le code de retour de cette API pour vérifier que la séquence de sauvegarde a réussi.

#### <a name="remarks"></a>Remarques

Si le moteur est configuré pour consigner les événements, un événement est consigné pour indiquer la résolution de la sauvegarde externe.

Si la séquence de sauvegarde n’est pas exécutée dans l’ordre et avec un appel réussi à **JetEndExternalBackup**, les sauvegardes incrémentielles suivantes peuvent contenir plus de données que celles prévues par l’application.

Pour plus d’informations sur la séquence de l’API de sauvegarde externe, consultez [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

avant Windows Vista, si la troncation du journal n’a pas été effectuée, le moteur a considéré que la sauvegarde était une sauvegarde de copie. Toutefois, la sauvegarde peut être une sauvegarde normale pour laquelle la troncation n’a pas été effectuée (par exemple, s’il y a des bases de données détachées). L’option JET_bitBackupTruncateDone peut être utilisée pour informer le moteur du moteur et autoriser les modifications d’en-tête de base de données appropriées.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[Paramètres de gestion des erreurs](./error-handling-parameters.md)  
[erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JET_ERR](./jet-err.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
