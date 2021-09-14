---
title: TextureCubeArray, objet
description: Type TextureCubeArray (tel qu’il existe dans Shader Model 4) et variables de ressource. Cet objet texture prend en charge ces méthodes en plus des méthodes dans le nuanceur modèle 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- TextureCubeArray, objet HLSL
- Objet TextureCubeArray HLSL, décrit
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922104"
---
# <a name="texturecubearray-object"></a>TextureCubeArray, objet

Type **TextureCubeArray** ([tel qu’il existe dans Shader Model 4](dx-graphics-hlsl-to-type.md)) et variables de ressource. Cet objet texture prend en charge ces méthodes en plus des méthodes dans le nuanceur modèle 4.

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **TextureCubeArray** a ces méthodes.



| Méthode                                                           | Description                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Gather**](texturecubearray-gather.md)                         | Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.<br/>                                                                |
| [**GatherAlpha**](texturecubearray-gatheralpha.md)               | Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.<br/>                                        |
| [**GatherBlue**](texturecubearray-gatherblue.md)                 | Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.<br/>                                         |
| [**GatherCmp**](texturecubearray-gathercmp.md)                   | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.<br/>                      |
| [**GatherCmpAlpha**](texturecubearray-gathercmpalpha.md)         | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison.<br/> |
| [**GatherCmpBlue**](texturecubearray-gathercmpblue.md)           | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison.<br/>  |
| [**GatherCmpGreen**](texturecubearray-gathercmpgreen.md)         | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant vert par rapport à une valeur de comparaison.<br/> |
| [**GatherCmpRed**](texturecubearray-gathercmpred.md)             | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison.<br/>   |
| [**GatherGreen**](texturecubearray-gathergreen.md)               | Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.<br/>                                        |
| [**GatherRed**](texturecubearray-gatherred.md)                   | Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.<br/>                                          |
| [**Exemple**](texturecubearray-sample.md)                         | Échantillonne une texture.<br/>                                                                                                                                  |
| [**SampleBias**](texturecubearray-samplebias.md)                 | Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.<br/>                                                                               |
| [**SampleCmp**](texturecubearray-samplecmp.md)                   | Échantillonne une texture en utilisant une valeur de comparaison pour rejeter des exemples.<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecubearray-samplecmplevelzero.md) | Échantillonne une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.<br/>                                                                |
| [**SampleGrad**](texturecubearray-samplegrad.md)                 | Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.<br/>                                                          |
| [**SampleLevel**](texturecubearray-samplelevel.md)               | Échantillonne une texture au niveau du mipmap spécifié.<br/>                                                                                                    |



 

## <a name="remarks"></a>Notes

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

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

 

 





