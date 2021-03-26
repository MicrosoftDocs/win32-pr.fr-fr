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
ms.openlocfilehash: 3b0cd944b175522ab7d722ae791f3548c6633b71
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678050"
---
# <a name="getrendertargetsampleposition"></a>GetRenderTargetSamplePosition

Obtient la position d’échantillonnage (x, y) pour un exemple d’index donné.



|                                                                                  |
|----------------------------------------------------------------------------------|
| float<2> GetRenderTargetSamplePosition (dans int<1> index<br/>); |



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                       | Description                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Évaluer*<br/> | \[dans \] un exemple d’index de base zéro.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Position (x, y) de l’échantillon donné.

## <a name="remarks"></a>Notes

Utilisez cette fonction et [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) pour déterminer le nombre et la position des emplacements d’échantillonnage pour une cible de rendu.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                        | Prise en charge |
|---------------------------------------------------------------------|-----------|
| [Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | non        |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





