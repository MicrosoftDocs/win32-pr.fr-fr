---
description: Spécifie les octets qui sont chiffrés dans une surface vidéo protégée.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: Structure D3DENCRYPTED_BLOCK_INFO (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520301"
---
# <a name="d3dencrypted_block_info-structure"></a>\_Structure d' \_ informations sur les blocs D3DENCRYPTED

Spécifie les octets qui sont chiffrés dans une surface vidéo protégée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**NumEncryptedBytesAtBeginning**
</dt> <dd>

Nombre d’octets chiffrés au début de la mémoire tampon.

</dd> <dt>

**NumBytesInSkipPattern**
</dt> <dd>

Nombre d’octets ignorés après le premier **NumEncryptedBytesAtBeginning** octets, puis après chaque bloc de **NumBytesInEncryptPattern** octets. Les octets ignorés ne sont pas chiffrés.

</dd> <dt>

**NumBytesInEncryptPattern**
</dt> <dd>

Nombre d’octets qui sont chiffrés après chaque bloc d’octets ignorés.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>D3d9types. h (inclure d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures vidéo Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




