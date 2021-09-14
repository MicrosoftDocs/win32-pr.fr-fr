---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- HLSL Texture1D
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8a60706ea2752109cdda9907ffe7c654efe531
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921255"
---
# <a name="texture1d"></a>Texture1D

Un type de texture 1D ([tel qu’il existe dans le nuanceur modèle 4](dx-graphics-hlsl-to-type.md)) et des variables de ressource. Cet objet texture prend en charge les méthodes suivantes en plus des méthodes dans le nuanceur modèle 4.



| Méthode                                                                  | Description                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1d-getdimensions.md)             | Obtient les dimensions de ressource.                                                              |
| [**Chargera**](texture1d-load.md)                                          | Lit les données de texture.                                                                        |
| [**Opérateur\[\]**](sm5-object-texture1d-operatorindex.md)              | Obtient une variable de ressource en lecture seule.                                                        |
| [**mips. And\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) | Obtient une variable de ressource en lecture seule.                                                        |
| [**Exemple**](texture1d-sample.md)                                      | Échantillonne une texture.                                                                         |
| [**SampleBias**](texture1d-samplebias.md)                              | Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.                      |
| [**SampleCmp**](texture1d-samplecmp.md)                                | Échantillonne une texture en utilisant une valeur de comparaison pour rejeter des exemples.                             |
| [**SampleCmpLevelZero**](texture1d-samplecmplevelzero.md)              | Échantillonne une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.       |
| [**SampleGrad**](texture1d-samplegrad.md)                              | Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé. |
| [**SampleLevel**](texture1d-samplelevel.md)                            | Échantillonne une texture au niveau du mipmap spécifié.                                           |



 

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

 

 




