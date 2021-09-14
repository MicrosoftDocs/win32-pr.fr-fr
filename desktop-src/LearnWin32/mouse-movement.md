---
title: Mouvement de la souris
description: Mouvement de la souris
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094330"
---
# <a name="mouse-movement"></a>Mouvement de la souris

lorsque la souris se déplace, Windows publie un message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . Par défaut, **WM \_ MOUSEMOVE** accède à la fenêtre qui contient le curseur. Vous pouvez remplacer ce comportement en *capturant* la souris, qui est décrite dans la section suivante.

Le message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) contient les mêmes paramètres que les messages pour les clics de souris. Les 16 bits les plus bas de *lParam* contiennent la coordonnée x, et les 16 bits suivants contiennent la coordonnée y. Utilisez les macros [**obten \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) et [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour décompresser les coordonnées de *lParam*. Le paramètre *wParam* contient une opération or au niveau du bit, indiquant l’état des autres **boutons de la** souris plus les touches Maj et Ctrl. Le code suivant obtient les coordonnées de la souris à partir de *lParam*.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



N’oubliez pas que ces coordonnées sont exprimées en pixels, et non en pixels indépendants du périphérique (DIP). Plus loin dans cette rubrique, nous examinerons le code qui effectue la conversion entre les deux unités.

Une fenêtre peut également recevoir un message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) si la position du curseur change par rapport à la fenêtre. Par exemple, si le curseur est positionné sur une fenêtre et que l’utilisateur masque la fenêtre, la fenêtre reçoit les messages **WM \_ MOUSEMOVE** même si la souris n’a pas été déplacée. L’une des conséquences de ce comportement est que les coordonnées de la souris peuvent ne pas changer entre les messages de la souris **WM \_** .

## <a name="capturing-mouse-movement-outside-the-window"></a>Capture du mouvement de la souris en dehors de la fenêtre

Par défaut, une fenêtre cesse de recevoir des messages [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) si la souris se trouve au-delà du bord de la zone cliente. Mais pour certaines opérations, vous devrez peut-être suivre la position de la souris au-delà de ce point. Par exemple, un programme de dessin peut permettre à l’utilisateur de faire glisser le rectangle de sélection au-delà du bord de la fenêtre, comme indiqué dans le diagramme suivant.

![illustration de la capture de la souris.](images/input01.png)

Pour recevoir des messages de déplacement de la souris au-delà du bord de la fenêtre, appelez la fonction [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) . Après l’appel de cette fonction, la fenêtre continue de recevoir les messages [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) tant que l’utilisateur maintient le bouton de la souris enfoncé, même si la souris se trouve en dehors de la fenêtre. La fenêtre de capture doit être la fenêtre de premier plan, et une seule fenêtre peut être la fenêtre de capture à la fois. Pour libérer la capture de la souris, appelez la fonction [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) .

En général, vous utilisez [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) et [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) de la façon suivante.

1.  Quand l’utilisateur appuie sur le bouton gauche de la souris, appelez [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) pour démarrer la capture de la souris.
2.  Répondre aux messages de déplacement de la souris.
3.  Quand l’utilisateur relâche le bouton gauche de la souris, appelez [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).

## <a name="example-drawing-circles"></a>Exemple : dessin de cercles

Nous allons étendre le programme Circle du [module 3](module-3---windows-graphics.md) en permettant à l’utilisateur de dessiner un cercle avec la souris. Démarrez avec l' [exemple](direct2d-circle-sample.md) de programme de la circonférence de Direct2D. Nous allons modifier le code de cet exemple pour ajouter un dessin simple. Tout d’abord, ajoutez une nouvelle variable membre à la `MainWindow` classe.


```C++
    D2D1_POINT_2F           ptMouse;
```



Cette variable stocke la position de la souris pendant que l’utilisateur fait glisser la souris. Dans le `MainWindow` constructeur, initialisez les variables *ellipse* et *ptMouse* .


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



Supprimez le corps de la `MainWindow::CalculateLayout` méthode, ce qui n’est pas obligatoire pour cet exemple.


```C++
    void    CalculateLayout() { }
```



Ensuite, déclarez les gestionnaires de messages pour les messages du bouton gauche, du bouton gauche vers le haut et du déplacement de la souris.


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



Les coordonnées de la souris sont exprimées en pixels physiques, mais Direct2D attend des pixels indépendants du périphérique (DIP). Pour gérer correctement les paramètres haute résolution, vous devez convertir les coordonnées en pixels en DIP. Pour plus d’informations sur la résolution des questions, consultez [PPP et Device-Independent pixels](dpi-and-device-independent-pixels.md). Le code suivant montre une classe d’assistance qui convertit les pixels en DIP.


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



Appelez `DPIScale::Initialize` dans votre gestionnaire [**WM \_ Create**](/windows/desktop/winmsg/wm-create) après avoir créé l’objet de fabrique Direct2D.


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



Pour faire en sorte que les coordonnées de la souris se trouvent dans les creux des messages de la souris, procédez comme suit :

1.  Utilisez les macros [**obten \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) et [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour connaître les coordonnées en pixels. Ces macros étant définies dans WindowsX. h, n’oubliez pas d’inclure cet en-tête dans votre projet.
2.  Appelez `DPIScale::PixelsToDipsX` et `DPIScale::PixelsToDipsY` pour convertir les pixels en DIP.

Ajoutez maintenant les gestionnaires de messages à votre procédure de fenêtre.


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



Enfin, implémentez les gestionnaires de messages eux-mêmes.

### <a name="left-button-down"></a>Bouton gauche enfoncé

Pour le message de bouton gauche, procédez comme suit :

1.  Appelez [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) pour commencer la capture de la souris.
2.  Stocke la position du clic de la souris dans la variable *ptMouse* . Cette position définit l’angle supérieur gauche du cadre englobant pour l’ellipse.
3.  Réinitialisez la structure d’ellipse.
4.  Appelez [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Cette fonction force la fenêtre à être redessinée.


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a>Déplacement de la souris

Pour le message de déplacement de la souris, vérifiez si le bouton gauche de la souris est enfoncé. Si c’est le cas, recalculez l’ellipse et redessinez la fenêtre. Dans Direct2D, une ellipse est définie par le point central et les rayons x et y. Nous voulons dessiner une ellipse qui correspond au cadre englobant défini par le point de la souris (*ptMouse*) et la position actuelle du curseur (*x*, *y*). un peu d’arithmétique est donc nécessaire pour trouver la largeur, la hauteur et la position de l’ellipse.

Le code suivant recalcule l’ellipse, puis appelle [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) pour repeindre la fenêtre.

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



### <a name="left-button-up"></a>Bouton gauche vers le haut

Pour le message de bouton de gauche, appelez simplement [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) pour libérer la capture de la souris.


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a>Suivant

[Autres opérations de la souris](other-mouse-operations.md)

 

 