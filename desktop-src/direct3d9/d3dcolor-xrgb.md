---
description: Initialise une couleur avec les valeurs de rouge, vert et bleu fournies.
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: Macro D3DCOLOR_XRGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 4932e34979b0913f27874e57cfa881f18fb16364
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228210"
---
# <a name="d3dcolor_xrgb-macro"></a>D3DCOLOR \_ macro XRGB

Initialise une couleur avec les valeurs de rouge, vert et bleu fournies.

## <a name="syntax"></a>Syntaxe


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
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

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur [**D3DCOLOR**](d3dcolor.md) qui correspond aux valeurs RVB fournies.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ RVBA**](d3dcolor-rgba.md)
</dt> </dl>

 

 




