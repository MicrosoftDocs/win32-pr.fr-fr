---
description: Initialise une couleur avec les valeurs (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: Macro D3DCOLOR_XYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: caa6bc1eb9586c1526a7af674040fd703ff0a75a5055ce42e13378206e82c879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300323"
---
# <a name="d3dcolor_xyuv-macro"></a>D3DCOLOR \_ macro XYUV

Initialise une couleur avec les valeurs (y, u, v).

## <a name="syntax"></a>Syntaxe


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

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

## <a name="return-value"></a>Valeur renvoyée

Retourne la valeur [**D3DCOLOR**](d3dcolor.md) qui correspond aux valeurs fournies (y, u, v).

## <a name="remarks"></a>Notes

Une couleur RVB peut être réduite à 16 bits par pixel par conversion en luminance et les différences de couleur avec les équations suivantes :


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



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

[**D3DCOLOR \_ AYUV**](d3dcolor-ayuv.md)
</dt> </dl>

 

 




