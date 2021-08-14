---
title: GetRenderTargetSamplePosition
description: Obtient la position d’échantillonnage (x, y) pour un exemple d’index donné.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- HLSL GetRenderTargetSamplePosition
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a406fcbd023d0688baf51cabbfea53438f3d58a6fba4d1fc7d1bf8d33077262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514333"
---
# <a name="getrendertargetsampleposition"></a>GetRenderTargetSamplePosition

Obtient la position d’échantillonnage (x, y) pour un exemple d’index donné.

float<2> GetRenderTargetSamplePosition (dans int<1> index<br/>);



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                       | Description                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Évaluer*<br/> | \[dans \] un exemple d’index de base zéro.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Position (x, y) de l’échantillon donné.

## <a name="remarks"></a>Remarques

Utilisez cette fonction et [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) pour déterminer le nombre et la position des emplacements d’échantillonnage pour une cible de rendu.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                        | Pris en charge |
|---------------------------------------------------------------------|-----------|
| [Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs | oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | non        |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





