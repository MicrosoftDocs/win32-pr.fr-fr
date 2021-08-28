---
title: Structure D3DX11_GROUP_DESC (D3dx11effect. h)
description: Décrit un groupe d’effets.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- Structure D3DX11_GROUP_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a189417b997647fd9c48a55010e96b32053c64031a03a8ac845e48c9a8e870a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096309"
---
# <a name="d3dx11_group_desc-structure"></a>\_Structure DESC du groupe D3DX11 \_

Décrit un groupe d’effets.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nom de ce groupe ( **null** uniquement si global).

</dd> <dt>

**Technologie**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de techniques contenues dans le groupe.

</dd> <dt>

**Annotations**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’annotations sur ce groupe.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le \_ groupe D3DX11 \_ desc est utilisé avec [**ID3DX11EffectTechnique :: GetDesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

