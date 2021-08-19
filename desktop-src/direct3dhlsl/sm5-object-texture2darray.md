---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- HLSL Texture2DArray
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aab6e5c0a500a9f34cbd4e418a35e96687650f3df863e1fe77576c66ade718e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023399"
---
# <a name="texture2darray"></a>Texture2DArray

Type Texture2DArray ([tel qu’il existe dans Shader Model 4](dx-graphics-hlsl-to-type.md)) et variables de ressource. Cet objet texture prend en charge les méthodes suivantes en plus des méthodes dans le nuanceur modèle 4.



| Méthode                                                                      | Description                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Gather**](texture2darray-gather.md)                                      | Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.                                                                |
| [**GatherRed**](texture2darray-gatherred.md)                                | Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.                                          |
| [**GatherGreen**](texture2darray-gathergreen.md)                            | Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.                                        |
| [**GatherBlue**](texture2darray-gatherblue.md)                              | Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.                                         |
| [**GatherAlpha**](texture2darray-gatheralpha.md)                            | Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.                                        |
| [**GatherCmp**](texture2darray-gathercmp.md)                                | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.                      |
| [**GatherCmpRed**](texture2darray-gathercmpred.md)                          | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison.   |
| [**GatherCmpGreen**](texture2darray-gathercmpgreen.md)                      | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant vert par rapport à une valeur de comparaison. |
| [**GatherCmpBlue**](texture2darray-gathercmpblue.md)                        | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison.  |
| [**GatherCmpAlpha**](texture2darray-gathercmpalpha.md)                      | Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison. |
| [**GetDimensions**](sm5-object-texture2darray-getdimensions.md)             | Obtient les dimensions de ressource.                                                                                                                       |
| [**Load**](texture2darray-load.md)                                          | Lit les données de texture.                                                                                                                                 |
| [**mips. And\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) | Obtient une variable de ressource en lecture seule.                                                                                                                 |
| [**Opérateur\[\]**](sm5-object-texture2darray-operatorindex.md)              | Obtient une variable de ressource en lecture seule.                                                                                                                 |
| [**Exemple**](texture2darray-sample.md)                                      | Échantillonne une texture.                                                                                                                                  |
| [**SampleBias**](texture2darray-samplebias.md)                              | Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.                                                                               |
| [**SampleCmp**](texture2darray-samplecmp.md)                                | Échantillonne une texture en utilisant une valeur de comparaison pour rejeter des exemples.                                                                                      |
| [**SampleCmpLevelZero**](texture2darray-samplecmplevelzero.md)              | Échantillonne une texture (mipmap niveau 0 uniquement), en utilisant une valeur de comparaison pour rejeter les exemples.                                                                |
| [**SampleGrad**](texture2darray-samplegrad.md)                              | Échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé.                                                          |
| [**SampleLevel**](texture2darray-samplelevel.md)                            | Échantillonne une texture au niveau du mipmap spécifié.                                                                                                    |



 

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

 

 




