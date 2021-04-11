---
description: 'En savoir plus sur : fonction JetOSSnapshotFreeze'
title: Fonction JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204073"
---
# <a name="jetossnapshotfreeze-function"></a>Fonction JetOSSnapshotFreeze


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetossnapshotfreeze-function"></a>Fonction JetOSSnapshotFreeze

La fonction **JetOSSnapshotFreeze** démarre un instantané. Pendant que l’instantané est en cours, aucune activité d’écriture sur le disque par le moteur ne peut avoir lieu.

**Windows XP :**  **JetOSSnapshotFreeze** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*snapId*

Identificateur de la session d’instantané.

*pcInstanceInfo*

Nombre d’instances en cours d’exécution dans le moteur qui font partie de la session d’instantané.

*paInstanceInfo*

Tableau de structures, une pour chaque instance en cours d’exécution qui fait partie de la session d’instantané, décrivant l’instance et les bases de données qui en font partie.

*grbit*

Options pour cet appel. Ce paramètre est réservé pour une utilisation ultérieure et la seule valeur valide prise en charge est 0.

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
<td><p>Les pointeurs fournis pour les paramètres de sortie ont la valeur NULL, la session d’instantané n’est pas valide ou le paramètre <em>Grbit</em> n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>La session d’instantané n’est pas dans l’état approprié pour démarrer un blocage (par exemple, un blocage précédent a échoué sur cette session auparavant).</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed</p></td>
<td><p>Le moteur n’est pas dans un État dans lequel un instantané peut être exécuté. Une ou plusieurs sauvegardes de streaming sont déjà en cours, ou une ou plusieurs instances passent par des étapes de récupération ou se terminent.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>L’identificateur de la session d’instantané n’est pas valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>La fonction a échoué en raison d’une condition de mémoire insuffisante.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads</p></td>
<td><p>La fonction a échoué en raison de l’échec du démarrage d’un nouveau thread qui n’a pas pu démarrer.</p></td>
</tr>
</tbody>
</table>


Si cette fonction est établie, aucune e/s d’écriture n’est émise pour les fichiers de base de données ou pour les fichiers journaux qui font partie des instances figées. En outre, les informations de l’instance sont correctement remplies et doivent être libérées ultérieurement en appelant [JetFreeBuffer](./jetfreebuffer-function.md) avec le pointeur vers le tableau d’informations d’instance qui a été retourné.

Si cette fonction échoue, le moteur continue de s’exécuter normalement avec les IOs se produisant comme d’habitude. Il n’est pas nécessaire d’appeler [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) si le gel échoue. En outre, les informations de l’instance ne sont pas remplies, il n’est donc pas nécessaire de libérer cette ressource.

#### <a name="remarks"></a>Notes

Pendant la période de blocage, aucune e/s d’écriture n’est émise pour les bases de données attachées ou les journaux de transactions, même s’il peut y avoir des e/s d’écriture émises dans les bases de données temporaires ou les fichiers de streaming.

L’État dans lequel se trouvent les bases de données et les fichiers journaux pendant le gel (l’État dans lequel les fichiers se trouvent dans une image d’instantané de volume) est tel qu’une récupération normale sera possible si ces fichiers sont restaurés ultérieurement.

Étant donné qu’il n’y a pas d’opérations d’écriture pendant la période de blocage, les appels d’API normaux dans le moteur peuvent être bloqués pour cet intervalle. L’application cliente doit être en mesure de gérer les appels d’API qui peuvent prendre plus de temps que d’habitude si un blocage se produit.

En raison des effets possibles décrits ci-dessus, il existe un délai d’expiration interne après lequel la session d’instantané arrêtera la phase de blocage, même si les API qui effectuent le dégel ou l’abandon n’étaient pas appelées. La valeur du délai d’attente peut être modifiée à l’aide du paramètre système [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) . Notez que l’intervalle de blocage classique est compris entre 10 secondes et le délai d’expiration par défaut est d’environ 60 secondes.

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
<td><p>Implémenté en tant que <strong>JetOSSnapshotFreezeW</strong> (Unicode) et <strong>JetOSSnapshotFreezeA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
