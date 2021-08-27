---
description: 'En savoir plus sur : fonction JetStopBackupInstance'
title: JetStopBackupInstance fonction)
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4dae676cfbbb0f2509a7d86fbb6507b8e2110f1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987242"
---
# <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance fonction)

La fonction **JetStopBackupInstance** empêche la continuation de l’activité liée à la sauvegarde de se poursuivre sur une instance en cours d’exécution spécifique, ce qui met fin à la sauvegarde en continu de manière prévisible.

**Windows xp :****JetStopBackupInstance** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Identifie l’instance en cours d’exécution à utiliser pour l’appel d’API.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Le paramètre d’instance spécifié a une valeur non valide (pas une instance en cours d’exécution).</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 



Si cette fonction réussit, l’instance qui a été spécifiée échouera avec les nouvelles API de sauvegarde en continu.

Si cette fonction échoue, aucune étape de préparation de l’arrêt de la sauvegarde sur l’instance ne sera effectuée et aucune modification de l’état de l’instance ne se produira.

#### <a name="remarks"></a>Remarques

La sauvegarde est généralement déclenchée par un événement à l’extérieur du mécanisme de processus et à l’aide de cette API, l’application ESENT elle-même effectue d’autres appels vers les API de sauvegarde en continu. La majorité des API de sauvegarde en continu échouent avec JET_errBackupAbortByServer. Ainsi, toute progression de la sauvegarde en continu (telle que [JetReadFileInstance](./jetreadfileinstance-function.md)) renverra une erreur. Les opérations de sauvegarde qui font partie de l’arrêt de la sauvegarde (comme [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) sont toujours autorisées.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
