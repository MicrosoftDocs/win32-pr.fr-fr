---
description: 'En savoir plus sur : fonction JetEndExternalBackupInstance'
title: JetEndExternalBackupInstance fonction)
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a017a0dbb4fa2f92c3e43a9dd2ff5649b65ee375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034906"
---
# <a name="jetendexternalbackupinstance-function"></a>JetEndExternalBackupInstance fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetendexternalbackupinstance-function"></a>JetEndExternalBackupInstance fonction)

La fonction **JetEndExternalBackupInstance** met fin à une session de sauvegarde externe. Cette API est la dernière API d’une série d’API qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).

**Windows XP : JetEndExternalBackupInstance** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance à utiliser pour cet appel.

**Windows 2000 :** Pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge. L’utilisation de cette instance globale est implicitement dans ce cas.

**Windows XP :** Pour Windows XP et versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (mode de compatibilité Windows 2000) lorsqu’une seule instance est prise en charge. Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Code de retour</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>L’opération s’est terminée avec succès.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByCaller</p></td>
<td><p><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</p>
<p>L’appelant a interrompu une sauvegarde au milieu de la séquence de sauvegarde sans signaler l’intention avec <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Cette erreur est le résultat d’un bogue dans le client de sauvegarde de Windows Server 2003 et versions ultérieures. Sur Windows XP, cette erreur est retournée pour un arrêt intentionnel de la séquence de sauvegarde externe.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p><strong>Windows Server 2003 :  </strong> Cette valeur de retour est introduite dans Windows Server 2003.</p>
<p>L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</p>
<p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>L’opération a échoué, car aucune sauvegarde externe n’est en cours.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge, alors que en fait, plusieurs instances existent déjà.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


Si la fonction réussit, la sauvegarde externe était un succès. Success indique que tous les fichiers (par exemple, les bases de données et les journaux) qui sont appropriés pour le type de sauvegarde (spécifié dans [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) ont été récupérés à partir du moteur de sauvegarde. Les fichiers sauvegardés peuvent être récupérés avec la récupération matérielle ([JetExternalRestore](./jetexternalrestore-function.md)).

Si cette fonction échoue, la sauvegarde externe se termine généralement. L’échec signifie que la sauvegarde n’est pas valide en raison d’une erreur de client ou d’utilisation de l’application. Il est important de vérifier le code de retour de cette API pour vérifier que la séquence de sauvegarde a réussi.

#### <a name="remarks"></a>Notes

Si le moteur est configuré pour consigner les événements, un événement est consigné pour indiquer la résolution de la sauvegarde externe.

Si la séquence de sauvegarde n’est pas exécutée dans l’ordre et avec un appel réussi à [JetEndExternalBackup](./jetendexternalbackup-function.md), les sauvegardes incrémentielles suivantes peuvent contenir plus de données que celles prévues par l’application.

Pour plus d’informations sur la séquence de l’API de sauvegarde externe, consultez [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

Avant Windows Vista, si la troncation du journal n’a pas été effectuée, le moteur a considéré que la sauvegarde était une sauvegarde de copie. Toutefois, la sauvegarde peut être une sauvegarde normale pour laquelle la troncation n’a pas été effectuée (par exemple, s’il y a des bases de données détachées). L’option JET_bitBackupTruncateDone peut être utilisée pour informer le moteur du moteur et permettre des modifications d’en-tête de base de données appropriées.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008 ou Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothèque</strong></p></td>
<td><p>Utilisez ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[Paramètres de gestion des erreurs](./error-handling-parameters.md)  
[Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JET_ERR](./jet-err.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
