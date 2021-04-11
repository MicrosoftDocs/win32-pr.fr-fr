---
title: Utilisation de Color dans Direct2D
description: Utilisation de Color dans Direct2D
ms.assetid: 74b1f12c-b1de-4df1-85ba-0cf7a0009499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb195a4ad0bdd9ff32f1123a8a57ff2ce0aadbde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314825"
---
# <a name="using-color-in-direct2d"></a>Utilisation de Color dans Direct2D

Direct2D utilise le modèle de couleurs RVB, dans lequel les couleurs sont formées en combinant différentes valeurs de rouge, de vert et de bleu. Un quatrième composant, alpha, mesure la transparence d’un pixel. Dans Direct2D, chacun de ces composants est une valeur à virgule flottante avec une plage de \[ 0,0 1,0 \] . Pour les trois composants de couleur, la valeur mesure l’intensité de la couleur. Pour le composant alpha, 0,0 signifie complètement transparent et 1,0 signifie complètement opaque. Le tableau suivant présente les couleurs qui résultent de différentes combinaisons de 100% d’intensité.



| Rouge | Vert | Bleu | Color   |
|-----|-------|------|---------|
| 0   | 0     | 0    | Noir   |
| 1   | 0     | 0    | Rouge     |
| 0   | 1     | 0    | Vert   |
| 0   | 0     | 1    | Bleu    |
| 0   | 1     | 1    | Cyan    |
| 1   | 0     | 1    | Magenta |
| 1   | 1     | 0    | Yellow  |
| 1   | 1     | 1    | Blancs   |



 

![image qui affiche les couleurs RVB.](images/graphics13.png)

Les valeurs de couleur comprises entre 0 et 1 produisent des nuances différentes de ces couleurs pures. Direct2D utilise la structure de [**\_ couleur d2d1 \_ F**](/windows/desktop/Direct2D/d2d1-color-f) pour représenter les couleurs. Par exemple, le code suivant spécifie magenta.


```C++
    // Initialize a magenta color.

    D2D1_COLOR_F clr;
    clr.r = 1;
    clr.g = 0;
    clr.b = 1;
    clr.a = 1;  // Opaque.
```



Vous pouvez également spécifier une couleur à l’aide de la classe [**d2d1 :: ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) , qui dérive de la structure de [**\_ couleur d2d1 \_ F**](/windows/desktop/Direct2D/d2d1-color-f) .


```C++
    // Equivalent to the previous example.

    D2D1::ColorF clr(1, 0, 1, 1);
```



## <a name="alpha-blending"></a>Fusion alpha

La fusion alpha crée des zones translucides en fusionnant la couleur de premier plan avec la couleur d’arrière-plan, à l’aide de la formule suivante.

<dl> couleur = AF * CF + (1-AF) * CB  
</dl>

où *CB* est la couleur d’arrière-plan, *CF* correspond à la couleur de premier plan et *AF* à la valeur alpha de la couleur de premier plan. Cette formule est appliquée par paire à chaque composant de couleur. Par exemple, supposons que la couleur de premier plan est **(R = 1,0, G = 0,4, B = 0,0)**, avec **alpha = 0,6** et que la couleur d’arrière-plan est **(R = 0,0, G = 0,5, B = 1,0)**. La couleur de fusion alpha résultante est la suivante :

R = (1,0 * 0,6 + 0 * 0,4) =. 6   
G = (0,4 * 0,6 + 0,5 * 0,4) =. 44  
B = (0 * 0,6 + 1,0 * 0,4) =. 40  

L’illustration suivante montre le résultat de cette opération de fusion.

![image qui affiche la fusion alpha.](images/graphics15.png)

## <a name="pixel-formats"></a>Formats de pixel

La structure de [**\_ couleur d2d1 \_ F**](/windows/desktop/Direct2D/d2d1-color-f) ne décrit pas comment un pixel est représenté en mémoire. Dans la plupart des cas, cela n’a pas d’importance. Direct2D gère tous les détails internes de la traduction des informations de couleur en pixels. Toutefois, vous devrez peut-être connaître le format de pixel si vous travaillez directement avec une bitmap en mémoire, ou si vous combinez Direct2D avec Direct3D ou GDI.

