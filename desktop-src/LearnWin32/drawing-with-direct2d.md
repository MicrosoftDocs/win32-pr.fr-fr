---
title: Dessiner avec Direct2D
description: Après avoir créé vos ressources graphiques, vous êtes prêt à dessiner.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f8f3cf82d3ce6f485a7c54700c32c9eb65d054
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463035"
---
# <a name="drawing-with-direct2d"></a><span data-ttu-id="ea765-103">Dessiner avec Direct2D</span><span class="sxs-lookup"><span data-stu-id="ea765-103">Drawing with Direct2D</span></span>

<span data-ttu-id="ea765-104">Après avoir créé vos ressources graphiques, vous êtes prêt à dessiner.</span><span class="sxs-lookup"><span data-stu-id="ea765-104">After you create your graphics resources, you are ready to draw.</span></span>

## <a name="drawing-an-ellipse"></a><span data-ttu-id="ea765-105">Dessin d’une ellipse</span><span class="sxs-lookup"><span data-stu-id="ea765-105">Drawing an Ellipse</span></span>

<span data-ttu-id="ea765-106">Le programme [Circle](your-first-direct2d-program.md) effectue une logique de dessin très simple :</span><span class="sxs-lookup"><span data-stu-id="ea765-106">The [Circle](your-first-direct2d-program.md) program performs very simple drawing logic:</span></span>

1.  <span data-ttu-id="ea765-107">Remplir l’arrière-plan avec une couleur unie.</span><span class="sxs-lookup"><span data-stu-id="ea765-107">Fill the background with a solid color.</span></span>
2.  <span data-ttu-id="ea765-108">Dessinez un cercle plein.</span><span class="sxs-lookup"><span data-stu-id="ea765-108">Draw a filled circle.</span></span>

![capture d’écran du programme Circle.](images/graphics08.png)

<span data-ttu-id="ea765-110">Étant donné que la cible de rendu est une fenêtre (par opposition à une image bitmap ou à une autre surface hors écran), le dessin s’effectue en réponse aux messages de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="ea765-110">Because the render target is a window (as opposed to a bitmap or other offscreen surface), drawing is done in response to [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) messages.</span></span> <span data-ttu-id="ea765-111">Le code suivant illustre la procédure de fenêtre pour le programme Circle.</span><span class="sxs-lookup"><span data-stu-id="ea765-111">The following code shows the window procedure for the Circle program.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

