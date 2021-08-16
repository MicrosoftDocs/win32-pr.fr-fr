---
title: Rendre des cibles, des appareils et des ressources
description: Rendre des cibles, des appareils et des ressources
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381d6e696cc9dce47cc8dad05b0e546371d50c51012daba725eb08f20d247eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387630"
---
# <a name="render-targets-devices-and-resources"></a>Rendre des cibles, des appareils et des ressources

Une *cible de rendu* est simplement l’emplacement où votre programme sera dessiné. En règle générale, la cible de rendu est une fenêtre (plus particulièrement, la zone cliente de la fenêtre). Il peut également s’agir d’une image bitmap en mémoire qui n’est pas affichée. Une cible de rendu est représentée par l’interface [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) .

Un *appareil* est une abstraction qui représente tout ce qui dessine les pixels. Un périphérique matériel utilise le GPU pour des performances plus rapides, alors qu’un périphérique logiciel utilise le processeur. L’application ne crée pas l’appareil. Au lieu de cela, l’appareil est créé implicitement lorsque l’application crée la cible de rendu. Chaque cible de rendu est associée à un appareil particulier, qu’il s’agisse d’un matériel ou d’un logiciel.

![diagramme qui montre la relation entre une cible de rendu et un appareil.](images/graphics09.png)

Une *ressource* est un objet que le programme utilise pour le dessin. Voici quelques exemples de ressources qui sont définies dans Direct2D :

-   **Pinceau**. Contrôle la façon dont les lignes et les régions sont peintes. Les types Brush incluent des pinceaux de couleur unie et des pinceaux de dégradé.
-   **Style de trait**. Contrôle l’apparence d’une ligne, par exemple Dash ou Solid.
-   **Géométrie**. Représente une collection de lignes et de courbes.
-   **Maille**. Forme formée de triangles. Les données de maillage peuvent être consommées directement par le GPU, contrairement aux données géométriques, qui doivent être converties avant le rendu.

Les cibles de rendu sont également considérées comme un type de ressource.

Certaines ressources tirent parti de l’accélération matérielle. Une ressource de ce type est toujours associée à un appareil particulier, matériel (GPU) ou logiciel (UC). Ce type de ressource est appelé *dépendant du périphérique*. Les pinceaux et les maillages sont des exemples de ressources dépendantes de l’appareil. Si l’appareil n’est plus disponible, la ressource doit être recréée pour un nouvel appareil.

D’autres ressources sont conservées dans la mémoire de l’UC, quel que soit l’appareil utilisé. Ces ressources sont *indépendantes des appareils*, car elles ne sont pas associées à un appareil particulier. Il n’est pas nécessaire de recréer des ressources indépendantes du périphérique quand l’appareil change. Les styles de trait et les géométries sont des ressources indépendantes du périphérique.

La documentation MSDN pour chaque ressource indique si la ressource est dépendante du périphérique ou indépendante du périphérique. Chaque type de ressource est représenté par une interface qui dérive de [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource). Par exemple, les pinceaux sont représentés par l’interface [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) .

## <a name="the-direct2d-factory-object"></a>Objet de fabrique Direct2D

La première étape de l’utilisation de Direct2D consiste à créer une instance de l’objet de fabrique Direct2D. Dans la programmation de l’ordinateur, une *fabrique* est un objet qui crée d’autres objets. La fabrique Direct2D crée les types d’objets suivants :

-   Cibles de rendu.
-   Ressources indépendantes du périphérique, telles que les styles de trait et les géométries.

Les ressources dépendantes de l’appareil, telles que les pinceaux et les bitmaps, sont créées par l’objet de la cible de rendu.

![diagramme qui affiche la fabrique Direct2D.](images/graphics10.png)

Pour créer l’objet de fabrique Direct2D, appelez la fonction [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



Le premier paramètre est un indicateur qui spécifie les options de création. Le **type de fabrique d2d1 indicateur à \_ \_ \_ \_ thread unique** signifie que vous n’allez pas appeler Direct2D à partir de plusieurs threads. Pour prendre en charge les appels à partir de plusieurs threads, spécifiez le **\_ type de fabrique d2d1 \_ \_ multithread \_**. Si votre programme utilise un seul thread pour appeler Direct2D, l’option à thread unique est plus efficace.

Le deuxième paramètre de la fonction [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) reçoit un pointeur vers l’interface [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) .

Vous devez créer l’objet de fabrique Direct2D avant le premier message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) . Le gestionnaire de messages [**WM \_ Create**](/windows/desktop/winmsg/wm-create) est un bon endroit pour créer la fabrique :


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a>Création de ressources Direct2D

Le programme Circle utilise les ressources suivantes dépendantes de l’appareil :

-   Cible de rendu associée à la fenêtre d’application.
-   Pinceau de couleur unie pour peindre le cercle.

Chacune de ces ressources est représentée par une interface COM :

-   L’interface [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) représente la cible de rendu.
-   L’interface [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) représente le pinceau.

Le programme Circle stocke les pointeurs vers ces interfaces en tant que variables membres de la `MainWindow` classe :


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



Le code suivant crée ces deux ressources.


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



Pour créer une cible de rendu pour une fenêtre, appelez la méthode [**ID2D1Factory :: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) sur la fabrique Direct2D.

-   Le premier paramètre spécifie des options qui sont communes à tout type de cible de rendu. Ici, nous transmettons les options par défaut en appelant la fonction d’assistance [**d2d1 :: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).
-   Le deuxième paramètre spécifie le handle vers la fenêtre plus la taille de la cible de rendu, en pixels.
-   Le troisième paramètre reçoit un pointeur [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) .

Pour créer le pinceau de couleur unie, appelez la méthode [**ID2D1RenderTarget :: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) sur la cible de rendu. La couleur est donnée sous la forme d’une valeur [**\_ \_ F de couleur d2d1**](/windows/desktop/Direct2D/d2d1-color-f) . Pour plus d’informations sur les couleurs dans Direct2D, consultez [utilisation de Color dans Direct2D](using-color-in-direct2d.md).

Notez également que si la cible de rendu existe déjà, la `CreateGraphicsResources` méthode retourne **S \_ OK** sans rien faire. La raison de cette conception sera évidente dans la rubrique suivante.

## <a name="next"></a>Suivant

[Dessiner avec Direct2D](drawing-with-direct2d.md)

 

 