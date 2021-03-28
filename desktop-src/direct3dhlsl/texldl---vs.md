---
title: texldl-vs
description: Échantillonner une texture avec un échantillonneur particulier. Le niveau de détail mipmap spécifique échantillonné doit être spécifié en tant que quatrième composant de la coordonnée de texture. | texldl-vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be9240f5307bb1e70b1f10cc1e392b92e5833fd8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043016"
---
# <a name="texldl---vs"></a>texldl-vs

Échantillonner une texture avec un échantillonneur particulier. Le niveau de détail mipmap spécifique échantillonné doit être spécifié en tant que quatrième composant de la coordonnée de texture.

## <a name="syntax"></a>Syntaxe



| texldl DST, src0, src1 |
|------------------------|



 

Où :

-   l’heure d’été est un registre de destination.
-   src0 est un registre source qui fournit les coordonnées de texture pour l’échantillon de texture.
-   src1 identifie le ou les registres de l’échantillonneur \# de source, où \# spécifie le numéro d’échantillonnage de texture à échantillonner. L’échantillonneur s’est associé à une texture et à un état de contrôle défini par l’énumération [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (par exemple, D3DSAMP \_ MINFILTER).

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| texldl                 |      |      |      |       | x    | x     |



 

texldl recherche la texture définie à l’étape d’échantillonnage référencée par src1. Le niveau de détail est sélectionné dans src0. w. Cette valeur peut être négative. dans ce cas, le niveau de détail sélectionné est le « avant toute chose un » (mappage le plus grand) avec le MAGFILTER. Comme src0. w est une valeur à virgule flottante, la valeur fractionnaire est utilisée pour interpoler (si MIPFILTER est linéaire) entre deux niveaux MIP. Les États de l’échantillonneur MIPMAPLODBIAS et MAXMIPLEVEL sont honorés. Pour plus d’informations sur les États de l’échantillonneur, consultez [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Si un programme Shader échantillonne à partir d’un échantillonneur qui n’a pas de texture définie, 0001 est obtenu dans le registre de destination.

Il s’agit d’une approximation de l’algorithme de l’appareil de référence.


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
   LOD = MAX( MAXMIPLEVEL, LOD);
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
-   l’heure d’été doit être un [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).
-   l’heure d’été peut accepter un masque d’écriture. Consultez [masquage du registre de destination](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).
-   Les valeurs par défaut pour les composants manquants sont 0 ou 1 et dépendent du format de texture.
-   src1 doit être un [échantillonneur (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) \# . src1 ne peut pas utiliser de modificateur de négation. src1 peut utiliser Swizzle, qui est appliqué après l’échantillonnage avant que le masque d’écriture soit respecté. L’échantillonneur doit avoir été déclaré (à l’aide de la [ \_ samplerType DCL (SM3-vs ASM)](dcl-samplertype---vs.md)) au début du nuanceur.
-   Le nombre de coordonnées requises pour exécuter l’exemple de texture dépend de la façon dont l’échantillonneur a été déclaré. Si elle a été déclarée en tant que cube, une coordonnée de texture à trois composants est requise (. RGB). La validation garantit que les coordonnées fournies à texldl sont suffisantes pour la dimension de texture déclarée pour l’échantillonneur. Toutefois, il n’est pas garanti que l’application définit effectivement une texture (via l’API) avec des dimensions égales à la dimension déclarée pour l’échantillonneur. Dans ce cas, le runtime tente de détecter les incompatibilités (éventuellement en débogage uniquement). L’échantillonnage d’une texture avec moins de dimensions que celles présentes dans la coordonnée de texture sera autorisé et sera supposé ignorer les composants de coordonnée de texture supplémentaires. Inversement, l’échantillonnage d’une texture avec davantage de dimensions que celles présentes dans la coordonnée de texture n’est pas autorisé.
-   Si le src0 (coordonnée de texture) est un [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ), les composants requis pour la recherche (décrite ci-dessus) doivent avoir été préalablement écrits.
-   Les textures RVB non signées d’échantillonnage entraînent des valeurs float comprises entre 0,0 et 1,0.
-   L’échantillonnage des textures signées entraîne des valeurs float comprises entre-1,0 et 1,0.
-   Lors de l’échantillonnage de textures à virgule flottante, Float16 signifie que les données seront comprises dans le \_ FLOAT16 maximal. Float32 signifie que la plage maximale du pipeline sera utilisée. L’échantillonnage en dehors de l’une des limites n’est pas défini.
-   Il n’existe aucune limite de lecture dépendante.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
