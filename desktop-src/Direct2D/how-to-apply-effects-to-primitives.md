---
title: Comment appliquer des effets aux primitives
description: Cette rubrique montre comment appliquer une série d’effets à des primitives Direct2D et DirectWrite.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafb171c20c567d1fbd6385d23cc3b2925efc154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382375"
---
# <a name="how-to-apply-effects-to-primitives"></a><span data-ttu-id="dee90-103">Comment appliquer des effets aux primitives</span><span class="sxs-lookup"><span data-stu-id="dee90-103">How to Apply Effects to Primitives</span></span>

<span data-ttu-id="dee90-104">Cette rubrique montre comment appliquer une série d’effets à des primitives [Direct2D](./direct2d-portal.md) et [DirectWrite](direct2d-and-directwrite.md) .</span><span class="sxs-lookup"><span data-stu-id="dee90-104">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span>

<span data-ttu-id="dee90-105">Vous pouvez utiliser l' [API des effets Direct2D](effects-overview.md) pour appliquer des graphiques d’effet à des primitives rendues par [Direct2D](./direct2d-portal.md) à une image.</span><span class="sxs-lookup"><span data-stu-id="dee90-105">You can use the [Direct2D effects API](effects-overview.md) to apply effect graphs to primitives rendered by [Direct2D](./direct2d-portal.md) to an image.</span></span> <span data-ttu-id="dee90-106">L’exemple suivant comporte deux rectangles arrondis et le texte « Direct2D ».</span><span class="sxs-lookup"><span data-stu-id="dee90-106">The example here has two rounded rectangles and the text "Direct2D".</span></span> <span data-ttu-id="dee90-107">Utilisez Direct2D pour dessiner les rectangles et [DirectWrite](direct2d-and-directwrite.md) pour dessiner le texte.</span><span class="sxs-lookup"><span data-stu-id="dee90-107">Use Direct2D to draw the rectangles and [DirectWrite](direct2d-and-directwrite.md) to draw the text.</span></span>

![rectangles avec le texte « Direct2D » dans.](images/direct2d-rounded.png)

<span data-ttu-id="dee90-109">À l’aide des [effets Direct2D](effects-overview.md), vous pouvez faire en sorte que cette image ressemble à l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="dee90-109">Using [Direct2D effects](effects-overview.md), you can make this image look like the next image.</span></span> <span data-ttu-id="dee90-110">Appliquez la [flou gaussien](gaussian-blur.md), [pointez l’éclairage spéculaire](specular-lighting.md), le [composite arithmétique](arithmetic-composite.md)et les effets [composites](composite.md) aux primitives 2D pour créer l’image ici.</span><span class="sxs-lookup"><span data-stu-id="dee90-110">Apply the [Gaussian Blur](gaussian-blur.md), [Point Specular Lighting](specular-lighting.md), [Arithmetic Composite](arithmetic-composite.md), and [Composite](composite.md) effects to the 2D primitives to create the image here.</span></span>

![les rectangles avec le texte « Direct2D » dans après plusieurs effets sont appliqués.](images/direct2d-svg.png)

