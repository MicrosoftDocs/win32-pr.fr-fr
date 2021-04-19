---
description: 'En savoir plus sur : fonction JetDeleteColumn2'
title: JetDeleteColumn2 fonction)
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35e19eb7ac7b133bb690b268426fec9822efefea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522467"
---
# <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2 fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2 fonction)

La fonction **JetDeleteColumn2** supprime une colonne d’une table de base de données ESE et permet de définir une option *Grbit* .

**Windows XP : JetDeleteColumn2** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table qui contient la colonne à supprimer.

*szColumnName*

Nom de la colonne à supprimer.

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
<td><p>JET_bitDeleteColumnIgnoreTemplateColumns</p></td>
<td><p>La définition de JET_bitDeleteColumIgnoreTemplateColumns oblige l’API à tenter uniquement de supprimer des colonnes dans la table dérivée. Si une colonne de ce nom existe dans la table de base, elle sera ignorée.</p></td>
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

L’appel de [JetDeleteColumn](./jetdeletecolumn-function.md) est identique à l’appel de **JetDeleteColumn2** avec *Grbit* défini sur zéro (0).

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
<td><p>Implémenté en tant que <strong>JetDeleteColumn2W</strong> (Unicode) et <strong>JetDeleteColumn2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)
