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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523225"
---
# <a name="d3dx10_sprite_flag-enumeration"></a><span data-ttu-id="b488a-104">D3DX10 \_ , indicateur de sprite \_</span><span class="sxs-lookup"><span data-stu-id="b488a-104">D3DX10\_SPRITE\_FLAG enumeration</span></span>

<span data-ttu-id="b488a-105">Indicateurs Sprite qui indiquent à l’API de dessin Sprite comment se comporter.</span><span class="sxs-lookup"><span data-stu-id="b488a-105">Sprite flags that tell the sprite drawing API how to behave.</span></span> <span data-ttu-id="b488a-106">Celles-ci sont passées dans [**ID3DX10Sprite :: Begin**](id3dx10sprite-begin.md).</span><span class="sxs-lookup"><span data-stu-id="b488a-106">These are passed into [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b488a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b488a-107">Syntax</span></span>


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a><span data-ttu-id="b488a-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="b488a-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b488a-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**\_Texture de tri d3dx10 Sprite \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b488a-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3DX10\_SPRITE\_SORT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="b488a-110">Triez les sprites par texture avant le rendu, de sorte que lorsqu’il y a de nombreux sprites avec la même texture, tous les sprites sont rendus en même temps, ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="b488a-110">Sort the sprites by texture before rendering so that when there are many sprites with the same texture that texture all of those sprites will be rendered at the same time, thereby improving performance.</span></span>

</dd> <dt>

<span data-ttu-id="b488a-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10 le \_ \_ Tri \_ de profondeur \_ vers l' \_ \_ avant**</span><span class="sxs-lookup"><span data-stu-id="b488a-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_BACK\_TO\_FRONT**</span></span>
</dt> <dd>

<span data-ttu-id="b488a-112">Triez les sprites de l’arrière vers l’avant jusqu’à ce que les plus éloignés de l’appareil photo soient dessinés en premier.</span><span class="sxs-lookup"><span data-stu-id="b488a-112">Sort the sprites from back to front to that those farther away from the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="b488a-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10 \_ \_ \_ de tri profondeur \_ de tri \_ de l’avant vers l' \_ arrière**</span><span class="sxs-lookup"><span data-stu-id="b488a-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_FRONT\_TO\_BACK**</span></span>
</dt> <dd>

<span data-ttu-id="b488a-114">Triez les sprites de l’avant vers l’arrière afin que ceux qui se rapprochent de l’appareil photo soient dessinés en premier.</span><span class="sxs-lookup"><span data-stu-id="b488a-114">Sort the sprites from front to back so that those closer to the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="b488a-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10 \_ Sprite \_ enregistrer l' \_ État**</span><span class="sxs-lookup"><span data-stu-id="b488a-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10\_SPRITE\_SAVE\_STATE**</span></span>
</dt> <dd>

<span data-ttu-id="b488a-116">Enregistre l’état de sorte que lorsque [**ID3DX10Sprite :: end**](id3dx10sprite-end.md) est appelé, il restaure l’état de la manière dont il se trouvait avant l’appel de [**ID3DX10Sprite :: Begin**](id3dx10sprite-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="b488a-116">Saves the state so that when [**ID3DX10Sprite::End**](id3dx10sprite-end.md) is called, it will restore the state to the way it was before [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) was called.</span></span>

</dd> <dt>

<span data-ttu-id="b488a-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10 \_ Sprite \_ ADDREF \_**</span><span class="sxs-lookup"><span data-stu-id="b488a-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10\_SPRITE\_ADDREF\_TEXTURES**</span></span>
</dt> <dd>

<span data-ttu-id="b488a-118">Appelle AddRef sur toutes les textures quand elles sont passées dans [**ID3DX10Sprite ::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md).</span><span class="sxs-lookup"><span data-stu-id="b488a-118">Calls AddRef on all of the textures when they are passed into [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b488a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b488a-119">Remarks</span></span>

<span data-ttu-id="b488a-120">Une fois qu’un tri avant ou arrière est effectué, il effectue automatiquement un tri secondaire en suivant la texture.</span><span class="sxs-lookup"><span data-stu-id="b488a-120">After a front-to-back or back-to-front sort is done, it will automatically do a secondary sort by texture.</span></span> <span data-ttu-id="b488a-121">Cela s’avère utile lorsqu’il existe de nombreux sprites avec la même texture tous sur le même plan, par exemple lors du dessin de l’interface utilisateur dans un jeu.</span><span class="sxs-lookup"><span data-stu-id="b488a-121">This is helpful for when there are many sprites with the same texture all on the same plane, such as when drawing the user interface in a game.</span></span>

## <a name="requirements"></a><span data-ttu-id="b488a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b488a-122">Requirements</span></span>



| <span data-ttu-id="b488a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b488a-123">Requirement</span></span> | <span data-ttu-id="b488a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b488a-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b488a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b488a-125">Header</span></span><br/> | <dl> <span data-ttu-id="b488a-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b488a-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b488a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b488a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b488a-128">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="b488a-128">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




