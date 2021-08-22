---
title: Comment appliquer des effets aux primitives
description: cette rubrique montre comment appliquer une série d’effets à Direct2D et DirectWrite primitives.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c17cbf1efe17d1c23c90382f3b95fb41e33946a93935b0be02fc5b41f314a8c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569580"
---
# <a name="how-to-apply-effects-to-primitives"></a>Comment appliquer des effets aux primitives

cette rubrique montre comment appliquer une série d’effets à [Direct2D](./direct2d-portal.md) et [DirectWrite](direct2d-and-directwrite.md) primitives.

Vous pouvez utiliser l' [API des effets Direct2D](effects-overview.md) pour appliquer des graphiques d’effet à des primitives rendues par [Direct2D](./direct2d-portal.md) à une image. L’exemple suivant comporte deux rectangles arrondis et le texte « Direct2D ». utilisez Direct2D pour dessiner les rectangles et les [DirectWrite](direct2d-and-directwrite.md) pour dessiner le texte.

![rectangles avec le texte « Direct2D » dans.](images/direct2d-rounded.png)

À l’aide des [effets Direct2D](effects-overview.md), vous pouvez faire en sorte que cette image ressemble à l’image suivante. Appliquez la [flou gaussien](gaussian-blur.md), [pointez l’éclairage spéculaire](specular-lighting.md), le [composite arithmétique](arithmetic-composite.md)et les effets [composites](composite.md) aux primitives 2D pour créer l’image ici.

![les rectangles avec le texte « Direct2D » dans après plusieurs effets sont appliqués.](images/direct2d-svg.png)

Une fois que vous avez effectué le rendu des rectangles et du texte sur une surface intermédiaire, vous pouvez l’utiliser comme entrée pour les objets [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) dans le graphique d’images.

Dans cet exemple, définissez l’image d’origine comme entrée pour l' [effet de flou gaussien](gaussian-blur.md) , puis définissez la sortie du flou comme entrée pour l' [effet d’éclairage spéculaire](specular-lighting.md). Le résultat de cet effet est ensuite composite avec l’image d’origine à deux reprises pour obtenir l’image finale rendue dans la fenêtre.

Voici un diagramme du graphique de l’image.

![diagramme de graphique d’effet.](images/effect-graph.png)

Ce graphique d’effet est constitué de quatre objets [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , chacun représentant un effet intégré différent. Vous pouvez créer et connecter des effets personnalisés de la même manière, après les avoir enregistrés à l’aide de [**ID1D1Factory1 :: RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring). Le code ci-dessous crée les effets, définit les propriétés et connecte le graphique d’effet présenté précédemment.

1.  Créez l’effet [flou gaussien](gaussian-blur.md) à l’aide de la méthode [**ID2D1DeviceContext :: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) et en spécifiant le CLSID approprié. Les CLSID des effets intégrés sont définis dans d2d1effects. h. Vous définissez ensuite l’écart type du flou à l’aide de la méthode [**ID2D1Effect :: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .

    ```C++
    // Create the Gaussian Blur Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect)
        );

    // Set the blur amount
    DX::ThrowIfFailed(
        gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, sc_gaussianBlurStDev)
        );
    ```

    

    L’effet [flou gaussien](gaussian-blur.md) brouille tous les canaux de l’image, y compris le canal alpha.

2.  Créez l’effet d' [éclairage spéculaire](point-specular.md) et définissez les propriétés. La position de la lumière est un vecteur de 3 valeurs à virgule flottante. vous devez donc la déclarer en tant que variable distincte et la passer à la méthode [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .

    ```C++
    // Create the Specular Lighting Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1PointSpecular, &specularLightingEffect)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, sc_specularLightPosition)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, sc_specularExponent)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, sc_specularSurfaceScale)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, sc_specularConstant)
        );
    ```

    

    L’effet d' [éclairage spéculaire](point-specular.md) utilise le canal alpha de l’entrée pour créer une carte de hauteur pour l’éclairage.

3.  Il existe deux effets composites différents que vous pouvez utiliser pour l’effet [composite](composite.md) et le [composite arithmétique](arithmetic-composite.md). Ce graphique d’effet utilise les deux.

    Créez l’effet [composite](composite.md) et définissez le mode d2d1 \_ composite \_ mode \_ source \_ dans, qui génère l’intersection des images source et de destination.

    L’effet [composite arithmétique](arithmetic-composite.md) compose les deux images d’entrée en fonction d’une formule définie par le World Wide Web Consortium (W3C) pour la norme SVG (Scalable Vector Graphics). Créez un composite arithmétique et définissez les coefficients pour la formule.

    ```C++
    // Create the Composite Effects
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect)
        );

    DX::ThrowIfFailed(
        compositeEffect->SetValue(D2D1_COMPOSITE_PROP_MODE, D2D1_COMPOSITE_MODE_SOURCE_IN)
        );

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &m_arithmeticCompositeEffect)
        );

    DX::ThrowIfFailed(
        m_arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, sc_arithmeticCoefficients)
        );
    ```

    

    Les coefficients pour l’effet [composite arithmétique](arithmetic-composite.md) sont indiqués ici.

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    Dans ce graphique d’effet, les deux effets composites prennent la sortie des autres effets et la surface intermédiaire comme entrées et les composent.

4.  Enfin, vous connectez les effets pour former le graphique en définissant les entrées sur les images et les bitmaps appropriées.

    Le premier effet, [gaussien flou](gaussian-blur.md), reçoit son entrée de la surface intermédiaire à laquelle vous avez rendu les primitives. Vous définissez l’entrée à l’aide de la méthode [**ID2D1Effect :: SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) et en spécifiant l’index d’un objet [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) . Les effets Flou gaussien et [éclairage spéculaire](point-specular.md) n’ont qu’une seule entrée. L’effet d’éclairage spéculaire utilise le canal alpha flou du flou gaussien

    Les effets composites [composite](composite.md) et [arithmétiques](arithmetic-composite.md) ont plusieurs entrées. Pour vous assurer que les images sont rassemblées dans le bon ordre, vous devez spécifier l’index correct pour chaque image d’entrée.

    ```C++
    // Connect the graph.
    // Apply a blur effect to the original image.
    gaussianBlurEffect->SetInput(0, m_inputImage.Get());

    // Apply a specular lighting effect to the result.
    specularLightingEffect->SetInputEffect(0, gaussianBlurEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    compositeEffect->SetInput(0, m_inputImage.Get());
    compositeEffect->SetInputEffect(1, specularLightingEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    m_arithmeticCompositeEffect->SetInput(0, m_inputImage.Get());
    m_arithmeticCompositeEffect->SetInputEffect(1, compositeEffect.Get());
    ```

    

5.  Transmettez l’objet d’effet [composite arithmétique](arithmetic-composite.md) dans la méthode [**ID2DDeviceContext ::D rawimage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) et il traite et dessine la sortie du graphique.

    ```C++
        // Draw the output of the effects graph.
        m_d2dContext->DrawImage(
            m_arithmeticCompositeEffect.Get(),
            D2D1::Point2F(
                (size.width - sc_inputBitmapSize.width) / 2,
                (size.height - sc_inputBitmapSize.height) / 2 + sc_offset
                )
            );
    ```

    

 

 