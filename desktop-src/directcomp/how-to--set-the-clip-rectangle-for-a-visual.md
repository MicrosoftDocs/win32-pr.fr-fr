---
title: Comment découper un objet Rectangle
description: Cette rubrique montre comment utiliser un objet clip rectangle pour découper un élément visuel ou une arborescence d’éléments visuels.
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d26019f37949b0111ee9b5958fa3fba2c9507cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232181"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a>Comment découper un objet Rectangle

> [!NOTE]
> pour les applications sur Windows 10, nous vous recommandons d’utiliser des api Windows. UI. Composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Cette rubrique montre comment utiliser un objet clip rectangle pour découper un élément visuel ou une arborescence d’éléments visuels.

L’exemple de cette rubrique définit un clip rectangulaire centré à l’emplacement de la souris, et applique le clip à un visuel qui est centré dans la zone cliente de la fenêtre de la cible de la composition. Cette capture d’écran montre le résultat de l’application de l’objet de clip rectangle au visuel.

![résultat de l’application d’un objet Rectangle à un élément visuel](images/clipwithrectangleclipobject.png)

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

### <a name="step-2-create-the-rectangle-clip-object"></a>Étape 2 : créer l’objet Clip Rectangle

Utilisez la méthode [**IDCompositionDevice :: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) pour créer une instance de l’objet Clip Rectangle.


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a>Étape 3 : définir les propriétés de l’objet Clip Rectangle

Appelez les méthodes de l’interface [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) de l’objet clip rectangle pour définir les propriétés du rectangle de découpage.

L’exemple suivant définit un rectangle de découpage centré autour de l’emplacement actuel de la souris. Les `m_offsetX` `m_offsetY` variables membres et contiennent les valeurs des propriétés OffsetX et OffsetY de l’élément visuel.


```C++
    if (SUCCEEDED(hr))
    {
        // Get the location of the mouse.
        POINT ptMouse = { };
        GetCursorPos(&ptMouse);
        ScreenToClient(m_hwnd, &ptMouse);

        // Create a 100-by-100 pixel rectangular clip that is 
        // centered at the mouse location, and is mapped to
        // the rectangle of the visual.
        m_pClip->SetLeft((ptMouse.x - m_offsetX) - 50.f);
        m_pClip->SetTop((ptMouse.y - m_offsetY) - 50.f);
        m_pClip->SetRight((ptMouse.x - m_offsetX) + 50.f);
        m_pClip->SetBottom((ptMouse.y - m_offsetY) + 50.f);
    }
```



Notez que l’interface [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) inclut les méthodes suivantes pour définir un rectangle de découpage avec des angles arrondis :

-   [**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))
-   [**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))
-   [**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))
-   [**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))

### <a name="step-4-set-the-clip-property-of-the-visual"></a>Étape 4 : définir la propriété clip de l’élément visuel

Utilisez la méthode [**IDCompositionVisual :: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) pour associer la propriété clip de l’élément visuel à l’objet Clip Rectangle.


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a>Étape 5 : valider la composition

Appelez la méthode [**IDCompositionDevice :: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) pour valider le lot de commandes à Microsoft DirectComposition pour traitement. Le résultat de l’application du rectangle de découpage s’affiche dans la fenêtre cible.


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a>Étape 6 : libérer les objets DirectComposition

Veillez à libérer l’objet de clip rectangle lorsque vous n’en avez plus besoin, ainsi qu’à l’objet périphérique, à l’objet cible de la composition et à tous les objets visuels. L’exemple suivant appelle la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) définie par l’application pour libérer les objets DirectComposition.


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Découpage](clipping.md)
</dt> </dl>

 

 