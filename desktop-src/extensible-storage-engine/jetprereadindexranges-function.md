---
description: 'En savoir plus sur : fonction JetPrereadIndexRanges'
title: JetPrereadIndexRanges fonction)
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112047"
---
# <a name="jetprereadindexranges-function"></a>JetPrereadIndexRanges fonction)


_**S’applique à :** Windows | Serveur Windows_

La fonction **JetPrereadIndexRanges** prélit les index pour améliorer les performances.

La fonction **JetPrereadIndexRanges** a été introduite dans le système d’exploitation Windows 8.

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table avec laquelle émettre les prélectures.

*rgIndexRanges*

Plages de clés à prélire.

*cIndexRanges*

Nombre de plages de clés à prélire, déterminé par le nombre d’éléments dans *rgIndexRanges*.

*pcRangesPreread*

Nombre de plages de clés réellement prélues.

*rgcolumnidPreread*

Liste des ID de colonne pour les colonnes de valeur longue à prélire. Par défaut, seul l’enregistrement sur la page est prélecture. Si les colonnes de valeur longue page non paginée doivent être prélues, leurs ID de colonne doivent être transmis via ce paramètre.

*ccolumnidPreread*

Nombre d’ID de colonne pour les colonnes de valeurs longues à prélire, déterminé par le nombre d’éléments dans *rgcolumnidPreread*.

*grbit*

Groupe de bits qui spécifie zéro, une ou plusieurs des valeurs de direction de prélecture énumérées dans le tableau suivant.

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
<td><p>Transférer</p></td>
<td><p>Lecture anticipée.</p></td>
</tr>
<tr class="even">
<td><p>Vers l'arrière</p></td>
<td><p>Prélire en arrière.</p></td>
</tr>
<tr class="odd">
<td><p>FirstPageOnly</p></td>
<td><p>Prélire uniquement la première page d’une colonne longue.</p></td>
</tr>
<tr class="even">
<td><p>NormalizedKey</p></td>
<td><p>Clé/signet normalisé fourni à la place de la valeur de colonne.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur retournée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant. Pour plus d’informations sur les erreurs ESE (Extensible Storage Engine) possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

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
</tbody>
</table>


#### <a name="remarks"></a>Notes

Si les enregistrements avec les plages de clés spécifiées ne se trouvent pas dans le cache des tampons, vous devez démarrer des lectures asynchrones pour placer les enregistrements dans le cache des tampons de la base de données.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Requiert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2012.</p></td>
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
