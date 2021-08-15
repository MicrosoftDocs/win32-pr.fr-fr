---
description: Décrit une table de Huffmans de la table de contrôle d’images JPEG.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: Structure DXGI_JPEG_DC_HUFFMAN_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b431bbccb66bcb24e068229493ef87f2ac96736161bb306609ac4dd479dfb7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987119"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a>\_Structure de \_ \_ table Huffman \_ dxgi JPEG DC

Décrit une table de Huffmans de la table de contrôle d’images JPEG.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
```



## <a name="members"></a>Membres

<dl> <dt>

**CodeCounts**
</dt> <dd>

Nombre de codes pour chaque longueur de code.

</dd> <dt>

**CodeValues**
</dt> <dd>

Valeurs de code Huffman, par ordre de croissance de la longueur de code.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




