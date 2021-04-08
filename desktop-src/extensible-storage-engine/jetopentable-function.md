---
description: 'En savoir plus sur : fonction JetOpenTable'
title: Fonction JetOpenTable
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749708"
---
# <a name="jetopentable-function"></a>Fonction JetOpenTable


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetopentable-function"></a>Fonction JetOpenTable

La fonction **JetOpenTable** ouvre un curseur sur une table créée précédemment.

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser.

*dbid*

Identificateur de base de données à utiliser pour rechercher la table.

*szTableName*

Nom de la table à ouvrir.

*pvParameters*

Action déconseillée. Affectez la valeur **null**.

*cbParameters*

Action déconseillée. Défini sur 0 (zéro).

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.

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
<td><p>JET_bitTableDenyRead</p></td>
<td><p>La table ne peut pas être ouverte pour un accès en lecture par une autre session de base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableDenyWrite</p></td>
<td><p>La table ne peut pas être ouverte pour un accès en écriture par une autre session de base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableNoCache</p></td>
<td><p>Ne mettez pas en cache les pages pour cette table.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTablePermitDDL</p></td>
<td><p>Autorise la modification DDL sur les tables marquées comme FixedDDL. Cette option doit être utilisée avec l’option JET_bitTableDenyRead.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTablePreread</p></td>
<td><p>Indique que la table n’est probablement pas dans le cache des tampons, et que la prélecture peut être bénéfique pour les performances.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableReadOnly</p></td>
<td><p>Demande l’accès en lecture seule à la table.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableSequential</p></td>
<td><p>La table doit être préextraite très agressivement du disque, car l’application l’analyse de manière séquentielle.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableUpdatable</p></td>
<td><p>Demande l’accès en écriture à la table.</p></td>
</tr>
</tbody>
</table>


*pTableID*

En cas de réussite, pointe vers l’identificateur de la table. En cas d’échec, le contenu de *pTableID* n’est pas défini.

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
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p><em>dbid</em> n’est pas un identificateur de base de données valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Une combinaison incorrecte de <em>Grbit</em> a été transmise.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Le nom donné dans <em>szTableName</em> n’est pas valide.</p>
<p>Pour plus d’informations sur les noms de table valides, consultez le paramètre <em>szTableName</em> dans <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Une tentative d’ouverture d’une table qui n’existe pas dans la base de données a été effectuée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour ouvrir un nouveau curseur. Consultez la section Notes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableInUse</p></td>
<td><p>La table est utilisée par une autre opération de base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>AVERTISSEMENT récupérable indiquant que la table est en cours d’utilisation par le système.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>La table est verrouillée par une autre opération de base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Tentative d’ouverture d’un trop grand nombre de tables uniques à la fois. Consultez la section Notes.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

Les tables ouvertes avec **JetOpenTable** doivent généralement être fermées avec [JetCloseTable](./jetclosetable-function.md). L’exception à cette règle se produit lorsque **JetOpenTable** est appelé dans une transaction et que la transaction est restaurée (avec [JetRollback](./jetrollback-function.md)). Lors de la restauration d’une transaction, la table est fermée automatiquement. Dans ce cas, il s’agit d’une erreur de fermeture de la table avec [JetCloseTable](./jetclosetable-function.md).

Il est légal d’ouvrir des tables système avec **JetOpenTable** (par exemple, MSysObjects, MSysUnicodeFixup). Le schéma des tables système peut changer. par conséquent, l’accès aux tables système est déconseillé. Le nombre de tables uniques qui peuvent être ouvertes simultanément est directement affecté par *JET_paramMaxOpenTables*. Si la table est actuellement ouverte, un nouveau curseur sera créé sur la table. Les ressources de curseur sont configurées à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec *JET_paramMaxCursors*. Voir aussi [JetDupCursor](./jetdupcursor-function.md).

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté en tant que <strong>JetOpenTableW</strong> (Unicode) et <strong>JetOpenTableA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres de ressource](./resource-parameters.md)
