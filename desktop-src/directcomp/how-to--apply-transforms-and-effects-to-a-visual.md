---
title: Comment appliquer des effets
description: Cette rubrique montre comment utiliser Microsoft DirectComposition pour appliquer des effets et des transformations 3D à un visuel.
ms.assetid: FE5A0BE9-B84C-4DE1-85D8-375897237F96
keywords:
- Comment appliquer des effets DirectComposition
- Effets DirectComposition, comment appliquer
- Transformations 3D DirectComposition
- Transformations 3D DirectComposition
- Opacité DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728496309f62aaa0027ca3751a6681384fb83c95
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383203"
---
# <a name="how-to-apply-effects"></a><span data-ttu-id="62663-108">Comment appliquer des effets</span><span class="sxs-lookup"><span data-stu-id="62663-108">How to apply effects</span></span>

> [!NOTE]
> <span data-ttu-id="62663-109">Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="62663-109">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="62663-110">Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="62663-110">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="62663-111">Cette rubrique montre comment utiliser Microsoft DirectComposition pour appliquer des effets et des transformations 3D à un visuel.</span><span class="sxs-lookup"><span data-stu-id="62663-111">This topic demonstrates how to use Microsoft DirectComposition to apply effects and 3D transformations to a visual.</span></span> <span data-ttu-id="62663-112">L’exemple de cette rubrique modifie l’opacité d’un visuel et le fait pivoter autour d’un axe vertical situé au centre de l’visuel.</span><span class="sxs-lookup"><span data-stu-id="62663-112">The example in this topic changes the opacity of a visual and rotates it around a vertical axis located at the center of the visual.</span></span> <span data-ttu-id="62663-113">Pour en savoir plus sur les autres effets pris en charge par DirectComposition, consultez [Effects](effects.md).</span><span class="sxs-lookup"><span data-stu-id="62663-113">To learn more about other effects supported by DirectComposition, see [Effects](effects.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="62663-114">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="62663-114">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="62663-115">Technologies</span><span class="sxs-lookup"><span data-stu-id="62663-115">Technologies</span></span>

-   [<span data-ttu-id="62663-116">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="62663-116">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="62663-117">Graphismes Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="62663-117">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="62663-118">Infrastructure DirectX Graphics (DXGI)</span><span class="sxs-lookup"><span data-stu-id="62663-118">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="62663-119">Prérequis</span><span class="sxs-lookup"><span data-stu-id="62663-119">Prerequisites</span></span>

-   <span data-ttu-id="62663-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="62663-120">C/C++</span></span>
-   <span data-ttu-id="62663-121">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="62663-121">Microsoft Win32</span></span>
-   <span data-ttu-id="62663-122">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="62663-122">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="62663-123">Instructions</span><span class="sxs-lookup"><span data-stu-id="62663-123">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="62663-124">Étape 1 : initialiser les objets DirectComposition</span><span class="sxs-lookup"><span data-stu-id="62663-124">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="62663-125">Créez l’objet appareil et l’objet cible de la composition.</span><span class="sxs-lookup"><span data-stu-id="62663-125">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="62663-126">Créez un visuel, définissez son contenu, puis ajoutez-le à l’arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="62663-126">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="62663-127">Pour plus d’informations, voir [How to Initialize DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="62663-127">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-a-3d-rotate-transform-object-an-effect-group-object-and-an-animation-object"></a><span data-ttu-id="62663-128">Étape 2 : créer un objet transformation de rotation 3D, un objet groupe d’effets et un objet d’animation</span><span class="sxs-lookup"><span data-stu-id="62663-128">Step 2: Create a 3D rotate transform object, an effect group object, and an animation object</span></span>

<span data-ttu-id="62663-129">Utilisez la méthode [**IDCompositionDevice :: CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) pour créer un objet de transformation de rotation 3D et la méthode [**CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) pour créer un objet de groupe d’effets.</span><span class="sxs-lookup"><span data-stu-id="62663-129">Use the [**IDCompositionDevice::CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) method to create a 3D rotate transform object, and the [**CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) method to create an effect group object.</span></span> <span data-ttu-id="62663-130">Cet exemple utilise également la méthode [**CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) pour créer un objet d’animation afin d’animer la transformation de rotation 3D.</span><span class="sxs-lookup"><span data-stu-id="62663-130">This example also uses the [**CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) method to create an animation object for animating the 3D rotate transform.</span></span> <span data-ttu-id="62663-131">Pour en savoir plus sur l’application d’animations, consultez [comment appliquer des animations](how-to--animate-a-visual.md).</span><span class="sxs-lookup"><span data-stu-id="62663-131">To learn more about applying animations, see [How to apply animations](how-to--animate-a-visual.md).</span></span>


```C++
    HRESULT hr = S_OK;

    IDCompositionAnimation *pAnimation = nullptr;
    IDCompositionRotateTransform3D *pRotate3D = nullptr;
    IDCompositionEffectGroup *pEffectGroup = nullptr;


    // Create a 3D rotate transform object.
    hr = m_pDevice->CreateRotateTransform3D(&pRotate3D);

    if (SUCCEEDED(hr))
    {
        // Create an effect group object.
        hr = m_pDevice->CreateEffectGroup(&pEffectGroup);
    }
    
    if (SUCCEEDED(hr))
    {
        // Create an animation object.
        hr = m_pDevice->CreateAnimation(&pAnimation);
    }
```





### <a name="step-3-define-the-animation-function"></a><span data-ttu-id="62663-132">Étape 3 : définir la fonction d’animation</span><span class="sxs-lookup"><span data-stu-id="62663-132">Step 3: Define the animation function</span></span>

<span data-ttu-id="62663-133">Utilisez les méthodes de l’objet [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) pour définir la fonction d’animation.</span><span class="sxs-lookup"><span data-stu-id="62663-133">Use the methods of the [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) object to define the animation function.</span></span>

<span data-ttu-id="62663-134">L’exemple suivant définit une fonction d’animation simple.</span><span class="sxs-lookup"><span data-stu-id="62663-134">The following example defines a simple animation function.</span></span> <span data-ttu-id="62663-135">Lorsqu’elle est appliquée à une propriété d’objet, la fonction d’animation modifie la valeur de la propriété de 0 à la valeur de l’argument *Degrees* au cours d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="62663-135">When applied to an object property, the animation function incrementally changes the property value from 0 to the value of the *degrees* argument over the course of one second.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Define the animation function.
        pAnimation->AddCubic(0.0f, 0.0f, degrees, 0.0f, 0.0f);
        pAnimation->End(1.0f, degrees);
```



### <a name="step-4-set-the-properties-of-the-3d-rotate-transform"></a><span data-ttu-id="62663-136">Étape 4 : définir les propriétés de la transformation de rotation 3D</span><span class="sxs-lookup"><span data-stu-id="62663-136">Step 4: Set the properties of the 3D rotate transform</span></span>

1.  <span data-ttu-id="62663-137">Appliquez la fonction d’animation à la propriété angle de la transformation de rotation 3D en appelant la méthode [**IDCompositionRotateTransform3D :: Seenchevêtrement**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform-setangle(idcompositionanimation)) .</span><span class="sxs-lookup"><span data-stu-id="62663-137">Apply the animation function to the Angle property of the 3D rotate transform by calling the [**IDCompositionRotateTransform3D::SetAngle**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform-setangle(idcompositionanimation)) method.</span></span>
2.  <span data-ttu-id="62663-138">Définissez l’axe de rotation pour la transformation de rotation 3D en appelant les méthodes [**IDCompositionRotateTransform3D :: SetAxisX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisx(float)), [**SetAxisY**](/windows/desktop/api/Dcomp/nf-dcomp-setaxisy)et [**SetAxisZ**](/windows/desktop/api/Dcomp/nf-dcomp-setaxisz) .</span><span class="sxs-lookup"><span data-stu-id="62663-138">Set the axis of rotation for the 3D rotate transform by calling the [**IDCompositionRotateTransform3D::SetAxisX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisx(float)), [**SetAxisY**](/windows/desktop/api/Dcomp/nf-dcomp-setaxisy), and [**SetAxisZ**](/windows/desktop/api/Dcomp/nf-dcomp-setaxisz) methods.</span></span>
3.  <span data-ttu-id="62663-139">Définissez le centre de rotation pour la transformation de rotation 3D en appelant les méthodes [**IDCompositionRotateTransform3D :: SetCenterX**](/previous-versions/windows/desktop/legacy/hh448982(v=vs.85)) et [**SetCenterY**](/previous-versions/windows/desktop/legacy/hh448988(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="62663-139">Set the center of rotation for the 3D rotate transform by calling the [**IDCompositionRotateTransform3D::SetCenterX**](/previous-versions/windows/desktop/legacy/hh448982(v=vs.85)) and [**SetCenterY**](/previous-versions/windows/desktop/legacy/hh448988(v=vs.85)) methods.</span></span>

<span data-ttu-id="62663-140">L’exemple suivant configure une transformation de rotation 3D pour tourner un visuel autour d’un axe vertical situé au centre de l’visuel.</span><span class="sxs-lookup"><span data-stu-id="62663-140">The following example sets up a 3D rotate transform for spinning a visual around a vertical axis located at the center of the visual.</span></span> <span data-ttu-id="62663-141">Les paramètres *m \_ bitmapWidth* et *m \_ bitmapHeight* sont la largeur et la hauteur de la bitmap, en pixels.</span><span class="sxs-lookup"><span data-stu-id="62663-141">The *m\_bitmapWidth* and *m\_bitmapHeight* parameters are the width and height of the bitmap, in pixels.</span></span>


```C++
        // Set the properties of the rotate transform object.  
        //
        // Apply the animation object to the Angle property so that
        // the visual will appear to spin around an axis. 
        pRotate3D->SetAngle(pAnimation);

        // Set a vertical axis through the center of the visual's bitmap. 
        pRotate3D->SetAxisX(0.0f);
        pRotate3D->SetAxisY(1.0f);
        pRotate3D->SetAxisZ(0.0f);

        // Set the center of rotation to the center of the visual's bitmap.
        pRotate3D->SetCenterX(m_bitmapWidth / 2.0f);
        pRotate3D->SetCenterY(m_bitmapHeight / 2.0f);
    }
```



### <a name="step-5-set-the-properties-of-the-effect-group-object"></a><span data-ttu-id="62663-142">Étape 5 : définir les propriétés de l’objet groupe d’effets</span><span class="sxs-lookup"><span data-stu-id="62663-142">Step 5: Set the properties of the effect group object</span></span>

1.  <span data-ttu-id="62663-143">Appliquez l’objet de transformation de rotation 3D à la propriété Transform3D de l’objet de groupe d’effets en appelant la méthode [**IDCompositionEffectGroup :: SetTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d) .</span><span class="sxs-lookup"><span data-stu-id="62663-143">Apply the 3D rotate transform object to the Transform3D property of the effect group object by calling the [**IDCompositionEffectGroup::SetTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d) method.</span></span>
2.  <span data-ttu-id="62663-144">Définissez la propriété Opacity de l’objet de groupe d’effets en appelant [**IDCompositionEffectGroup :: SetOpacity**](/windows/win32/api/dcomp/nf-dcomp-idcompositioneffectgroup-setopacity(float)).</span><span class="sxs-lookup"><span data-stu-id="62663-144">Set the Opacity property of the effect group object by calling the [**IDCompositionEffectGroup::SetOpacity**](/windows/win32/api/dcomp/nf-dcomp-idcompositioneffectgroup-setopacity(float)).</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Apply the rotate transform object to the Tranform3D property
        // of the effect group object.
        hr = pEffectGroup->SetTransform3D(pRotate3D);
    }


    if (SUCCEEDED(hr))
    {
        // Set the Opacity of the effect group object.
        hr = pEffectGroup->SetOpacity(opacity);
    }
```





### <a name="step-6-apply-the-effect-group-object-to-the-effect-property-of-the-visual"></a><span data-ttu-id="62663-145">Étape 6 : appliquer l’objet de groupe d’effets à la propriété Effect du visuel</span><span class="sxs-lookup"><span data-stu-id="62663-145">Step 6: Apply the effect group object to the Effect property of the visual</span></span>

<span data-ttu-id="62663-146">Appelez la méthode [**IDCompositionVisual :: SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) pour appliquer l’objet de groupe d’effets au visuel.</span><span class="sxs-lookup"><span data-stu-id="62663-146">Call the [**IDCompositionVisual::SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) method to apply the effect group object to the visual.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Apply the effect group object to the Effect property of the visual.
        hr = pVisual->SetEffect(pEffectGroup);
    }
```



### <a name="step-7-commit-the-composition"></a><span data-ttu-id="62663-147">Étape 7 : valider la composition</span><span class="sxs-lookup"><span data-stu-id="62663-147">Step 7: Commit the composition</span></span>

<span data-ttu-id="62663-148">Appelez la méthode [**IDCompositionDevice :: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) pour valider le lot de commandes à DirectComposition pour le traitement.</span><span class="sxs-lookup"><span data-stu-id="62663-148">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the batch of commands to DirectComposition for processing.</span></span> <span data-ttu-id="62663-149">La composition résultante apparaît dans la fenêtre cible.</span><span class="sxs-lookup"><span data-stu-id="62663-149">The resulting composition appears in the target window.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to DirectComposition.
        hr = m_pDevice->Commit();
    }
```



### <a name="step-8-free-the-directcomposition-objects"></a><span data-ttu-id="62663-150">Étape 8 : libérer les objets DirectComposition</span><span class="sxs-lookup"><span data-stu-id="62663-150">Step 8: Free the DirectComposition objects</span></span>

<span data-ttu-id="62663-151">Veillez à libérer l’objet d’animation, l’objet transformation de rotation 3D et l’objet groupe d’effets lorsque vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="62663-151">Be sure to free the animation object, the 3D rotate transform object, and the effect group object when you no longer need them.</span></span> <span data-ttu-id="62663-152">L’exemple suivant appelle la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) définie par l’application pour libérer les objets.</span><span class="sxs-lookup"><span data-stu-id="62663-152">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the objects.</span></span>


