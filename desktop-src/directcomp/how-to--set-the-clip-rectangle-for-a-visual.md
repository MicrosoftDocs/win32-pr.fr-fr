---
title: Comment découper un objet Rectangle
description: Cette rubrique montre comment utiliser un objet clip rectangle pour découper un élément visuel ou une arborescence d’éléments visuels.
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d26019f37949b0111ee9b5958fa3fba2c9507cb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032070"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a><span data-ttu-id="16037-103">Comment découper un objet Rectangle</span><span class="sxs-lookup"><span data-stu-id="16037-103">How to clip with a rectangle clip object</span></span>

> [!NOTE]
> <span data-ttu-id="16037-104">Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="16037-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="16037-105">Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="16037-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="16037-106">Cette rubrique montre comment utiliser un objet clip rectangle pour découper un élément visuel ou une arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="16037-106">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span>

<span data-ttu-id="16037-107">L’exemple de cette rubrique définit un clip rectangulaire centré à l’emplacement de la souris, et applique le clip à un visuel qui est centré dans la zone cliente de la fenêtre de la cible de la composition.</span><span class="sxs-lookup"><span data-stu-id="16037-107">The example in this topic defines a rectangular clip that is centered at the mouse location, and applies the clip to a visual that is centered in the client area of the composition target window.</span></span> <span data-ttu-id="16037-108">Cette capture d’écran montre le résultat de l’application de l’objet de clip rectangle au visuel.</span><span class="sxs-lookup"><span data-stu-id="16037-108">This screen shot shows the result of applying the rectangle clip object to the visual.</span></span>

