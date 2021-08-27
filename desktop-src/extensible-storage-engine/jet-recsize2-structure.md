---
description: 'En savoir plus sur : structure JET_RECSIZE2'
title: Structure JET_RECSIZE2
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
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
ms.openlocfilehash: 0b99f5aa60f90a753a9c5d095e7a63417485b1fd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469836"
---
# <a name="jet_recsize2-structure"></a>Structure JET_RECSIZE2


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_recsize2-structure"></a>Structure JET_RECSIZE2

La structure **JET_RECSIZE2** est utilisée par [JetGetRecordSize2](./jetgetrecordsize2-function.md) pour retourner des informations sur les conditions d’utilisation d’un enregistrement dans l’espace de données utilisateur, le nombre de colonnes définies, le nombre de valeurs et l’espace de charge de la structure d’enregistrement ESE.

**Windows 7 :** la structure **JET_RECSIZE2** est introduite dans le système d’exploitation Windows 7.

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
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
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

**cCompressedColumns**

Nombre total de colonnes compressées.

**cbDataCompressed**

Taille compressée des données utilisateur dans cet enregistrement. C’est le même que cbData si aucune valeur long intrinsèque n’est compressée.

**cbLongValueDataCompressed**

Taille compressée des données utilisateur dans l’arborescence de valeurs longues. Cela est identique à celui des données cbLongValue si aucune valeur longue séparée n’est compressée.

### <a name="remarks"></a>Remarques

Le nombre total de valeurs dans l’enregistrement serait **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

Les données logiques de l’enregistrement sont (cbData + cbLongValueData) et la taille physique des données est (cbDataCompressed + cbLongValueDataCompressed). Cela peut être utilisé pour calculer le taux de compression des données stockées.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows système d’exploitation Vista.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite le système d’exploitation Windows Server 2008.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetGetRecordSize](./jetgetrecordsize-function.md)  
[JetGetRecordSize2](./jetgetrecordsize2-function.md)
