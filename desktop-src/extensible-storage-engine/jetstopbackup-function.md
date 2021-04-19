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
ms.openlocfilehash: c47a1454e5846fae510a7b91c197d4b180fd14a7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106531382"
---
# <a name="jetstopbackup-function"></a>JetStopBackup fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetstopbackup-function"></a>JetStopBackup fonction)

La fonction **JetStopBackup** empêche toute activité liée à la sauvegarde en continu de continuer sur une instance en cours d’exécution spécifique, ce qui met fin à la sauvegarde en continu de manière prévisible.

**Windows XP :**  Cette fonction est introduite dans Windows XP.

[JetStopService](./jetstopservice-function.md) est l’appel hérité lorsqu’une seule instance est autorisée. Dans ce cas, la seule instance active est celle qui est préparée pour l’arrêt.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

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
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Il n’est pas évident de déterminer l’instance à préparer pour l’arrêt lors de l’utilisation de <a href="gg269240(v=exchg.10).md">JetStopService</a> avec plusieurs modes d’instance.</p>
<p><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</p></td>
</tr>
</tbody>
</table>


Si cette fonction réussit, l’instance commence à faire échouer les nouvelles API de sauvegarde en continu.

Si cette fonction échoue, aucune étape de préparation de l’arrêt de la sauvegarde sur l’instance ne sera effectuée et aucune modification de l’état de l’instance ne se produira.

#### <a name="remarks"></a>Notes

La sauvegarde est généralement déclenchée par un événement à l’extérieur du mécanisme de processus et à l’aide de cette API, l’application ESENT elle-même effectue d’autres appels vers les API de sauvegarde en continu. La majorité des API de sauvegarde en continu échouent avec JET_errBackupAbortByServer. Par conséquent, toute progression de la sauvegarde en continu (telle que [JetReadFileInstance](./jetreadfileinstance-function.md)) renverra une erreur. Les opérations de sauvegarde qui font partie de l’arrêt de la sauvegarde (par exemple, [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) sont toujours autorisées.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
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

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
