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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922087"
---
# <a name="how-to-apply-2d-transforms"></a>Comment appliquer des transformations 2D

> [!NOTE]
> pour les applications sur Windows 10, nous vous recommandons d’utiliser des api Windows. UI. Composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Cette rubrique montre comment appliquer des transformations 2D à un visuel à l’aide de Microsoft DirectComposition. L’exemple de cette rubrique applique un groupe de transformations qui :

1.  Faire pivoter le visuel de 180 degrés.
2.  Augmentez l’échelle du visuel à trois fois sa taille d’origine.
3.  Translate (déplace) le visuel 150 pixels à droite de sa position d’origine.

Les captures d’écran suivantes montrent le visuel avant et après l’application des transformations 2D.

![résultat de l’application d’un groupe de transformations 2D à un visuel](images/apply2dtransform.png)

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [DirectComposition](directcomposition-portal.md)
-   [Graphismes Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [Infrastructure DirectX Graphics (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Microsoft Win32
-   COM (Component Object Model)

## <a name="instructions"></a>Instructions

### <a name="step-1-initialize-directcomposition-objects"></a>Étape 1 : initialiser les objets DirectComposition

1.  Créez l’objet appareil et l’objet cible de la composition.
2.  Créez un visuel, définissez son contenu, puis ajoutez-le à l’arborescence d’éléments visuels.

Pour plus d’informations, voir [How to Initialize DirectComposition](initialize-directcomposition.md).

### <a name="step-2-create-the-transform-group-array"></a>Étape 2 : créer le tableau de groupes de transformations


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a>Étape 3 : créer les objets de transformation, définir leurs propriétés et les ajouter au tableau du groupe de transformations

1.  Utilisez les méthodes [**IDCompositionDevice :: CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**:: CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)et [**:: CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) pour créer les objets de transformation.
2.  Utilisez les fonctions membres des interfaces [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)et [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) pour définir les propriétés des transformations.
3.  Copiez les pointeurs d’interface de transformation dans le tableau du groupe de transformations.


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



### <a name="step-4-create-the-transform-group-object"></a>Étape 4 : créer l’objet de groupe de transformations

Appelez la méthode [**IDCompositionDevice :: CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) pour créer l’objet de groupe de transformations.


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a>Étape 5 : appliquer l’objet de groupe de transformations au visuel

Utilisez la méthode [**IDCompositionVisual :: setTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) pour associer la propriété Transform de l’objet visuel à l’objet de groupe transformer.


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a>Étape 6 : valider la composition

Appelez la méthode [**IDCompositionDevice :: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) pour valider les mises à jour apportées au visuel à DirectComposition pour le traitement. Le résultat de l’application du groupe de transformations 2D s’affiche dans la fenêtre cible.


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a>Étape 7 : libérer les objets DirectComposition

Veillez à libérer le groupe d’objets de transformation 2D lorsque vous n’en avez plus besoin. L’exemple suivant appelle la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) définie par l’application pour libérer les objets de transformation.


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



N’oubliez pas également de libérer l’objet appareil, l’objet cible de la composition et les visuels avant la fermeture de votre application.

## <a name="complete-example"></a>Exemple complet


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transformations](transforms.md)
</dt> </dl>

 

 