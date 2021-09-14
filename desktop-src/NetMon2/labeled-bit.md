---
description: La structure de bits ÉTIQUETÉe \_ définit une paire de bits d’étiquette.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: Structure de LABELED_BIT (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011529"
---
# <a name="labeled_bit-structure"></a>Structure de bits ÉTIQUETÉe \_

La structure de **\_ bits étiquetée** définit une paire de bits d’étiquette.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a>Membres

<dl> <dt>

**BitNumber**
</dt> <dd>

Numéro de BIT de la paire de bits d’étiquette. Les valeurs sont comprises entre 0 et 255. Affectez le BIT utilisé dans la comparaison de la valeur de la propriété au membre **Bitnumber** .

</dd> <dt>

**LabelOff**
</dt> <dd>

Chaîne ou étiquette qui s’affiche lorsque le BIT spécifié dans **BitNumber** est égal à zéro. Par exemple, une étiquette possible est « bit désactivé ».

</dd> <dt>

**LabelOn**
</dt> <dd>

Chaîne ou étiquette qui s’affiche lorsque le BIT spécifié dans **BitNumber** est égal à 1. Par exemple, une étiquette possible est « bit ON ».

</dd> </dl>

## <a name="remarks"></a>Notes

Un tableau de **structures \_ binaires étiquetées** est utilisé pour définir un ensemble de paires de bits d’étiquette. Un pointeur vers le tableau est spécifié dans le membre **lpLabeledBit** de la structure [Set](set.md) . Les paires sont utilisées lorsque vous souhaitez afficher une étiquette en fonction de la valeur de chaque BIT. En général, ce type de jeu est utilisé pour indiquer la valeur d’activation ou de désactivation de BITs.

Lorsqu’un jeu de bits est spécifié, Moniteur réseau affiche uniquement les BITs inclus dans le tableau de structures d' **ensemble** . Les BITs qui ne sont pas dans la structure **Set** ne sont pas affichés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




