---
description: Décrit une table de Huffmans de l’AC JPEG.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: Structure DXGI_JPEG_AC_HUFFMAN_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 21e279e4974d221a6feba6f135343d122f30f3da1edb18210e0e14f92fdb94a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518372"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a>\_Structure de \_ \_ table Huffman \_ dxgi JPEG AC

Décrit une table de Huffmans de l’AC JPEG.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
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

 

 




