---
description: 'En savoir plus sur : fonction JetGetRecordSize'
title: JetGetRecordSize fonction)
TOCTitle: JetGetRecordSize Function
ms:assetid: a28567ed-c732-4509-9f8d-6f8104f62a86
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294045(v=EXCHG.10)
ms:contentKeyID: 32765644
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 255ca71f3b57c0d1f1bc8440a9a6d4697c09c670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952544"
---
# <a name="jetgetrecordsize-function"></a>JetGetRecordSize fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgetrecordsize-function"></a>JetGetRecordSize fonction)

La fonction **JetGetRecordSize** récupère les informations sur la taille des enregistrements à partir de l’emplacement souhaité.

**Windows Vista : JetGetRecordSize** est introduit dans Windows Vista.

```cpp
    JET_ERR JET_API JetGetRecordSize(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Identifie le contexte de session de base de données qui sera utilisé pour l’appel d’API.

*TableID*

Identifie la table ou le curseur qui sera utilisé pour l’appel d’API. Le curseur doit être positionné sur un enregistrement ou avoir une mise à jour préparée.

*precsize*

Pointeur vers une mémoire tampon de sortie pour la structure [JET_RECSIZE](./jet-recsize-structure.md) .

*grbit*

Il s’agit d’une ou plusieurs des valeurs suivantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRecordSizeInCopyBuffer</p></td>
<td><p>Cela récupère la taille de l’enregistrement qui se trouve dans le tampon de copie préparé pour la mise à jour. Dans le cas contraire, l' <em>TableID</em> ou le curseur doit être positionné sur un enregistrement et cet enregistrement sera utilisé.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordSizeRunningTotal</p></td>
<td><p>Lorsque ce bit est spécifié, le <a href="gg294072(v=exchg.10).md">JET_RECSIZE</a> n’est pas mis à zéro avant de remplir le contenu, ce qui agit efficacement comme une accumulation des statistiques pour plusieurs enregistrements visités ou mis à jour.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRecordSizeLocal</p></td>
<td><p>Ainsi, l’API ignore les valeurs longues non intrinsèques. Par exemple, seul l’enregistrement local de la page sera utilisé.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>L’une des options demandées n’est pas valide ou n’est pas implémentée. Cette erreur est retournée par la fonction <strong>JetGetRecordSize</strong> lorsqu’un <em>Grbit</em> illégal est spécifié.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p><strong>Windows XP :</strong>  Les JET_errInstanceUnavailable sont retournées uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Il n’est pas conforme d’utiliser la même session à partir de plusieurs threads en même temps.</p>
<p><strong>Windows XP :</strong>  Les JET_errInstanceUnavailable sont retournées uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Cela peut se produire si le curseur a été placé de manière incorrecte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Si le curseur n’est pas positionné dans une transaction, cela peut se produire si un autre thread supprime l’enregistrement de cette session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Peut être retourné si une precsize <strong>null</strong><em></em> a été passée.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

La taille de la clé accumulée dans le champ **cbOverhead** de [JET_RECSIZE](./jet-recsize-structure.md)est affectée par JET_bitRecordSizeInCopyBuffer. Si ce bit est spécifié, la taille de clé accumulée dans le champ **cbOverhead** est la taille de la clé complète. Si ce bit n’est pas utilisé, la taille cumulée de la clé n’inclut pas la taille enregistrée en raison de la compression de préfixe de clé.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_TABLEID](./jet-tableid.md)
