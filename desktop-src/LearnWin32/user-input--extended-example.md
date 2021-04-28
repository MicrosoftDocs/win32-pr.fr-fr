---
<span data-ttu-id="67aab-101">title : exemple d’entrée utilisateur étendue Description : entrée utilisateur : exemple étendu ms. AssetID : A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms. topic : article ms. Date : 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="67aab-101">title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="user-input-extended-example"></a><span data-ttu-id="67aab-102">Entrée utilisateur : exemple étendu</span><span class="sxs-lookup"><span data-stu-id="67aab-102">User Input: Extended Example</span></span>

<span data-ttu-id="67aab-103">Nous allons combiner tout ce que nous avons appris sur les entrées utilisateur pour créer un programme de dessin simple.</span><span class="sxs-lookup"><span data-stu-id="67aab-103">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="67aab-104">Voici une capture d’écran du programme :</span><span class="sxs-lookup"><span data-stu-id="67aab-104">Here is a screen shot of the program:</span></span>

![capture d’écran du programme de dessin](images/input03.png)

<span data-ttu-id="67aab-106">L’utilisateur peut dessiner des ellipses dans différentes couleurs, et sélectionner, déplacer ou supprimer des ellipses.</span><span class="sxs-lookup"><span data-stu-id="67aab-106">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="67aab-107">Pour que l’interface utilisateur reste simple, le programme ne permet pas à l’utilisateur de sélectionner les couleurs des ellipses.</span><span class="sxs-lookup"><span data-stu-id="67aab-107">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="67aab-108">Au lieu de cela, le programme parcourt automatiquement une liste prédéfinie de couleurs.</span><span class="sxs-lookup"><span data-stu-id="67aab-108">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="67aab-109">Le programme ne prend pas en charge les formes autres que les ellipses.</span><span class="sxs-lookup"><span data-stu-id="67aab-109">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="67aab-110">Évidemment, ce programme ne remportera pas de récompenses pour les logiciels graphiques.</span><span class="sxs-lookup"><span data-stu-id="67aab-110">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="67aab-111">Toutefois, il s’agit toujours d’un exemple utile pour apprendre à partir de.</span><span class="sxs-lookup"><span data-stu-id="67aab-111">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="67aab-112">Vous pouvez télécharger le code source complet à partir d’un [exemple de dessin simple](simple-drawing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="67aab-112">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="67aab-113">Cette section couvre uniquement quelques points importants.</span><span class="sxs-lookup"><span data-stu-id="67aab-113">This section will just cover some highlights.</span></span>

<span data-ttu-id="67aab-114">Les points de suspension sont représentés dans le programme par une structure qui contient les données de sélection ([**\_ ellipse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) et la couleur ([**d2d1 de \_ couleur \_ F**](/windows/desktop/Direct2D/d2d1-color-f)).</span><span class="sxs-lookup"><span data-stu-id="67aab-114">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="67aab-115">La structure définit également deux méthodes : une méthode pour dessiner l’ellipse et une méthode pour effectuer un test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="67aab-115">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


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



<span data-ttu-id="67aab-116">Le programme utilise le même pinceau de couleur unie pour dessiner le remplissage et le contour de chaque ellipse, en modifiant la couleur si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="67aab-116">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="67aab-117">Dans Direct2D, la modification de la couleur d’un pinceau de couleur unie est une opération efficace.</span><span class="sxs-lookup"><span data-stu-id="67aab-117">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="67aab-118">Ainsi, l’objet pinceau de couleur unie prend en charge une méthode [**setColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) .</span><span class="sxs-lookup"><span data-stu-id="67aab-118">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="67aab-119">Les ellipses sont stockées dans un conteneur de **liste** STL :</span><span class="sxs-lookup"><span data-stu-id="67aab-119">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="67aab-120">**le \_ ptr partagé** est une classe de pointeur intelligent qui a été ajoutée à C++ dans TR1 et formalisée en C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="67aab-120">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="67aab-121">Visual Studio 2010 ajoute la prise en charge des fonctionnalités **partagées \_ PT** r et autres C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="67aab-121">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="67aab-122">Pour plus d’informations, consultez [exploration des nouvelles fonctionnalités C++ et MFC dans Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) dans *MSDN Magazine*.</span><span class="sxs-lookup"><span data-stu-id="67aab-122">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="67aab-123">(Cette ressource n’est peut-être pas disponible dans certaines langues et certains pays.)</span><span class="sxs-lookup"><span data-stu-id="67aab-123">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="67aab-124">Le programme comporte trois modes :</span><span class="sxs-lookup"><span data-stu-id="67aab-124">The program has three modes:</span></span>

-   <span data-ttu-id="67aab-125">Mode dessin.</span><span class="sxs-lookup"><span data-stu-id="67aab-125">Draw mode.</span></span> <span data-ttu-id="67aab-126">L’utilisateur peut dessiner de nouvelles ellipses.</span><span class="sxs-lookup"><span data-stu-id="67aab-126">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="67aab-127">Mode de sélection.</span><span class="sxs-lookup"><span data-stu-id="67aab-127">Selection mode.</span></span> <span data-ttu-id="67aab-128">L’utilisateur peut sélectionner une ellipse.</span><span class="sxs-lookup"><span data-stu-id="67aab-128">The user can select an ellipse.</span></span>
-   <span data-ttu-id="67aab-129">Mode glisser.</span><span class="sxs-lookup"><span data-stu-id="67aab-129">Drag mode.</span></span> <span data-ttu-id="67aab-130">L’utilisateur peut faire glisser une ellipse sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="67aab-130">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="67aab-131">L’utilisateur peut basculer entre le mode dessin et le mode de sélection en utilisant les mêmes raccourcis clavier que ceux décrits dans [tables d’accélérateurs](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="67aab-131">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="67aab-132">À partir du mode de sélection, le programme passe en mode glisser si l’utilisateur clique sur une ellipse.</span><span class="sxs-lookup"><span data-stu-id="67aab-132">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="67aab-133">Il repasse en mode de sélection lorsque l’utilisateur relâche le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="67aab-133">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="67aab-134">La sélection actuelle est stockée sous la forme d’un itérateur dans la liste des ellipses.</span><span class="sxs-lookup"><span data-stu-id="67aab-134">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="67aab-135">La méthode d’assistance `MainWindow::Selection` retourne un pointeur vers l’ellipse sélectionnée ou la valeur **nullptr** si aucune sélection n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="67aab-135">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


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



<span data-ttu-id="67aab-136">Le tableau suivant récapitule les effets de l’entrée de souris dans chacun des trois modes.</span><span class="sxs-lookup"><span data-stu-id="67aab-136">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="67aab-137">Entrée de la souris</span><span class="sxs-lookup"><span data-stu-id="67aab-137">Mouse Input</span></span>      | <span data-ttu-id="67aab-138">Mode dessin</span><span class="sxs-lookup"><span data-stu-id="67aab-138">Draw Mode</span></span>                                          | <span data-ttu-id="67aab-139">Mode de sélection</span><span class="sxs-lookup"><span data-stu-id="67aab-139">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="67aab-140">Mode glisser</span><span class="sxs-lookup"><span data-stu-id="67aab-140">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="67aab-141">Bouton gauche enfoncé</span><span class="sxs-lookup"><span data-stu-id="67aab-141">Left button down</span></span> | <span data-ttu-id="67aab-142">Définissez la capture de la souris et commencez à dessiner une nouvelle ellipse.</span><span class="sxs-lookup"><span data-stu-id="67aab-142">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="67aab-143">Libère la sélection actuelle et effectue un test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="67aab-143">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="67aab-144">Si une ellipse est atteinte, capturez le curseur, sélectionnez l’ellipse et basculez en mode glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="67aab-144">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="67aab-145">Aucune action.</span><span class="sxs-lookup"><span data-stu-id="67aab-145">No action.</span></span>                 |
| <span data-ttu-id="67aab-146">Déplacement de la souris</span><span class="sxs-lookup"><span data-stu-id="67aab-146">Mouse move</span></span>       | <span data-ttu-id="67aab-147">Si le bouton gauche est enfoncé, redimensionnez l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="67aab-147">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="67aab-148">Aucune action.</span><span class="sxs-lookup"><span data-stu-id="67aab-148">No action.</span></span>                                                                                                                                   | <span data-ttu-id="67aab-149">Déplacer l’ellipse sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="67aab-149">Move the selected ellipse.</span></span> |
| <span data-ttu-id="67aab-150">Bouton gauche vers le haut</span><span class="sxs-lookup"><span data-stu-id="67aab-150">Left button up</span></span>   | <span data-ttu-id="67aab-151">Arrêter le dessin de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="67aab-151">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="67aab-152">Aucune action.</span><span class="sxs-lookup"><span data-stu-id="67aab-152">No action.</span></span>                                                                                                                                   | <span data-ttu-id="67aab-153">Basculez en mode de sélection.</span><span class="sxs-lookup"><span data-stu-id="67aab-153">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="67aab-154">La méthode suivante de la `MainWindow` classe gère les messages [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) .</span><span class="sxs-lookup"><span data-stu-id="67aab-154">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


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



<span data-ttu-id="67aab-155">Les coordonnées de la souris sont passées à cette méthode en pixels, puis converties en adresses IP (DIP).</span><span class="sxs-lookup"><span data-stu-id="67aab-155">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="67aab-156">Il est important de ne pas confondre ces deux unités.</span><span class="sxs-lookup"><span data-stu-id="67aab-156">It is important not to confuse these two units.</span></span> <span data-ttu-id="67aab-157">Par exemple, la fonction [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) utilise des pixels, mais le dessin et le test de positionnement utilisent des DIP.</span><span class="sxs-lookup"><span data-stu-id="67aab-157">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="67aab-158">La règle générale est que les fonctions liées à l’entrée de souris ou Windows utilisent des pixels, tandis que Direct2D et DirectWrite utilisent des DIP.</span><span class="sxs-lookup"><span data-stu-id="67aab-158">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="67aab-159">Testez toujours votre programme à un paramètre de haute résolution et n’oubliez pas de marquer votre programme comme prenant en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="67aab-159">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="67aab-160">Pour plus d’informations, consultez [dpi et Device-Independent pixels](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="67aab-160">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="67aab-161">Voici le code qui gère les messages [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="67aab-161">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


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



<span data-ttu-id="67aab-162">La logique de redimensionnement d’une ellipse a été décrite précédemment, dans la section [exemple : dessiner des cercles](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="67aab-162">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="67aab-163">Notez également l’appel à [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="67aab-163">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="67aab-164">Cela permet de s’assurer que la fenêtre est redessinée.</span><span class="sxs-lookup"><span data-stu-id="67aab-164">This makes sure that the window is repainted.</span></span> <span data-ttu-id="67aab-165">Le code suivant gère les messages [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="67aab-165">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


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



<span data-ttu-id="67aab-166">Comme vous pouvez le voir, les gestionnaires de messages pour l’entrée de la souris ont tous un code de branchement, selon le mode actuel.</span><span class="sxs-lookup"><span data-stu-id="67aab-166">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="67aab-167">C’est une conception acceptable pour ce programme relativement simple.</span><span class="sxs-lookup"><span data-stu-id="67aab-167">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="67aab-168">Toutefois, cela peut rapidement devenir trop complexe si de nouveaux modes sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="67aab-168">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="67aab-169">Pour un programme plus volumineux, une architecture MVC (Model-View-Controller) peut être une meilleure conception.</span><span class="sxs-lookup"><span data-stu-id="67aab-169">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="67aab-170">Dans ce type d’architecture, le *contrôleur*, qui gère l’entrée d’utilisateur, est séparé du *modèle*, qui gère les données d’application.</span><span class="sxs-lookup"><span data-stu-id="67aab-170">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="67aab-171">Lorsque le programme change de mode, le curseur change pour fournir des commentaires à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="67aab-171">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


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



<span data-ttu-id="67aab-172">Enfin, n’oubliez pas de définir le curseur lorsque la fenêtre reçoit un message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) :</span><span class="sxs-lookup"><span data-stu-id="67aab-172">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="67aab-173">Résumé</span><span class="sxs-lookup"><span data-stu-id="67aab-173">Summary</span></span>

<span data-ttu-id="67aab-174">Dans ce module, vous avez appris à gérer l’entrée au clavier et à la souris. Comment définir des raccourcis clavier ; et comment mettre à jour l’image de curseur pour refléter l’état actuel du programme.</span><span class="sxs-lookup"><span data-stu-id="67aab-174">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 
