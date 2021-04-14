---
title: Comment appliquer des transformations 2D
description: Cette rubrique montre comment appliquer des transformations 2D à un visuel à l’aide de Microsoft DirectComposition.
ms.assetid: DED74416-C85A-4220-89BD-3F9BEF786B7D
keywords:
- Comment appliquer des transformations 2D DirectComposition
- Transformations 2D DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52d2e0ce9fbb56547c42ea4ea18d57d173a7e40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382452"
---
# <a name="how-to-apply-2d-transforms"></a><span data-ttu-id="c4570-105">Comment appliquer des transformations 2D</span><span class="sxs-lookup"><span data-stu-id="c4570-105">How to apply 2D transforms</span></span>

> [!NOTE]
> <span data-ttu-id="c4570-106">Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c4570-106">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="c4570-107">Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="c4570-107">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="c4570-108">Cette rubrique montre comment appliquer des transformations 2D à un visuel à l’aide de Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c4570-108">This topic demonstrates how to apply 2D transforms to a visual by using Microsoft DirectComposition.</span></span> <span data-ttu-id="c4570-109">L’exemple de cette rubrique applique un groupe de transformations qui :</span><span class="sxs-lookup"><span data-stu-id="c4570-109">The example in this topic applies a group of transforms that:</span></span>

1.  <span data-ttu-id="c4570-110">Faire pivoter le visuel de 180 degrés.</span><span class="sxs-lookup"><span data-stu-id="c4570-110">Rotate the visual by 180 degrees.</span></span>
2.  <span data-ttu-id="c4570-111">Augmentez l’échelle du visuel à trois fois sa taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="c4570-111">Scale up the visual to three times its original size.</span></span>
3.  <span data-ttu-id="c4570-112">Translate (déplace) le visuel 150 pixels à droite de sa position d’origine.</span><span class="sxs-lookup"><span data-stu-id="c4570-112">Translate (move) the visual 150 pixels to the right of its original position.</span></span>

<span data-ttu-id="c4570-113">Les captures d’écran suivantes montrent le visuel avant et après l’application des transformations 2D.</span><span class="sxs-lookup"><span data-stu-id="c4570-113">The following screen shots show the visual before and after applying the 2D transforms.</span></span>