<span data-ttu-id="dee90-112">Une fois que vous avez effectué le rendu des rectangles et du texte sur une surface intermédiaire, vous pouvez l’utiliser comme entrée pour les objets [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) dans le graphique d’images.</span><span class="sxs-lookup"><span data-stu-id="dee90-112">After you render the rectangles and text to a intermediate surface, you can use this as input for [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects in the image graph.</span></span>

<span data-ttu-id="dee90-113">Dans cet exemple, définissez l’image d’origine comme entrée pour l' [effet de flou gaussien](gaussian-blur.md) , puis définissez la sortie du flou comme entrée pour l' [effet d’éclairage spéculaire](specular-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="dee90-113">In this example, set the original image as the input to the [Gaussian Blur effect](gaussian-blur.md) and then set the output of the blur as the input for the [Point Specular Lighting effect](specular-lighting.md).</span></span> <span data-ttu-id="dee90-114">Le résultat de cet effet est ensuite composite avec l’image d’origine à deux reprises pour obtenir l’image finale rendue dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dee90-114">The result of this effect is then composited with the original image twice to get the final image that is rendered to the window.</span></span>

<span data-ttu-id="dee90-115">Voici un diagramme du graphique de l’image.</span><span class="sxs-lookup"><span data-stu-id="dee90-115">Here is a diagram of the image graph.</span></span>

![diagramme de graphique d’effet.](images/effect-graph.png)

<span data-ttu-id="dee90-117">Ce graphique d’effet est constitué de quatre objets [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , chacun représentant un effet intégré différent.</span><span class="sxs-lookup"><span data-stu-id="dee90-117">This effect graph consists of four [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects, each representing a different built-in effect.</span></span> <span data-ttu-id="dee90-118">Vous pouvez créer et connecter des effets personnalisés de la même manière, après les avoir enregistrés à l’aide de [**ID1D1Factory1 :: RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span><span class="sxs-lookup"><span data-stu-id="dee90-118">You can create and connect custom effects in the same way, after you register them using [**ID1D1Factory1::RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span></span> <span data-ttu-id="dee90-119">Le code ci-dessous crée les effets, définit les propriétés et connecte le graphique d’effet présenté précédemment.</span><span class="sxs-lookup"><span data-stu-id="dee90-119">The code here creates the effects, sets the properties, and connects the effect graph shown earlier.</span></span>

1.  <span data-ttu-id="dee90-120">Créez l’effet [flou gaussien](gaussian-blur.md) à l’aide de la méthode [**ID2D1DeviceContext :: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) et en spécifiant le CLSID approprié.</span><span class="sxs-lookup"><span data-stu-id="dee90-120">Create the [Gaussian blur](gaussian-blur.md) effect using the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method and specifying the proper CLSID.</span></span> <span data-ttu-id="dee90-121">Les CLSID des effets intégrés sont définis dans d2d1effects. h.</span><span class="sxs-lookup"><span data-stu-id="dee90-121">The CLSIDs for the built-in effects are defined in d2d1effects.h.</span></span> <span data-ttu-id="dee90-122">Vous définissez ensuite l’écart type du flou à l’aide de la méthode [**ID2D1Effect :: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .</span><span class="sxs-lookup"><span data-stu-id="dee90-122">You then set the standard deviation of the blur using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

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

    

    <span data-ttu-id="dee90-123">L’effet [flou gaussien](gaussian-blur.md) brouille tous les canaux de l’image, y compris le canal alpha.</span><span class="sxs-lookup"><span data-stu-id="dee90-123">The [Gaussian blur](gaussian-blur.md) effect blurs all of the channels of the image, including the alpha channel.</span></span>

2.  <span data-ttu-id="dee90-124">Créez l’effet d' [éclairage spéculaire](point-specular.md) et définissez les propriétés.</span><span class="sxs-lookup"><span data-stu-id="dee90-124">Create the [specular lighting](point-specular.md) effect and set the properties.</span></span> <span data-ttu-id="dee90-125">La position de la lumière est un vecteur de 3 valeurs à virgule flottante. vous devez donc la déclarer en tant que variable distincte et la passer à la méthode [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .</span><span class="sxs-lookup"><span data-stu-id="dee90-125">The position of the light is a vector of 3 floating point values, so you must declare it as a separate variable and pass it to the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

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

    

    <span data-ttu-id="dee90-126">L’effet d' [éclairage spéculaire](point-specular.md) utilise le canal alpha de l’entrée pour créer une carte de hauteur pour l’éclairage.</span><span class="sxs-lookup"><span data-stu-id="dee90-126">The [specular lighting](point-specular.md) effect uses the alpha channel of the input to create a height map for the lighting.</span></span>

3.  <span data-ttu-id="dee90-127">Il existe deux effets composites différents que vous pouvez utiliser pour l’effet [composite](composite.md) et le [composite arithmétique](arithmetic-composite.md).</span><span class="sxs-lookup"><span data-stu-id="dee90-127">There are two different composite effects that you can use the [composite](composite.md) effect and the [arithmetic composite](arithmetic-composite.md).</span></span> <span data-ttu-id="dee90-128">Ce graphique d’effet utilise les deux.</span><span class="sxs-lookup"><span data-stu-id="dee90-128">This effect graph uses both.</span></span>

    <span data-ttu-id="dee90-129">Créez l’effet [composite](composite.md) et définissez le mode d2d1 \_ composite \_ mode \_ source \_ dans, qui génère l’intersection des images source et de destination.</span><span class="sxs-lookup"><span data-stu-id="dee90-129">Create the [composite](composite.md) effect and set the mode to D2D1\_COMPOSITE\_MODE\_SOURCE\_IN, which outputs the intersection of the source and destination images.</span></span>

    <span data-ttu-id="dee90-130">L’effet [composite arithmétique](arithmetic-composite.md) compose les deux images d’entrée en fonction d’une formule définie par le World Wide Web Consortium (W3C) pour la norme SVG (Scalable Vector Graphics).</span><span class="sxs-lookup"><span data-stu-id="dee90-130">The [arithmetic composite](arithmetic-composite.md) effect composes the two input images based on a formula defined by the World Wide Web Consortium (W3C) for the Scalable Vector Graphics (SVG) standard.</span></span> <span data-ttu-id="dee90-131">Créez un composite arithmétique et définissez les coefficients pour la formule.</span><span class="sxs-lookup"><span data-stu-id="dee90-131">Create arithmetic composite and set the coefficients for the formula.</span></span>

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

    

    <span data-ttu-id="dee90-132">Les coefficients pour l’effet [composite arithmétique](arithmetic-composite.md) sont indiqués ici.</span><span class="sxs-lookup"><span data-stu-id="dee90-132">The coefficients for the [arithmetic composite](arithmetic-composite.md) effect are shown here.</span></span>

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    <span data-ttu-id="dee90-133">Dans ce graphique d’effet, les deux effets composites prennent la sortie des autres effets et la surface intermédiaire comme entrées et les composent.</span><span class="sxs-lookup"><span data-stu-id="dee90-133">In this effect graph, both of the composite effects take the output of the other effects and the intermediate surface as inputs and composites them.</span></span>

4.  <span data-ttu-id="dee90-134">Enfin, vous connectez les effets pour former le graphique en définissant les entrées sur les images et les bitmaps appropriées.</span><span class="sxs-lookup"><span data-stu-id="dee90-134">Finally, you connect the effects to form the graph by setting the inputs to the proper images and bitmaps.</span></span>

    <span data-ttu-id="dee90-135">Le premier effet, [gaussien flou](gaussian-blur.md), reçoit son entrée de la surface intermédiaire à laquelle vous avez rendu les primitives.</span><span class="sxs-lookup"><span data-stu-id="dee90-135">The first effect, [Gaussian blur](gaussian-blur.md), receives its input from the intermediate surface that you rendered the primitives to.</span></span> <span data-ttu-id="dee90-136">Vous définissez l’entrée à l’aide de la méthode [**ID2D1Effect :: SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) et en spécifiant l’index d’un objet [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) .</span><span class="sxs-lookup"><span data-stu-id="dee90-136">You set the input using the [**ID2D1Effect::SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method and specifying the index of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) object.</span></span> <span data-ttu-id="dee90-137">Les effets Flou gaussien et [éclairage spéculaire](point-specular.md) n’ont qu’une seule entrée.</span><span class="sxs-lookup"><span data-stu-id="dee90-137">The Gaussian blur and [specular lighting](point-specular.md) effects have only a single input.</span></span> <span data-ttu-id="dee90-138">L’effet d’éclairage spéculaire utilise le canal alpha flou du flou gaussien</span><span class="sxs-lookup"><span data-stu-id="dee90-138">The specular lighting effect uses the blurred alpha channel of the Gaussian blur</span></span>

    <span data-ttu-id="dee90-139">Les effets composites [composite](composite.md) et [arithmétiques](arithmetic-composite.md) ont plusieurs entrées.</span><span class="sxs-lookup"><span data-stu-id="dee90-139">The [composite](composite.md) and [arithmetic composite](arithmetic-composite.md) effects have multiple inputs.</span></span> <span data-ttu-id="dee90-140">Pour vous assurer que les images sont rassemblées dans le bon ordre, vous devez spécifier l’index correct pour chaque image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="dee90-140">To make sure the images are put together in the right order, you must specify the correct index for each input image.</span></span>

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

    

5.  <span data-ttu-id="dee90-141">Transmettez l’objet d’effet [composite arithmétique](arithmetic-composite.md) dans la méthode [**ID2DDeviceContext ::D rawimage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) et il traite et dessine la sortie du graphique.</span><span class="sxs-lookup"><span data-stu-id="dee90-141">Pass the [arithmetic composite](arithmetic-composite.md) effect object into the [**ID2DDeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method and it processes and draws the output of the graph.</span></span>

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

    

 

 