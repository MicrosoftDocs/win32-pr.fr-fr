---
description: Décrit une table de quantification JPEG.
ms.assetid: DE1AAB15-B0B8-4594-BBCE-5F8EE5CE0AF7
title: Structure DXGI_JPEG_QUANTIZATION_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_QUANTIZATION_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b0a097cb4c364ecc14e471f7c15f642aa65e912
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535805"
---
# <a name="dxgi_jpeg_quantization_table-structure"></a>\_Structure de \_ table de quantification dxgi JPEG \_

Décrit une table de quantification JPEG.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DXGI_JPEG_QUANTIZATION_TABLE {
  BYTE Elements[64];
} DXGI_JPEG_QUANTIZATION_TABLE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Éléments**
</dt> <dd>

Tableau d’octets contenant les éléments de la table de quantification.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




