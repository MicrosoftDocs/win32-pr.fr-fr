---
title: Exemple d’entrée d’utilisateur étendu
description: .
ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdde7f14dda356d0f65103c77e3b73c2f0de50a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104554227"
---
# <a name="user-input-extended-example"></a><span data-ttu-id="280c8-103">Entrée utilisateur : exemple étendu</span><span class="sxs-lookup"><span data-stu-id="280c8-103">User Input: Extended Example</span></span>

<span data-ttu-id="280c8-104">Nous allons combiner tout ce que nous avons appris sur les entrées utilisateur pour créer un programme de dessin simple.</span><span class="sxs-lookup"><span data-stu-id="280c8-104">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="280c8-105">Voici une capture d’écran du programme :</span><span class="sxs-lookup"><span data-stu-id="280c8-105">Here is a screen shot of the program:</span></span>

![capture d’écran du programme de dessin](images/input03.png)

<span data-ttu-id="280c8-107">L’utilisateur peut dessiner des ellipses dans différentes couleurs, et sélectionner, déplacer ou supprimer des ellipses.</span><span class="sxs-lookup"><span data-stu-id="280c8-107">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="280c8-108">Pour que l’interface utilisateur reste simple, le programme ne permet pas à l’utilisateur de sélectionner les couleurs des ellipses.</span><span class="sxs-lookup"><span data-stu-id="280c8-108">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="280c8-109">Au lieu de cela, le programme parcourt automatiquement une liste prédéfinie de couleurs.</span><span class="sxs-lookup"><span data-stu-id="280c8-109">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="280c8-110">Le programme ne prend pas en charge les formes autres que les ellipses.</span><span class="sxs-lookup"><span data-stu-id="280c8-110">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="280c8-111">Évidemment, ce programme ne remportera pas de récompenses pour les logiciels graphiques.</span><span class="sxs-lookup"><span data-stu-id="280c8-111">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="280c8-112">Toutefois, il s’agit toujours d’un exemple utile pour apprendre à partir de.</span><span class="sxs-lookup"><span data-stu-id="280c8-112">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="280c8-113">Vous pouvez télécharger le code source complet à partir d’un [exemple de dessin simple](simple-drawing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="280c8-113">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="280c8-114">Cette section couvre uniquement quelques points importants.</span><span class="sxs-lookup"><span data-stu-id="280c8-114">This section will just cover some highlights.</span></span>

<span data-ttu-id="280c8-115">Les points de suspension sont représentés dans le programme par une structure qui contient les données de sélection ([**\_ ellipse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) et la couleur ([**d2d1 de \_ couleur \_ F**](/windows/desktop/Direct2D/d2d1-color-f)).</span><span class="sxs-lookup"><span data-stu-id="280c8-115">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="280c8-116">La structure définit également deux méthodes : une méthode pour dessiner l’ellipse et une méthode pour effectuer un test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="280c8-116">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


```C++
struct MyEllipse
{
    D2D1_ELLIPSE    ellipse;
    D2D1_COLOR_F    color;

    void Draw(ID2D1RenderTarget *pRT, ID2D1SolidColorBrush *pBrush)
    {
        pBrush->SetColor(color);
        pRT->FillEllipse(ellipse, pBrush);
        pBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black));
        pRT->DrawEllipse(ellipse, pBrush, 1.0f);
    }

    BOOL HitTest(float x, float y)
    {
        const float a = ellipse.radiusX;
        const float b = ellipse.radiusY;
        const float x1 = x - ellipse.point.x;
        const float y1 = y - ellipse.point.y;
        const float d = ((x1 * x1) / (a * a)) + ((y1 * y1) / (b * b));
        return d <= 1.0f;
    }
};
```



<span data-ttu-id="280c8-117">Le programme utilise le même pinceau de couleur unie pour dessiner le remplissage et le contour de chaque ellipse, en modifiant la couleur si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="280c8-117">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="280c8-118">Dans Direct2D, la modification de la couleur d’un pinceau de couleur unie est une opération efficace.</span><span class="sxs-lookup"><span data-stu-id="280c8-118">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="280c8-119">Ainsi, l’objet pinceau de couleur unie prend en charge une méthode [**setColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) .</span><span class="sxs-lookup"><span data-stu-id="280c8-119">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="280c8-120">Les ellipses sont stockées dans un conteneur de **liste** STL :</span><span class="sxs-lookup"><span data-stu-id="280c8-120">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="280c8-121">**le \_ ptr partagé** est une classe de pointeur intelligent qui a été ajoutée à C++ dans TR1 et formalisée en C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="280c8-121">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="280c8-122">Visual Studio 2010 ajoute la prise en charge des fonctionnalités **partagées \_ PT** r et autres C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="280c8-122">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="280c8-123">Pour plus d’informations, consultez [exploration des nouvelles fonctionnalités C++ et MFC dans Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) dans *MSDN Magazine*.</span><span class="sxs-lookup"><span data-stu-id="280c8-123">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="280c8-124">(Cette ressource n’est peut-être pas disponible dans certaines langues et certains pays.)</span><span class="sxs-lookup"><span data-stu-id="280c8-124">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="280c8-125">Le programme comporte trois modes :</span><span class="sxs-lookup"><span data-stu-id="280c8-125">The program has three modes:</span></span>

-   <span data-ttu-id="280c8-126">Mode dessin.</span><span class="sxs-lookup"><span data-stu-id="280c8-126">Draw mode.</span></span> <span data-ttu-id="280c8-127">L’utilisateur peut dessiner de nouvelles ellipses.</span><span class="sxs-lookup"><span data-stu-id="280c8-127">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="280c8-128">Mode de sélection.</span><span class="sxs-lookup"><span data-stu-id="280c8-128">Selection mode.</span></span> <span data-ttu-id="280c8-129">L’utilisateur peut sélectionner une ellipse.</span><span class="sxs-lookup"><span data-stu-id="280c8-129">The user can select an ellipse.</span></span>
-   <span data-ttu-id="280c8-130">Mode glisser.</span><span class="sxs-lookup"><span data-stu-id="280c8-130">Drag mode.</span></span> <span data-ttu-id="280c8-131">L’utilisateur peut faire glisser une ellipse sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="280c8-131">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="280c8-132">L’utilisateur peut basculer entre le mode dessin et le mode de sélection en utilisant les mêmes raccourcis clavier que ceux décrits dans [tables d’accélérateurs](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="280c8-132">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="280c8-133">À partir du mode de sélection, le programme passe en mode glisser si l’utilisateur clique sur une ellipse.</span><span class="sxs-lookup"><span data-stu-id="280c8-133">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="280c8-134">Il repasse en mode de sélection lorsque l’utilisateur relâche le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="280c8-134">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="280c8-135">La sélection actuelle est stockée sous la forme d’un itérateur dans la liste des ellipses.</span><span class="sxs-lookup"><span data-stu-id="280c8-135">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="280c8-136">La méthode d’assistance `MainWindow::Selection` retourne un pointeur vers l’ellipse sélectionnée ou la valeur **nullptr** si aucune sélection n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="280c8-136">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


```C++
    list<shared_ptr<MyEllipse>>::iterator   selection;
     
    shared_ptr<MyEllipse> Selection() 
    { 
        if (selection == ellipses.end()) 
        { 
            return nullptr;
        }
        else
        {
            return (*selection);
        }
    }

    void    ClearSelection() { selection = ellipses.end(); }
```



<span data-ttu-id="280c8-137">Le tableau suivant récapitule les effets de l’entrée de souris dans chacun des trois modes.</span><span class="sxs-lookup"><span data-stu-id="280c8-137">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="280c8-138">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="280c8-138">Mouse Input</span></span>      | <span data-ttu-id="280c8-139">Mode dessin</span><span class="sxs-lookup"><span data-stu-id="280c8-139">Draw Mode</span></span>                                          | <span data-ttu-id="280c8-140">Mode de sélection</span><span class="sxs-lookup"><span data-stu-id="280c8-140">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="280c8-141">Mode glisser</span><span class="sxs-lookup"><span data-stu-id="280c8-141">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="280c8-142">Bouton gauche enfoncé</span><span class="sxs-lookup"><span data-stu-id="280c8-142">Left button down</span></span> | <span data-ttu-id="280c8-143">Définissez la capture de la souris et commencez à dessiner une nouvelle ellipse.</span><span class="sxs-lookup"><span data-stu-id="280c8-143">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="280c8-144">Libère la sélection actuelle et effectue un test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="280c8-144">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="280c8-145">Si une ellipse est atteinte, capturez le curseur, sélectionnez l’ellipse et basculez en mode glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="280c8-145">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="280c8-146">Aucune action.</span><span class="sxs-lookup"><span data-stu-id="280c8-146">No action.</span></span>                 |
| <span data-ttu-id="280c8-147">Déplacement de la souris</span><span class="sxs-lookup"><span data-stu-id="280c8-147">Mouse move</span></span>       | <span data-ttu-id="280c8-148">Si le bouton gauche est enfoncé, redimensionnez l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="280c8-148">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="280c8-149">Aucune action.</span><span class="sxs-lookup"><span data-stu-id="280c8-149">No action.</span></span>                                                                                                                                   | <span data-ttu-id="280c8-150">Déplacer l’ellipse sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="280c8-150">Move the selected ellipse.</span></span> |
| <span data-ttu-id="280c8-151">Bouton gauche vers le haut</span><span class="sxs-lookup"><span data-stu-id="280c8-151">Left button up</span></span>   | <span data-ttu-id="280c8-152">Arrêter le dessin de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="280c8-152">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="280c8-153">Aucune action.</span><span class="sxs-lookup"><span data-stu-id="280c8-153">No action.</span></span>                                                                                                                                   | <span data-ttu-id="280c8-154">Basculez en mode de sélection.</span><span class="sxs-lookup"><span data-stu-id="280c8-154">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="280c8-155">La méthode suivante de la `MainWindow` classe gère les messages [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) .</span><span class="sxs-lookup"><span data-stu-id="280c8-155">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if (mode == DrawMode)
    {
        POINT pt = { pixelX, pixelY };

        if (DragDetect(m_hwnd, pt))
        {
            SetCapture(m_hwnd);
        
            // Start a new ellipse.
            InsertEllipse(dipX, dipY);
        }
    }
    else
    {
        ClearSelection();

        if (HitTest(dipX, dipY))
        {
            SetCapture(m_hwnd);

            ptMouse = Selection()->ellipse.point;
            ptMouse.x -= dipX;
            ptMouse.y -= dipY;

            SetMode(DragMode);
        }
    }
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



<span data-ttu-id="280c8-156">Les coordonnées de la souris sont passées à cette méthode en pixels, puis converties en adresses IP (DIP).</span><span class="sxs-lookup"><span data-stu-id="280c8-156">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="280c8-157">Il est important de ne pas confondre ces deux unités.</span><span class="sxs-lookup"><span data-stu-id="280c8-157">It is important not to confuse these two units.</span></span> <span data-ttu-id="280c8-158">Par exemple, la fonction [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) utilise des pixels, mais le dessin et le test de positionnement utilisent des DIP.</span><span class="sxs-lookup"><span data-stu-id="280c8-158">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="280c8-159">La règle générale est que les fonctions liées à l’entrée de souris ou Windows utilisent des pixels, tandis que Direct2D et DirectWrite utilisent des DIP.</span><span class="sxs-lookup"><span data-stu-id="280c8-159">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="280c8-160">Testez toujours votre programme à un paramètre de haute résolution et n’oubliez pas de marquer votre programme comme prenant en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="280c8-160">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="280c8-161">Pour plus d’informations, consultez [dpi et Device-Independent pixels](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="280c8-161">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="280c8-162">Voici le code qui gère les messages [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="280c8-162">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if ((flags & MK_LBUTTON) && Selection())
    { 
        if (mode == DrawMode)
        {
            // Resize the ellipse.
            const float width = (dipX - ptMouse.x) / 2;
            const float height = (dipY - ptMouse.y) / 2;
            const float x1 = ptMouse.x + width;
            const float y1 = ptMouse.y + height;

            Selection()->ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);
        }
        else if (mode == DragMode)
        {
            // Move the ellipse.
            Selection()->ellipse.point.x = dipX + ptMouse.x;
            Selection()->ellipse.point.y = dipY + ptMouse.y;
        }
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="280c8-163">La logique de redimensionnement d’une ellipse a été décrite précédemment, dans la section [exemple : dessiner des cercles](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="280c8-163">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="280c8-164">Notez également l’appel à [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="280c8-164">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="280c8-165">Cela permet de s’assurer que la fenêtre est redessinée.</span><span class="sxs-lookup"><span data-stu-id="280c8-165">This makes sure that the window is repainted.</span></span> <span data-ttu-id="280c8-166">Le code suivant gère les messages [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="280c8-166">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    if ((mode == DrawMode) && Selection())
    {
        ClearSelection();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
    else if (mode == DragMode)
    {
        SetMode(SelectMode);
    }
    ReleaseCapture(); 
}
```



<span data-ttu-id="280c8-167">Comme vous pouvez le voir, les gestionnaires de messages pour l’entrée de la souris ont tous un code de branchement, selon le mode actuel.</span><span class="sxs-lookup"><span data-stu-id="280c8-167">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="280c8-168">C’est une conception acceptable pour ce programme relativement simple.</span><span class="sxs-lookup"><span data-stu-id="280c8-168">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="280c8-169">Toutefois, cela peut rapidement devenir trop complexe si de nouveaux modes sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="280c8-169">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="280c8-170">Pour un programme plus volumineux, une architecture MVC (Model-View-Controller) peut être une meilleure conception.</span><span class="sxs-lookup"><span data-stu-id="280c8-170">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="280c8-171">Dans ce type d’architecture, le *contrôleur*, qui gère l’entrée d’utilisateur, est séparé du *modèle*, qui gère les données d’application.</span><span class="sxs-lookup"><span data-stu-id="280c8-171">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="280c8-172">Lorsque le programme change de mode, le curseur change pour fournir des commentaires à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="280c8-172">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


```C++
void MainWindow::SetMode(Mode m)
{
    mode = m;

    // Update the cursor
    LPWSTR cursor;
    switch (mode)
    {
    case DrawMode:
        cursor = IDC_CROSS;
        break;

    case SelectMode:
        cursor = IDC_HAND;
        break;

    case DragMode:
        cursor = IDC_SIZEALL;
        break;
    }

    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
}
```



<span data-ttu-id="280c8-173">Enfin, n’oubliez pas de définir le curseur lorsque la fenêtre reçoit un message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) :</span><span class="sxs-lookup"><span data-stu-id="280c8-173">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="280c8-174">Résumé</span><span class="sxs-lookup"><span data-stu-id="280c8-174">Summary</span></span>

<span data-ttu-id="280c8-175">Dans ce module, vous avez appris à gérer l’entrée au clavier et à la souris. Comment définir des raccourcis clavier ; et comment mettre à jour l’image de curseur pour refléter l’état actuel du programme.</span><span class="sxs-lookup"><span data-stu-id="280c8-175">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 