![résultat de l’application d’un groupe de transformations 2D à un visuel](images/apply2dtransform.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="c4570-115">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="c4570-115">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c4570-116">Technologies</span><span class="sxs-lookup"><span data-stu-id="c4570-116">Technologies</span></span>

-   [<span data-ttu-id="c4570-117">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="c4570-117">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="c4570-118">Graphismes Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="c4570-118">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="c4570-119">Infrastructure DirectX Graphics (DXGI)</span><span class="sxs-lookup"><span data-stu-id="c4570-119">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="c4570-120">Prérequis</span><span class="sxs-lookup"><span data-stu-id="c4570-120">Prerequisites</span></span>

-   <span data-ttu-id="c4570-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="c4570-121">C/C++</span></span>
-   <span data-ttu-id="c4570-122">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="c4570-122">Microsoft Win32</span></span>
-   <span data-ttu-id="c4570-123">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="c4570-123">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="c4570-124">Instructions</span><span class="sxs-lookup"><span data-stu-id="c4570-124">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="c4570-125">Étape 1 : initialiser les objets DirectComposition</span><span class="sxs-lookup"><span data-stu-id="c4570-125">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="c4570-126">Créez l’objet appareil et l’objet cible de la composition.</span><span class="sxs-lookup"><span data-stu-id="c4570-126">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="c4570-127">Créez un visuel, définissez son contenu, puis ajoutez-le à l’arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="c4570-127">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="c4570-128">Pour plus d’informations, voir [How to Initialize DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="c4570-128">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-transform-group-array"></a><span data-ttu-id="c4570-129">Étape 2 : créer le tableau de groupes de transformations</span><span class="sxs-lookup"><span data-stu-id="c4570-129">Step 2: Create the transform group array</span></span>


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a><span data-ttu-id="c4570-130">Étape 3 : créer les objets de transformation, définir leurs propriétés et les ajouter au tableau du groupe de transformations</span><span class="sxs-lookup"><span data-stu-id="c4570-130">Step 3: Create the transform objects, set their properties, and add them to the transform group array</span></span>

1.  <span data-ttu-id="c4570-131">Utilisez les méthodes [**IDCompositionDevice :: CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**:: CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)et [**:: CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) pour créer les objets de transformation.</span><span class="sxs-lookup"><span data-stu-id="c4570-131">Use the [**IDCompositionDevice::CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**::CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform), and [**::CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) methods to create the transform objects.</span></span>
2.  <span data-ttu-id="c4570-132">Utilisez les fonctions membres des interfaces [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)et [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) pour définir les propriétés des transformations.</span><span class="sxs-lookup"><span data-stu-id="c4570-132">Use the member functions of the [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform), and [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) interfaces to set the properties of the transforms.</span></span>
3.  <span data-ttu-id="c4570-133">Copiez les pointeurs d’interface de transformation dans le tableau du groupe de transformations.</span><span class="sxs-lookup"><span data-stu-id="c4570-133">Copy the transform interface pointers to the transform group array.</span></span>


```C++
IDCompositionRotateTransform *pRotateTransform = nullptr;
IDCompositionScaleTransform *pScaleTransform = nullptr;
IDCompositionTranslateTransform *pTranslateTransform = nullptr;
IDCompositionTransform *pTransformGroup = nullptr;

// Create the rotate transform.
hr = pDevice->CreateRotateTransform(&pRotateTransform);

if (SUCCEEDED(hr))
{
    // Set the center of rotation to the center point of the visual.
    hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
    
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
    }

    // Set the rotate angle to 180 degrees.
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetAngle(180.0f);
    }

    // Add the rotate transform to the transform group array.
    pTransforms[0] = pRotateTransform;

    // Create the scale transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateScaleTransform(&pScaleTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Set the scaling origin to the upper-right corner of the visual.
    hr = pScaleTransform->SetCenterX(0.0f);
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetCenterY(0.0f);
    }

    // Set the scaling factor to three for both the width and height. 
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleX(3.0f);
    }
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleY(3.0f);
    }

    // Add the scale transform to the transform group array.
    pTransforms[1] = pScaleTransform;

    // Create the translate transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Move the visual 150 pixels to the right.
    hr = pTranslateTransform->SetOffsetX(150.0f);
    if (SUCCEEDED(hr)) {
        hr = pTranslateTransform->SetOffsetY(0.0f);
    }

    // Add the translate transform to the transform group array.
    pTransforms[2] = pTranslateTransform;
}
```



### <a name="step-4-create-the-transform-group-object"></a><span data-ttu-id="c4570-134">Étape 4 : créer l’objet de groupe de transformations</span><span class="sxs-lookup"><span data-stu-id="c4570-134">Step 4: Create the transform group object</span></span>

<span data-ttu-id="c4570-135">Appelez la méthode [**IDCompositionDevice :: CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) pour créer l’objet de groupe de transformations.</span><span class="sxs-lookup"><span data-stu-id="c4570-135">Call the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method to create the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a><span data-ttu-id="c4570-136">Étape 5 : appliquer l’objet de groupe de transformations au visuel</span><span class="sxs-lookup"><span data-stu-id="c4570-136">Step 5: Apply the transform group object to the visual</span></span>

<span data-ttu-id="c4570-137">Utilisez la méthode [**IDCompositionVisual :: setTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) pour associer la propriété Transform de l’objet visuel à l’objet de groupe transformer.</span><span class="sxs-lookup"><span data-stu-id="c4570-137">Use the [**IDCompositionVisual::SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) method to associate the Transform property of the visual with the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a><span data-ttu-id="c4570-138">Étape 6 : valider la composition</span><span class="sxs-lookup"><span data-stu-id="c4570-138">Step 6: Commit the composition</span></span>

<span data-ttu-id="c4570-139">Appelez la méthode [**IDCompositionDevice :: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) pour valider les mises à jour apportées au visuel à DirectComposition pour le traitement.</span><span class="sxs-lookup"><span data-stu-id="c4570-139">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the updates to the visual to DirectComposition for processing.</span></span> <span data-ttu-id="c4570-140">Le résultat de l’application du groupe de transformations 2D s’affiche dans la fenêtre cible.</span><span class="sxs-lookup"><span data-stu-id="c4570-140">The result of applying the group of 2D transforms appears in the target window.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a><span data-ttu-id="c4570-141">Étape 7 : libérer les objets DirectComposition</span><span class="sxs-lookup"><span data-stu-id="c4570-141">Step 7: Free the DirectComposition objects</span></span>

<span data-ttu-id="c4570-142">Veillez à libérer le groupe d’objets de transformation 2D lorsque vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="c4570-142">Be sure to free the group of 2D transform objects when you no longer need them.</span></span> <span data-ttu-id="c4570-143">L’exemple suivant appelle la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) définie par l’application pour libérer les objets de transformation.</span><span class="sxs-lookup"><span data-stu-id="c4570-143">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the transform objects.</span></span>


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



<span data-ttu-id="c4570-144">N’oubliez pas également de libérer l’objet appareil, l’objet cible de la composition et les visuels avant la fermeture de votre application.</span><span class="sxs-lookup"><span data-stu-id="c4570-144">Also remember to free the device object, the composition target object, and the visuals before your application exits.</span></span>

## <a name="complete-example"></a><span data-ttu-id="c4570-145">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="c4570-145">Complete example</span></span>


```C++
#define BITMAP_WIDTH  80.0
#define BITMAP_HEIGHT 80.0

HRESULT DemoApp::ApplyTransformGroup(IDCompositionDevice *pDevice, 
                                     IDCompositionVisual *pVisual)
{
    HRESULT hr = S_OK;

    if (pDevice == nullptr || pVisual == nullptr)
        return E_INVALIDARG; 
    
    IDCompositionTransform *pTransforms[3];

    IDCompositionRotateTransform *pRotateTransform = nullptr;
    IDCompositionScaleTransform *pScaleTransform = nullptr;
    IDCompositionTranslateTransform *pTranslateTransform = nullptr;
    IDCompositionTransform *pTransformGroup = nullptr;

    // Create the rotate transform.
    hr = pDevice->CreateRotateTransform(&pRotateTransform);

    if (SUCCEEDED(hr))
    {
        // Set the center of rotation to the center point of the visual.
        hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
        
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
        }

        // Set the rotate angle to 180 degrees.
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetAngle(180.0f);
        }

        // Add the rotate transform to the transform group array.
        pTransforms[0] = pRotateTransform;

        // Create the scale transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateScaleTransform(&pScaleTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Set the scaling origin to the upper-right corner of the visual.
        hr = pScaleTransform->SetCenterX(0.0f);
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetCenterY(0.0f);
        }

        // Set the scaling factor to three for both the width and height. 
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleX(3.0f);
        }
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleY(3.0f);
        }

        // Add the scale transform to the transform group array.
        pTransforms[1] = pScaleTransform;

        // Create the translate transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Move the visual 150 pixels to the right.
        hr = pTranslateTransform->SetOffsetX(150.0f);
        if (SUCCEEDED(hr)) {
            hr = pTranslateTransform->SetOffsetY(0.0f);
        }

        // Add the translate transform to the transform group array.
        pTransforms[2] = pTranslateTransform;
    }

    if (SUCCEEDED(hr))
    {
        // Create the transform group.
        hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the transform group to the visual.
        hr = pVisual->SetTransform(pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the composition.
        hr = pDevice->Commit();
    }

    // Release the transform objects.
    for (int i = 0; i < 3; i++)
    {
        SafeRelease(&pTransforms[i]);
    }

    // Release the transform group pointer.
    SafeRelease(&pTransformGroup);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c4570-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4570-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4570-147">Transformations</span><span class="sxs-lookup"><span data-stu-id="c4570-147">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 