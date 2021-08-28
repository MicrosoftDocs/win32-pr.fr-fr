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
ms.openlocfilehash: a7ea4520a75e83c77a6403a583e9131a15df337b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988226"
---
# <a name="jet_recsize-structure"></a>Structure JET_RECSIZE


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_recsize-structure"></a>Structure JET_RECSIZE

La structure **JET_RECSIZE** est utilisée par [JetGetRecordSize](./jetgetrecordsize-function.md) pour retourner des informations sur les conditions d’utilisation d’un enregistrement dans l’espace de données utilisateur, le nombre de colonnes définies, le nombre de valeurs et l’espace de charge de la structure d’enregistrement ESE.

**Windows Vista :** la structure **JET_RECSIZE** est introduite dans Windows Vista.

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

### <a name="remarks"></a>Remarques

Le nombre total de valeurs dans l’enregistrement serait **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetGetRecordSize](./jetgetrecordsize-function.md)
