---
description: 'Indicateurs Sprite qui indiquent à l’API de dessin Sprite comment se comporter. Celles-ci sont passées dans ID3DX10Sprite :: Begin.'
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: Énumération D3DX10_SPRITE_FLAG (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 21ba4f035b43b1a002b014909fb4d0a02a64d1e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922795"
---
# <a name="d3dx10_sprite_flag-enumeration"></a>D3DX10 \_ , indicateur de sprite \_

Indicateurs Sprite qui indiquent à l’API de dessin Sprite comment se comporter. Celles-ci sont passées dans [**ID3DX10Sprite :: Begin**](id3dx10sprite-begin.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**\_Texture de tri d3dx10 Sprite \_ \_**
</dt> <dd>

Triez les sprites par texture avant le rendu, de sorte que lorsqu’il y a de nombreux sprites avec la même texture, tous les sprites sont rendus en même temps, ce qui améliore les performances.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10 le \_ \_ Tri \_ de profondeur \_ vers l' \_ \_ avant**
</dt> <dd>

Triez les sprites de l’arrière vers l’avant jusqu’à ce que les plus éloignés de l’appareil photo soient dessinés en premier.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10 \_ \_ \_ de tri profondeur \_ de tri \_ de l’avant vers l' \_ arrière**
</dt> <dd>

Triez les sprites de l’avant vers l’arrière afin que ceux qui se rapprochent de l’appareil photo soient dessinés en premier.

</dd> <dt>

<span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10 \_ Sprite \_ enregistrer l' \_ État**
</dt> <dd>

Enregistre l’état de sorte que lorsque [**ID3DX10Sprite :: end**](id3dx10sprite-end.md) est appelé, il restaure l’état de la manière dont il se trouvait avant l’appel de [**ID3DX10Sprite :: Begin**](id3dx10sprite-begin.md) .

</dd> <dt>

<span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10 \_ Sprite \_ ADDREF \_**
</dt> <dd>

Appelle AddRef sur toutes les textures quand elles sont passées dans [**ID3DX10Sprite ::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Une fois qu’un tri avant ou arrière est effectué, il effectue automatiquement un tri secondaire en suivant la texture. Cela s’avère utile lorsqu’il existe de nombreux sprites avec la même texture tous sur le même plan, par exemple lors du dessin de l’interface utilisateur dans un jeu.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




