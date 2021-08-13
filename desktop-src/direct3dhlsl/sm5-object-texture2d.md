---
title: Texture2D
description: Texture2D
ms.assetid: e4f9cfd8-65e6-4375-8f87-736bca32cad4
keywords:
- HLSL Texture2D
topic_type:
- apiref
api_name:
- Texture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad13843dd74ab7cc188c3ab37d76df978f2a5fbd4bc6c292cfddfdf7c5841b33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789375"
---
# <a name="texture2d"></a>Texture2D

Type Texture2D ([tel qu’il existe dans Shader Model 4](dx-graphics-hlsl-to-type.md)) et variables de ressource. Cet objet texture prend en charge les méthodes suivantes en plus des méthodes dans le nuanceur modèle 4.



| Méthode                                                                 | Description                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Gather**](texture2d-gather.md)                                      | Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.                                                                |
| [**GatherRed**](texture2d-gatherred.md)                                | Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.                                          |
| [**GatherGreen**](texture2d-gathergreen.md)                            | Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.                                        |
| [**GatherBlue**](texture2d-gatherblue.md)                              | Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.                                         |
| [**GatherAlpha**](texture2d-gatheralpha.md)                            | Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.                                        |
| [**GatherCmp**](texture2d-gathercmp.md)                                | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.                      |
| [**GatherCmpRed**](texture2d-gathercmpred.md)                          | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison.   |
| [**GatherCmpGreen**](texture2d-gathercmpgreen.md)                      | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant vert par rapport à une valeur de comparaison. |
| [**GatherCmpBlue**](texture2d-gathercmpblue.md)                        | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison.  |
| [**GatherCmpAlpha**](texture2d-gathercmpalpha.md)                      | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison. |
| [**GetDimensions**](sm5-object-texture2d-getdimensions.md)             | Obtient les dimensions de ressource.                                                                                                                       |
| [**Load**](texture2d-load.md)                                          | Lit les données de texture.                                                                                                                                 |
| [**mips. And\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) | Obtient une variable de ressource en lecture seule.                                                                                                                 |
| [**Opérateur\[\]**](sm5-object-texture2d-operatorindex.md)              | Obtient une variable de ressource en lecture seule.                                                                                                                 |
| [**Exemple**](texture-sample-overload.md)                               | Échantillonne une texture.                                                                                                                                  |
| [**SampleBias**](texture2d-samplebias.md)                              | Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.                                                                               |
| [**SampleCmp**](texture2d-samplecmp.md)                                | Échantillonne une texture en utilisant une valeur de comparaison pour rejeter des exemples.                                                                                      |
| [**SampleCmpLevelZero**](texture2d-samplecmplevelzero.md)              | Échantillonne une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.                                                                |
| [**SampleGrad**](texture2d-samplegrad.md)                              | Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.                                                          |
| [**SampleLevel**](texture2d-samplelevel.md)                            | Échantillonne une texture au niveau du mipmap spécifié.                                                                                                    |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cet objet est pris en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




