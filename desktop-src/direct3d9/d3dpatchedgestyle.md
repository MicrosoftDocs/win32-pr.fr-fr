---
description: Définit si le mode de pavage actuel est discret ou continu.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Énumération D3DPATCHEDGESTYLE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922636"
---
# <a name="d3dpatchedgestyle-enumeration"></a>Énumération D3DPATCHEDGESTYLE

Définit si le mode de pavage actuel est discret ou continu.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ discret**
</dt> <dd>

Style de contour discret. En mode discret, vous pouvez spécifier la facettisation float, mais elle sera tronquée en entiers.

</dd> <dt>

<span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ continu**
</dt> <dd>

Style de périphérie continue. En mode continu, la facettisation est spécifiée en tant que valeurs float qui peuvent être modifiées facilement pour réduire les artefacts « dépilés ».

</dd> <dt>

<span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Notez que le pavage continu produit un modèle de pavage complètement différent de celui de la même polygonalisation (ce qui est plus apparent en mode filaire). Ainsi, 4,0 Continuous n’est pas le même que 4 discret.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




