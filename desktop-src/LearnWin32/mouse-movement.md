---
title: Mouvement de la souris
description: Mouvement de la souris
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "106531241"
---
# <a name="mouse-movement"></a><span data-ttu-id="27114-103">Mouvement de la souris</span><span class="sxs-lookup"><span data-stu-id="27114-103">Mouse Movement</span></span>

<span data-ttu-id="27114-104">Lorsque la souris se déplace, Windows publie un message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="27114-104">When the mouse moves, Windows posts a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="27114-105">Par défaut, **WM \_ MOUSEMOVE** accède à la fenêtre qui contient le curseur.</span><span class="sxs-lookup"><span data-stu-id="27114-105">By default, **WM\_MOUSEMOVE** goes to the window that contains the cursor.</span></span> <span data-ttu-id="27114-106">Vous pouvez remplacer ce comportement en *capturant* la souris, qui est décrite dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="27114-106">You can override this behavior by *capturing* the mouse, which is described in the next section.</span></span>

<span data-ttu-id="27114-107">Le message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) contient les mêmes paramètres que les messages pour les clics de souris.</span><span class="sxs-lookup"><span data-stu-id="27114-107">The [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message contains the same parameters as the messages for mouse clicks.</span></span> <span data-ttu-id="27114-108">Les 16 bits les plus bas de *lParam* contiennent la coordonnée x, et les 16 bits suivants contiennent la coordonnée y.</span><span class="sxs-lookup"><span data-stu-id="27114-108">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="27114-109">Utilisez les macros [**obten \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) et [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour décompresser les coordonnées de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="27114-109">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span> <span data-ttu-id="27114-110">Le paramètre *wParam* contient une opération or au niveau du bit, indiquant l’état des autres **boutons de la** souris plus les touches Maj et Ctrl.</span><span class="sxs-lookup"><span data-stu-id="27114-110">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span> <span data-ttu-id="27114-111">Le code suivant obtient les coordonnées de la souris à partir de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="27114-111">The following code gets the mouse coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="27114-112">N’oubliez pas que ces coordonnées sont exprimées en pixels, et non en pixels indépendants du périphérique (DIP).</span><span class="sxs-lookup"><span data-stu-id="27114-112">Remember that these coordinates are in pixels, not device-independent pixels (DIPs).</span></span> <span data-ttu-id="27114-113">Plus loin dans cette rubrique, nous examinerons le code qui effectue la conversion entre les deux unités.</span><span class="sxs-lookup"><span data-stu-id="27114-113">Later in this topic, we will look at code that converts between the two units.</span></span>

<span data-ttu-id="27114-114">Une fenêtre peut également recevoir un message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) si la position du curseur change par rapport à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="27114-114">A window can also receive a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message if the position of the cursor changes relative to the window.</span></span> <span data-ttu-id="27114-115">Par exemple, si le curseur est positionné sur une fenêtre et que l’utilisateur masque la fenêtre, la fenêtre reçoit les messages **WM \_ MOUSEMOVE** même si la souris n’a pas été déplacée.</span><span class="sxs-lookup"><span data-stu-id="27114-115">For example, if the cursor is positioned over a window, and the user hides the window, the window receives **WM\_MOUSEMOVE** messages even if the mouse did not move.</span></span> <span data-ttu-id="27114-116">L’une des conséquences de ce comportement est que les coordonnées de la souris peuvent ne pas changer entre les messages de la souris **WM \_** .</span><span class="sxs-lookup"><span data-stu-id="27114-116">One consequence of this behavior is that the mouse coordinates might not change between **WM\_MOUSEMOVE** messages.</span></span>

## <a name="capturing-mouse-movement-outside-the-window"></a><span data-ttu-id="27114-117">Capture du mouvement de la souris en dehors de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="27114-117">Capturing Mouse Movement Outside the Window</span></span>

<span data-ttu-id="27114-118">Par défaut, une fenêtre cesse de recevoir des messages [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) si la souris se trouve au-delà du bord de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="27114-118">By default, a window stops receiving [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages if the mouse moves past the edge of the client area.</span></span> <span data-ttu-id="27114-119">Mais pour certaines opérations, vous devrez peut-être suivre la position de la souris au-delà de ce point.</span><span class="sxs-lookup"><span data-stu-id="27114-119">But for some operations, you might need to track the mouse position beyond this point.</span></span> <span data-ttu-id="27114-120">Par exemple, un programme de dessin peut permettre à l’utilisateur de faire glisser le rectangle de sélection au-delà du bord de la fenêtre, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="27114-120">For example, a drawing program might enable the user to drag the selection rectangle beyond the edge of the window, as shown in the following diagram.</span></span>

![illustration de la capture de la souris.](images/input01.png)

<span data-ttu-id="27114-122">Pour recevoir des messages de déplacement de la souris au-delà du bord de la fenêtre, appelez la fonction [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) .</span><span class="sxs-lookup"><span data-stu-id="27114-122">To receive mouse-move messages past the edge of the window, call the [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) function.</span></span> <span data-ttu-id="27114-123">Après l’appel de cette fonction, la fenêtre continue de recevoir les messages [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) tant que l’utilisateur maintient le bouton de la souris enfoncé, même si la souris se trouve en dehors de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="27114-123">After this function is called, the window will continue to receive [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages for as long as the user holds at least one mouse button down, even if the mouse moves outside the window.</span></span> <span data-ttu-id="27114-124">La fenêtre de capture doit être la fenêtre de premier plan, et une seule fenêtre peut être la fenêtre de capture à la fois.</span><span class="sxs-lookup"><span data-stu-id="27114-124">The capture window must be the foreground window, and only one window can be the capture window at a time.</span></span> <span data-ttu-id="27114-125">Pour libérer la capture de la souris, appelez la fonction [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) .</span><span class="sxs-lookup"><span data-stu-id="27114-125">To release mouse capture, call the [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) function.</span></span>

<span data-ttu-id="27114-126">En général, vous utilisez [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) et [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) de la façon suivante.</span><span class="sxs-lookup"><span data-stu-id="27114-126">You would typically use [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) and [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) in the following way.</span></span>

1.  <span data-ttu-id="27114-127">Quand l’utilisateur appuie sur le bouton gauche de la souris, appelez [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) pour démarrer la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="27114-127">When the user presses the left mouse button, call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to start capturing the mouse.</span></span>
2.  <span data-ttu-id="27114-128">Répondre aux messages de déplacement de la souris.</span><span class="sxs-lookup"><span data-stu-id="27114-128">Respond to mouse-move messages.</span></span>
3.  <span data-ttu-id="27114-129">Quand l’utilisateur relâche le bouton gauche de la souris, appelez [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span><span class="sxs-lookup"><span data-stu-id="27114-129">When the user releases the left mouse button, call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span></span>

## <a name="example-drawing-circles"></a><span data-ttu-id="27114-130">Exemple : dessin de cercles</span><span class="sxs-lookup"><span data-stu-id="27114-130">Example: Drawing Circles</span></span>

<span data-ttu-id="27114-131">Nous allons étendre le programme Circle du [module 3](module-3---windows-graphics.md) en permettant à l’utilisateur de dessiner un cercle avec la souris.</span><span class="sxs-lookup"><span data-stu-id="27114-131">Let's extend the Circle program from [Module 3](module-3---windows-graphics.md) by enabling the user to draw a circle with the mouse.</span></span> <span data-ttu-id="27114-132">Démarrez avec l' [exemple](direct2d-circle-sample.md) de programme de la circonférence de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="27114-132">Start with the [Direct2D Circle Sample](direct2d-circle-sample.md) program.</span></span> <span data-ttu-id="27114-133">Nous allons modifier le code de cet exemple pour ajouter un dessin simple.</span><span class="sxs-lookup"><span data-stu-id="27114-133">We will modify the code in this sample to add simple drawing.</span></span> <span data-ttu-id="27114-134">Tout d’abord, ajoutez une nouvelle variable membre à la `MainWindow` classe.</span><span class="sxs-lookup"><span data-stu-id="27114-134">First, add a new member variable to the `MainWindow` class.</span></span>


```C++
    D2D1_POINT_2F           ptMouse;
```



<span data-ttu-id="27114-135">Cette variable stocke la position de la souris pendant que l’utilisateur fait glisser la souris.</span><span class="sxs-lookup"><span data-stu-id="27114-135">This variable stores the mouse-down position while the user is dragging the mouse.</span></span> <span data-ttu-id="27114-136">Dans le `MainWindow` constructeur, initialisez les variables *ellipse* et *ptMouse* .</span><span class="sxs-lookup"><span data-stu-id="27114-136">In the `MainWindow` constructor, initialize the *ellipse* and *ptMouse* variables.</span></span>


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



<span data-ttu-id="27114-137">Supprimez le corps de la `MainWindow::CalculateLayout` méthode, ce qui n’est pas obligatoire pour cet exemple.</span><span class="sxs-lookup"><span data-stu-id="27114-137">Remove the body of the `MainWindow::CalculateLayout` method; it's not required for this example.</span></span>


```C++
    void    CalculateLayout() { }
```



<span data-ttu-id="27114-138">Ensuite, déclarez les gestionnaires de messages pour les messages du bouton gauche, du bouton gauche vers le haut et du déplacement de la souris.</span><span class="sxs-lookup"><span data-stu-id="27114-138">Next, declare message handlers for the left-button down, left-button up, and mouse-move messages.</span></span>


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



<span data-ttu-id="27114-139">Les coordonnées de la souris sont exprimées en pixels physiques, mais Direct2D attend des pixels indépendants du périphérique (DIP).</span><span class="sxs-lookup"><span data-stu-id="27114-139">Mouse coordinates are given in physical pixels, but Direct2D expects device-independent pixels (DIPs).</span></span> <span data-ttu-id="27114-140">Pour gérer correctement les paramètres haute résolution, vous devez convertir les coordonnées en pixels en DIP.</span><span class="sxs-lookup"><span data-stu-id="27114-140">To handle high-DPI settings correctly, you must translate the pixel coordinates into DIPs.</span></span> <span data-ttu-id="27114-141">Pour plus d’informations sur la résolution des questions, consultez [PPP et Device-Independent pixels](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="27114-141">For more discussion about DPI, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span> <span data-ttu-id="27114-142">Le code suivant montre une classe d’assistance qui convertit les pixels en DIP.</span><span class="sxs-lookup"><span data-stu-id="27114-142">The following code shows a helper class that converts pixels into DIPs.</span></span>


```C++
class DPIScale
{
    static float scaleX;
    static float scaleY;

public:
    static void Initialize(ID2D1Factory *pFactory)
    {
        FLOAT dpiX, dpiY;
        pFactory->GetDesktopDpi(&dpiX, &dpiY);
        scaleX = dpiX/96.0f;
        scaleY = dpiY/96.0f;
    }

    template <typename T>
    static D2D1_POINT_2F PixelsToDips(T x, T y)
    {
        return D2D1::Point2F(static_cast<float>(x) / scaleX, static_cast<float>(y) / scaleY);
    }
};

float DPIScale::scaleX = 1.0f;
float DPIScale::scaleY = 1.0f;
```



<span data-ttu-id="27114-143">Appelez `DPIScale::Initialize` dans votre gestionnaire [**WM \_ Create**](/windows/desktop/winmsg/wm-create) après avoir créé l’objet de fabrique Direct2D.</span><span class="sxs-lookup"><span data-stu-id="27114-143">Call `DPIScale::Initialize` in your [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) handler, after you create the Direct2D factory object.</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        DPIScale::Initialize(pFactory);
        return 0;
```



<span data-ttu-id="27114-144">Pour faire en sorte que les coordonnées de la souris se trouvent dans les creux des messages de la souris, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="27114-144">To get the mouse coordinates in DIPs from the mouse messages, do the following:</span></span>

1.  <span data-ttu-id="27114-145">Utilisez les macros [**obten \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) et [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour connaître les coordonnées en pixels.</span><span class="sxs-lookup"><span data-stu-id="27114-145">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to get the pixel coordinates.</span></span> <span data-ttu-id="27114-146">Ces macros étant définies dans WindowsX. h, n’oubliez pas d’inclure cet en-tête dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="27114-146">These macros are defined in WindowsX.h, so remember to include that header in your project.</span></span>
2.  <span data-ttu-id="27114-147">Appelez `DPIScale::PixelsToDipsX` et `DPIScale::PixelsToDipsY` pour convertir les pixels en DIP.</span><span class="sxs-lookup"><span data-stu-id="27114-147">Call `DPIScale::PixelsToDipsX` and `DPIScale::PixelsToDipsY` to convert pixels to DIPs.</span></span>

<span data-ttu-id="27114-148">Ajoutez maintenant les gestionnaires de messages à votre procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="27114-148">Now add the message handlers to your window procedure.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        OnLButtonDown(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;

    case WM_LBUTTONUP: 
        OnLButtonUp();
        return 0;

    case WM_MOUSEMOVE: 
        OnMouseMove(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;
```



<span data-ttu-id="27114-149">Enfin, implémentez les gestionnaires de messages eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="27114-149">Finally, implement the message handlers themselves.</span></span>

### <a name="left-button-down"></a><span data-ttu-id="27114-150">Bouton gauche enfoncé</span><span class="sxs-lookup"><span data-stu-id="27114-150">Left Button Down</span></span>

<span data-ttu-id="27114-151">Pour le message de bouton gauche, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="27114-151">For the left-button down message, do the following:</span></span>

1.  <span data-ttu-id="27114-152">Appelez [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) pour commencer la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="27114-152">Call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to begin capturing the mouse.</span></span>
2.  <span data-ttu-id="27114-153">Stocke la position du clic de la souris dans la variable *ptMouse* .</span><span class="sxs-lookup"><span data-stu-id="27114-153">Store the position of the mouse click in the *ptMouse* variable.</span></span> <span data-ttu-id="27114-154">Cette position définit l’angle supérieur gauche du cadre englobant pour l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="27114-154">This position defines the upper left corner of the bounding box for the ellipse.</span></span>
3.  <span data-ttu-id="27114-155">Réinitialisez la structure d’ellipse.</span><span class="sxs-lookup"><span data-stu-id="27114-155">Reset the ellipse structure.</span></span>
4.  <span data-ttu-id="27114-156">Appelez [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="27114-156">Call [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="27114-157">Cette fonction force la fenêtre à être redessinée.</span><span class="sxs-lookup"><span data-stu-id="27114-157">This function forces the window to be repainted.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a><span data-ttu-id="27114-158">Déplacement de la souris</span><span class="sxs-lookup"><span data-stu-id="27114-158">Mouse Move</span></span>

<span data-ttu-id="27114-159">Pour le message de déplacement de la souris, vérifiez si le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="27114-159">For the mouse-move message, check whether the left mouse button is down.</span></span> <span data-ttu-id="27114-160">Si c’est le cas, recalculez l’ellipse et redessinez la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="27114-160">If it is, recalculate the ellipse and repaint the window.</span></span> <span data-ttu-id="27114-161">Dans Direct2D, une ellipse est définie par le point central et les rayons x et y.</span><span class="sxs-lookup"><span data-stu-id="27114-161">In Direct2D, an ellipse is defined by the center point and x- and y-radii.</span></span> <span data-ttu-id="27114-162">Nous voulons dessiner une ellipse qui correspond au cadre englobant défini par le point de la souris (*ptMouse*) et la position actuelle du curseur (*x*, *y*). un peu d’arithmétique est donc nécessaire pour trouver la largeur, la hauteur et la position de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="27114-162">We want to draw an ellipse that fits the bounding box defined by the mouse-down point (*ptMouse*) and the current cursor position (*x*, *y*), so a bit of arithmetic is needed to find the width, height, and position of the ellipse.</span></span>

<span data-ttu-id="27114-163">Le code suivant recalcule l’ellipse, puis appelle [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) pour repeindre la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="27114-163">The following code recalculates the ellipse and then calls [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) to repaint the window.</span></span>

![Diagramme qui affiche une ellipse avec des rayons x et y.](images/input02.png)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    if (flags & MK_LBUTTON) 
    { 
        const D2D1_POINT_2F dips = DPIScale::PixelsToDips(pixelX, pixelY);

        const float width = (dips.x - ptMouse.x) / 2;
        const float height = (dips.y - ptMouse.y) / 2;
        const float x1 = ptMouse.x + width;
        const float y1 = ptMouse.y + height;

        ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);

        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



### <a name="left-button-up"></a><span data-ttu-id="27114-165">Bouton gauche vers le haut</span><span class="sxs-lookup"><span data-stu-id="27114-165">Left Button Up</span></span>

<span data-ttu-id="27114-166">Pour le message de bouton de gauche, appelez simplement [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) pour libérer la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="27114-166">For the left-button-up message, simply call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) to release the mouse capture.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a><span data-ttu-id="27114-167">Suivant</span><span class="sxs-lookup"><span data-stu-id="27114-167">Next</span></span>

[<span data-ttu-id="27114-168">Autres opérations de la souris</span><span class="sxs-lookup"><span data-stu-id="27114-168">Other Mouse Operations</span></span>](other-mouse-operations.md)

 

 