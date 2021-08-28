---
description: 'En savoir plus sur : structure JET_SETINFO'
title: Structure JET_SETINFO
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4198598a95134291e9b9aa88eb9dcdf4ada79045
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983812"
---
# <a name="jet_setinfo-structure"></a>Structure JET_SETINFO


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_setinfo-structure"></a>Structure JET_SETINFO

La structure **JET_SETINFO** contient des paramètres d’entrée facultatifs pour [JetSetColumn](./jetsetcolumn-function.md). Un pointeur **null** peut être passé là où un pointeur vers cette structure serait autrement passé. La signification de la transmission d’une **valeur null** est la même que le passage de **JET_SETINFO** avec **cbStruct** défini sur sizeof (JET_SETINFO), **ibLongValue** défini sur 0 (zéro) et **itagSequence** défini sur 1.

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a>Membres

**cbStruct**

Taille, en octets, de la **JET_SETINFO**. Cette valeur confirme la présence des champs suivants.

**ibLongValue**

Offset au premier octet à définir dans une colonne de type [JET_coltypLongBinary](./jet-coltyp.md) ou [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Décrit le numéro de séquence de la valeur dans une colonne à valeurs multiples à définir. Le tableau de valeurs est de base un. La première valeur est Sequence 1, et non 0 (zéro). Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé comme **itagSequence** si cette valeur est remplacée. La valeur 0 (zéro) signifie que vous pouvez ajouter une nouvelle instance de valeur de colonne à la fin de la séquence de valeurs de colonne.

Avec une colonne qui peut contenir plusieurs valeurs, il est possible d’utiliser un numéro de séquence supérieur à 1 dans [JetSetColumn](./jetsetcolumn-function.md) et [JetRetrieveColumn](./jetretrievecolumn-function.md) ou 0 dans [JetSetColumn](./jetsetcolumn-function.md). Dans l’implémentation actuelle du moteur, toute colonne créée avec JET_bitColumnTagged peut contenir plusieurs valeurs. Les colonnes créées avec JET_bitColumnMultiValued différent des colonnes avec balises à valeurs multiples uniquement dans la manière dont elles sont indexées. Pour plus d’informations, consultez [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetSetColumn](./jetsetcolumn-function.md)
