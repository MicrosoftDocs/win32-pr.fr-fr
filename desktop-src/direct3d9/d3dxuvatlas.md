---
description: Définit des options pour effectuer des calculs de distance géodésique, lors de l’ajustement d’une texture à une surface incurvée. Utilisez cet indicateur pour choisir entre la haute qualité et les calculs rapides lors du calcul d’un Atlas de textures.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Énumération D3DXUVATLAS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 1edcf2b1cbe2363f805bee1f5eb67f5558702ea9e163a865e1a6c51d6f5ed6ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523835"
---
# <a name="d3dxuvatlas-enumeration"></a>Énumération D3DXUVATLAS

Définit des options pour effectuer des calculs de distance géodésique, lors de l’ajustement d’une texture à une surface incurvée. Utilisez cet indicateur pour choisir entre la haute qualité et les calculs rapides lors du calcul d’un Atlas de textures.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS \_ par défaut**
</dt> <dd>

Les mailles avec plus de 25 000 visages auront la méthode de distance geodasic rapide appliquée, tandis que la méthode de distance géodésique de qualité supérieure sera appliquée aux mailles avec moins de 25 000 visages.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**\_Fast géodésique \_ D3DXUVATLAS**
</dt> <dd>

Utilise des approximations pour améliorer la vitesse de représentation graphique au détriment d’une augmentation ou de plusieurs graphiques en sortie de la maille.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**Qualité de la \_ géodésique D3DXUVATLAS \_**
</dt> <dd>

Fournit de meilleurs graphiques de qualité, mais nécessite plus de temps et de mémoire que rapide.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




