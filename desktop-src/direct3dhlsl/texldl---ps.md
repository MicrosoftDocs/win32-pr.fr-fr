---
title: texldl-PS
description: Échantillonner une texture avec un échantillonneur particulier. Le niveau de détail mipmap spécifique échantillonné doit être spécifié en tant que quatrième composant de la coordonnée de texture. | texldl-PS
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918076"
---
# <a name="texldl---ps"></a>texldl-PS

Échantillonner une texture avec un échantillonneur particulier. Le niveau de détail mipmap spécifique échantillonné doit être spécifié en tant que quatrième composant de la coordonnée de texture.

## <a name="syntax"></a>Syntaxe



| texldl DST, src0, src1 |
|------------------------|



 

Où :

-   l’heure d’été est un registre de destination.
-   src0 est un registre source qui fournit les coordonnées de texture pour l’échantillon de texture. Consultez [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifie le ou les registres de l’échantillonneur \# de source, où \# spécifie le numéro d’échantillonnage de texture à échantillonner. L’échantillonneur s’est associé à une texture et à un état de contrôle défini par l’énumération [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (par exemple, D3DSAMP \_ MINFILTER).

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldl                |      |      |      |      |      |      |       | x    | x     |



 

texldl recherche la texture définie à l’étape d’échantillonnage référencée par src1. Le niveau de détail est sélectionné dans src0. w. Cette valeur peut être négative dans le cas où le niveau de détail sélectionné est le avant toute chose (le plus grand mappage) avec le MAGFILTER. Étant donné que src0. w est une valeur à virgule flottante, la valeur fractionnaire est utilisée pour interpoler (si MIPFILTER est linéaire) entre deux niveaux MIP. Les États de l’échantillonneur MIPMAPLODBIAS et MAXMIPLEVEL sont honorés. Pour plus d’informations sur les États de l’échantillonneur, consultez [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Si un programme de nuanceur échantillonne à partir d’un échantillonneur qui n’a pas de texture définie, 0001 est obtenu dans le registre de destination.

Voici un algorithme approximatif que suit l’appareil de référence :


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



Restrictions :

-   Les coordonnées de texture ne doivent pas être mises à l’échelle par taille de texture.
-   l’heure d’été doit être un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   l’heure d’été peut accepter un writemask. Voir [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).
-   Les valeurs par défaut pour les composants manquants sont 0 ou 1 et dépendent du format de texture.
-   src1 doit être un [échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# . src1 ne peut pas utiliser de modificateur de négation (voir [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)). src1 peut utiliser Swizzle (voir [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), qui est appliqué après l’échantillonnage, mais avant le masque d’écriture (voir masque d’écriture de registre de destination) est respecté. L’échantillonneur doit avoir été déclaré (à l’aide de la [ \_ samplerType DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)) au début du nuanceur.
-   Le nombre de coordonnées requises pour exécuter l’exemple de texture dépend de la façon dont l’échantillonneur a été déclaré. Si elle a été déclarée en tant que cube, une coordonnée de texture à trois composants est requise (. RGB). La validation garantit que les coordonnées fournies pour Tex \_ LDL sont suffisantes pour la dimension de texture déclarée pour l’échantillonneur. Toutefois, il n’est pas garanti que l’application définit en fait une texture (via l’API) dont les dimensions sont égales à la dimension déclarée pour l’échantillonneur. Dans ce cas, le runtime tente de détecter les incompatibilités (éventuellement en débogage uniquement). L’échantillonnage d’une texture avec moins de dimensions que celles présentes dans la coordonnée de texture sera autorisé et supposé ignorer les composants de coordonnée de texture supplémentaires. Inversement, l’échantillonnage d’une texture avec plus de dimensions que celles présentes dans la coordonnée de texture n’est pas conforme.
-   Si le src0 (coordonnée de texture) est un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md), les composants requis pour la recherche (décrite ci-dessus) doivent avoir été préalablement écrits.
-   Les textures RVB non signées d’échantillonnage entraînent des valeurs float comprises entre 0,0 et 1,0.
-   L’échantillonnage des textures signées entraîne des valeurs float comprises entre-1,0 et 1,0.
-   Lors de l’échantillonnage de textures à virgule flottante, Float16 signifie que les données seront comprises dans le \_ FLOAT16 maximal. Float32 signifie que la plage maximale du pipeline sera utilisée. L’échantillonnage en dehors de l’une des limites n’est pas défini.
-   Il n’existe aucune limite de lecture dépendante.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
