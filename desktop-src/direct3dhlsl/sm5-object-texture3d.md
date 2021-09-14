---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- HLSL Texture3D
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922252"
---
# <a name="texture3d"></a>Texture3D

Type Texture3D ([tel qu’il existe dans Shader Model 4](dx-graphics-hlsl-to-type.md)) et variables de ressource. Cet objet texture prend en charge les méthodes suivantes en plus des méthodes dans le nuanceur modèle 4.



| Méthode                                                                  | Description                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture3d-getdimensions.md)             | Obtient les dimensions de ressource.                                                              |
| [**Chargera**](texture3d-load.md)                                          | Lit les données de texture.                                                                        |
| [**mips. And\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) | Obtient une variable de ressource en lecture seule.                                                        |
| [**Opérateur\[\]**](sm5-object-texture3d-operatorindex.md)              | Obtient une variable de ressource en lecture seule.                                                        |
| [**Exemple**](texture3d-sample.md)                                      | Échantillonne une texture.                                                                         |
| [**SampleBias**](texture3d-samplebias.md)                              | Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.                      |
| [**SampleGrad**](texture3d-samplegrad.md)                              | Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé. |
| [**SampleLevel**](texture3d-samplelevel.md)                            | Échantillonne une texture au niveau du mipmap spécifié.                                           |



 

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

 

 




