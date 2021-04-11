---
title: Rendre des cibles, des appareils et des ressources
description: Rendre des cibles, des appareils et des ressources
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314928"
---
# <a name="render-targets-devices-and-resources"></a><span data-ttu-id="75c38-103">Rendre des cibles, des appareils et des ressources</span><span class="sxs-lookup"><span data-stu-id="75c38-103">Render Targets, Devices, and Resources</span></span>

<span data-ttu-id="75c38-104">Une *cible de rendu* est simplement l’emplacement où votre programme sera dessiné.</span><span class="sxs-lookup"><span data-stu-id="75c38-104">A *render target* is simply the location where your program will draw.</span></span> <span data-ttu-id="75c38-105">En règle générale, la cible de rendu est une fenêtre (plus particulièrement, la zone cliente de la fenêtre).</span><span class="sxs-lookup"><span data-stu-id="75c38-105">Typically, the render target is a window (specifically, the client area of the window).</span></span> <span data-ttu-id="75c38-106">Il peut également s’agir d’une image bitmap en mémoire qui n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="75c38-106">It could also be a bitmap in memory that is not displayed.</span></span> <span data-ttu-id="75c38-107">Une cible de rendu est représentée par l’interface [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="75c38-107">A render target is represented by the [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span>

<span data-ttu-id="75c38-108">Un *appareil* est une abstraction qui représente tout ce qui dessine les pixels.</span><span class="sxs-lookup"><span data-stu-id="75c38-108">A *device* is an abstraction that represents whatever actually draws the pixels.</span></span> <span data-ttu-id="75c38-109">Un périphérique matériel utilise le GPU pour des performances plus rapides, alors qu’un périphérique logiciel utilise le processeur.</span><span class="sxs-lookup"><span data-stu-id="75c38-109">A hardware device uses the GPU for faster performance, whereas a software device uses the CPU.</span></span> <span data-ttu-id="75c38-110">L’application ne crée pas l’appareil.</span><span class="sxs-lookup"><span data-stu-id="75c38-110">The application does not create the device.</span></span> <span data-ttu-id="75c38-111">Au lieu de cela, l’appareil est créé implicitement lorsque l’application crée la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="75c38-111">Instead, the device is created implicitly when the application creates the render target.</span></span> <span data-ttu-id="75c38-112">Chaque cible de rendu est associée à un appareil particulier, qu’il s’agisse d’un matériel ou d’un logiciel.</span><span class="sxs-lookup"><span data-stu-id="75c38-112">Each render target is associated with a particular device, either hardware or software.</span></span>

![diagramme qui montre la relation entre une cible de rendu et un appareil.](images/graphics09.png)

<span data-ttu-id="75c38-114">Une *ressource* est un objet que le programme utilise pour le dessin.</span><span class="sxs-lookup"><span data-stu-id="75c38-114">A *resource* is an object that the program uses for drawing.</span></span> <span data-ttu-id="75c38-115">Voici quelques exemples de ressources qui sont définies dans Direct2D :</span><span class="sxs-lookup"><span data-stu-id="75c38-115">Here are some examples of resources that are defined in Direct2D:</span></span>

-   <span data-ttu-id="75c38-116">**Pinceau**.</span><span class="sxs-lookup"><span data-stu-id="75c38-116">**Brush**.</span></span> <span data-ttu-id="75c38-117">Contrôle la façon dont les lignes et les régions sont peintes.</span><span class="sxs-lookup"><span data-stu-id="75c38-117">Controls how lines and regions are painted.</span></span> <span data-ttu-id="75c38-118">Les types Brush incluent des pinceaux de couleur unie et des pinceaux de dégradé.</span><span class="sxs-lookup"><span data-stu-id="75c38-118">Brush types include solid-color brushes and gradient brushes.</span></span>
-   <span data-ttu-id="75c38-119">**Style de trait**.</span><span class="sxs-lookup"><span data-stu-id="75c38-119">**Stroke style**.</span></span> <span data-ttu-id="75c38-120">Contrôle l’apparence d’une ligne, par exemple Dash ou Solid.</span><span class="sxs-lookup"><span data-stu-id="75c38-120">Controls the appearance of a line—for example, dashed or solid.</span></span>
-   <span data-ttu-id="75c38-121">**Géométrie**.</span><span class="sxs-lookup"><span data-stu-id="75c38-121">**Geometry**.</span></span> <span data-ttu-id="75c38-122">Représente une collection de lignes et de courbes.</span><span class="sxs-lookup"><span data-stu-id="75c38-122">Represents a collection of lines and curves.</span></span>
-   <span data-ttu-id="75c38-123">**Maille**.</span><span class="sxs-lookup"><span data-stu-id="75c38-123">**Mesh**.</span></span> <span data-ttu-id="75c38-124">Forme formée de triangles.</span><span class="sxs-lookup"><span data-stu-id="75c38-124">A shape formed out of triangles.</span></span> <span data-ttu-id="75c38-125">Les données de maillage peuvent être consommées directement par le GPU, contrairement aux données géométriques, qui doivent être converties avant le rendu.</span><span class="sxs-lookup"><span data-stu-id="75c38-125">Mesh data can be consumed directly by the GPU, unlike geometry data, which must be converted before rendering.</span></span>

<span data-ttu-id="75c38-126">Les cibles de rendu sont également considérées comme un type de ressource.</span><span class="sxs-lookup"><span data-stu-id="75c38-126">Render targets are also considered a type of resource.</span></span>

<span data-ttu-id="75c38-127">Certaines ressources tirent parti de l’accélération matérielle.</span><span class="sxs-lookup"><span data-stu-id="75c38-127">Some resources benefit from hardware acceleration.</span></span> <span data-ttu-id="75c38-128">Une ressource de ce type est toujours associée à un appareil particulier, matériel (GPU) ou logiciel (UC).</span><span class="sxs-lookup"><span data-stu-id="75c38-128">A resource of this type is always associated with a particular device, either hardware (GPU) or software (CPU).</span></span> <span data-ttu-id="75c38-129">Ce type de ressource est appelé *dépendant du périphérique*.</span><span class="sxs-lookup"><span data-stu-id="75c38-129">This type of resource is called *device-dependent*.</span></span> <span data-ttu-id="75c38-130">Les pinceaux et les maillages sont des exemples de ressources dépendantes de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="75c38-130">Brushes and meshes are examples of device-dependent resources.</span></span> <span data-ttu-id="75c38-131">Si l’appareil n’est plus disponible, la ressource doit être recréée pour un nouvel appareil.</span><span class="sxs-lookup"><span data-stu-id="75c38-131">If the device becomes unavailable, the resource must be re-created for a new device.</span></span>

<span data-ttu-id="75c38-132">D’autres ressources sont conservées dans la mémoire de l’UC, quel que soit l’appareil utilisé.</span><span class="sxs-lookup"><span data-stu-id="75c38-132">Other resources are kept in CPU memory, regardless of what device is used.</span></span> <span data-ttu-id="75c38-133">Ces ressources sont *indépendantes des appareils*, car elles ne sont pas associées à un appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="75c38-133">These resources are *device-independent*, because they are not associated with a particular device.</span></span> <span data-ttu-id="75c38-134">Il n’est pas nécessaire de recréer des ressources indépendantes du périphérique quand l’appareil change.</span><span class="sxs-lookup"><span data-stu-id="75c38-134">It is not necessary to re-create device-independent resources when the device changes.</span></span> <span data-ttu-id="75c38-135">Les styles de trait et les géométries sont des ressources indépendantes du périphérique.</span><span class="sxs-lookup"><span data-stu-id="75c38-135">Stroke styles and geometries are device-independent resources.</span></span>

<span data-ttu-id="75c38-136">La documentation MSDN pour chaque ressource indique si la ressource est dépendante du périphérique ou indépendante du périphérique.</span><span class="sxs-lookup"><span data-stu-id="75c38-136">The MSDN documentation for each resource states whether the resource is device-dependent or device-independent.</span></span> <span data-ttu-id="75c38-137">Chaque type de ressource est représenté par une interface qui dérive de [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span><span class="sxs-lookup"><span data-stu-id="75c38-137">Every resource type is represented by an interface that derives from [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span></span> <span data-ttu-id="75c38-138">Par exemple, les pinceaux sont représentés par l’interface [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) .</span><span class="sxs-lookup"><span data-stu-id="75c38-138">For example, brushes are represented by the [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) interface.</span></span>

## <a name="the-direct2d-factory-object"></a><span data-ttu-id="75c38-139">Objet de fabrique Direct2D</span><span class="sxs-lookup"><span data-stu-id="75c38-139">The Direct2D Factory Object</span></span>

<span data-ttu-id="75c38-140">La première étape de l’utilisation de Direct2D consiste à créer une instance de l’objet de fabrique Direct2D.</span><span class="sxs-lookup"><span data-stu-id="75c38-140">The first step when using Direct2D is to create an instance of the Direct2D factory object.</span></span> <span data-ttu-id="75c38-141">Dans la programmation de l’ordinateur, une *fabrique* est un objet qui crée d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="75c38-141">In computer programming, a *factory* is an object that creates other objects.</span></span> <span data-ttu-id="75c38-142">La fabrique Direct2D crée les types d’objets suivants :</span><span class="sxs-lookup"><span data-stu-id="75c38-142">The Direct2D factory creates the following types of objects:</span></span>

-   <span data-ttu-id="75c38-143">Cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="75c38-143">Render targets.</span></span>
-   <span data-ttu-id="75c38-144">Ressources indépendantes du périphérique, telles que les styles de trait et les géométries.</span><span class="sxs-lookup"><span data-stu-id="75c38-144">Device-independent resources, such as stroke styles and geometries.</span></span>

<span data-ttu-id="75c38-145">Les ressources dépendantes de l’appareil, telles que les pinceaux et les bitmaps, sont créées par l’objet de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="75c38-145">Device-dependent resources, such as brushes and bitmaps, are created by the render target object.</span></span>

![diagramme qui affiche la fabrique Direct2D.](images/graphics10.png)

<span data-ttu-id="75c38-147">Pour créer l’objet de fabrique Direct2D, appelez la fonction [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .</span><span class="sxs-lookup"><span data-stu-id="75c38-147">To create the Direct2D factory object, call the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



<span data-ttu-id="75c38-148">Le premier paramètre est un indicateur qui spécifie les options de création.</span><span class="sxs-lookup"><span data-stu-id="75c38-148">The first parameter is a flag that specifies creation options.</span></span> <span data-ttu-id="75c38-149">Le **type de fabrique d2d1 indicateur à \_ \_ \_ \_ thread unique** signifie que vous n’allez pas appeler Direct2D à partir de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="75c38-149">The **D2D1\_FACTORY\_TYPE\_SINGLE\_THREADED** flag means that you will not call Direct2D from multiple threads.</span></span> <span data-ttu-id="75c38-150">Pour prendre en charge les appels à partir de plusieurs threads, spécifiez le **\_ type de fabrique d2d1 \_ \_ multithread \_**.</span><span class="sxs-lookup"><span data-stu-id="75c38-150">To support calls from multiple threads, specify **D2D1\_FACTORY\_TYPE\_MULTI\_THREADED**.</span></span> <span data-ttu-id="75c38-151">Si votre programme utilise un seul thread pour appeler Direct2D, l’option à thread unique est plus efficace.</span><span class="sxs-lookup"><span data-stu-id="75c38-151">If your program uses a single thread to call into Direct2D, the single-threaded option is more efficient.</span></span>

<span data-ttu-id="75c38-152">Le deuxième paramètre de la fonction [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) reçoit un pointeur vers l’interface [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="75c38-152">The second parameter to the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function receives a pointer to the [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) interface.</span></span>

<span data-ttu-id="75c38-153">Vous devez créer l’objet de fabrique Direct2D avant le premier message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="75c38-153">You should create the Direct2D factory object before the first [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="75c38-154">Le gestionnaire de messages [**WM \_ Create**](/windows/desktop/winmsg/wm-create) est un bon endroit pour créer la fabrique :</span><span class="sxs-lookup"><span data-stu-id="75c38-154">The [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message handler is a good place to create the factory:</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a><span data-ttu-id="75c38-155">Création de ressources Direct2D</span><span class="sxs-lookup"><span data-stu-id="75c38-155">Creating Direct2D Resources</span></span>

<span data-ttu-id="75c38-156">Le programme Circle utilise les ressources suivantes dépendantes de l’appareil :</span><span class="sxs-lookup"><span data-stu-id="75c38-156">The Circle program uses the following device-dependent resources:</span></span>

-   <span data-ttu-id="75c38-157">Cible de rendu associée à la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="75c38-157">A render target that is associated with the application window.</span></span>
-   <span data-ttu-id="75c38-158">Pinceau de couleur unie pour peindre le cercle.</span><span class="sxs-lookup"><span data-stu-id="75c38-158">A solid-color brush to paint the circle.</span></span>

<span data-ttu-id="75c38-159">Chacune de ces ressources est représentée par une interface COM :</span><span class="sxs-lookup"><span data-stu-id="75c38-159">Each of these resources is represented by a COM interface:</span></span>

-   <span data-ttu-id="75c38-160">L’interface [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) représente la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="75c38-160">The [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) interface represents the render target.</span></span>
-   <span data-ttu-id="75c38-161">L’interface [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) représente le pinceau.</span><span class="sxs-lookup"><span data-stu-id="75c38-161">The [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interface represents the brush.</span></span>

<span data-ttu-id="75c38-162">Le programme Circle stocke les pointeurs vers ces interfaces en tant que variables membres de la `MainWindow` classe :</span><span class="sxs-lookup"><span data-stu-id="75c38-162">The Circle program stores pointers to these interfaces as member variables of the `MainWindow` class:</span></span>


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



<span data-ttu-id="75c38-163">Le code suivant crée ces deux ressources.</span><span class="sxs-lookup"><span data-stu-id="75c38-163">The following code creates these two resources.</span></span>


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



<span data-ttu-id="75c38-164">Pour créer une cible de rendu pour une fenêtre, appelez la méthode [**ID2D1Factory :: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) sur la fabrique Direct2D.</span><span class="sxs-lookup"><span data-stu-id="75c38-164">To create a render target for a window, call the [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method on the Direct2D factory.</span></span>

-   <span data-ttu-id="75c38-165">Le premier paramètre spécifie des options qui sont communes à tout type de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="75c38-165">The first parameter specifies options that are common to any type of render target.</span></span> <span data-ttu-id="75c38-166">Ici, nous transmettons les options par défaut en appelant la fonction d’assistance [**d2d1 :: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span><span class="sxs-lookup"><span data-stu-id="75c38-166">Here, we pass in default options by calling the helper function [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span></span>
-   <span data-ttu-id="75c38-167">Le deuxième paramètre spécifie le handle vers la fenêtre plus la taille de la cible de rendu, en pixels.</span><span class="sxs-lookup"><span data-stu-id="75c38-167">The second parameter specifies the handle to the window plus the size of the render target, in pixels.</span></span>
-   <span data-ttu-id="75c38-168">Le troisième paramètre reçoit un pointeur [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="75c38-168">The third parameter receives an [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) pointer.</span></span>

<span data-ttu-id="75c38-169">Pour créer le pinceau de couleur unie, appelez la méthode [**ID2D1RenderTarget :: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) sur la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="75c38-169">To create the solid-color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method on the render target.</span></span> <span data-ttu-id="75c38-170">La couleur est donnée sous la forme d’une valeur [**\_ \_ F de couleur d2d1**](/windows/desktop/Direct2D/d2d1-color-f) .</span><span class="sxs-lookup"><span data-stu-id="75c38-170">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) value.</span></span> <span data-ttu-id="75c38-171">Pour plus d’informations sur les couleurs dans Direct2D, consultez [utilisation de Color dans Direct2D](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="75c38-171">For more information about colors in Direct2D, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>

<span data-ttu-id="75c38-172">Notez également que si la cible de rendu existe déjà, la `CreateGraphicsResources` méthode retourne **S \_ OK** sans rien faire.</span><span class="sxs-lookup"><span data-stu-id="75c38-172">Also, notice that if the render target already exists, the `CreateGraphicsResources` method returns **S\_OK** without doing anything.</span></span> <span data-ttu-id="75c38-173">La raison de cette conception sera évidente dans la rubrique suivante.</span><span class="sxs-lookup"><span data-stu-id="75c38-173">The reason for this design will become clear in the next topic.</span></span>

## <a name="next"></a><span data-ttu-id="75c38-174">Suivant</span><span class="sxs-lookup"><span data-stu-id="75c38-174">Next</span></span>

[<span data-ttu-id="75c38-175">Dessiner avec Direct2D</span><span class="sxs-lookup"><span data-stu-id="75c38-175">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)

 

 