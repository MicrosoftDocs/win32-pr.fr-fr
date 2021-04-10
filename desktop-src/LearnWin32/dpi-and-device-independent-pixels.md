---
title: PPP et Device-Independent pixels
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'En savoir plus sur : PPP et Device-Independent pixels'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868661"
---
# <a name="dpi-and-device-independent-pixels"></a>PPP et Device-Independent pixels

Pour programmer efficacement avec les graphiques Windows, vous devez comprendre deux concepts connexes :

-   Points par pouce (DPI)
-   DIP (Device-Independent Pixel).

Commençons par PPP. Cela nécessite un bref détournement dans la typographie. Dans la typographie, la taille du type est mesurée en unités appelées *points*. Un point est égal à 1/72 de pouce.

<dl> 1 PT = 1/72 pouces  
</dl>

> [!Note]  
> Il s’agit de la définition de la publication sur le Bureau du point. Historiquement, la mesure exacte d’un point a varié.

 

Par exemple, une police à 12 points est conçue pour tenir au sein d’une ligne de texte 1/6 "(12/72). Évidemment, cela ne signifie pas que chaque caractère de la police correspond exactement à 1/6. En fait, certains caractères peuvent être plus grands que 1/6». Par exemple, dans de nombreuses polices, le caractère Å est plus haut que la hauteur nominale de la police. Pour s’afficher correctement, la police a besoin d’espace supplémentaire entre le texte. Cet espace est appelé le *début*.

L’illustration suivante montre une police de point de 72. Les lignes pleines affichent un cadre englobant 1 de haut autour du texte. La ligne en pointillés est appelée ligne de *base*. La plupart des caractères d’une police se trouvent dans la ligne de base. La hauteur de la police comprend la partie au-dessus de la ligne de base (le plus *haut) et* la partie au-dessous de la ligne de base (la *descente*). Dans la police indiquée ici, la hauteur est de 56 points et la descente est de 16 points.

![illustration qui montre une police de point de 72.](images/graphics11.png)

Toutefois, en cas d’affichage d’un ordinateur, la mesure de la taille du texte est problématique, car les pixels ne sont pas tous de la même taille. La taille d’un pixel dépend de deux facteurs : la résolution d’affichage et la taille physique de l’analyse. Par conséquent, les pouces physiques ne sont pas une mesure utile, car il n’existe aucune relation fixe entre les pouces et les pixels physiques. Au lieu de cela, les polices sont mesurées en unités *logiques* . Une police de point 72 est définie pour être d’une hauteur de pouce logique. Les pouces logiques sont ensuite convertis en pixels. Pendant de nombreuses années, Windows a utilisé la conversion suivante : un pouce logique est égal à 96 pixels. À l’aide de ce facteur d’échelle, une police de 72 points est rendue sous la forme de 96 pixels de haut. Une police de 12 points a une hauteur de 16 pixels.

<dl> 12 points = 12/72 de pouce logique = 1/6 de pouce logique = 96/6 pixels = 16 pixels  
</dl>

Ce facteur d’échelle est décrit comme étant de 96 points par pouce (DPI). Le terme « points » dérive de l’impression, où les points physiques de l’encre sont mis sur le papier. Pour les écrans d’ordinateur, il serait plus précis d’indiquer 96 pixels par pouce logique, mais le terme PPP est bloqué.

Étant donné que les tailles réelles des pixels varient, le texte lisible sur un moniteur peut être trop petit sur un autre moniteur. En outre, les utilisateurs ont des préférences différentes. certaines personnes préfèrent du texte plus grand. C’est la raison pour laquelle Windows permet à l’utilisateur de modifier le paramètre PPP. Par exemple, si l’utilisateur définit l’affichage sur 144 PPP, une police de 72 point est de 144 pixels de haut. Les paramètres ppp standard sont 100% (96 ppp), 125% (120 ppp) et 150% (144 PPP). L’utilisateur peut également appliquer un paramètre personnalisé. À partir de Windows 7, PPP est un paramètre par utilisateur.

## <a name="dwm-scaling"></a>Mise à l’échelle DWM

Si un programme ne compte pas pour la résolution PPP, les erreurs suivantes peuvent être apparentes aux paramètres haute résolution :

-   Éléments d’interface utilisateur découpés.
-   Disposition incorrecte.
-   Bitmaps et icônes pixellisée.
-   Coordonnées de souris incorrectes, qui peuvent affecter le test de positionnement, le glisser-déplacer, etc.

