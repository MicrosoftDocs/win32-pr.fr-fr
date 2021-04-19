---
description: Initialise une couleur avec les valeurs de rouge, vert, bleu et alpha fournies.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: Macro D3DCOLOR_RGBA (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523814"
---
# <a name="d3dcolor_rgba-macro"></a>D3DCOLOR, \_ macro

Initialise une couleur avec les valeurs de rouge, vert, bleu et alpha fournies.

## <a name="syntax"></a>Syntaxe


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*r* 
</dt> <dd>

Composant rouge de la couleur. Cette valeur doit être comprise entre 0 et 255.

</dd> <dt>

*activée* 
</dt> <dd>

Composant vert de la couleur. Cette valeur doit être comprise entre 0 et 255.

</dd> <dt>

*b* 
</dt> <dd>

Composant bleu de la couleur. Cette valeur doit être comprise entre 0 et 255.

</dd> <dt>

*un* 
</dt> <dd>

Composant alpha de la couleur. Cette valeur doit être comprise entre 0 et 255.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur [**D3DCOLOR**](d3dcolor.md) qui correspond aux valeurs RVBA fournies.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ XRGB**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




