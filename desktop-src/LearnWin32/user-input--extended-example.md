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
# <a name="user-input-extended-example"></a>Entrée utilisateur : exemple étendu

Nous allons combiner tout ce que nous avons appris sur les entrées utilisateur pour créer un programme de dessin simple. Voici une capture d’écran du programme :

![capture d’écran du programme de dessin](images/input03.png)

L’utilisateur peut dessiner des ellipses dans différentes couleurs, et sélectionner, déplacer ou supprimer des ellipses. Pour que l’interface utilisateur reste simple, le programme ne permet pas à l’utilisateur de sélectionner les couleurs des ellipses. Au lieu de cela, le programme parcourt automatiquement une liste prédéfinie de couleurs. Le programme ne prend pas en charge les formes autres que les ellipses. Évidemment, ce programme ne remportera pas de récompenses pour les logiciels graphiques. Toutefois, il s’agit toujours d’un exemple utile pour apprendre à partir de. Vous pouvez télécharger le code source complet à partir d’un [exemple de dessin simple](simple-drawing-sample.md). Cette section couvre uniquement quelques points importants.

Les points de suspension sont représentés dans le programme par une structure qui contient les données de sélection ([**\_ ellipse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) et la couleur ([**d2d1 de \_ couleur \_ F**](/windows/desktop/Direct2D/d2d1-color-f)). La structure définit également deux méthodes : une méthode pour dessiner l’ellipse et une méthode pour effectuer un test de positionnement.


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



Le programme utilise le même pinceau de couleur unie pour dessiner le remplissage et le contour de chaque ellipse, en modifiant la couleur si nécessaire. Dans Direct2D, la modification de la couleur d’un pinceau de couleur unie est une opération efficace. Ainsi, l’objet pinceau de couleur unie prend en charge une méthode [**setColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) .

Les ellipses sont stockées dans un conteneur de **liste** STL :


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> **le \_ ptr partagé** est une classe de pointeur intelligent qui a été ajoutée à C++ dans TR1 et formalisée en C + + 0x. Visual Studio 2010 ajoute la prise en charge des fonctionnalités **partagées \_ PT** r et autres C + + 0x. Pour plus d’informations, consultez [exploration des nouvelles fonctionnalités C++ et MFC dans Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) dans *MSDN Magazine*. (Cette ressource n’est peut-être pas disponible dans certaines langues et certains pays.)

 

Le programme comporte trois modes :

-   Mode dessin. L’utilisateur peut dessiner de nouvelles ellipses.
-   Mode de sélection. L’utilisateur peut sélectionner une ellipse.
-   Mode glisser. L’utilisateur peut faire glisser une ellipse sélectionnée.

L’utilisateur peut basculer entre le mode dessin et le mode de sélection en utilisant les mêmes raccourcis clavier que ceux décrits dans [tables d’accélérateurs](accelerator-tables.md). À partir du mode de sélection, le programme passe en mode glisser si l’utilisateur clique sur une ellipse. Il repasse en mode de sélection lorsque l’utilisateur relâche le bouton de la souris. La sélection actuelle est stockée sous la forme d’un itérateur dans la liste des ellipses. La méthode d’assistance `MainWindow::Selection` retourne un pointeur vers l’ellipse sélectionnée ou la valeur **nullptr** si aucune sélection n’est effectuée.


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



Le tableau suivant récapitule les effets de l’entrée de souris dans chacun des trois modes.



| Entrée de la souris      | Mode dessin                                          | Mode de sélection                                                                                                                               | Mode glisser                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Bouton gauche enfoncé | Définissez la capture de la souris et commencez à dessiner une nouvelle ellipse. | Libère la sélection actuelle et effectue un test de positionnement. Si une ellipse est atteinte, capturez le curseur, sélectionnez l’ellipse et basculez en mode glisser-déplacer. | Aucune action.                 |
| Déplacement de la souris       | Si le bouton gauche est enfoncé, redimensionnez l’ellipse.    | Aucune action.                                                                                                                                   | Déplacer l’ellipse sélectionnée. |
| Bouton gauche vers le haut   | Arrêter le dessin de l’ellipse.                          | Aucune action.                                                                                                                                   | Basculez en mode de sélection.  |



 

La méthode suivante de la `MainWindow` classe gère les messages [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) .


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



Les coordonnées de la souris sont passées à cette méthode en pixels, puis converties en adresses IP (DIP). Il est important de ne pas confondre ces deux unités. Par exemple, la fonction [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) utilise des pixels, mais le dessin et le test de positionnement utilisent des DIP. La règle générale est que les fonctions liées à l’entrée de souris ou Windows utilisent des pixels, tandis que Direct2D et DirectWrite utilisent des DIP. Testez toujours votre programme à un paramètre de haute résolution et n’oubliez pas de marquer votre programme comme prenant en charge DPI. Pour plus d’informations, consultez [dpi et Device-Independent pixels](dpi-and-device-independent-pixels.md).

Voici le code qui gère les messages [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .


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



La logique de redimensionnement d’une ellipse a été décrite précédemment, dans la section [exemple : dessiner des cercles](mouse-movement.md). Notez également l’appel à [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Cela permet de s’assurer que la fenêtre est redessinée. Le code suivant gère les messages [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) .


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



Comme vous pouvez le voir, les gestionnaires de messages pour l’entrée de la souris ont tous un code de branchement, selon le mode actuel. C’est une conception acceptable pour ce programme relativement simple. Toutefois, cela peut rapidement devenir trop complexe si de nouveaux modes sont ajoutés. Pour un programme plus volumineux, une architecture MVC (Model-View-Controller) peut être une meilleure conception. Dans ce type d’architecture, le *contrôleur*, qui gère l’entrée d’utilisateur, est séparé du *modèle*, qui gère les données d’application.

Lorsque le programme change de mode, le curseur change pour fournir des commentaires à l’utilisateur.


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



Enfin, n’oubliez pas de définir le curseur lorsque la fenêtre reçoit un message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) :


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a>Résumé

Dans ce module, vous avez appris à gérer l’entrée au clavier et à la souris. Comment définir des raccourcis clavier ; et comment mettre à jour l’image de curseur pour refléter l’état actuel du programme.

 

 