---
description: 'En savoir plus sur : fonction JetTruncateLogInstance'
title: JetTruncateLogInstance fonction)
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7286b97b80c323eb6bba7b9d28057bf45eec3920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515058"
---
# <a name="jettruncateloginstance-function"></a>JetTruncateLogInstance fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jettruncateloginstance-function"></a>JetTruncateLogInstance fonction)

La fonction **JetTruncateLogInstance** est utilisée lors d’une sauvegarde lancée par [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) pour supprimer tous les fichiers journaux des transactions qui ne seront plus nécessaires une fois la sauvegarde en cours terminée avec succès.

**Windows XP :**  **JetTruncateLogInstance** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance à utiliser pour cet appel.

Pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge. L’utilisation de cette instance globale est implicitement dans ce cas.

Pour Windows XP et versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (mode de compatibilité Windows 2000) lorsqu’une seule instance est prise en charge. Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.

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
<td><p>JET_errBackupAbortByServer</p></td>
<td><p><strong>Windows Server 2003 :</strong>  Cette valeur de retour est introduite dans Windows Server 2003.</p>
<p>L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>L’opération de sauvegarde a échoué, car elle était appelée hors séquence. <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> retourne cette erreur s’il existe des descripteurs de fichiers en attente qui ont été créés à l’aide de <a href="gg269249(v=exchg.10).md">JetOpenFile</a> pour l’instance.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs paramètres a généré un résultat inattendu. Cela peut se produire pour <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> lorsque le handle d’instance spécifié n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>L’opération a échoué, car aucune sauvegarde externe n’est en cours.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


Si cette fonction réussit, l’ensemble des fichiers journaux des transactions qui ne seront plus nécessaires une fois la sauvegarde actuelle terminée est supprimé. L’ordinateur d’état de sauvegarde est avancé, de sorte que la sauvegarde des fichiers de base de données n’est plus autorisée. Seuls les fichiers de correctifs de base de données et les fichiers journaux des transactions sont autorisés à être ouverts pour la sauvegarde au-delà de ce point.

Si cette fonction échoue, l’ordinateur d’état de sauvegarde peut être avancé, de sorte que la sauvegarde des fichiers de base de données n’est plus autorisée. Un certain nombre de fichiers journaux de transactions peuvent être supprimés moins que le nombre souhaité, mais ils seront toujours supprimés du plus ancien au plus récent.

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

[Fichiers ESE (Extensible Storage Engine)](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
