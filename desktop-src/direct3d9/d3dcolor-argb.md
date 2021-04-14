---
description: Initialise une couleur avec les valeurs d’alpha, de rouge, de vert et de bleu fournies.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: Macro D3DCOLOR_ARGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322746"
---
# <a name="d3dcolor_argb-macro"></a>D3DCOLOR, \_ macro

Initialise une couleur avec les valeurs d’alpha, de rouge, de vert et de bleu fournies.

## <a name="syntax"></a>Syntaxe


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*un* 
</dt> <dd>

Composant alpha de la couleur. Cette valeur doit être comprise entre 0 et 255.

</dd> <dt>

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

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur [D3DCOLOR](d3dcolor.md) qui correspond aux valeurs ARVB fournies.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ RVBA**](d3dcolor-rgba.md)
</dt> <dt>

[**D3DCOLOR \_ XRGB**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




