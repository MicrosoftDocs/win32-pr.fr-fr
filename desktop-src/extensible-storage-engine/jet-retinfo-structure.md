---
description: 'En savoir plus sur : structure JET_RETINFO'
title: Structure JET_RETINFO
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: 3ddf6f7b2ef129ab620a61616d975c8b8470022e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470785"
---
# <a name="jet_retinfo-structure"></a>Structure JET_RETINFO


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_retinfo-structure"></a>Structure JET_RETINFO

La structure **JET_RETINFO** contient des paramètres d’entrée et de sortie facultatifs pour [JetRetrieveColumn](./jetretrievecolumn-function.md). Un pointeur NULL peut être passé là où un pointeur vers cette structure serait autrement passé. Le fait de passer un pointeur null est le même que si vous passez **JET_RETINFO** avec **cbStruct** défini sur sizeof (JET_RETINFO), **ibLongValue** défini sur 0 (zéro) et **itagSequence** défini sur 1.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a>Membres

**cbStruct**

Doit être défini sur la taille de la structure **JET_RETINFO** , en octets, et sert à confirmer la présence des champs suivants.

**ibLongValue**

Offset au premier octet à récupérer d’une colonne de type [JET_coltypLongBinary](./jet-coltyp.md)ou [JET_coltypLongText](./jet-coltyp.md). Notez que la quantité de données récupérées à partir de ce décalage est inférieure à la taille de la mémoire tampon de sortie et à la taille des données dans la valeur réelle après cet offset.

**itagSequence**

Décrit le numéro de séquence de la valeur dans une colonne à valeurs multiples. Notez que le tableau de valeurs est de base un. La première valeur est séquence 1, et non 0. Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé en tant que **itagSequence**

Avec une colonne qui peut contenir plusieurs valeurs, il est possible d’utiliser un numéro de séquence supérieur à 1 dans [JetSetColumn](./jetsetcolumn-function.md) et [JetRetrieveColumn](./jetretrievecolumn-function.md) ou 0 dans [JetSetColumn](./jetsetcolumn-function.md). Dans l’implémentation actuelle du moteur, toute colonne créée avec JET_bitColumnTagged peut contenir plusieurs valeurs. Les colonnes créées avec JET_bitColumnMultiValued différent des colonnes avec balises à valeurs multiples uniquement dans la manière dont elles sont indexées. Pour plus d’informations, consultez [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

**columnidNextTagged**

Retourne la valeur columnID de la colonne balisée, à valeurs multiples ou fragmentées récupérées lorsque toutes les colonnes avec balises sont récupérées en passant 0 comme ColumnID à [JetRetrieveColumn](./jetretrievecolumn-function.md).

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_RETINFO]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)
