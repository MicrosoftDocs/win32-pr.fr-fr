---
title: FMA (Corecrt \_ Math. h)
description: Retourne l’addition fusionnée double précision de a \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- HLSL FMA
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b9a6932a1b0f0f8f1f7bc674920162def49e556c8d5b757547d4837caa60b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120203"
---
# <a name="fma"></a>fma

Retourne l’addition fusionnée double précision d’un \* b + c.



| *RET* FMA (double *a*, *b*, *c*); |
|----------------------------------|



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="a"></span><span id="A"></span>*un*
</dt> <dd>

\[dans \] la première valeur de l’addition fusionnée.

</dd> <dt>

<span id="b"></span><span id="B"></span>*p*
</dt> <dd>

\[dans \] la deuxième valeur de l’addition fusionnée.

</dd> <dt>

<span id="c"></span><span id="C"></span>*secteur*
</dt> <dd>

\[dans \] la troisième valeur de l’addition fusionnée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Addition fusionnée double précision des paramètres *a* \* *b*  +  *c*. La valeur retournée doit être précise à 0,5 unités de précision minimale (ULP).

## <a name="remarks"></a>Remarques

L’intrinsèque **FMA** doit prendre en charge les valeurs NaN, les fichiers INF et les dénormes.

Pour utiliser l’intrinsèque **FMA** dans votre code de nuanceur, appelez la méthode [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) avec les [**\_ options d3d11 Feature \_ d3d11 \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) pour vérifier que l’appareil Direct3D prend en charge l’option de fonctionnalité [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) . L’intrinsèque **FMA** requiert un pilote d’affichage WDDM 1,2, et tous les pilotes d’affichage WDDM 1,2 doivent prendre en charge **FMA**. Si votre application crée un appareil de rendu avec le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 ou 11,1 et que la cible de compilation est Shader Model 5 ou version ultérieure, le code source HLSL peut utiliser l’intrinsèque **FMA** .

### <a name="type-description"></a>Description du type



| Nom  | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *un*   | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**Cliquer**](/windows/desktop/WinProg/windows-data-types)                       | n'importe laquelle                          |
| *b*   | identique à l’entrée *a*                                                                                              | [**Cliquer**](/windows/desktop/WinProg/windows-data-types)                       | mêmes dimensions que l’entrée *a* |
| *c*   | identique à l’entrée *a*                                                                                              | [**Cliquer**](/windows/desktop/WinProg/windows-data-types)                       | mêmes dimensions que l’entrée *a* |
| *Av* | identique à l’entrée *a*                                                                                              | [**Cliquer**](/windows/desktop/WinProg/windows-data-types)                       | mêmes dimensions que l’entrée *a* |



 

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                | Pris en charge |
|-------------------------------------------------------------|-----------|
| [Shader Model 5 ou version ultérieure](d3d11-graphics-reference-sm5.md) | oui       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