<span data-ttu-id="ea765-112">Voici le code qui dessine le cercle.</span><span class="sxs-lookup"><span data-stu-id="ea765-112">Here is the code that draws the circle.</span></span>

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="ea765-113">L’interface [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) est utilisée pour toutes les opérations de dessin.</span><span class="sxs-lookup"><span data-stu-id="ea765-113">The [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface is used for all drawing operations.</span></span> <span data-ttu-id="ea765-114">La méthode du programme `OnPaint` effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea765-114">The program's `OnPaint` method does the following:</span></span>

1.  <span data-ttu-id="ea765-115">La méthode [**ID2D1RenderTarget :: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) signale le début du dessin.</span><span class="sxs-lookup"><span data-stu-id="ea765-115">The [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method signals the start of drawing.</span></span>
2.  <span data-ttu-id="ea765-116">La méthode [**ID2D1RenderTarget :: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) remplit l’intégralité de la cible de rendu avec une couleur unie.</span><span class="sxs-lookup"><span data-stu-id="ea765-116">The [**ID2D1RenderTarget::Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) method fills the entire render target with a solid color.</span></span> <span data-ttu-id="ea765-117">La couleur est donnée sous la forme d’une structure [**\_ \_ F de couleur d2d1**](/windows/desktop/Direct2D/d2d1-color-f) .</span><span class="sxs-lookup"><span data-stu-id="ea765-117">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) structure.</span></span> <span data-ttu-id="ea765-118">Vous pouvez utiliser la classe [**d2d1 :: ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) pour initialiser la structure.</span><span class="sxs-lookup"><span data-stu-id="ea765-118">You can use the [**D2D1::ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) class to initialize the structure.</span></span> <span data-ttu-id="ea765-119">Pour plus d’informations, consultez [utilisation de Color dans Direct2D](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="ea765-119">For more information, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>
3.  <span data-ttu-id="ea765-120">La méthode [**ID2D1RenderTarget :: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) dessine une Ellipse remplie à l’aide du pinceau spécifié pour le remplissage.</span><span class="sxs-lookup"><span data-stu-id="ea765-120">The [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws a filled ellipse, using the specified brush for the fill.</span></span> <span data-ttu-id="ea765-121">Une ellipse est spécifiée par un point central et les rayons x et y.</span><span class="sxs-lookup"><span data-stu-id="ea765-121">An ellipse is specified by a center point and the x- and y-radii.</span></span> <span data-ttu-id="ea765-122">Si les rayons x et y sont identiques, le résultat est un cercle.</span><span class="sxs-lookup"><span data-stu-id="ea765-122">If the x- and y-radii are the same, the result is a circle.</span></span>
4.  <span data-ttu-id="ea765-123">La méthode [**ID2D1RenderTarget :: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) signale l’achèvement du dessin pour ce frame.</span><span class="sxs-lookup"><span data-stu-id="ea765-123">The [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method signals the completion of drawing for this frame.</span></span> <span data-ttu-id="ea765-124">Toutes les opérations de dessin doivent être placées entre les appels à [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) et **EndDraw**.</span><span class="sxs-lookup"><span data-stu-id="ea765-124">All drawing operations must be placed between calls to [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw**.</span></span>

<span data-ttu-id="ea765-125">Les méthodes [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)et [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) ont toutes un type de retour **void** .</span><span class="sxs-lookup"><span data-stu-id="ea765-125">The [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear), and [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) methods all have a **void** return type.</span></span> <span data-ttu-id="ea765-126">Si une erreur se produit pendant l’exécution de l’une de ces méthodes, l’erreur est signalée par la valeur de retour de la méthode [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="ea765-126">If an error occurs during the execution of any of these methods, the error is signaled through the return value of the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="ea765-127">La `CreateGraphicsResources` méthode est présentée dans la rubrique [création de ressources Direct2D](render-targets--devices--and-resources.md).</span><span class="sxs-lookup"><span data-stu-id="ea765-127">The `CreateGraphicsResources` method is shown in the topic [Creating Direct2D Resources](render-targets--devices--and-resources.md).</span></span> <span data-ttu-id="ea765-128">Cette méthode crée la cible de rendu et le pinceau de couleur unie.</span><span class="sxs-lookup"><span data-stu-id="ea765-128">This method creates the render target and the solid-color brush.</span></span>

<span data-ttu-id="ea765-129">L’appareil peut mettre en mémoire tampon les commandes de dessin et différer de leur exécution jusqu’à ce que [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) soit appelé.</span><span class="sxs-lookup"><span data-stu-id="ea765-129">The device might buffer the drawing commands and defer executing them until [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) is called.</span></span> <span data-ttu-id="ea765-130">Vous pouvez forcer l’appareil à exécuter des commandes de dessin en attente en appelant [**ID2D1RenderTarget :: Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span><span class="sxs-lookup"><span data-stu-id="ea765-130">You can force the device to execute any pending drawing commands by calling [**ID2D1RenderTarget::Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span> <span data-ttu-id="ea765-131">Toutefois, le vidage peut réduire les performances.</span><span class="sxs-lookup"><span data-stu-id="ea765-131">Flushing can reduce performance, however.</span></span>

## <a name="handling-device-loss"></a><span data-ttu-id="ea765-132">Gestion de la perte d’appareil</span><span class="sxs-lookup"><span data-stu-id="ea765-132">Handling Device Loss</span></span>

<span data-ttu-id="ea765-133">Pendant que votre programme est en cours d’exécution, le périphérique graphique que vous utilisez peut devenir indisponible.</span><span class="sxs-lookup"><span data-stu-id="ea765-133">While your program is running, the graphics device that you are using might become unavailable.</span></span> <span data-ttu-id="ea765-134">Par exemple, l’appareil peut être perdu si la résolution d’affichage change ou si l’utilisateur supprime la carte d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ea765-134">For example, the device can be lost if the display resolution changes, or if the user removes the display adapter.</span></span> <span data-ttu-id="ea765-135">Si l’appareil est perdu, la cible de rendu devient également non valide, ainsi que toutes les ressources dépendantes de l’appareil qui ont été associées à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ea765-135">If the device is lost, the render target also becomes invalid, along with any device-dependent resources that were associated with the device.</span></span> <span data-ttu-id="ea765-136">Direct2D signale un appareil perdu en renvoyant le code d’erreur **D2DERR \_ recreate \_ target** à partir de la méthode [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="ea765-136">Direct2D signals a lost device by returning the error code **D2DERR\_RECREATE\_TARGET** from the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="ea765-137">Si vous recevez ce code d’erreur, vous devez recréer la cible de rendu et toutes les ressources dépendantes de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ea765-137">If you receive this error code, you must re-create the render target and all device-dependent resources.</span></span>

<span data-ttu-id="ea765-138">Pour supprimer une ressource, il suffit de libérer l’interface pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="ea765-138">To discard a resource, simply release the interface for that resource.</span></span>


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



<span data-ttu-id="ea765-139">La création d’une ressource peut être une opération coûteuse, donc ne recréez pas vos ressources pour chaque message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="ea765-139">Creating a resource can be an expensive operation, so do not recreate your resources for every [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="ea765-140">Créez une ressource une seule fois et mettez en cache le pointeur de ressource jusqu’à ce que la ressource soit non valide en raison de la perte de l’appareil, ou jusqu’à ce que vous n’ayez plus besoin de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="ea765-140">Create a resource once, and cache the resource pointer until the resource becomes invalid due to device loss, or until you no longer need that resource.</span></span>

## <a name="the-direct2d-render-loop"></a><span data-ttu-id="ea765-141">La boucle de rendu Direct2D</span><span class="sxs-lookup"><span data-stu-id="ea765-141">The Direct2D Render Loop</span></span>

<span data-ttu-id="ea765-142">Indépendamment de ce que vous dessinez, votre programme doit effectuer une boucle semblable à la suivante.</span><span class="sxs-lookup"><span data-stu-id="ea765-142">Regardless of what you draw, your program should perform a loop similar to following.</span></span>

1.  <span data-ttu-id="ea765-143">Créer des ressources indépendantes du périphérique.</span><span class="sxs-lookup"><span data-stu-id="ea765-143">Create device-independent resources.</span></span>
2.  <span data-ttu-id="ea765-144">Affiche la scène.</span><span class="sxs-lookup"><span data-stu-id="ea765-144">Render the scene.</span></span>
    1.  <span data-ttu-id="ea765-145">Vérifiez s’il existe une cible de rendu valide.</span><span class="sxs-lookup"><span data-stu-id="ea765-145">Check if a valid render target exists.</span></span> <span data-ttu-id="ea765-146">Si ce n’est pas le cas, créez la cible de rendu et les ressources dépendantes de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ea765-146">If not, create the render target and the device-dependent resources.</span></span>
    2.  <span data-ttu-id="ea765-147">Appelez [**ID2D1RenderTarget :: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span><span class="sxs-lookup"><span data-stu-id="ea765-147">Call [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span></span>
    3.  <span data-ttu-id="ea765-148">Émettez les commandes de dessin.</span><span class="sxs-lookup"><span data-stu-id="ea765-148">Issue drawing commands.</span></span>
    4.  <span data-ttu-id="ea765-149">Appelez [**ID2D1RenderTarget :: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="ea765-149">Call [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>
    5.  <span data-ttu-id="ea765-150">Si [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) retourne **D2DERR \_ \_ cible de recréation**, ignorez la cible de rendu et les ressources dépendantes de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ea765-150">If [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) returns **D2DERR\_RECREATE\_TARGET**, discard the render target and device-dependent resources.</span></span>
3.  <span data-ttu-id="ea765-151">Répétez l’étape 2 chaque fois que vous devez mettre à jour ou redessiner la scène.</span><span class="sxs-lookup"><span data-stu-id="ea765-151">Repeat step 2 whenever you need to update or redraw the scene.</span></span>

<span data-ttu-id="ea765-152">Si la cible de rendu est une fenêtre, l’étape 2 se produit chaque fois que la fenêtre reçoit un message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="ea765-152">If the render target is a window, step 2 occurs whenever the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="ea765-153">La boucle présentée ici gère la perte d’appareil en ignorant les ressources dépendantes de l’appareil et en les recréant au début de la boucle suivante (étape 2a).</span><span class="sxs-lookup"><span data-stu-id="ea765-153">The loop shown here handles device loss by discarding the device-dependent resources and re-creating them at the start of the next loop (step 2a).</span></span>

## <a name="next"></a><span data-ttu-id="ea765-154">Suivant</span><span class="sxs-lookup"><span data-stu-id="ea765-154">Next</span></span>

[<span data-ttu-id="ea765-155">PPP et Device-Independent pixels</span><span class="sxs-lookup"><span data-stu-id="ea765-155">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)

 

 