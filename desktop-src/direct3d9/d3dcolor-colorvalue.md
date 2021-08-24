---
description: Initialise une couleur avec les valeurs à virgule flottante rouge, vert, bleu et alpha fournies.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: Macro D3DCOLOR_COLORVALUE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f4ee10003e0f4fdeae937d8ac786b4d389a91ec0326c2d6288d10af2a63e2286
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751229"
---
# <a name="d3dcolor_colorvalue-macro"></a>D3DCOLOR \_ macro COLORVALUE

Initialise une couleur avec les valeurs à virgule flottante rouge, vert, bleu et alpha fournies.

## <a name="syntax"></a>Syntaxe


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*r* 
</dt> <dd>

Composant rouge de la couleur. Cette valeur doit être une valeur à virgule flottante comprise entre 0,0 et 1,0.

</dd> <dt>

*activée* 
</dt> <dd>

Composant vert de la couleur. Cette valeur doit être une valeur à virgule flottante comprise entre 0,0 et 1,0.

</dd> <dt>

*b* 
</dt> <dd>

Composant bleu de la couleur. Cette valeur doit être une valeur à virgule flottante comprise entre 0,0 et 1,0.

</dd> <dt>

*un* 
</dt> <dd>

Composant alpha de la couleur. Cette valeur doit être une valeur à virgule flottante comprise entre 0,0 et 1,0.

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
</dt> </dl>

 

 




