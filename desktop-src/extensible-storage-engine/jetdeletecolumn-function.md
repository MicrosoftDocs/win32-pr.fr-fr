---
description: 'En savoir plus sur : fonction JetDeleteColumn'
title: JetDeleteColumn fonction)
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7d577447942e36cd49763727473d3f6ddc659b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103954025"
---
# <a name="jetdeletecolumn-function"></a>JetDeleteColumn fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetdeletecolumn-function"></a>JetDeleteColumn fonction)

La fonction **JetDeleteColumn** supprime une colonne d’une table de base de données ESE.

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table à partir de laquelle la colonne doit être supprimée.

*szColumnName*

Nom de la colonne à supprimer.

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
<td><p>JET_errColumnInUse</p></td>
<td><p>La colonne est en cours d’utilisation. Il est peut-être actuellement utilisé par un index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedDDL</p></td>
<td><p>Une tentative de modification du DDL fixe a été effectuée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedInheritedDDL</p></td>
<td><p>La colonne nommée dans <em>szColumnName</em> existe dans la table de modèle, et la DDL d’une table de modèle ne peut pas être modifiée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Cela peut être retourné si un nom incorrect pour <em>szColumnName</em> a été donné.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>La table n’est pas accessible en écriture. Cela peut être retourné si la base de données a été ouverte en mode lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La transaction est une transaction en lecture seule.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

L’appel de **JetDeleteColumn** est identique à l’appel de [JetDeleteColumn2](./jetdeletecolumn2-function.md) avec *Grbit* défini sur zéro (0).

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
<td><p>Implémenté en tant que <strong>JetDeleteColumnW</strong> (Unicode) et <strong>JetDeleteColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
