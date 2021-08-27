---
description: 'En savoir plus sur : fonction JetStopBackup'
title: JetStopBackup fonction)
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd5f7fe7096b0562aa9fc4ce8d15f77a4ccf205f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469696"
---
# <a name="jetstopbackup-function"></a>JetStopBackup fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetstopbackup-function"></a>JetStopBackup fonction)

La fonction **JetStopBackup** empêche toute activité liée à la sauvegarde en continu de continuer sur une instance en cours d’exécution spécifique, ce qui met fin à la sauvegarde en continu de manière prévisible.

**Windows XP :**  cette fonction est introduite dans Windows XP.

[JetStopService](./jetstopservice-function.md) est l’appel hérité lorsqu’une seule instance est autorisée. Dans ce cas, la seule instance active est celle qui est préparée pour l’arrêt.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Il n’est pas évident de déterminer l’instance à préparer pour l’arrêt lors de l’utilisation de <a href="gg269240(v=exchg.10).md">JetStopService</a> avec plusieurs modes d’instance.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 



Si cette fonction réussit, l’instance commence à faire échouer les nouvelles API de sauvegarde en continu.

Si cette fonction échoue, aucune étape de préparation de l’arrêt de la sauvegarde sur l’instance ne sera effectuée et aucune modification de l’état de l’instance ne se produira.

#### <a name="remarks"></a>Remarques

La sauvegarde est généralement déclenchée par un événement à l’extérieur du mécanisme de processus et à l’aide de cette API, l’application ESENT elle-même effectue d’autres appels vers les API de sauvegarde en continu. La majorité des API de sauvegarde en continu échouent avec JET_errBackupAbortByServer. Par conséquent, toute progression de la sauvegarde en continu (telle que [JetReadFileInstance](./jetreadfileinstance-function.md)) renverra une erreur. Les opérations de sauvegarde qui font partie de l’arrêt de la sauvegarde (par exemple, [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) sont toujours autorisées.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