Pour vous assurer que les anciens programmes fonctionnent aux paramètres haute résolution, le DWM implémente un secours utile. Si un programme n’est pas marqué comme prenant en charge DPI, le DWM met à l’échelle la totalité de l’interface utilisateur pour correspondre au paramètre PPP. Par exemple, à 144 PPP, l’interface utilisateur est mise à l’échelle de 150%, y compris du texte, des graphiques, des contrôles et des tailles de fenêtre. Si le programme crée une fenêtre 500 × 500, la fenêtre s’affiche en réalité sous la forme 750 × 750 pixels et le contenu de la fenêtre est mis à l’échelle en conséquence.

Ce comportement signifie que les anciens programmes « fonctionnent » dans les paramètres haute résolution. Toutefois, la mise à l’échelle aboutit également à une apparence légèrement floue, car la mise à l’échelle est appliquée après le dessin de la fenêtre.

## <a name="dpi-aware-applications"></a>Applications DPI-Aware

Pour éviter la mise à l’échelle DWM, un programme peut se marquer comme prenant en charge DPI. Cela indique au DWM de ne pas effectuer de mise à l’échelle DPI automatique. Toutes les nouvelles applications doivent être conçues pour être compatibles DPI, car la reconnaissance DPI améliore l’apparence de l’interface utilisateur à des paramètres ppp plus élevés.

Un programme déclare lui-même la prise en charge DPI par le biais de son manifeste d’application. Un *manifeste* est un simple fichier XML qui décrit une dll ou une application. Le manifeste est généralement incorporé dans le fichier exécutable, bien qu’il puisse être fourni sous la forme d’un fichier distinct. Un manifeste contient des informations telles que les dépendances de DLL, le niveau de privilège demandé et la version de Windows pour laquelle le programme a été conçu.

Pour déclarer que votre programme prend en charge DPI, incluez les informations suivantes dans le manifeste.

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

La liste présentée ici n’est qu’un manifeste partiel, mais l’éditeur de liens de Visual Studio génère automatiquement le reste du manifeste. Pour inclure un manifeste partiel dans votre projet, procédez comme suit dans Visual Studio.

1.  Dans le menu **projet** , cliquez sur **propriété**.
2.  Dans le volet gauche, développez **Propriétés de configuration**, développez **outil manifeste**, puis cliquez sur **entrée et sortie**.
3.  Dans la zone de texte **fichiers manifeste supplémentaires** , tapez le nom du fichier manifeste, puis cliquez sur **OK**.

En marquant votre programme comme prenant en charge DPI, vous indiquez au DWM de ne pas mettre à l’échelle la fenêtre de votre application. Maintenant, si vous créez une fenêtre 500 × 500, la fenêtre occupe 500 × 500 pixels, quel que soit le paramètre PPP de l’utilisateur.

## <a name="gdi-and-dpi"></a>GDI et PPP

Le dessin GDI est mesuré en pixels. Cela signifie que si votre programme est marqué comme prenant en charge DPI et que vous demandez à GDI de dessiner un rectangle 200 × 100, le rectangle résultant sera 200 pixels de largeur et 100 pixels de haut sur l’écran. Toutefois, les tailles de police GDI sont mises à l’échelle au paramètre PPP actuel. En d’autres termes, si vous créez une police de point de 72, la taille de la police sera de 96 pixels à 96 ppp, mais 144 pixels à 144 DPI. Voici une police de 72 points rendue à 144 PPP à l’aide de GDI.

![diagramme qui affiche la mise à l’échelle des polices en DPI dans GDI.](images/graphics12.png)

Si votre application prend en charge DPI et que vous utilisez GDI pour le dessin, mettez à l’échelle toutes vos coordonnées de dessin pour qu’elles correspondent aux PPP.

## <a name="direct2d-and-dpi"></a>Direct2D et PPP

Direct2D effectue automatiquement une mise à l’échelle pour correspondre au paramètre PPP. Dans Direct2D, les coordonnées sont mesurées en unités appelées *pixels indépendants du périphérique* (DIP). Une DIP est définie comme 1/96ème d’un pouce *logique* . Dans Direct2D, toutes les opérations de dessin sont spécifiées dans des DIP, puis mises à l’échelle avec le paramètre PPP actuel.



