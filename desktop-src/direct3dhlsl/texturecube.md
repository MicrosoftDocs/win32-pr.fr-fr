---
title: TextureCube, objet
description: Type TextureCube (tel qu’il existe dans Shader Model 4) et variables de ressource. Cet objet texture prend en charge ces méthodes en plus des méthodes dans le nuanceur modèle 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- TextureCube, objet HLSL
- Objet TextureCube HLSL, décrit
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 939c79895ae1c24665fc70d6b6cf2ced19854e2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854782"
---
# <a name="texturecube-object"></a>TextureCube, objet

Type **TextureCube** ([tel qu’il existe dans Shader Model 4](dx-graphics-hlsl-to-type.md)) et variables de ressource. Cet objet texture prend en charge ces méthodes en plus des méthodes dans le nuanceur modèle 4.

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **TextureCube** a ces méthodes.



| Méthode                                                      | Description                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Gather**](texturecube-gather.md)                         | Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.<br/>                                                                |
| [**GatherAlpha**](texturecube-gatheralpha.md)               | Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.<br/>                                        |
| [**GatherBlue**](texturecube-gatherblue.md)                 | Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.<br/>                                         |
| [**GatherCmp**](texturecube-gathercmp.md)                   | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.<br/>                      |
| [**GatherCmpAlpha**](texturecube-gathercmpalpha.md)         | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison.<br/> |
| [**GatherCmpBlue**](texturecube-gathercmpblue.md)           | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison.<br/>  |
| [**GatherCmpGreen**](texturecube-gathercmpgreen.md)         | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant vert par rapport à une valeur de comparaison.<br/> |
| [**GatherCmpRed**](texturecube-gathercmpred.md)             | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison.<br/>   |
| [**GatherGreen**](texturecube-gathergreen.md)               | Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.<br/>                                        |
| [**GatherRed**](texturecube-gatherred.md)                   | Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.<br/>                                          |
| [**Exemple**](texturecube-sample.md)                         | Échantillonne une texture.<br/>                                                                                                                                  |
| [**SampleBias**](texturecube-samplebias.md)                 | Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.<br/>                                                                               |
| [**SampleCmp**](texturecube-samplecmp.md)                   | Échantillonne une texture en utilisant une valeur de comparaison pour rejeter des exemples.<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecube-samplecmplevelzero.md) | Échantillonne une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.<br/>                                                                |
| [**SampleGrad**](texturecube-samplegrad.md)                 | Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.<br/>                                                          |
| [**SampleLevel**](texturecube-samplelevel.md)               | Échantillonne une texture au niveau du mipmap spécifié.<br/>                                                                                                    |



 

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

 

 





