---
description: Cette rubrique décrit les considérations et les stratégies d’optimisation avec la bibliothèque DirectXMath.
ms.assetid: bcbf8ae1-ed49-fdf7-812d-b2089537ab28
title: Optimisation du code avec la bibliothèque DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c88657115f026eee4c4ce8dd51075c03a50e272
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520646"
---
# <a name="code-optimization-with-the-directxmath-library"></a>Optimisation du code avec la bibliothèque DirectXMath

Cette rubrique décrit les considérations et les stratégies d’optimisation avec la bibliothèque DirectXMath.

-   [Utiliser des accesseurs avec modération](#use-accessors-sparingly)
-   [Utiliser les paramètres de compilation corrects](#use-correct-compilation-settings)
-   [Utiliser les fonctions est lorsque cela est approprié](#use-est-functions-when-appropriate)
-   [Utiliser des types de données alignés et des opérations](#use-aligned-data-types-and-operations)
-   [Aligner correctement les allocations](#properly-align-allocations)
-   [Éviter les surcharges d’opérateur lorsque cela est possible](#avoid-operator-overloads-when-possible)
-   [Nombres dénormalisés](#denormals)
-   [Tirez parti de la double de la virgule flottante entière](#take-advantage-of-the-integer-floating-point-duality)
-   [Préférer les formulaires de modèle](#prefer-template-forms)
-   [Utilisation de DirectXMath avec Direct3D](#using-directxmath-with-direct3d)
-   [Rubriques connexes](#related-topics)

## <a name="use-accessors-sparingly"></a>Utiliser des accesseurs avec modération

Les opérations basées sur des vecteurs utilisent les jeux d’instructions SIMD et utilisent des registres spéciaux. L’accès à des composants individuels nécessite de passer des registres SIMD aux types scalaires, puis de les replacer.

Dans la mesure du possible, il est plus efficace d’initialiser tous les composants d’un [**XMVECTOR**](xmvector-data-type.md) à la fois, au lieu d’utiliser une série d’accesseurs vectoriels individuels.

## <a name="use-correct-compilation-settings"></a>Utiliser les paramètres de compilation corrects

pour Windows cibles x86, activez/arch : SSE2. pour toutes les cibles de Windows, activez/fp : fast.

Par défaut, la compilation par rapport à la bibliothèque DirectXMath pour les cibles x86 des fenêtres est effectuée avec des \_ \_ \_ intrinsèques SSE \_ définis. Cela signifie que toutes les fonctionnalités de DirectXMath utilisent des instructions SSE2. Toutefois, ce n’est pas le cas pour un autre code.

Le code en dehors de DirectXMath est géré à l’aide des valeurs par défaut du compilateur. Sans ce commutateur, le code généré peut souvent utiliser le code X87 moins efficace.

Nous vous recommandons vivement de toujours utiliser la dernière version disponible du compilateur.

## <a name="use-est-functions-when-appropriate"></a>Utiliser les fonctions est lorsque cela est approprié

De nombreuses fonctions ont une fonction d’estimation équivalente se terminant par est. Ces fonctions échangent une certaine précision pour améliorer les performances. Les fonctions est appropriées pour les calculs non critiques où la précision peut être sacrifiée à la vitesse. La quantité exacte de précision et d’augmentation de la vitesse perdue dépend de la plateforme.

Par exemple, la fonction [**XMVector3AngleBetweenNormalsEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) peut être utilisée à la place de la fonction [**XMVector3AngleBetweenNormals**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals) .

## <a name="use-aligned-data-types-and-operations"></a>Utiliser des types de données alignés et des opérations

Les jeux d’instructions SIMD sur les versions de Windows prenant en charge SSE2 ont généralement des versions alignées et non alignées des opérations de mémoire. L’utilisation des opérations alignées est plus rapide et doit être préférable dans la mesure du possible.

La bibliothèque DirectXMath fournit des fonctionnalités alignées et non alignées par le biais de types de vecteurs variants, d’une structure et de fonctions. Ces variantes sont indiquées par un « A » à la fin du nom.

Par exemple, il existe une structure [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) non alignée et une structure [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) alignée, qui sont utilisées respectivement par les fonctions [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) et [**XMStoreFloat4A**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a) .

## <a name="properly-align-allocations"></a>Aligner correctement les allocations

Les versions alignées des intrinsèques [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) sous-jacents de la bibliothèque DirectXMath sont plus rapides que le non aligné.

Pour cette raison, les opérations DirectXMath utilisant des objets [**XMVECTOR**](xmvector-data-type.md) et [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) supposent que ces objets sont alignés sur 16 octets. cela est automatique pour les allocations basées sur la pile, si le code est compilé par rapport à la bibliothèque DirectXMath à l’aide de la Windows recommandée (consultez [utiliser la Compilation correcte Paramètres](#use-correct-compilation-settings)) paramètres du compilateur. Toutefois, il est important de s’assurer que l’allocation du tas contenant les objets **XMVECTOR** et **XMMATRIX** , ou les casts vers ces types, répondent à ces exigences d’alignement.

alors que les allocations de mémoire 64 bits Windows sont alignées sur 16 octets, par défaut sur les versions 32 bits de Windows mémoire allouée est uniquement alignée sur 8 octets. Pour plus d’informations sur le contrôle de l’alignement de la mémoire, consultez [ \_ \_ malloc aligné](/cpp/c-runtime-library/reference/aligned-malloc).

Lorsque vous utilisez des types DirectXMath alignés avec la bibliothèque STL (Standard Template Library), vous devez fournir un allocateur personnalisé qui garantit l’alignement sur 16 octets. Consultez le [blog](https://devblogs.microsoft.com/cppblog/the-mallocator/) de l’équipe Visual C++ pour obtenir un exemple d’écriture d’un allocateur personnalisé (au lieu de malloc/Free, vous souhaiterez utiliser \_ \_ le malloc aligné et l' \_ alignement \_ gratuit dans votre implémentation).

> [!Note]  
> Certains modèles STL modifient l’alignement du type fourni. Par exemple, [créez un \_<>partagé ](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true) pour ajouter des informations de suivi internes qui peuvent ou non respecter l’alignement du type d’utilisateur fourni, ce qui entraîne des données membres non alignées. Dans ce cas, vous devez utiliser des types non alignés au lieu de types alignés. si vous dérivez de classes existantes, y compris de nombreux objets Windows Runtime, vous pouvez également modifier l’alignement d’une classe ou d’une structure.

 

## <a name="avoid-operator-overloads-when-possible"></a>Éviter les surcharges d’opérateur lorsque cela est possible

En guise de fonctionnalité pratique, plusieurs types tels que [**XMVECTOR**](xmvector-data-type.md) et [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) ont des surcharges d’opérateur pour les opérations arithmétiques courantes. Ces surcharges d’opérateur ont tendance à créer de nombreux objets temporaires. Nous vous recommandons d’éviter ces surcharges d’opérateur dans le code qui respecte les performances.

## <a name="denormals"></a>Nombres dénormalisés

Pour prendre en charge les calculs proches de 0, la norme IEEE 754 à virgule flottante prend en charge le débordement graduel. Un dépassement de capacité négatif graduel est implémenté par le biais de l’utilisation de valeurs dénormalisées, et de nombreuses implémentations matérielles sont lentes lors de la gestion des dénormals. Une optimisation à prendre en compte est la désactivation de la gestion des dénormals pour les opérations vectorielles utilisées par DirectXMath.

La modification de la gestion des dénormals s’effectue à l’aide de la routine [ \_ controlfp \_ s](/cpp/c-runtime-library/reference/controlfp-s) sur une base pré-thread, ce qui peut améliorer les performances. Utilisez ce code pour modifier la gestion des dénormals :


```
  #include <float.h>;
    unsigned int control_word;
    _controlfp_s( &control_word, _DN_FLUSH, _MCW_DN );
```



> [!Note]  
> sur les versions 64 bits de Windows, les instructions [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) sont utilisées pour tous les calculs, pas seulement pour les opérations de vecteur. La modification du traitement dénormal affecte tous les calculs à virgule flottante dans votre programme, pas seulement les opérations vectorielles utilisées par DirectXMath.

 

## <a name="take-advantage-of-the-integer-floating-point-duality"></a>Tirez parti de la double de la virgule flottante entière

DirectXMath prend en charge les vecteurs de 4 valeurs à virgule flottante simple précision ou 4 32 bits (signé ou non signé).

Étant donné que les jeux d’instructions utilisés pour implémenter la bibliothèque DirectXMath peuvent traiter les mêmes données que plusieurs types différents, par exemple, traiter le même vecteur comme des données à virgule flottante et des entiers, certaines optimisations peuvent être réalisées. Vous pouvez utiliser ces optimisations à l’aide des routines d’initialisation de vecteur entier et des opérateurs de bits pour manipuler les valeurs à virgule flottante.

Le format binaire des nombres à virgule flottante simple précision utilisé par la bibliothèque DirectXMath est entièrement conforme à la norme IEEE 764 :

``` syntax
     SIGN    EXPONENT   MANTISSA
     X       XXXXXXXX   XXXXXXXXXXXXXXXXXXXXXXX
     1 bit   8 bits     23 bits
```

Lorsque vous utilisez le nombre à virgule flottante simple précision IEEE 764, il est important de garder à l’esprit que certaines représentations ont une signification particulière (autrement dit, elles ne sont pas conformes à la description précédente). Voici quelques exemples :

-   Un zéro positif est 0
-   Zéro négatif est 0x80000000
-   Q \_ NaN est 07FC0000
-   + INF est 0x7F800000
-   -Le fichier INF est 0xFF800000

## <a name="prefer-template-forms"></a>Préférer les formulaires de modèle

Le formulaire de modèle existe pour [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle), [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert), [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft), [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)et [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright). L’utilisation de ces fonctions au lieu du formulaire de fonction générale permet au compilateur de créer des implémentations bien plus efficent. Pour [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)), cette valeur est souvent réduite à une ou deux \_ mm \_ \_ . Pour ARM-néon, le modèle **XMVectorSwizzle** peut utiliser un certain nombre de cas spéciaux plutôt que les Swizzle/permutements VTBL plus généraux.

## <a name="using-directxmath-with-direct3d"></a>Utilisation de DirectXMath avec Direct3D

Une utilisation courante de DirectXMath consiste à effectuer des calculs graphiques à utiliser avec Direct3D. Avec Direct3D 10. x et Direct3D 11. x, vous pouvez utiliser la bibliothèque DirectXMath de l’une des façons suivantes :

-   Utilisez les [constantes](ovw-xnamath-reference-constants.md) d’espace de noms de couleurs directement dans le paramètre *ColorRGBA* dans un appel à la méthode [**ID3D11DeviceContext :: ClearRenderTargetView**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview) ou [**ID3D10Device :: ClearRenderTargetView**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview) . Pour Direct3D 9, vous devez effectuer la conversion vers le type [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) pour l’utiliser comme paramètre *Color* dans un appel à la méthode [**IDirect3DDevice9 :: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) .
-   Utilisez les types [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) / [**XMVECTOR**](xmvector-data-type.md) et [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) pour configurer des structures de mémoire tampon constantes pour les références par les types HLSL [**float4**](../direct3dhlsl/dx-graphics-hlsl-scalar.md) ou [**Matrix**](../direct3dhlsl/dx-graphics-hlsl-matrix.md)/float4x4.
    > [!Note]  
    > [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / Les types [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) sont au format de ligne principale. Par conséquent, si vous utilisez le commutateur de compilateur/ZPR (indicateur de compilation [**\_ \_ \_ colonne \_ principale de matrice D3DCOMPILE**](../direct3dhlsl/d3dcompile-constants.md) ) ou si \_ vous [](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md) déclarez le type de matrice en HLSL, vous devez transposer la matrice lorsque vous la définissez dans la mémoire tampon constante.

     

-   Avec Direct3D 10. x et Direct3D 11. x, vous pouvez supposer que le pointeur retourné par la méthode Map (par exemple, [**ID3D11DeviceContext :: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) dans le membre **pData** ([**D3D10 \_ mappé \_ TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d).**pData**, [**D3D10 \_ mappé \_ TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d).**pData**, ou sous- [**\_ \_ ressource mappée d3d11**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource).**pData**) est aligné sur 16 octets si vous utilisez le [niveau de fonctionnalité](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ 0 ou une valeur supérieure, ou chaque fois que vous utilisez des ressources de mise en [**\_ \_ lots de l’utilisation de d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>
