---
title: Effets (Direct2D)
description: Vue d’ensemble des effets Direct2D.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd29a4b2968e91bd0d516a74ec01538f69821bb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031607"
---
# <a name="effects"></a><span data-ttu-id="324e5-103">Effets</span><span class="sxs-lookup"><span data-stu-id="324e5-103">Effects</span></span>

## <a name="what-are-direct2d-effects"></a><span data-ttu-id="324e5-104">Que sont les effets de Direct2D ?</span><span class="sxs-lookup"><span data-stu-id="324e5-104">What are Direct2D effects?</span></span>

<span data-ttu-id="324e5-105">Vous pouvez utiliser Direct2D pour appliquer un ou plusieurs effets de haute qualité à une image ou à un ensemble d’images.</span><span class="sxs-lookup"><span data-stu-id="324e5-105">You can use Direct2D to apply one or more high quality effects to an image or a set of images.</span></span> <span data-ttu-id="324e5-106">Les API Effects sont basées sur [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) et tirent parti des fonctionnalités GPU pour le traitement des images.</span><span class="sxs-lookup"><span data-stu-id="324e5-106">The effects APIs are built on [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) and take advantage of GPU features for image processing.</span></span> <span data-ttu-id="324e5-107">Vous pouvez enchaîner des effets dans un graphique d’effet et composer ou mélanger la sortie d’effets.</span><span class="sxs-lookup"><span data-stu-id="324e5-107">You can chain effects in an effect graph and compose or blend the output of effects.</span></span>

<span data-ttu-id="324e5-108">Un effet Direct2D effectue une tâche de création d’images, telle que la modification de la luminosité, la désaturation d’une image ou la création d’une ombre portée.</span><span class="sxs-lookup"><span data-stu-id="324e5-108">A Direct2D effect performs an imaging task, like changing brightness, de-saturating an image, or creating a drop shadow.</span></span> <span data-ttu-id="324e5-109">Les effets peuvent accepter zéro ou plusieurs images d’entrée, exposer plusieurs propriétés qui contrôlent leur fonctionnement et générer une seule image de sortie.</span><span class="sxs-lookup"><span data-stu-id="324e5-109">Effects can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="324e5-110">Chaque effet crée un graphique de transformation interne constitué de transformations individuelles.</span><span class="sxs-lookup"><span data-stu-id="324e5-110">Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="324e5-111">Chaque transformation représente une opération d’image unique.</span><span class="sxs-lookup"><span data-stu-id="324e5-111">Each transform represents a single image operation.</span></span> <span data-ttu-id="324e5-112">L’objectif principal d’une transformation est d’héberger les nuanceurs qui sont exécutés pour chaque pixel de sortie.</span><span class="sxs-lookup"><span data-stu-id="324e5-112">The main purpose of a transform is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="324e5-113">Ces nuanceurs peuvent inclure des nuanceurs de pixels, des nuanceurs de sommets, l’étape de fusion d’un GPU et des nuanceurs de calcul.</span><span class="sxs-lookup"><span data-stu-id="324e5-113">These shaders can include pixel shaders, vertex shaders, the blend stage of a GPU, and compute shaders.</span></span>

<span data-ttu-id="324e5-114">Les [effets intégrés](built-in-effects.md) et les effets personnalisés [Direct2D](./direct2d-portal.md) que vous pouvez effectuer à l’aide de l' [API effets personnalisés](custom-effects.md) fonctionnent de cette façon.</span><span class="sxs-lookup"><span data-stu-id="324e5-114">Both the [Direct2D](./direct2d-portal.md) [built-in effects](built-in-effects.md) and custom effects you can make using the [custom effects API](custom-effects.md) work this way.</span></span>

<span data-ttu-id="324e5-115">Il existe une plage d' [effets intégrés](built-in-effects.md) à partir de catégories telles que celles-ci.</span><span class="sxs-lookup"><span data-stu-id="324e5-115">There are a range of [built-in effects](built-in-effects.md) from categories like the ones here.</span></span> <span data-ttu-id="324e5-116">Pour obtenir une liste complète, consultez la section [effets intégrés](built-in-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="324e5-116">See the [Built-in Effects](built-in-effects.md) section for a full list.</span></span>

