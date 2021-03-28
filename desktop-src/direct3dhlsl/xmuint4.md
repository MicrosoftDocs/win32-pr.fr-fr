---
title: XMUINT4, structure
description: Décrit un vecteur d’entier non signé 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4 structure HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0b02ffe64e7b4c4479723b4e36abd87f6bd03b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974442"
---
# <a name="xmuint4-structure"></a>XMUINT4, structure

Décrit un vecteur d’entier non signé 4D.

## <a name="syntax"></a>Syntaxe


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a>Membres

<dl> <dt>

**x**
</dt> <dd>

composant x du vecteur.

</dd> <dt>

**y**
</dt> <dd>

composant y du vecteur.

<dl> <dt>

**Lettre**
</dt> <dd>

composant z du vecteur.

<dl> <dt>

**w**
</dt> <dd>

composant w du vecteur.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures](format-conversion-structures.md)
</dt> <dt>

[Décompresser et compresser le \_ format DXGI pour la modification des images In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





