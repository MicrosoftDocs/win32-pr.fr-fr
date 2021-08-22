---
title: Dessiner avec Direct2D
description: Après avoir créé vos ressources graphiques, vous êtes prêt à dessiner.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d8a346300b32fe1c716e51efe6bfb8fdbf6220fb2ff17df6de617de27ba1a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535073"
---
# <a name="drawing-with-direct2d"></a>Dessiner avec Direct2D

Après avoir créé vos ressources graphiques, vous êtes prêt à dessiner.

## <a name="drawing-an-ellipse"></a>Dessin d’une ellipse

Le programme [Circle](your-first-direct2d-program.md) effectue une logique de dessin très simple :

1.  Remplir l’arrière-plan avec une couleur unie.
2.  Dessinez un cercle plein.

![capture d’écran du programme Circle.](images/graphics08.png)

Étant donné que la cible de rendu est une fenêtre (par opposition à une image bitmap ou à une autre surface hors écran), le dessin s’effectue en réponse aux messages de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) . Le code suivant illustre la procédure de fenêtre pour le programme Circle.


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

Voici le code qui dessine le cercle.

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



L’interface [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) est utilisée pour toutes les opérations de dessin. La méthode du programme `OnPaint` effectue les opérations suivantes :

1.  La méthode [**ID2D1RenderTarget :: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) signale le début du dessin.
2.  La méthode [**ID2D1RenderTarget :: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) remplit l’intégralité de la cible de rendu avec une couleur unie. La couleur est donnée sous la forme d’une structure [**\_ \_ F de couleur d2d1**](/windows/desktop/Direct2D/d2d1-color-f) . Vous pouvez utiliser la classe [**d2d1 :: ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) pour initialiser la structure. Pour plus d’informations, consultez [utilisation de Color dans Direct2D](using-color-in-direct2d.md).
3.  La méthode [**ID2D1RenderTarget :: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) dessine une Ellipse remplie à l’aide du pinceau spécifié pour le remplissage. Une ellipse est spécifiée par un point central et les rayons x et y. Si les rayons x et y sont identiques, le résultat est un cercle.
4.  La méthode [**ID2D1RenderTarget :: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) signale l’achèvement du dessin pour ce frame. Toutes les opérations de dessin doivent être placées entre les appels à [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) et **EndDraw**.

Les méthodes [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)et [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) ont toutes un type de retour **void** . Si une erreur se produit pendant l’exécution de l’une de ces méthodes, l’erreur est signalée par la valeur de retour de la méthode [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . La `CreateGraphicsResources` méthode est présentée dans la rubrique [création de ressources Direct2D](render-targets--devices--and-resources.md). Cette méthode crée la cible de rendu et le pinceau de couleur unie.

L’appareil peut mettre en mémoire tampon les commandes de dessin et différer de leur exécution jusqu’à ce que [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) soit appelé. Vous pouvez forcer l’appareil à exécuter des commandes de dessin en attente en appelant [**ID2D1RenderTarget :: Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush). Toutefois, le vidage peut réduire les performances.

## <a name="handling-device-loss"></a>Gestion de la perte d’appareil

Pendant que votre programme est en cours d’exécution, le périphérique graphique que vous utilisez peut devenir indisponible. Par exemple, l’appareil peut être perdu si la résolution d’affichage change ou si l’utilisateur supprime la carte d’affichage. Si l’appareil est perdu, la cible de rendu devient également non valide, ainsi que toutes les ressources dépendantes de l’appareil qui ont été associées à l’appareil. Direct2D signale un appareil perdu en renvoyant le code d’erreur **D2DERR \_ recreate \_ target** à partir de la méthode [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Si vous recevez ce code d’erreur, vous devez recréer la cible de rendu et toutes les ressources dépendantes de l’appareil.

Pour supprimer une ressource, il suffit de libérer l’interface pour cette ressource.


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



La création d’une ressource peut être une opération coûteuse, donc ne recréez pas vos ressources pour chaque message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) . Créez une ressource une seule fois et mettez en cache le pointeur de ressource jusqu’à ce que la ressource soit non valide en raison de la perte de l’appareil, ou jusqu’à ce que vous n’ayez plus besoin de cette ressource.

## <a name="the-direct2d-render-loop"></a>La boucle de rendu Direct2D

Indépendamment de ce que vous dessinez, votre programme doit effectuer une boucle semblable à la suivante.

1.  Créer des ressources indépendantes du périphérique.
2.  Affiche la scène.
    1.  Vérifiez s’il existe une cible de rendu valide. Si ce n’est pas le cas, créez la cible de rendu et les ressources dépendantes de l’appareil.
    2.  Appelez [**ID2D1RenderTarget :: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).
    3.  Émettez les commandes de dessin.
    4.  Appelez [**ID2D1RenderTarget :: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).
    5.  Si [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) retourne **D2DERR \_ \_ cible de recréation**, ignorez la cible de rendu et les ressources dépendantes de l’appareil.
3.  Répétez l’étape 2 chaque fois que vous devez mettre à jour ou redessiner la scène.

Si la cible de rendu est une fenêtre, l’étape 2 se produit chaque fois que la fenêtre reçoit un message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) .

La boucle présentée ici gère la perte d’appareil en ignorant les ressources dépendantes de l’appareil et en les recréant au début de la boucle suivante (étape 2a).

## <a name="next"></a>Suivant

[PPP et Device-Independent pixels](dpi-and-device-independent-pixels.md)

 

 