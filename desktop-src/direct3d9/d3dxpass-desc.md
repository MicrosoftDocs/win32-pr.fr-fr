---
description: Décrit une passe pour un objet Effect.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: Structure D3DXPASS_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 9666f0385c592adbc4378cbc693a5ce7a628092bbbb1695fd39527817c7ca04e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894049"
---
# <a name="d3dxpass_desc-structure"></a>D3DXPASS \_ desc, structure

Décrit une passe pour un objet Effect.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Valeur de chaîne utilisée pour la passe.

</dd> <dt>

**Annotations**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Les annotations sont des données spécifiques à l’utilisateur qui peuvent être attachées à n’importe quelle technique, passe ou paramètre. Consultez [Ajouter des informations pour appliquer des paramètres avec des \_ Annotations](using-an-effect.md).

</dd> <dt>

**pVertexShaderFunction**
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Pointeur désignant la fonction de nuanceur de sommets. Si un effet est créé avec [D3DXFX qui \_ ne peut pas être \_ cloné](d3dxfx.md), cette structure retourne un pointeur **null** lorsqu’il est appelé par [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).

</dd> <dt>

**pPixelShaderFunction**
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Pointeur vers la fonction de nuanceur de pixels. Si un effet est créé avec [D3DXFX qui \_ ne peut pas être \_ cloné](d3dxfx.md), cette structure retourne un pointeur **null** lorsqu’il est appelé par [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’effet](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