L’énumération de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) définit une liste de formats de pixel. La liste est relativement longue, mais seules quelques-unes d’entre elles sont pertinentes pour Direct2D. (Les autres sont utilisés par Direct3D).



| Format de pixel                                                                                                                           | Description                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>**DXGI \_ format \_ B8G8R8A8 \_ UNORM**<br/> | Il s’agit du format de pixel le plus courant. Tous les composants de pixel (rouge, vert, bleu et alpha) sont des entiers non signés 8 bits. Les composants sont organisés dans l’ordre *BGRA* en mémoire. (Voir l’illustration qui suit.)<br/>                                          |
| <span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>**DXGI \_ format \_ R8G8B8A8 \_ UNORM**<br/> | Les composants de pixel sont des entiers non signés 8 bits, dans l’ordre *RVBA* . En d’autres termes, les composants rouge et bleu sont permutés, par rapport au **\_ format dxgi \_ B8G8R8A8 \_ UNORM**. Ce format est pris en charge uniquement pour les périphériques matériels.<br/>                             |
| <span id="DXGI_FORMAT_A8_UNORM"></span><span id="dxgi_format_a8_unorm"></span>**\_Format dxgi \_ a8 \_ UNORM**<br/>                   | Ce format contient un composant alpha de 8 bits, sans composants RGB. Il est utile pour créer des masques d’opacité. Pour en savoir plus sur l’utilisation des masques d’opacité dans Direct2D, consultez [vue d’ensemble des cibles de rendu a8 compatibles](/windows/desktop/Direct2D/compatible-a8-rendertargets).<br/> |



 

L’illustration suivante montre la disposition des pixels BGRA.

![diagramme qui affiche la disposition en pixels BGRA.](images/graphics14.png)

Pour obtenir le format de pixel d’une cible de rendu, appelez [**ID2D1RenderTarget :: GetPixelFormat**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat). Le format de Pixel peut ne pas correspondre à la résolution d’affichage. Par exemple, l’affichage peut être défini sur une couleur de 16 bits, même si la cible de rendu utilise la couleur 32 bits.

### <a name="alpha-mode"></a>Mode Alpha

Une cible de rendu a également un mode alpha, qui définit la manière dont les valeurs alpha sont traitées.



| Mode Alpha                           | Description                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D2D1 \_ \_ mode Alpha \_ ignore**        | Aucune fusion alpha n’est effectuée. Les valeurs alpha sont ignorées.                                                                                                                                                                                                                                                                          |
| **\_Mode d2d1 \_ alpha \_ simple**      | Alpha direct. Les composants de couleur du pixel représentent l’intensité de couleur avant la fusion alpha.                                                                                                                                                                                                                           |
| **D2D1 \_ \_ mode Alpha \_ prémultiplié** | Alpha prémultiplié. Les composants de couleur du pixel représentent l’intensité de couleur multipliée par la valeur alpha. Ce format est plus efficace à afficher que la valeur alpha directe, car le terme (AF CF) de la formule de fusion alpha est précalculé. Toutefois, ce format n’est pas approprié pour le stockage dans un fichier image. |



 

Voici un exemple de la différence entre alpha simple et prémultiplié par Alpha. Supposons que la couleur souhaitée est un rouge pur (100% d’intensité) avec 50% alpha. En tant que type Direct2D, cette couleur est représentée sous la forme (1, 0, 0, 0,5). À l’aide de la composante alpha directe et en supposant que les composants de couleur 8 bits, le composant rouge du pixel est 0xFF. À l’aide de l’alpha prémultiplié, le composant rouge est mis à l’échelle de 50% à égal à 0x80.

Le type de données [**d2d1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) représente toujours les couleurs à l’aide de l’alpha simple. Direct2D convertit les pixels en format alpha prémultiplié, si nécessaire.

Si vous savez que votre programme n’effectuera aucune fusion alpha, créez la cible de rendu en utilisant le mode Alpha **d2d1 \_ \_ \_ Ignorer** le mode Alpha. Ce mode peut améliorer les performances, car Direct2D peut ignorer les calculs alpha. Pour plus d’informations, consultez [amélioration des performances des applications Direct2D](/windows/desktop/Direct2D/improving-direct2d-performance).

## <a name="next"></a>Suivant

[Application de transformations dans Direct2D](applying-transforms-in-direct2d.md)

 