```C++
    // Release the DirectComposition objects.
    SafeRelease(&pAnimation);
    SafeRelease(&pRotate3D);
    SafeRelease(&pEffectGroup);
```



<span data-ttu-id="62663-153">N’oubliez pas également de libérer l’objet appareil, l’objet cible de la composition et le visuel avant la fermeture de votre application.</span><span class="sxs-lookup"><span data-stu-id="62663-153">Also remember to free the device object, the composition target object, and the visual before your application exits.</span></span> <span data-ttu-id="62663-154">Pour plus d’informations, voir [How to Initialize DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="62663-154">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

## <a name="complete-example"></a><span data-ttu-id="62663-155">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="62663-155">Complete example</span></span>


```C++
//
// ApplyEffects.h
//
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

#pragma once
// Modify the following definitions if you need to target a platform prior to the ones specified below.
// Refer to MSDN for the latest info on corresponding values for different platforms.
#ifndef WINVER              // Allow use of features specific to Windows 7 or later.
#define WINVER 0x0700       // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT        // Allow use of features specific to Windows 7 or later.
#define _WIN32_WINNT 0x0700 // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN     // Exclude rarely-used items from Windows headers

// Windows Header Files:
#include <windows.h>

// C RunTime Header Files
#include <math.h>

// DirectComposition and Direct3D Header Files
#include <dcomp.h>
#include <d3d11.h>

/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
    )
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}

#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT Initialize();

    void RunMessageLoop();

private:
    HRESULT InitializeDirectCompositionDevice();

    HRESULT CreateResources();
    void DiscardResources();

    HRESULT OnPaint();
    HRESULT OnClientClick(int xPos, int yPos);
    HRESULT OnMouseMove(int xPos, int yPos);

    HRESULT LoadResourceGDIBitmap(
        PCWSTR resourceName, 
        HBITMAP &hbmp
        );

    HRESULT MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface);

    HRESULT SetVisualOpacity(IDCompositionVisual *pVisual, float opacity);
    HRESULT RotateVisual(IDCompositionVisual *pVisual,float degrees);

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

 private:
    HWND m_hwnd;
    HBITMAP m_hBitmap;
    int m_bitmapWidth;
    int m_bitmapHeight;
    ID3D11Device *m_pD3D11Device;
    IDCompositionDevice *m_pDevice;
    IDCompositionTarget *m_pCompTarget;
    IDCompositionVisual *m_pVisual;
 };


//
// ApplyEffects.cpp
//
// THIS CODE AND INFORMATION IS PROVIDED &quot;AS IS&quot; WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

// Instructions: Hover over the image to see the opacity change. Click
//   the image to apply a 3D rotation.

#include &quot;ApplyEffects.h&quot;

#define OFFSET_X 20
#define OFFSET_Y 20
#define TRANSPARENT 0.5
#define OPAQUE 1.0

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE /* hInstance */,
    HINSTANCE /* hPrevInstance */,
    LPSTR /* lpCmdLine */,
    int /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
    // unlikely event that HeapSetInformation fails.
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);
    if (SUCCEEDED(CoInitialize(NULL)))
    {
        {
            DemoApp app;

            if (SUCCEEDED(app.Initialize()))
            {
                app.RunMessageLoop();
            }
        }
        CoUninitialize();
    }

    return 0;
}

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                         *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_hwnd(NULL),
    m_hBitmap(NULL),
    m_pDevice(nullptr),
    m_pCompTarget(nullptr),
    m_pD3D11Device(nullptr),
    m_pVisual(nullptr),
    m_bitmapHeight(0),
    m_bitmapWidth(0)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()
{
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pVisual);
}

/*******************************************************************
*                                                                  *
*  Create the application window.                                  *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::Initialize()
{
    HRESULT hr;

    // Register the window class.
    WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
    wcex.style         = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc   = DemoApp::WndProc;
    wcex.cbClsExtra    = 0;
    wcex.cbWndExtra    = sizeof(LONG_PTR);
    wcex.hInstance     = HINST_THISCOMPONENT;
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
    wcex.lpszMenuName  = NULL;
    wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wcex.lpszClassName = L&quot;DirectCompDemoApp&quot;;

    RegisterClassEx(&wcex);

    // Create the application window.
    //
    // Because the CreateWindow function takes its size in pixels, we
    // obtain the system DPI and use it to scale the window size.
    int dpiX = 0;
    int dpiY = 0;
    HDC hdc = GetDC(NULL);
    if (hdc)
    {
        dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
        dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
        ReleaseDC(NULL, hdc);
    }

    m_hwnd = CreateWindow(
        L&quot;DirectCompDemoApp&quot;,
        L&quot;DirectComposition Demo Application&quot;,
        WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT,
        CW_USEDEFAULT,
        static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
        static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
        NULL,
        NULL,
        HINST_THISCOMPONENT,
        this
        );

    hr = m_hwnd ? S_OK : E_FAIL;

    if (SUCCEEDED(hr))
    {   
        // Initialize DirectComposition resources, such as the
        // device object and composition target object.
        hr = InitializeDirectCompositionDevice();
    }

    if (SUCCEEDED(hr))
    {
        hr = CreateResources();
    }

    if (SUCCEEDED(hr))
    {
       ShowWindow(m_hwnd, SW_SHOWNORMAL);
       UpdateWindow(m_hwnd);
    }    

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the DirectComposition device object and    *
*  and the composition target object. These objects endure for    *
*  the lifetime of the application.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::InitializeDirectCompositionDevice()
{
    HRESULT hr = S_OK;

    D3D_FEATURE_LEVEL featureLevelSupported;

    // Create the D3D device object.
    D3D11CreateDevice(
        nullptr,
        D3D_DRIVER_TYPE_HARDWARE,
        NULL,
        D3D11_CREATE_DEVICE_BGRA_SUPPORT,
        NULL,
        0,
        D3D11_SDK_VERSION,
        &m_pD3D11Device,
        &featureLevelSupported,
        NULL);

    IDXGIDevice *pDXGIDevice = nullptr;

    hr = (m_pD3D11Device == nullptr) ? E_UNEXPECTED : S_OK;
    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = m_pD3D11Device->QueryInterface(&pDXGIDevice);
    }

    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, 
                __uuidof(IDCompositionDevice), 
                reinterpret_cast<void **>(&m_pDevice));
    }

    if (SUCCEEDED(hr))
    {
        // Create the composition target object.
        hr = m_pDevice->CreateTargetForHwnd(m_hwnd, TRUE, &m_pCompTarget);   
    }

    SafeRelease(&pDXGIDevice);

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the GDI bitmap that the application gives  *
*  to DirectComposition to be composed.                           *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateResources()
{
    HRESULT hr = S_OK;

    hr = LoadResourceGDIBitmap(L&quot;Penguins&quot;, m_hBitmap);
   
    return hr;
}

/******************************************************************
*                                                                 *
*  Discard device-specific resources.                             *
*                                                                 *
******************************************************************/

void DemoApp::DiscardResources()
{
    DeleteObject(m_hBitmap);
}

/******************************************************************
*                                                                 *
*  The main window&#39;s message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}

/******************************************************************
*                                                                 *
*  Called when the application&#39;s main window is painted. This     *
*  method builds a simple visual tree and passes it to            *
*  DirectComposition.                                             *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnPaint()
{
    HRESULT hr = S_OK;
    IDCompositionSurface *pSurface = nullptr;

    // Create a visual object.          
    hr = m_pDevice->CreateVisual(&m_pVisual);  

    if (SUCCEEDED(hr))
    {
        // Create a composition surface and render a GDI bitmap 
        // to the surface.
        hr = MyCreateGDIRenderedDCompSurface(m_hBitmap, &pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the bitmap content of the visual. 
        hr = m_pVisual->SetContent(pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the horizontal and vertical position of the visual relative
        // to the upper-left corner of the composition target window.
        m_pVisual->SetOffsetX(OFFSET_X);  
        m_pVisual->SetOffsetY(OFFSET_Y);  
        hr = SetVisualOpacity(m_pVisual, TRANSPARENT);
    }

   if (SUCCEEDED(hr))
    {
        // Set the visual to be the root of the visual tree.          
        hr = m_pCompTarget->SetRoot(m_pVisual);  
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  Called when the mouse moves in the main window&#39;s client area.  *
*  This method determines whether the mouse cursor is over the    *
*  visual, and calls an application-defined function to set the   *
*  visual&#39;s opacity.                                              *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnMouseMove(int xPos, int yPos)
{
    HRESULT hr = S_OK;
    static BOOL fOverImage = FALSE;

    // Determine whether the cursor is over the visual.
    if ((xPos >= OFFSET_X && xPos <= (OFFSET_X + m_bitmapWidth))
        && (yPos >= OFFSET_Y && yPos <= (OFFSET_Y + m_bitmapHeight)))
    {
        if (!fOverImage)
        {
            // The cursor has moved over the visual, so make the visual 
            // 100% opaque.
            hr = SetVisualOpacity(m_pVisual, OPAQUE);
            fOverImage = TRUE;
        }
    }

    else if (fOverImage)
    {
        // The cursor has moved off the visual, so make the visual
        // 50% opaque.
        hr = SetVisualOpacity(m_pVisual, TRANSPARENT);
        fOverImage = FALSE;
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  Changes the opacity of a visual.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::SetVisualOpacity(IDCompositionVisual *pVisual, float opacity)
{
    HRESULT hr = S_OK;
    IDCompositionEffectGroup *pEffectGroup = nullptr;

    // Validate the input arguments.
    if (pVisual == NULL || (opacity > 1.0f || opacity < 0.0f))
        return E_INVALIDARG;

    // Create an effect group object.
    hr = m_pDevice->CreateEffectGroup(&pEffectGroup);

    if (SUCCEEDED(hr))
    {
        // Set the Opacity of the effect group object.
        hr = pEffectGroup->SetOpacity(opacity);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the effect group object to the Effect property of the visual.
        hr = m_pVisual->SetEffect(pEffectGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to DirectComposition.
        hr = m_pDevice->Commit();
    }

    // Free the effect group object.
    SafeRelease(&pEffectGroup);

    return hr;
}


/******************************************************************
*                                                                 *
*  Called when the user clicks in the main window&#39;s client area.  *
*  This method determines whether the mouse cursor is over the    *
*  visual and calls an application-defined function to rotate the *
*  visual.                                                        *
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnClientClick(int xPos, int yPos)
{
    HRESULT hr = S_OK;

    // Determine whether the mouse cursor is over the visual. If so,
    // rotate the visual.
    if ((xPos >= OFFSET_X && xPos <= (OFFSET_X + m_bitmapWidth))
        && (yPos >= OFFSET_Y && yPos <= (OFFSET_Y + m_bitmapHeight)))
    {
        hr = RotateVisual(m_pVisual, 360.0f);
    }
    
    return hr;
}

/******************************************************************
*                                                                 *
*  Performs an animated 3D rotation of a visual.                  *
*                                                                 *
******************************************************************/

HRESULT DemoApp::RotateVisual(IDCompositionVisual *pVisual, float degrees)
{
    HRESULT hr = S_OK;

    IDCompositionAnimation *pAnimation = nullptr;
    IDCompositionRotateTransform3D *pRotate3D = nullptr;
    IDCompositionEffectGroup *pEffectGroup = nullptr;

    // Validate the input arguments.
    if (pVisual == NULL || (degrees > 360.0f || degrees < -360.0f))
        return E_INVALIDARG;

    // Create a 3D rotate transform object.
    hr = m_pDevice->CreateRotateTransform3D(&pRotate3D);

    if (SUCCEEDED(hr))
    {
        // Create an effect group object.
        hr = m_pDevice->CreateEffectGroup(&pEffectGroup);
    }
    
    if (SUCCEEDED(hr))
    {
        // Create an animation object.
        hr = m_pDevice->CreateAnimation(&pAnimation);
    }

    if (SUCCEEDED(hr))
    {
        // Define the animation function.
        pAnimation->AddCubic(0.0f, 0.0f, degrees, 0.0f, 0.0f);
        pAnimation->End(1.0f, degrees);

        // Set the properties of the rotate transform object.  
        //
        // Apply the animation object to the Angle property so that
        // the visual will appear to spin around an axis. 
        pRotate3D->SetAngle(pAnimation);

        // Set a vertical axis through the center of the visual&#39;s bitmap. 
        pRotate3D->SetAxisX(0.0f);
        pRotate3D->SetAxisY(1.0f);
        pRotate3D->SetAxisZ(0.0f);

        // Set the center of rotation to the center of the visual&#39;s bitmap.
        pRotate3D->SetCenterX(m_bitmapWidth / 2.0f);
        pRotate3D->SetCenterY(m_bitmapHeight / 2.0f);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the rotate transform object to the Tranform3D property
        // of the effect group object.
        hr = pEffectGroup->SetTransform3D(pRotate3D);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the effect group object to the Effect property of the visual.
        hr = pVisual->SetEffect(pEffectGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to DirectComposition.
        hr = m_pDevice->Commit();
    }

    // Release the DirectComposition objects.
    SafeRelease(&pAnimation);
    SafeRelease(&pRotate3D);
    SafeRelease(&pEffectGroup);

    return hr;
}


/******************************************************************
*                                                                 *
*  The window&#39;s message handler.                                  *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
            );

        result = 1;
    }
    else
    {
        DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
            ::GetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA
                )));

        bool wasHandled = false;

        if (pDemoApp)
        {
            switch (message)
            {
            case WM_LBUTTONDOWN:
                {
                    pDemoApp->OnClientClick(LOWORD(lParam), HIWORD(lParam));
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_MOUSEMOVE:
                {
                    pDemoApp->OnMouseMove(LOWORD(lParam), HIWORD(lParam));
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_PAINT:
                {
                    pDemoApp->OnPaint();
                    ValidateRect(hwnd, NULL);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                    pDemoApp->DiscardResources();
                }
                wasHandled = true;
                result = 1;
                break;
            }
        }

        if (!wasHandled)
        {
            result = DefWindowProc(hwnd, message, wParam, lParam);
        }
    }

    return result;
}

/******************************************************************
*                                                                 *
*  This method loads the specified GDI bitmap from the            *
*  application resources, creates a new bitmap that is in a       *
*  format that DirectComposition can use, and copies the contents *
*  of the original bitmap to the new bitmap.                      *
*                                                                 *
******************************************************************/

HRESULT DemoApp::LoadResourceGDIBitmap(PCWSTR resourceName, HBITMAP &hbmp)
{
    hbmp = static_cast<HBITMAP>(LoadImageW(HINST_THISCOMPONENT, resourceName, 
        IMAGE_BITMAP, 0, 0, LR_DEFAULTCOLOR));  
 
    return hbmp ? S_OK : E_FAIL;
}

// CreateGDIRenderedDCompSurface - Creates a DirectComposition surface and 
//   copies the bitmap to the surface. 
//
// Parameters:
//   hBitmap - a GDI bitmap.
//   ppSurface - the composition surface object.
//                                                                 
HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface)
{
    HRESULT hr = S_OK;

    int bmpSize = 0;
    BITMAP bmp = { };
    HBITMAP hBitmapOld = NULL;

    HDC hSurfaceDC = NULL;  
    HDC hBitmapDC = NULL;

    IDXGISurface1 *pDXGISurface = nullptr;
    IDCompositionSurface *pDCSurface = nullptr;
    POINT pointOffset = { };

    hr =  hBitmap ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Get information about the bitmap.
        bmpSize = GetObject(hBitmap, sizeof(BITMAP), &bmp);
    }

    hr = bmpSize ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Save the bitmap dimensions.
        m_bitmapWidth = bmp.bmWidth;
        m_bitmapHeight = bmp.bmHeight;

        // Create a DirectComposition-compatible surface that is the same size 
        // as the bitmap.
        hr = m_pDevice->CreateSurface(m_bitmapWidth, m_bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, &pDCSurface);
    }

    hr = pDCSurface ? S_OK : E_FAIL;
    if (SUCCEEDED(hr)) 
    {
        // Begin rendering to the surface.
        hr = pDCSurface->BeginDraw(NULL, __uuidof(IDXGISurface1), 
            reinterpret_cast<void**>(&pDXGISurface), &pointOffset);
    }

    if (SUCCEEDED(hr)) 
    {
        // Get the device context (DC) for the surface.
        pDXGISurface->GetDC(FALSE, &hSurfaceDC);
    }

    hr = hSurfaceDC ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Create a compatible (DC) and select the surface 
        // into the DC.
        hBitmapDC = CreateCompatibleDC(hSurfaceDC);
        if (hBitmapDC != NULL)
        {
            hBitmapOld = (HBITMAP)SelectObject(hBitmapDC, hBitmap);
            BitBlt(hSurfaceDC, pointOffset.x, pointOffset.y, 
                m_bitmapWidth, m_bitmapHeight, hBitmapDC, 0, 0, SRCCOPY);
            
            if (hBitmapOld)
            {
                SelectObject(hBitmapDC, hBitmapOld);
            }
            DeleteDC(hBitmapDC);
        }

        pDXGISurface->ReleaseDC(NULL);
    }

    // End the rendering.
    pDCSurface->EndDraw();
    *ppSurface = pDCSurface;

    SafeRelease(&pDXGISurface);

    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="62663-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62663-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62663-157">Effets</span><span class="sxs-lookup"><span data-stu-id="62663-157">Effects</span></span>](effects.md)
</dt> </dl>

 

 