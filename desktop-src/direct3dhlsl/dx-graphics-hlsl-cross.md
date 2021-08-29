---
title: cross
description: Retourne le produit croisé de deux vecteurs 3D à virgule flottante.
ms.assetid: 5f1832af-6bc5-49a7-956a-fd762f674f5f
keywords:
- HLSL croisé
topic_type:
- apiref
api_name:
- cross
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 117a679209b64b7e63741bb83bbbbf9bda2f5c00c96f9197e0d734a547d490bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068299"
---
# <a name="cross"></a>cross

Retourne le produit croisé de deux vecteurs 3D à virgule flottante.



| *RET* inter (*x*, *y*) |
|-----------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] le premier vecteur 3D à virgule flottante.<br/>  |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[dans \] le deuxième vecteur 3D à virgule flottante.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Produit croisé du paramètre *x* et du paramètre *y* .

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| *y*   | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| *Av* | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 3    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Pris en charge             |
|------------------------------------------------------------------------------------|-----------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | oui                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 et PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