![résultat de l’application d’un objet Rectangle à un élément visuel](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="16037-110">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="16037-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="16037-111">Technologies</span><span class="sxs-lookup"><span data-stu-id="16037-111">Technologies</span></span>

-   [<span data-ttu-id="16037-112">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="16037-112">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="16037-113">Graphismes Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="16037-113">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="16037-114">Infrastructure DirectX Graphics (DXGI)</span><span class="sxs-lookup"><span data-stu-id="16037-114">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="16037-115">Prérequis</span><span class="sxs-lookup"><span data-stu-id="16037-115">Prerequisites</span></span>

-   <span data-ttu-id="16037-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="16037-116">C/C++</span></span>
-   <span data-ttu-id="16037-117">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="16037-117">Microsoft Win32</span></span>
-   <span data-ttu-id="16037-118">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="16037-118">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="16037-119">Instructions</span><span class="sxs-lookup"><span data-stu-id="16037-119">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="16037-120">Étape 1 : initialiser les objets DirectComposition</span><span class="sxs-lookup"><span data-stu-id="16037-120">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="16037-121">Créez l’objet appareil et l’objet cible de la composition.</span><span class="sxs-lookup"><span data-stu-id="16037-121">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="16037-122">Créez un visuel, définissez son contenu, puis ajoutez-le à l’arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="16037-122">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="16037-123">Pour plus d’informations, voir [How to Initialize DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="16037-123">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-rectangle-clip-object"></a><span data-ttu-id="16037-124">Étape 2 : créer l’objet Clip Rectangle</span><span class="sxs-lookup"><span data-stu-id="16037-124">Step 2: Create the rectangle clip object</span></span>

<span data-ttu-id="16037-125">Utilisez la méthode [**IDCompositionDevice :: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) pour créer une instance de l’objet Clip Rectangle.</span><span class="sxs-lookup"><span data-stu-id="16037-125">Use the [**IDCompositionDevice::CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) method to create an instance of the rectangle clip object.</span></span>


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a><span data-ttu-id="16037-126">Étape 3 : définir les propriétés de l’objet Clip Rectangle</span><span class="sxs-lookup"><span data-stu-id="16037-126">Step 3: Set the properties of the rectangle clip object</span></span>

<span data-ttu-id="16037-127">Appelez les méthodes de l’interface [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) de l’objet clip rectangle pour définir les propriétés du rectangle de découpage.</span><span class="sxs-lookup"><span data-stu-id="16037-127">Call the methods of the rectangle clip object's [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface to set the properties of the clip rectangle.</span></span>

<span data-ttu-id="16037-128">L’exemple suivant définit un rectangle de découpage centré autour de l’emplacement actuel de la souris.</span><span class="sxs-lookup"><span data-stu-id="16037-128">The following example defines a clip rectangle that is centered around the current mouse location.</span></span> <span data-ttu-id="16037-129">Les `m_offsetX` `m_offsetY` variables membres et contiennent les valeurs des propriétés OffsetX et OffsetY de l’élément visuel.</span><span class="sxs-lookup"><span data-stu-id="16037-129">The `m_offsetX` and `m_offsetY` member variables contain the values of the OffsetX and OffsetY properties of the visual.</span></span>


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



<span data-ttu-id="16037-130">Notez que l’interface [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) inclut les méthodes suivantes pour définir un rectangle de découpage avec des angles arrondis :</span><span class="sxs-lookup"><span data-stu-id="16037-130">Note that the [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface includes the following methods for defining a clip rectangle that has rounded corners:</span></span>

-   <span data-ttu-id="16037-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="16037-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span></span>
-   <span data-ttu-id="16037-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="16037-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span></span>
-   <span data-ttu-id="16037-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="16037-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span></span>
-   <span data-ttu-id="16037-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="16037-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span></span>

### <a name="step-4-set-the-clip-property-of-the-visual"></a><span data-ttu-id="16037-135">Étape 4 : définir la propriété clip de l’élément visuel</span><span class="sxs-lookup"><span data-stu-id="16037-135">Step 4: Set the Clip property of the visual</span></span>

<span data-ttu-id="16037-136">Utilisez la méthode [**IDCompositionVisual :: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) pour associer la propriété clip de l’élément visuel à l’objet Clip Rectangle.</span><span class="sxs-lookup"><span data-stu-id="16037-136">Use the [**IDCompositionVisual::SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) method to associate the Clip property of the visual with the rectangle clip object.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a><span data-ttu-id="16037-137">Étape 5 : valider la composition</span><span class="sxs-lookup"><span data-stu-id="16037-137">Step 5: Commit the composition</span></span>

<span data-ttu-id="16037-138">Appelez la méthode [**IDCompositionDevice :: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) pour valider le lot de commandes à Microsoft DirectComposition pour traitement.</span><span class="sxs-lookup"><span data-stu-id="16037-138">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the batch of commands to Microsoft DirectComposition for processing.</span></span> <span data-ttu-id="16037-139">Le résultat de l’application du rectangle de découpage s’affiche dans la fenêtre cible.</span><span class="sxs-lookup"><span data-stu-id="16037-139">The result of applying the clip rectangle appears in the target window.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a><span data-ttu-id="16037-140">Étape 6 : libérer les objets DirectComposition</span><span class="sxs-lookup"><span data-stu-id="16037-140">Step 6: Free the DirectComposition objects</span></span>

<span data-ttu-id="16037-141">Veillez à libérer l’objet de clip rectangle lorsque vous n’en avez plus besoin, ainsi qu’à l’objet périphérique, à l’objet cible de la composition et à tous les objets visuels.</span><span class="sxs-lookup"><span data-stu-id="16037-141">Be sure to free the rectangle clip object when you no longer need it, as well as the device object, the composition target object, and any visual objects.</span></span> <span data-ttu-id="16037-142">L’exemple suivant appelle la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) définie par l’application pour libérer les objets DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="16037-142">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the DirectComposition objects.</span></span>


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a><span data-ttu-id="16037-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="16037-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16037-144">Portion</span><span class="sxs-lookup"><span data-stu-id="16037-144">Clipping</span></span>](clipping.md)
</dt> </dl>

 

 