---
description: 'En savoir plus sur : fonction JetGetTruncateLogInfoInstance'
title: JetGetTruncateLogInfoInstance fonction)
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d51243ff6ca4b2bbaec77233bbe00437f55e0f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519543"
---
# <a name="jetgettruncateloginfoinstance-function"></a>JetGetTruncateLogInfoInstance fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgettruncateloginfoinstance-function"></a>JetGetTruncateLogInfoInstance fonction)

La fonction **JetGetTruncateLogInfoInstance** est utilisée lors d’une sauvegarde initiée par [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) pour interroger une instance afin d’obtenir les noms des fichiers journaux des transactions qui peuvent être supprimés en toute sécurité une fois la sauvegarde terminée.

**Windows XP :**  **JetGetTruncateLogInfoInstance** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance à utiliser pour cet appel.

*szz*

Mémoire tampon de sortie qui reçoit la liste des chaînes terminées par le caractère null qui décrivent l’ensemble des fichiers journaux des transactions qui peuvent être supprimés en toute sécurité une fois la sauvegarde terminée.

La liste des chaînes retournées dans cette mémoire tampon est au même format qu’une chaîne multiple utilisée par le registre. Chaque chaîne terminée par le caractère NULL est retournée dans l’ordre et suivie d’une marque de fin null finale.

*cbMax*

Taille maximale, en octets, de la mémoire tampon de sortie.

*pcbActual*

Pointeur vers la mémoire tampon de sortie qui reçoit la quantité réelle de données de chaîne.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs valeurs de paramètre a entraîné un résultat inattendu.</p>
<p><strong>Windows XP et versions ultérieures :</strong>  Cela peut se produire pour <strong>JetGetTruncateLogInfoInstance</strong> lorsque le handle d’instance spécifié n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p><strong>Windows XP :</strong>  Cette valeur de retour a été introduite dans Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p>
<p><strong>Windows XP :</strong>  Cette valeur de retour a été introduite dans Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>L’opération a échoué, car aucune sauvegarde externe n’est en cours.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>JetGetTruncateLogInfoInstance</strong></p></td>
<td><p>Des descripteurs de fichiers en attente ont été créés à l’aide de <a href="gg269249(v=exchg.10).md">JetOpenFile</a> pour l’instance.</p></td>
</tr>
</tbody>
</table>


Si cette fonction réussit, les informations demandées sur l’ensemble des fichiers journaux des transactions qui peuvent être supprimés en toute sécurité une fois la sauvegarde terminée, sont placées dans les tampons de sortie où elles sont fournies. L’ordinateur d’état de sauvegarde est avancé, de sorte que la sauvegarde des fichiers de base de données n’est plus autorisée. Seuls les fichiers de correctifs de base de données et les fichiers journaux de transactions peuvent être ouverts pour la sauvegarde au-delà de ce point.

Si cette fonction échoue, l’état des mémoires tampons de sortie n’est pas défini. L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance.

#### <a name="remarks"></a>Notes

Cette API ne retourne pas d’erreur ou d’avertissement si la mémoire tampon de sortie est trop petite pour accepter la liste complète des fichiers qui doivent faire partie du jeu de fichiers de sauvegarde. L’application doit toujours fournir une mémoire tampon pour recevoir la taille réelle de cette liste et utiliser ces informations pour déterminer si la liste a été tronquée.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté en tant que <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) et <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
