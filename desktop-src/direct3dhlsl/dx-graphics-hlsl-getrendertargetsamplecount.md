---
title: GetRenderTargetSampleCount
description: Obtient le nombre d’échantillons pour une cible de rendu.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- HLSL GetRenderTargetSampleCount
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54414d7af326c1a069585f9d5deaa3e728d421a65490c5b9f5322b98e06f531e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120133"
---
# <a name="getrendertargetsamplecount"></a>GetRenderTargetSampleCount

Obtient le nombre d’échantillons pour une cible de rendu.



| *Uint* GetRenderTargetSampleCount() |
|-------------------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                 | Description |
|--------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>None<br/> |             |



 

## <a name="return-value"></a>Valeur renvoyée

Nombre d’échantillons.

## <a name="remarks"></a>Remarques

Utilisez cette fonction et [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) pour déterminer le nombre et la position des emplacements d’échantillonnage pour une cible de rendu.

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

 

 





