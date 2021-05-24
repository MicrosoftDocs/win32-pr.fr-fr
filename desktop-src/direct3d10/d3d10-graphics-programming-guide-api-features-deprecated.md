---
description: La liste des fonctionnalités disponibles dans Direct3D 10 est disponible ici. Cette page répertorie les fonctionnalités Direct3D 9 qui ne sont plus prises en charge dans Direct3D 10.
ms.assetid: ad3eff8e-a225-47c0-a53f-b1a3c94bcaac
title: Fonctionnalités dépréciées (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bb06738f046b92290d35cff180f3879f4fa737
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335543"
---
# <a name="deprecated-features-direct3d-10"></a>Fonctionnalités dépréciées (Direct3D 10)

La liste des fonctionnalités disponibles dans Direct3D 10 est disponible [ici](d3d10-graphics-programming-guide-api-features.md). Cette page répertorie les fonctionnalités Direct3D 9 qui ne sont plus prises en charge dans Direct3D 10.

Les principales modifications de fonctionnalités dans Direct3D 10 sont les suivantes :

- Direct3D 10 ne prend plus en charge la transformation et le pipeline d’éclairage de la fonction fixe.
- Direct3D 10 ne prend plus en charge le mélangeur de texture de fonction fixe (parfois appelé nuanceur de pixels de fonction fixe).
- Direct3D 10 implémente de nouvelles règles de pixellisation, qui sont plus simples et plus claires que les règles GDI héritées qui sont implémentées dans Direct3D 9. Par exemple, le contrôle de dernier Pixel pour les lignes n’est plus pris en charge.

Voici la liste complète des fonctionnalités de Direct3D 9 qui ont été dépréciées dans Direct3D 10.

- **Alpha Blend**. Alpha Blend est maintenant programmé indépendamment de Color Blend. Direct3D 10 ajoute un basculement d’activation de la fusion alpha qui est activé par défaut. Pour plus d’informations [, consultez objets d’État (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) .
- **Test alpha**. Le test alpha est un comportement de pixel à fonction fixe pour Direct3D 9. Le test alpha est déplacé vers des nuanceurs de pixels programmables pour Direct3D 10 et versions ultérieures. Pour plus d’informations sur l’émulation de la fonctionnalité de test Direct3D 9 alpha dans Direct3D 10 et versions ultérieures, consultez l’exemple FixedFuncEMU dans le [Kit de développement logiciel (SDK) DirectX pour le 2010 juin](https://www.microsoft.com/download/en/details.aspx?id=6812).
- **Options du mode fondu**. BOTHSRCALPHA a été supprimé de D3D10 \_ Blend, car il est redondant avec BOTHINVSRCALPHA. Pour plus d’informations, consultez [**D3D10 \_ Blend**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend) .
- **Bloquer les formats de compression**. Il n’existe aucune distinction entre les caractères alpha prémultipliés par Alpha ou non prémultipliés dans Direct3D 10. Ces formats Direct3D 9 sont mappés à ces formats Direct3D 10 : 

    | Direct3D 9 | Direct3D 10 |
    |------------|-------------|
    | DXT1       | BC1\*       |
    | DXT2,DXT3  | BC2\*       |
    | DXT4, DXT5  | BC3\*       |

    

     

    Pour plus d’informations, consultez [compression de bloc (Direct3D 10)](d3d10-graphics-programming-guide-resources-block-compression.md) .

-   **Plans de clip**. Au lieu d’utiliser des plans de clip, Direct3D 10 implémente les distances des éléments et les distances de réforme, avec jusqu’à 8 composants chacun dans 2 éléments d’attributs de vertex. Pour plus d’informations, consultez [sémantique (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-semantics.md) . L' [exemple FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fournit un exemple d’émulation de plans de clip dans Direct3D 10.
-   **Tramage**. Direct3D 10 ne prend pas en charge l’écriture de données dépendantes vers une cible de rendu.
-   **Le pipeline de transformation et d’éclairage à fonction fixe n’est pas disponible**. Au lieu de cela, vous devez utiliser des nuanceurs. Pour plus d’informations, consultez [étapes de nuanceur (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   **Mélangeur de texture de fonction fixe (également appelé nuanceur de pixels de fonction fixe)**. Au lieu de cela, vous devez utiliser des nuanceurs. Pour plus d’informations, consultez [étapes de nuanceur (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   Les **modes de remplissage** ont changé. Direct3D 10 implémente des modes de remplissage solides et filaires. Le point de D3DFILLMODE a été supprimé, utilisez un nuanceur Geometry pour émuler le mode point si nécessaire. L' [exemple FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fournit un exemple d’émulation du point de D3DFILLMODE dans Direct3D 10. Pour plus d’informations, consultez [**\_ \_ mode de remplissage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) et [étapes de nuanceur D3D10 (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   **Formats**. Le matériel peut utiliser des formats exposés par l’API. Les formats de luminance ne sont plus implémentés.
-   **Filtrage mipmap**. Suppression de l’option permettant de sélectionner le mode sans filtre. Au lieu de cela, utilisez une texture avec un seul mipmap ou affectez à l’état de l’échantillonneur MaxLOD la valeur 0. Pour plus d’informations [, consultez objets d’État (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) .
-   **Palettes**. Les applications doivent utiliser une lecture de texture dépendante à la place.
-   **Modèles de nuanceur de pixels et vertex**: 1 \_ x, 2 \_ x et 3 \_ 0. Direct3D 10 prend en charge le modèle de nuanceur 4. Pour plus d’informations, consultez [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md) .
-   **Points sprites**. Utilisez un nuanceur Geometry à la place. Pour plus d’informations, consultez [étapes de nuanceur (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   **Règles de pixellisation**. Les règles de pixellisation de ligne GDI héritées sont remplacées par des règles plus simples. Le contrôle de dernier Pixel pour les lignes n’est plus pris en charge. Pour plus d’informations [, consultez règles de pixellisation (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-rules.md) .
-   **Modes d’ombrage**. D3DSHADEMODE (qui prend en charge l’ombrage plat/Gouraud/Phong) a été supprimé. Direct3D 10 implémente deux modificateurs d’interpolation pour les sorties de nuanceur vertex à la place. Consultez l’exemple [FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) pour obtenir un exemple d’émulation de Direct3D 9 Gouraud et des modes d’ombrage plat dans Direct3D 10.
-   instruction **texldp** . Une application doit implémenter une charge de texture prévue avec des instructions HLSL supplémentaires. Pour plus d’informations, consultez [Référence du langage HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) . L' [exemple FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fournit un exemple d’émulation de Texldp dans Direct3D 10.
-   Texture des **coordonnées de texture-index** (TCI)-l’état de l’étape (D3DTSS \_ TEXCOORDINDEX) n’est plus pris en charge.
-   **Fans de triangle**. Une application doit convertir des ventilateurs-ventilateurs existants en listes de triangles ou en bandes triangulaires. Pour émuler certains comportements à l’aide de DrawPrimitive dans des API plus anciennes, essayez d’utiliser DrawIndexed dans Direct3D 10. Pour plus d’informations, consultez [topologies de primitives (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) .
-   **Mise en mémoire tampon W**. La prise en charge du matériel n’est pas garantie ; Il est recommandé qu’une application utilise des mémoires tampons de profondeur haute précision à la place. Pour plus d’informations, consultez [Configuration des fonctionnalités de Depth-Stencil (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md) .
-   **Modes de retour à la ligne** (habillage des coordonnées de texture). L’encapsulation d’adresse de texture (telle que Wrap, miroir, Clamp, etc.) existe toujours. Consultez [**D3D10 \_ sampler \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) et [**D3D10 \_ texture \_ \_ mode Address**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités de l’API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
