---
title: D3DCOLORtoUBYTE4
description: Convertit un vecteur 4D à virgule flottante défini par un D3DCOLOR en UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- HLSL D3DCOLORtoUBYTE4
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854932"
---
# <a name="d3dcolortoubyte4"></a>D3DCOLORtoUBYTE4

Convertit un vecteur 4D à virgule flottante défini par un D3DCOLOR en UBYTE4.



| *RET* D3DCOLORtoUBYTE4 (*x*) |
|-----------------------------|



 

Cette fonction Swizzles et met à l’échelle les composants du paramètre *x* . Utilisez cette fonction pour compenser l’absence de prise en charge de UBYTE4 dans un matériel.

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] le Vector4 à virgule flottante à convertir.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Représentation UBYTE4 du paramètre *x* .

## <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| *Av* | [**graphiques**](dx-graphics-hlsl-intrinsic-functions.md) | [**entière**](/windows/desktop/WinProg/windows-data-types)                      | 4    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge |
|------------------------------------------------------------------------------------|-----------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | Oui       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

