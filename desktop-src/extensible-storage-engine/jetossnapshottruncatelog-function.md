---
description: 'En savoir plus sur : fonction JetOSSnapshotTruncateLog'
title: JetOSSnapshotTruncateLog fonction)
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520098"
---
# <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog fonction)

La fonction **JetOSSnapshotTruncateLog** active la troncation du journal pour toutes les instances qui font partie de la session d’instantané.

**Windows Vista :**  **JetOSSnapshotTruncateLog** est introduit dans Windows Vista.

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*snapId*

Identificateur de la session d’instantané.

*grbit*

Options pour cet appel. Ce paramètre peut avoir une combinaison des valeurs suivantes.

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
<td><p>JET_bitAllDatabasesSnapshot</p></td>
<td><p>Toutes les bases de données sont attachées afin que le moteur de stockage puisse calculer et effectuer la troncation du journal.</p></td>
</tr>
<tr class="even">
<td><p>0 (zéro)</p></td>
<td><p>Aucune troncation ne se produit.</p></td>
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
<td><p>Le paramètre <em>Grbit</em> n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>La session d’instantané n’est pas dans l’État dans lequel une troncation peut se produire. Les causes possibles sont :</p>
<ul>
<li><p>l’appel est effectué après le délai d’expiration de la session d’instantané</p></li>
<li><p>la session a été spécifiée en tant qu’instantané de copie</p></li>
</ul></td>
</tr>
</tbody>
</table>


En cas de réussite, les fichiers journaux pour une partie ou l’ensemble des instances de la session d’instantané seront tronqués, si possible.

#### <a name="remarks"></a>Notes

Cette fonction doit être appelée uniquement si l’instantané a été créé avec l’option JET_bitContinueAfterThaw. Dans le cas contraire, la session d’instantané se terminera après l’appel de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) .

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

[Paramètres de gestion des erreurs](./error-handling-parameters.md)  
[Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
