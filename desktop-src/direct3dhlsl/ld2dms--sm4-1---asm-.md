---
title: ld2dms (SM 4.1-ASM)
description: Lit des échantillons individuels à partir de textures à échantillons multiples à deux dimensions.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916288"
---
# <a name="ld2dms-sm41---asm"></a>ld2dms (SM 4.1-ASM)

Lit des échantillons individuels à partir de textures à échantillons multiples à deux dimensions.



| ld2dms \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , sampleIndex (opérande scalaire) |
|------------------------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                               | Description                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse du résultat de l’opération. <br/>                                                                 |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[dans \] les coordonnées de texture nécessaires à l’exécution de l’exemple.<br/>                                                    |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] un registre de texture (t \# ) qui doit avoir été déclaré, identifiant la texture ou la mémoire tampon à partir de laquelle effectuer l’extraction<br/> |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[dans \] Idendifies les exemples à lire à partir de *srcResource*.<br/>                                                       |



 

## <a name="remarks"></a>Notes

Cette instruction est une alternative simplifiée à l' [exemple](sample--sm4---asm-.md) d’instruction. Il extrait les données de la texture spécifiée sans aucun filtrage (par exemple, échantillonnage par points) à l’aide de l’entier fourni *srcAddress* et *sampleIndex*.

*srcAddress* fournit l’ensemble des coordonnées de texture nécessaires pour exécuter l’exemple sous la forme d’entiers non signés. Si *srcAddress* est en dehors de la plage \[ 0... ( \# texels dans la dimension-1) \] , **ld2dms** retourne toujours 0 dans tous les composants présents dans le format de la ressource, et les valeurs par défaut (0, 0, 0, 1,0 f/0x00000001) pour les composants manquants.

*sampleIndex* ne doit pas nécessairement être un littéral. Il n’est pas nécessaire de spécifier le nombre d’échantillons multiples sur la ressource de texture et il fonctionne avec des affichages de profondeur ou de stencil.

Une application qui souhaite obtenir un contrôle plus flexible sur le comportement de l’adresse hors limites doit utiliser l' **exemple** d’instruction à la place, car elle honore l’état de l’échantillonneur/de la mise en miroir/de la bordure/de la bordure.

*srcAddress. b* (Swizzle) est ignoré pour Texture2Ds. Si la valeur est en dehors de la plage d’index de tableau disponibles \[ 0... ( Array size-1) \] , puis **ld2dms** retourne toujours 0 dans tous les composants présents dans le format de la ressource, et les valeurs par défaut (0, 0, 0, 1.0 f/0x00000001) pour les composants manquants.

Pour les tableaux Texture2D, *srcAddress. b* (après Swizzle) fournit l’index de tableau. Oherwise a le même comportement que Texture2D.

*srcAddress. a* (Swizzle) est toujours ignoré. Le compilateur HLSL ne sortira jamais quoi que ce soit.

*srcResource* est un registre de texture (t \# ) qui doit avoir été déclaré (22.3.11), identifiant la texture à partir de laquelle effectuer l’extraction.

L’extraction de t \# qui n’a rien lié à elle retourne 0 pour tous les composants.

### <a name="address-offset"></a>Décalage d’adresse

Le \[ \_ suffixe aoffimmi (u, v, w) facultatif \] (décalage d’adresse par entier immédiat) indique que les coordonnées de texture du **ld2dms** doivent être décalées par un ensemble d’espaces de constantes d’espace de Texel immédiat fournis. Les valeurs littérales sont un ensemble de numéros de compléments de 4 bits 2, dont la plage d’entiers est comprise entre \[ -8 et 7 \] .

Les décalages sont ajoutés aux coordonnées de texture, dans l’espace Texel.

Les décalages d’adresse ne sont pas appliqués le long de l’axe de tableau des tableaux Texture1D/2D.

Les composants *\_ aoffimmi v, w* sont ignorés pour Texture1Ds.

Le composant *\_ aoffimmi w* est ignoré pour Texture2Ds.

Étant donné que les coordonnées de texture pour les **ld2dms** sont des entiers non signés, si le décalage entraîne l’accès à l’adresse sous zéro, elle est renvoyée à une adresse de grande taille et entraîne un accès en dehors des limites, ce qui correspond à la valeur **LD** retourne 0 dans tous les composants présents dans le format de la ressource, et les valeurs par défaut (0, 0,

### <a name="sample-number"></a>Nombre d’échantillons

**ld2dms** peut être utilisé sur n’importe quelle ressource. **ld2dms** fonctionne de la même façon que **LD** , sauf sur les ressources multsample 2D, en utilisant l’opérande *sampleIndex* supplémentaire (de base 0) pour identifier l’échantillon à lire à partir de la ressource.

Le résultat de la spécification d’un *sampleIndex* qui dépasse le nombre d’exemples dans la ressource n’est pas défini, mais ne peut pas retourner de données en dehors de l’espace d’adressage du contexte de périphérique.

### <a name="return-type-control"></a>Contrôle de type de retour

Le format de données retourné par **ld2dms** au registre de destination est déterminé de la même façon que pour l' **exemple** d’instruction. Elle est basée sur le format lié au paramètre *srcResource* (t \# ).

Comme avec l' **exemple** d’instruction, les valeurs retournées pour **ld2dms** sont 4-vectors avec des valeurs par défaut spécifiques au format pour les composants qui ne sont pas présents dans le format. Swizzle sur *srcResource* détermine comment Swizzle le résultat à 4 composants à partir de la charge de texture, après quoi. Mask sur *dest* détermine les composants de *dest* qui sont mis à jour.

Quand une valeur float 32 bits est lue par **ld2dms** dans un registre 32 bits, les bits ne sont pas touchés ; autrement dit, les valeurs dénormales restent dénormalisées. Contrairement à l' **exemple** d’instruction.

### <a name="miscellaneous-details"></a>Détails divers

Comme aucun filtrage n’est associé à cette instruction, les concepts tels que LOD Bias ne s’appliquent pas. En conséquence, il n’y a aucun paramètre de l' *échantillonneur \#* .

### <a name="restrictions"></a>Restrictions

-   *srcResource* doit être un \# Registre t, et non un TextureCube, Texture1D ou Texture1DArray. *srcResource* ne peut pas être un ConstantBuffer, qui ne peut pas être lié à des \# registres t.
-   L’adressage relatif sur *srcResource* n’est pas autorisé.
-   *srcAddress* et *sampleIndex* doivent être un registre Temp (r \# /x \# ), constant (CB \# ) ou Input (v \# ).
-   *dest* doit être un registre Temp (r \# /x \# ) ou Output (o \* \# ).

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