-   [<span data-ttu-id="324e5-117">Filtrage</span><span class="sxs-lookup"><span data-stu-id="324e5-117">Filtering</span></span>](built-in-effects.md)
-   [<span data-ttu-id="324e5-118">Composition et fusion</span><span class="sxs-lookup"><span data-stu-id="324e5-118">Composition and Blending</span></span>](built-in-effects.md)
-   [<span data-ttu-id="324e5-119">Transparence</span><span class="sxs-lookup"><span data-stu-id="324e5-119">Transparency</span></span>](built-in-effects.md)
-   [<span data-ttu-id="324e5-120">Color</span><span class="sxs-lookup"><span data-stu-id="324e5-120">Color</span></span>](built-in-effects.md)
-   [<span data-ttu-id="324e5-121">Éclairage et stylisation</span><span class="sxs-lookup"><span data-stu-id="324e5-121">Lighting and Stylizing</span></span>](built-in-effects.md)
-   [<span data-ttu-id="324e5-122">Transformation et mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="324e5-122">Transforming and Scaling</span></span>](built-in-effects.md)
-   [<span data-ttu-id="324e5-123">Sources</span><span class="sxs-lookup"><span data-stu-id="324e5-123">Sources</span></span>](built-in-effects.md)

<span data-ttu-id="324e5-124">Vous pouvez appliquer des effets à n’importe quelle bitmap, y compris : les images chargées par le [composant WIC (Windows Imaging Component)](/windows/desktop/wic/-wic-api), les primitives dessinées par [Direct2D](./direct2d-portal.md), le texte de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)ou les scènes rendues par [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span><span class="sxs-lookup"><span data-stu-id="324e5-124">You can apply effects to any bitmap, including: images loaded by the [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), primitives drawn by [Direct2D](./direct2d-portal.md), text from [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), or scenes rendered by [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

<span data-ttu-id="324e5-125">Avec les effets Direct2D, vous pouvez écrire vos propres effets que vous pouvez utiliser pour vos applications.</span><span class="sxs-lookup"><span data-stu-id="324e5-125">With Direct2D effects you can write your own effects that you can use for your applications.</span></span> <span data-ttu-id="324e5-126">Une infrastructure d’effet personnalisée vous permet d’utiliser des fonctionnalités GPU, telles que les nuanceurs de pixels, les nuanceurs de vertex et l’unité de fusion.</span><span class="sxs-lookup"><span data-stu-id="324e5-126">A custom effect framework allows you to use GPU features such as pixel shaders, vertex shaders, and the blending unit.</span></span> <span data-ttu-id="324e5-127">Vous pouvez également inclure d’autres effets intégrés ou personnalisés dans votre effet personnalisé.</span><span class="sxs-lookup"><span data-stu-id="324e5-127">You can also include other built-in or custom effects in your custom effect.</span></span> <span data-ttu-id="324e5-128">L’infrastructure pour la création d’effets personnalisés est la même que celle utilisée pour créer les effets intégrés de [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="324e5-128">The framework for building custom effects is the same one that was used to create the built-in effects of [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="324e5-129">L' [API d’effet Direct2D](custom-effects.md) fournit un ensemble d’interfaces pour créer et enregistrer des effets.</span><span class="sxs-lookup"><span data-stu-id="324e5-129">The [Direct2D effect author API](custom-effects.md) provides a set of interfaces to create and register effects.</span></span>

### <a name="more-effects-topics"></a><span data-ttu-id="324e5-130">Rubriques supplémentaires sur les effets</span><span class="sxs-lookup"><span data-stu-id="324e5-130">More effects topics</span></span>

<span data-ttu-id="324e5-131">Le reste de cette rubrique explique les principes fondamentaux des effets Direct2D, comme l’application d’un effet à une image.</span><span class="sxs-lookup"><span data-stu-id="324e5-131">The rest of this topic explains the basics of Direct2D effects, like applying an effect to an image.</span></span> <span data-ttu-id="324e5-132">Le tableau ci-dessous contient des liens vers des rubriques supplémentaires sur les effets.</span><span class="sxs-lookup"><span data-stu-id="324e5-132">The table here has links to additional topics about effects.</span></span>

| <span data-ttu-id="324e5-133">Rubrique</span><span class="sxs-lookup"><span data-stu-id="324e5-133">Topic</span></span>                                                                                                                    | <span data-ttu-id="324e5-134">Description</span><span class="sxs-lookup"><span data-stu-id="324e5-134">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="324e5-135">Liaison de nuanceurs d’effet</span><span class="sxs-lookup"><span data-stu-id="324e5-135">Effect Shader Linking</span></span>](effect-shader-linking.md)<br/>                                                            | <span data-ttu-id="324e5-136">Direct2D utilise une optimisation appelée liaison de nuanceur d’effet qui combine plusieurs passes de rendu de graphique d’effet dans une seule passe.</span><span class="sxs-lookup"><span data-stu-id="324e5-136">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span><br/>                                               |
| [<span data-ttu-id="324e5-137">Effets personnalisés</span><span class="sxs-lookup"><span data-stu-id="324e5-137">Custom effects</span></span>](custom-effects.md)<br/>                                                                          | <span data-ttu-id="324e5-138">Montre comment écrire vos propres effets personnalisés à l’aide du langage HLSL standard.</span><span class="sxs-lookup"><span data-stu-id="324e5-138">Shows you how to write your own custom effects using standard HLSL.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="324e5-139">Comment charger une image dans des effets Direct2D à l’aide de FilePicker</span><span class="sxs-lookup"><span data-stu-id="324e5-139">How to load an image into Direct2D Effects using the FilePicker</span></span>](load-a-id2d1image-using-the-filepicker.md)<br/> | <span data-ttu-id="324e5-140">Montre comment utiliser [**Windows :: Storage ::P ickers :: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) pour charger une image dans des effets Direct2D.</span><span class="sxs-lookup"><span data-stu-id="324e5-140">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into Direct2D effects.</span></span><br/>                                      |
| [<span data-ttu-id="324e5-141">Guide pratique pour enregistrer le contenu Direct2D dans un fichier image</span><span class="sxs-lookup"><span data-stu-id="324e5-141">How to save Direct2D content to an image file</span></span>](save-direct2d-content-to-an-image-file.md)<br/>                   | <span data-ttu-id="324e5-142">Cette rubrique montre comment utiliser [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) pour enregistrer du contenu sous la forme d’un [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) dans un fichier image encodé comme JPEG.</span><span class="sxs-lookup"><span data-stu-id="324e5-142">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span><br/> |
| [<span data-ttu-id="324e5-143">Comment appliquer des effets aux primitives</span><span class="sxs-lookup"><span data-stu-id="324e5-143">How to Apply Effects to Primitives</span></span>](how-to-apply-effects-to-primitives.md)<br/>                                  | <span data-ttu-id="324e5-144">Cette rubrique montre comment appliquer une série d’effets à des primitives [Direct2D](./direct2d-portal.md) et [DirectWrite](direct2d-and-directwrite.md) .</span><span class="sxs-lookup"><span data-stu-id="324e5-144">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span><br/>                           |
| [<span data-ttu-id="324e5-145">Contrôle de la précision et du découpage numérique dans les graphiques d’effet</span><span class="sxs-lookup"><span data-stu-id="324e5-145">Controlling Precision and Numerical Clipping in Effect Graphs</span></span>](precision-and-clipping-in-effect-graphs.md)<br/>  | <span data-ttu-id="324e5-146">Les applications qui restituent des effets à l’aide de Direct2D doivent veiller à atteindre le niveau souhaité de qualité et de prévisibilité en ce qui concerne la précision numérique.</span><span class="sxs-lookup"><span data-stu-id="324e5-146">Applications that render effects using Direct2D must take care to achieve the desired level of quality and predictability with respect to numerical precision.</span></span> <br/>                    |

## <a name="applying-an-effect-to-an-image"></a><span data-ttu-id="324e5-147">Application d’un effet à une image</span><span class="sxs-lookup"><span data-stu-id="324e5-147">Applying an effect to an image</span></span>

<span data-ttu-id="324e5-148">Vous pouvez utiliser l’API Direct2D Effects pour appliquer des transformations aux images.</span><span class="sxs-lookup"><span data-stu-id="324e5-148">You can use the Direct2D effects API to apply transforms to images.</span></span>

> [!Note]  
> <span data-ttu-id="324e5-149">Cet exemple suppose que vous avez déjà créé des objets [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) et [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="324e5-149">This example assumes that you already have [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) objects created.</span></span> <span data-ttu-id="324e5-150">Pour plus d’informations sur la création de ces objets, consultez le guide pratique [pour charger une image dans des effets Direct2D à l’aide des](load-a-id2d1image-using-the-filepicker.md) [contextes](devices-and-device-contexts.md)FilePicker et Device.</span><span class="sxs-lookup"><span data-stu-id="324e5-150">For more information on creating these objects see [How to load an image into Direct2D effects using the FilePicker](load-a-id2d1image-using-the-filepicker.md) and [Devices and Device Contexts](devices-and-device-contexts.md).</span></span>

 

1.  <span data-ttu-id="324e5-151">Déclarez une variable [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , puis créez un effet de [source bitmap](bitmap-source.md) à l’aide de la méthode [**ID2DDeviceContext :: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) .</span><span class="sxs-lookup"><span data-stu-id="324e5-151">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create a [bitmap source](bitmap-source.md) effect using the [**ID2DDeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method.</span></span>

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  <span data-ttu-id="324e5-152">Définissez la propriété BitmapSource sur la source de bitmap WIC à l’aide de [**ID2D1Effect :: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span><span class="sxs-lookup"><span data-stu-id="324e5-152">Set the BitmapSource property to the WIC bitmap source using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span></span>

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  <span data-ttu-id="324e5-153">Déclarez une variable [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , puis créez l’effet [flou gaussien](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="324e5-153">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create the [gaussian blur](gaussian-blur.md) effect.</span></span>

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  <span data-ttu-id="324e5-154">Définissez l’entrée pour recevoir l’image de l’effet de source bitmap.</span><span class="sxs-lookup"><span data-stu-id="324e5-154">Set the input to receive the image from the bitmap source effect.</span></span> <span data-ttu-id="324e5-155">Définissez la valeur de flou de la méthode [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) et de la propriété d’écart type.</span><span class="sxs-lookup"><span data-stu-id="324e5-155">Set the blur amount the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method and the standard deviation property.</span></span>

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  <span data-ttu-id="324e5-156">Utilisez le contexte de périphérique pour dessiner la sortie d’image résultante.</span><span class="sxs-lookup"><span data-stu-id="324e5-156">Use the device context to draw the resulting image output.</span></span>

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    <span data-ttu-id="324e5-157">La méthode [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) doit être appelée entre les appels [**ID2DDeviceContext :: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) et [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) comme d’autres opérations de rendu Direct2D.</span><span class="sxs-lookup"><span data-stu-id="324e5-157">The [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method must be called between the [**ID2DDeviceContext::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) calls like other Direct2D render operations.</span></span> <span data-ttu-id="324e5-158">**DrawImage** peut prendre une image ou la sortie d’un effet et la rendre sur la surface cible.</span><span class="sxs-lookup"><span data-stu-id="324e5-158">**DrawImage** can take an image or the output of an effect and render it to the target surface.</span></span>

## <a name="spatial-transforms"></a><span data-ttu-id="324e5-159">Transformations spatiales</span><span class="sxs-lookup"><span data-stu-id="324e5-159">Spatial Transforms</span></span>

<span data-ttu-id="324e5-160">Direct2D fournit des effets intégrés qui peuvent transformer les images en espace 2D et 3D, ainsi que la mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="324e5-160">Direct2D provides built-in effects that can transform images in 2D and 3D space, as well as scaling.</span></span> <span data-ttu-id="324e5-161">Les effets de la mise à l’échelle et de la transformation offrent différents niveaux de qualité, tels que les cubiques les plus proches, linéaires, cubiques, linéaires, anisotrope et de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="324e5-161">The scale and transform effects offer various quality levels like: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

> [!Note]  
> <span data-ttu-id="324e5-162">Le mode anisotrope génère des mipmaps lors de la mise à l’échelle, toutefois, si vous affectez à la propriété **Cached** la valeur true sur les effets qui sont entrés dans la transformation, le des mipmaps ne sera pas généré à chaque fois pour des images suffisamment petites.</span><span class="sxs-lookup"><span data-stu-id="324e5-162">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to the transform the mipmaps won't be generated every time for sufficiently small images.</span></span>

 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));

affineTransformEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,  0.1f, 0.9f, 8.0f, 45.0f);
DX::ThrowIfFailed(affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="324e5-163">Cette utilisation de l’effet de transformation affine 2D fait pivoter légèrement le bitmap dans le sens inverse.</span><span class="sxs-lookup"><span data-stu-id="324e5-163">This use of the 2D affine transform effect rotates the bitmap counterclockwise slightly.</span></span>



| <span data-ttu-id="324e5-164">Avant</span><span class="sxs-lookup"><span data-stu-id="324e5-164">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![effet affin 2D avant image.](images/default-before.jpg)      |
| <span data-ttu-id="324e5-166">After</span><span class="sxs-lookup"><span data-stu-id="324e5-166">After</span></span>                                                             |
| ![effet affin 2D après l’image.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a><span data-ttu-id="324e5-168">Composition d’images</span><span class="sxs-lookup"><span data-stu-id="324e5-168">Compositing images</span></span>

<span data-ttu-id="324e5-169">Certains effets acceptent plusieurs entrées et les composent en une image résultante.</span><span class="sxs-lookup"><span data-stu-id="324e5-169">Some effects accept multiple inputs and composite them into one resulting image.</span></span>

<span data-ttu-id="324e5-170">Les effets composites composites et arithmétiques intégrés fournissent différents modes. pour plus d’informations, consultez la rubrique [composite](composite.md) .</span><span class="sxs-lookup"><span data-stu-id="324e5-170">The built-in composite and arithmetic composite effects provide various modes, for more info see the [composite](composite.md) topic.</span></span> <span data-ttu-id="324e5-171">L’effet de [fusion](blend.md) offre un large éventail de modes d’accélération GPU disponibles.</span><span class="sxs-lookup"><span data-stu-id="324e5-171">The [blend](blend.md) effect has a variety of GPU accelerated modes available.</span></span>


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="324e5-172">L’effet composite combine les images de différentes manières selon le mode que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="324e5-172">The composite effect combines images in various different ways according to the mode you specify.</span></span>

## <a name="pixel-adjustments"></a><span data-ttu-id="324e5-173">Réglages des pixels</span><span class="sxs-lookup"><span data-stu-id="324e5-173">Pixel adjustments</span></span>

<span data-ttu-id="324e5-174">Certains effets Direct2D intégrés vous permettent de modifier les données de pixels.</span><span class="sxs-lookup"><span data-stu-id="324e5-174">There are a few built-in Direct2D effects that allow you to alter the pixel data.</span></span> <span data-ttu-id="324e5-175">Par exemple, l’effet matrice de couleurs peut être utilisé pour modifier la couleur d’une image.</span><span class="sxs-lookup"><span data-stu-id="324e5-175">For example, the color matrix effect can be used to change the color of an image.</span></span>


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect));

colorMatrixEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
DX::ThrowIfFailed(colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="324e5-176">Ce code prend l’image et modifie la couleur comme indiqué dans les exemples d’images ici.</span><span class="sxs-lookup"><span data-stu-id="324e5-176">This code takes the image and alters the color as shown in the example images here.</span></span>



| <span data-ttu-id="324e5-177">Avant</span><span class="sxs-lookup"><span data-stu-id="324e5-177">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![effet de matrice de couleurs avant l’image.](images/default-before.jpg) |
| <span data-ttu-id="324e5-179">After</span><span class="sxs-lookup"><span data-stu-id="324e5-179">After</span></span>                                                           |
| ![effet de matrice de couleurs après l’image.](images/15-colormatrix.png)  |



 

<span data-ttu-id="324e5-181">Pour plus d’informations, consultez la section [Color Built-in Effects](how-to-create-a-solid-color-brush.md) .</span><span class="sxs-lookup"><span data-stu-id="324e5-181">See the [color built-in effects](how-to-create-a-solid-color-brush.md) section for more info.</span></span>

## <a name="building-effect-graphs"></a><span data-ttu-id="324e5-182">Génération de graphiques d’effets</span><span class="sxs-lookup"><span data-stu-id="324e5-182">Building effect graphs</span></span>

<span data-ttu-id="324e5-183">Vous pouvez regrouper des effets pour transformer des images.</span><span class="sxs-lookup"><span data-stu-id="324e5-183">You can chain effects together to transform images.</span></span> <span data-ttu-id="324e5-184">Par exemple, le code suivant applique une ombre et une transformation 2D, puis compose les résultats ensemble.</span><span class="sxs-lookup"><span data-stu-id="324e5-184">For example, the code here applies a shadow and a 2D transform, then composites the results together.</span></span>


```C++
ComPtr<ID2D1Effect> shadowEffect;
ComPtr<ID2D1Effect> affineTransformEffect;
ComPtr<ID2D1Effect> compositeEffect;

DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

shadowEffect->SetInput(0, bitmap.Get());
affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

compositeEffect->SetInputEffect(0, affineTransformEffect.Get());
compositeEffect->SetInput(1, bitmap.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="324e5-185">Voici le résultat.</span><span class="sxs-lookup"><span data-stu-id="324e5-185">Here is the result.</span></span>

![sortie de l’effet d’ombre.](images/effect-overview-shadow.png)

<span data-ttu-id="324e5-187">Les effets prennent les objets [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) comme entrée.</span><span class="sxs-lookup"><span data-stu-id="324e5-187">Effects take [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) objects as input.</span></span> <span data-ttu-id="324e5-188">Vous pouvez utiliser un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , car l’interface est dérivée de **ID2D1Image**.</span><span class="sxs-lookup"><span data-stu-id="324e5-188">You can use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) because the interface is derived from **ID2D1Image**.</span></span> <span data-ttu-id="324e5-189">Vous pouvez également utiliser [**ID2D1Effect :: GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) pour obtenir la sortie d’un objet [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) en tant que **ID2D1Image** ou utiliser la méthode **SetInputEffect** , qui convertit la sortie pour vous.</span><span class="sxs-lookup"><span data-stu-id="324e5-189">You can also use the [**ID2D1Effect::GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) to get the output of an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object as an **ID2D1Image** or use the **SetInputEffect** method, which converts the output for you.</span></span> <span data-ttu-id="324e5-190">Dans la plupart des cas, un graphique d’effet se compose d’objets **ID2D1Effect** chaînés directement ensemble, ce qui facilite l’application de plusieurs effets à une image pour créer des visuels attrayants.</span><span class="sxs-lookup"><span data-stu-id="324e5-190">In most cases an effect graph consists of **ID2D1Effect** objects directly chained together, which makes it easy to apply multiple effects to an image to create compelling visuals.</span></span>

<span data-ttu-id="324e5-191">Pour plus d’informations, consultez [comment appliquer des effets à des primitives](how-to-apply-effects-to-primitives.md) .</span><span class="sxs-lookup"><span data-stu-id="324e5-191">See [How to apply effects to primitives](how-to-apply-effects-to-primitives.md) for more info.</span></span>

## <a name="related-topics"></a><span data-ttu-id="324e5-192">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="324e5-192">Related topics</span></span>

[<span data-ttu-id="324e5-193">Exemple d’effets d’images de base Direct2D</span><span class="sxs-lookup"><span data-stu-id="324e5-193">Direct2D basic image effects sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[<span data-ttu-id="324e5-194">Effets intégrés</span><span class="sxs-lookup"><span data-stu-id="324e5-194">Built-in Effects</span></span>](built-in-effects.md)