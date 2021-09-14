---
description: La \_ structure d’octets étiquetée définit une paire de bits étiquetée. L’étiquette de la paire de bits étiquetée s’affiche lorsqu’une valeur de propriété d’octet spécifique est détectée.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: Structure de LABELED_BYTE (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011526"
---
# <a name="labeled_byte-structure"></a>Structure d’octets ÉTIQUETÉe \_

La structure d' **\_ octets étiquetée** définit une paire de bits étiquetée. L' **étiquette** de la paire de bits étiquetée s’affiche lorsqu’une valeur de propriété d’octet spécifique est détectée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Valeur**
</dt> <dd>

Valeur d’octet de la propriété que vous souhaitez détecter.

</dd> <dt>

**Étiquette**
</dt> <dd>

Description textuelle ou étiquette qui s’affiche lorsque la valeur spécifiée dans le membre de **valeur** est détectée.

</dd> </dl>

## <a name="remarks"></a>Notes

Le membre **lpLabeledByteTable** de la structure [Set](set.md) pointe vers un tableau de structures d' **ensemble** qui définissent un ou plusieurs membres **étiquette** des paires valeur octet. Ces paires sont utilisées lorsque vous souhaitez afficher une étiquette à la place d’une valeur d’octet spécifique trouvée dans le paquet de protocole.

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

 

 




