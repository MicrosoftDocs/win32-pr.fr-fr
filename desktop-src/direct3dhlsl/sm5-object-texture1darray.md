---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- HLSL Texture1DArray
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030348"
---
# <a name="texture1darray"></a>Texture1DArray

Type Texture1DArray ([tel qu’il existe dans Shader Model 4](dx-graphics-hlsl-to-type.md)) et variables de ressource. Cet objet texture prend en charge les méthodes suivantes en plus des méthodes dans le nuanceur modèle 4.



| Méthode                                                                       | Description                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1darray-getdimensions.md)             | Obtient les dimensions de ressource.                                                              |
| [**Load**](texture1darray-load.md)                                          | Lit les données de texture.                                                                        |
| [**mips. And\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) | Obtient une variable de ressource en lecture seule.                                                        |
| [**Opérateur\[\]**](sm5-object-texture1darray-operatorindex.md)              | Obtient une variable de ressource en lecture seule.                                                        |
| [**Exemple**](texture1darray-sample.md)                                      | Échantillonne une texture.                                                                         |
| [**SampleBias**](texture1darray-samplebias.md)                              | Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.                      |
| [**SampleCmp**](texture1darray-samplecmp.md)                                | Échantillonne une texture en utilisant une valeur de comparaison pour rejeter des exemples.                             |
| [**SampleCmpLevelZero**](texture1darray-samplecmplevelzero.md)              | Échantillonne une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.       |
| [**SampleGrad**](texture1darray-samplegrad.md)                              | Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé. |
| [**SampleLevel**](texture1darray-samplelevel.md)                            | Échantillonne une texture au niveau du mipmap spécifié.                                           |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cet objet est pris en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




