---
title: rcp
description: Calcule une réciproque rapide, approximative et par composant.
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- RCP HLSL
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb66fd2edf543dfb8beaf23dd2105925d15d169ee1b134019fb54da8fdf889e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672219"
---
# <a name="rcp"></a>rcp

Calcule une réciproque rapide, approximative et par composant.



| *RET* RCP (*x*) |
|----------------|



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

\[dans \] la valeur d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Réciproque du paramètre *x* .

## <a name="type-description"></a>Description du type



| Name  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md)                      | Taille                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types) ou [ **double**](/windows/desktop/WinProg/windows-data-types) | n'importe laquelle                            |
| *Av* | identique à l’entrée *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types) ou [ **double**](/windows/desktop/WinProg/windows-data-types) | la ou les mêmes dimensions comme entrée *x* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 