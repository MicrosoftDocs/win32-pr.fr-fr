---
title: exemple (SM4-ASM)
description: Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné. | exemple (SM4-ASM)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953689"
---
# <a name="sample-sm4---asm"></a>exemple (SM4-ASM)

Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné.



| exemple \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler |
|--------------------------------------------------------------------------------------------------------|



 



| Élément                                                                                                               | Description                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse du résultat de l’opération.<br/>                                      |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[dans \] un ensemble de coordonnées de texture. Pour plus d’informations, consultez la section **Notes** .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] un registre de texture. Pour plus d’informations, consultez la section **Notes** .<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[dans \] un registre d’échantillonneur. Pour plus d’informations, consultez la section **Notes** .<br/>           |



 

## <a name="remarks"></a>Notes

Les données sources peuvent provenir de n’importe quel type de ressource, autre que des mémoires tampons.

*srcAddress* fournit l’ensemble des coordonnées de texture nécessaires pour exécuter l’exemple, sous la forme de valeurs à virgule flottante référençant l’espace normalisé dans la texture. Les modes de renvoi à la ligne de l’adresse (Wrap/Mirror/collier/bordure, etc.) sont appliqués pour les coordonnées de texture en dehors de \[ 0... 1 \] plage, tirées de l’état de l’échantillonneur (s \# ) et appliquées après l’application d’un décalage d’adresse à des coordonnées de texture.

*srcResource* est un registre de texture (t \# ). Il s’agit simplement d’un espace réservé pour une texture, y compris le type de données de retour de la ressource échantillonnée. Toutes ces informations sont déclarées dans le préambule du nuanceur. La ressource réelle à échantillonner est liée au nuanceur en externe à l’emplacement \# (pour t \# ).

*srcSampler* est un ou plusieurs registres d’échantillonnage. Il s’agit simplement d’un espace réservé pour une collection de contrôles de filtrage tels que point et Linear, mappage MIP et les contrôles d’habillage d’adresse.

L’ensemble d’informations nécessaires au matériel pour effectuer l’échantillonnage est divisé en deux parties orthogonales. Tout d’abord, le registre de texture fournit des informations sur le type de données sources, notamment des informations indiquant si la texture contient des données sRVB. Elle fait également référence à la mémoire réelle échantillonnée. Deuxièmement, le registre de l’échantillonneur définit le mode de filtrage à appliquer.

### <a name="array-resources"></a>Ressources de groupe

Pour les tableaux Texture1D, le composant *srcAddress* g (pos-Swizzle) sélectionne la tranche de tableau à partir de laquelle effectuer l’extraction. Elle est toujours traitée comme une valeur float mise à l’échelle, plutôt que l’espace normalisé pour les coordonnées de texture standard, et un arrondi vers le plus proche est appliqué à la valeur, suivi d’une bride à la plage BufferArray disponible.

Pour les tableaux Texture2D, le composant *srcAddress* b (pos-Swizzle) sélectionne la tranche de tableau à partir de laquelle effectuer l’extraction, sinon en utilisant la même sémantique que celle décrite pour les groupes Texture1D.

### <a name="address-offset"></a>Décalage d’adresse

Le \[ \_ suffixe aoffimmi (u, v, w) facultatif \] (décalage d’adresse par entier immédiat) indique que les coordonnées de la texture de l’échantillon doivent être décalées par un jeu d’espaces de texture de l’espace de Texel immédiat fournis. Les valeurs littérales sont un ensemble de numéros de compléments de 4 bits 2, dont la plage d’entiers est comprise entre \[ -8 et 7 \] . Ce modificateur est défini pour toutes les ressources, y compris les tableaux Texture1D/2D et Texture3D, mais il n’est pas défini pour TextureCube.

Le matériel peut tirer parti d’une connaissance immédiate selon laquelle un parcours sur une certaine empreinte des texels à propos d’un emplacement commun est effectué par un ensemble d’instructions d’exemple. Cela peut être transmis à l’aide \_ de aoffimmi (u, v, w).

Les décalages sont ajoutés aux coordonnées de texture, dans l’espace Texel, par rapport à chaque miplevel accédé. Ainsi, même si les coordonnées de texture sont fournies en tant que valeurs float normalisées, le décalage applique un décalage d’entier d’espace Texel.

Les décalages d’adresse ne sont pas appliqués le long de l’axe de tableau des tableaux Texture1D/2D.

\_aoffimmi v, w Components sont ignorés pour Texture1Ds.

\_le composant aoffimmi w est ignoré pour Texture2Ds.

Les modes de renvoi à la ligne de l’adresse (Wrap/Mirror/collier/bordure, etc.) du ou des États de l’échantillonneur \# sont appliqués après l’application d’un décalage d’adresse à des coordonnées de texture.

### <a name="return-type-control"></a>Contrôle de type de retour

Le format de données retourné par l’exemple au registre de destination est déterminé par le format de ressource ( \_ format dxgi \* ) lié au paramètre *srcResource* (t \# ). Par exemple, si le t spécifié \# a été lié à une ressource au format \_ dxgi \_ A8B8G8R8 \_ UNORM \_ sRVB, l’opération d’échantillonnage convertira les texels échantillonnés de gamma 2,0 à 1,0, appliquera le filtrage et le résultat sera écrit dans le registre de destination en tant que valeurs à virgule flottante dans la plage \[ 0.. 1 \] .

Les valeurs retournées sont 4-vectors (avec des valeurs par défaut spécifiques au format pour les composants qui ne sont pas présents au format). Swizzle sur *srcResource* détermine comment Swizzle le résultat à 4 composants à partir de l’échantillon de texture/filtre, après quoi. Mask sur *dest* détermine les composants de *dest* qui sont mis à jour.

Quand **Sample** lit une valeur float 32 bits dans un registre 32 bits, avec l’échantillonnage de point (aucun filtrage), il peut ou non vider les valeurs dénormalisées, mais les autres valeurs ne sont pas modifiées. Si l’incertitude avec les valeurs de dénormalisation par échantillonnage des points est un problème pour une application, utilisez l’instruction [LD](ld--sm4---asm-.md) , qui garantit que les valeurs float 32 bits sont lues sans modification.

### <a name="lod-calculation"></a>Calcul LOD

Pour plus d’informations sur la façon dont les dérivés sont calculés dans le processus de détermination de LOD pour le filtrage, consultez [Deriv \_ RTX](deriv-rtx--sm4---asm-.md) et [Deriv \_ propriété](deriv-rty--sm4---asm-.md). L' **exemple** d’instruction calcule implicitement les dérivés sur les coordonnées de texture à l’aide de la même définition que celle utilisée par les instructions du nuanceur **Deriv** . Cela ne s’applique pas à l' [exemple \_ l](sample-l--sm4---asm-.md) ou à des exemples d’instructions [ \_ d](sample-d--sm4---asm-.md) . Pour ces instructions, LOD ou les dérivés sont fournis directement par l’application.

Pour l' **exemple** d’instruction, les implémentations peuvent choisir de partager le même calcul de LOD sur les 4 pixels d’un tampon 2x2 (mais pas de plus grande zone) ou d’effectuer des calculs de LOD par pixel.

### <a name="miscellaneous-details"></a>Détails divers

Pour la mémoire tampon & Texture1D, les composants *srcAddress* . GBA (pos-Swizzle) sont ignorés. Pour les tableaux Texture1D, les composants *srcAddress* . BA (pos-Swizzle) sont ignorés. Pour Texture2Ds, *srcAddress* . a Component (pos-Swizzle) est ignoré.

L’extraction à partir d’un emplacement d’entrée auquel rien n’est lié retourne 0 pour tous les composants.

### <a name="restrictions"></a>Restrictions

-   *srcResource* doit être un \# Registre t. *srcResource* ne peut pas être un ConstantBuffer, qui ne peut pas être lié à des \# registres t.
-   *srcSampler* doit être un \# Registre s.
-   L’adressage relatif sur *srcResource* ou *srcSampler* n’est pas autorisé.
-   *srcAddress* doit être un registre Temp (r \# /X \# ), constantBuffer (CB \# ), Input (v \# ) ou une ou plusieurs valeurs immédiates.
-   *dest* doit être un registre Temp (r \# /x \# ) ou Output (o \* \# ).
-   \_aoffimmi (u, v, w) n’est pas autorisé pour TextureCubes.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