| Paramètre PPP | Taille d’adresse DIP    |
|-------------|-------------|
| 96          | 1 pixel     |
| 120         | 1,25 pixels |
| 144         | 1,5 pixels  |



 

Par exemple, si le paramètre PPP de l’utilisateur est de 144 PPP et que vous demandez à Direct2D de dessiner un rectangle 200 × 100, le rectangle sera 300 × 150 pixels physiques. De plus, DirectWrite mesure les tailles de police dans des DIP, plutôt que des points. Pour créer une police de 12 points, spécifiez 16 DIP (12 points = 1/6 de pouce logique = 96/6 DIP). Lorsque le texte est dessiné à l’écran, Direct2D convertit les DIP en pixels physiques. L’avantage de ce système est que les unités de mesure sont cohérentes pour le texte et le dessin, quel que soit le paramètre PPP actuel.

Un mot de prudence : les coordonnées de la souris et de la fenêtre sont toujours données en pixels physiques, et non en DIP. Par exemple, si vous traitez le message [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) , la position de la souris est indiquée en pixels physiques. Pour dessiner un point à cette position, vous devez convertir les coordonnées en pixels en DIP.

## <a name="converting-physical-pixels-to-dips"></a>Conversion de pixels physiques en DIP

La conversion de pixels physiques en DIP utilise la formule suivante.

<dl> DIP = pixels/(DPI/96.0)  
</dl>

Pour connaître le paramètre ppp, appelez la méthode [**ID2D1Factory :: GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) . La valeur PPP est retournée sous la forme de deux valeurs à virgule flottante, une pour l’axe des x et une pour l’axe des y. En théorie, ces valeurs peuvent différer. Calculez un facteur d’échelle distinct pour chaque axe.


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



Voici une autre façon d’utiliser le paramètre PPP si vous n’utilisez pas Direct2D :


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> Sur Windows 10, la version 1903,  [**ID2D1Factory :: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) est dépréciée et la recommandation est [**DisplayInformation :: LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) pour les applications du Windows Store ou [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) pour les applications de bureau. Si vous souhaitez toujours l’utiliser, supprimez le message d’erreur du compilateur en écrivant la ligne [**#pragma avertissement (supprimer : 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) juste avant l’appel de [**ID2D1Factory :: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) . Bien qu’il ne soit pas recommandé, il est possible de définir la reconnaissance par défaut des PPP par programmation à l’aide de [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext). Une fois qu’une fenêtre (HWND) a été créée dans votre processus, la modification du mode de reconnaissance PPP n’est plus prise en charge. Si vous définissez le mode de prise en forme des PPP par défaut du processus par programme, vous devez appeler l’API correspondante avant la création de tous les HWND. Pour plus d’informations, consultez [définition de la prise en face PPP par défaut d’un processus](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).

## <a name="resizing-the-render-target"></a>Redimensionnement de la cible de rendu

Si la taille de la fenêtre change, vous devez redimensionner la cible de rendu pour qu’elle corresponde. Dans la plupart des cas, vous devrez également mettre à jour la disposition et redessiner la fenêtre. Le code suivant illustre ces étapes.


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



La fonction [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) obtient la nouvelle taille de la zone cliente, en pixels physiques (et non en DIP). La méthode [**ID2D1HwndRenderTarget :: Resize**](../direct2d/id2d1hwndrendertarget-resize.md) met à jour la taille de la cible de rendu, également spécifiée en pixels. La fonction [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) force une redessine en ajoutant la zone cliente entière à la région de mise à jour de la fenêtre. (Consultez [peinture de la fenêtre](painting-the-window.md), dans le module 1.)

À mesure que la fenêtre s’agrandit ou rétrécit, vous devez généralement recalculer la position des objets que vous dessinez. Par exemple, dans le programme Circle, le rayon et le point central doivent être mis à jour :


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



La méthode [**ID2D1RenderTarget ::**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) Desize retourne la taille de la cible de rendu dans des DIP (et non des pixels), qui est l’unité appropriée pour le calcul de la disposition. Il existe une méthode étroitement liée, [**ID2D1RenderTarget :: GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), qui retourne la taille en pixels physiques. Pour une cible de rendu **HWND** , cette valeur correspond à la taille retournée par [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect). Mais souvenez-vous que le dessin est effectué en DIP, et non en pixels.

## <a name="next"></a>Suivant

[Utilisation de Color dans Direct2D](using-color-in-direct2d.md)

 

 
