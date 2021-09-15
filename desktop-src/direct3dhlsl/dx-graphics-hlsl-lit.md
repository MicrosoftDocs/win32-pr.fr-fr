---
title: orange
description: Retourne un vecteur de coefficient d’éclairage.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- en HLSL allumé
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523909"
---
# <a name="lit"></a>orange

Retourne un vecteur de coefficient d’éclairage.



| *RET* allumé (*n \_ point \_ l*, *n \_ point \_ h*, *m*) |
|------------------------------------------|



 

Cette fonction retourne un vecteur de coefficient d’éclairage (ambiant, diffuse, spéculaire, 1) où :

-   ambiant = 1
-   diffuse = n · l < 0 ? 0 : n · budget
-   spéculaire = n · l < 0 \| \| n · h < 0 ? 0 : (n · h) ^ m

Où le vecteur n est le vecteur normal, l est la direction de la lumière et h est le demi-vecteur.

## <a name="parameters"></a>Paramètres



| Élément                                                                       | Description                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ point \_ l*<br/> | \[dans \] le produit scalaire de la surface normalisée normale et le vecteur clair.<br/> |
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ points \_ h*<br/> | \[dans \] le produit scalaire du vecteur demi-angle et de la surface normal.<br/>       |
| <span id="m"></span><span id="M"></span>*lecteur*<br/>                     | \[dans \] un exposant spéculaire.<br/>                                                   |



 

## <a name="return-value"></a>Valeur renvoyée

Vecteur du coefficient d’éclairage.

## <a name="type-description"></a>Description du type



| Nom        | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *n \_ point \_ l* | [**Scala**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ points \_ h* | [**Scala**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**Scala**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *Av*       | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge           |
|------------------------------------------------------------------------------------|---------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | Oui                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Oui (vs \_ 1 \_ 1 uniquement) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

