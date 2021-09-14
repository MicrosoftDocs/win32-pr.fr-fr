---
description: Initialise une couleur à l’aide des valeurs (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: Macro D3DCOLOR_AYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095317"
---
# <a name="d3dcolor_ayuv-macro"></a>D3DCOLOR \_ macro AYUV

Initialise une couleur à l’aide des valeurs (a, y, u, v).

## <a name="syntax"></a>Syntaxe


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*un* 
</dt> <dd>

Composant alpha de la couleur. Cette valeur doit être comprise entre 0 et 255.

</dd> <dt>

*y* 
</dt> <dd>

Composant luminance de la couleur. Cette valeur doit être comprise entre 0 et 255.

</dd> <dt>

*u* 
</dt> <dd>

Luminosité bleue de la couleur. Cette valeur doit être comprise entre 0 et 255.

</dd> <dt>

*v* 
</dt> <dd>

Luminosité rouge de la couleur. Cette valeur doit être comprise entre 0 et 255.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur [D3DCOLOR](d3dcolor.md) qui correspond aux valeurs ARVB fournies.

## <a name="remarks"></a>Notes

Une couleur RVB peut être réduite à 16 bits par pixel par conversion en luminance et les différences de couleur avec les équations suivantes :


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



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

[**D3DCOLOR \_ XYUV**](d3dcolor-xyuv.md)
</dt> </dl>

 

 




