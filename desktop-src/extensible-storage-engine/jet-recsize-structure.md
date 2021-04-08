---
description: 'En savoir plus sur : structure JET_RECSIZE'
title: Structure JET_RECSIZE
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749853"
---
# <a name="jet_recsize-structure"></a>Structure JET_RECSIZE


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_recsize-structure"></a>Structure JET_RECSIZE

La structure **JET_RECSIZE** est utilisée par [JetGetRecordSize](./jetgetrecordsize-function.md) pour retourner des informations sur les conditions d’utilisation d’un enregistrement dans l’espace de données utilisateur, le nombre de colonnes définies, le nombre de valeurs et l’espace de charge de la structure d’enregistrement ESE.

**Windows Vista :** La structure **JET_RECSIZE** est introduite dans Windows Vista.

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
    } JET_RECSIZE;
```

### <a name="members"></a>Membres

**cbData**

Jeu de données utilisateur dans l’enregistrement.

**Remarque**  La taille de la clé n’est pas incluse dans ce.

**cbLongValueData**

Données utilisateur associées à l’enregistrement, mais stockées dans l’arborescence de valeurs longues.

**Remarque**  Cela ne compte pas les valeurs longues intrinsèques.

**cbOverhead**

Surcharge de la structure d’enregistrement ESE pour cet enregistrement. Cela comprend la taille de la clé de l’enregistrement.

**cbLongValueOverhead**

Charge des données de valeur longue.

**Remarque**  Cela ne compte pas les valeurs longues intrinsèques.

**cNonTaggedColumns**

Nombre total de colonnes fixes et variables définies dans cet enregistrement.

**cTaggedColumns**

Nombre total de colonnes avec balises définies dans cet enregistrement.

**cLongValues**

Nombre total de valeurs longues stockées dans l’arborescence de valeurs longues pour cet enregistrement.

**Remarque**  Cela ne compte pas les valeurs longues intrinsèques.

**cMultiValues**

Accumulation du nombre total de valeurs au-delà de la première pour toutes les colonnes de l’enregistrement.

### <a name="remarks"></a>Notes

Le nombre total de valeurs dans l’enregistrement serait **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

### <a name="requirements"></a>Configuration requise

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
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JetGetRecordSize](./jetgetrecordsize-function.md)
