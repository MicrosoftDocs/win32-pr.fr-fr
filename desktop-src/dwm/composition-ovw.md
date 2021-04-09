---
title: Activer et contrôler la composition DWM
description: Les API de composition Gestionnaire de fenêtrage (DWM) fournissent plusieurs fonctions permettant de définir et d’interroger des informations de base utilisées par le DWM.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Gestionnaire de fenêtrage (DWM), composition
- DWM (Gestionnaire de fenêtrage), composition
- composition
- composition du Bureau
- colorisation
- rendu de région non cliente
- Gestionnaire de fenêtrage (DWM), colorisation
- DWM (Gestionnaire de fenêtrage), colorisation
- Gestionnaire de fenêtrage (DWM), rendu de région non client
- DWM (Gestionnaire de fenêtrage), rendu de région non client
- Gestionnaire de fenêtrage (DWM), messagerie
- DWM (Gestionnaire de fenêtrage), messagerie
- messagerie
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: 8d7654f479896002b4bc65df613fab9506caf2a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840645"
---
# <a name="enable-and-control-dwm-composition"></a>Activer et contrôler la composition DWM

Les API de composition Gestionnaire de fenêtrage (DWM) fournissent plusieurs fonctions permettant de définir et d’interroger des informations de base utilisées par le DWM. Ces API vous permettent d’interroger et de modifier l’état de la composition. En outre, vous pouvez définir et interroger la stratégie de rendu pour différents attributs de fenêtre DWM.

## <a name="retrieving-colorization-information"></a>Récupération des informations de colorisation

La couleur de la zone non cliente d’une fenêtre est déterminée par le thème de couleur système actuel. La valeur de colorisation est fournie via les API DWM pour permettre à votre application de correspondre à l’interface utilisateur du client avec le thème de couleur système.

Pour accéder à cette valeur de colorisation et surveiller la modification de couleur, utilisez la fonction [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) et le message [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) .

Cet exemple montre comment gérer le message de couleur modifiée et accéder à la nouvelle couleur.

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a>Contrôle du rendu d’une région non cliente

La transparence de la zone non cliente d’une fenêtre et des effets de transition sont deux des effets visuels que le DWM active. Votre application doit peut-être désactiver ou réactiver ces effets pour des raisons de style ou de compatibilité. Les fonctions suivantes sont utilisées pour gérer la transparence et le comportement d’effet de transition.

- [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

Pour récupérer l’état de rendu non client actuel pour la fenêtre d’une application, appelez [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) avec *dwAttribute* défini sur [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute). Comme vous pouvez le voir dans la documentation de [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), lorsque vous transmettez cet indicateur à **DwmGetWindowAttribute**, la valeur d’attribut Récupérée est de type **bool**. Les différents indicateurs font en sorte que **DwmGetWindowAttribute** retourne des valeurs de types différents. Voici un exemple de code :

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

L’exemple suivant montre comment utiliser l’indicateur [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) avec **DwmGetWindowAttribute** pour récupérer le rectangle de limites de cadre étendu d’une fenêtre. La documentation de cet indicateur nous indique que la valeur de l’attribut récupéré est de type **Rect**.

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> Suivez le même modèle de programmation que celui illustré ci-dessus lorsque vous appelez [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) avec des indicateurs pour différents attributs. La rubrique d’énumération [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) indique, dans la ligne pour chaque indicateur, le type de valeur auquel vous devez passer un pointeur dans le paramètre *pvAttribute* pour **DwmGetWindowAttribute**. Le paramètre *cbAttribute* contient la taille, en octets, de cet objet.

[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) permet à votre application de définir la stratégie de rendu de la zone non cliente. Cette fonction détermine également la manière dont votre application doit gérer les effets de transition DWM.

L’exemple suivant désactive le rendu de la zone non cliente. Cela provoque la désactivation des appels précédents à [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) ou à [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

En plus de contrôler le rendu de la zone non cliente, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) peut également contrôler les effets de transition DWM. Vous pouvez définir le comportement de transition en utilisant **DWMWA \_ transitions \_ FORCEDISABLED** comme paramètre *dwAttribute* .

## <a name="messages"></a>Messages

Les messages suivants fournissent une notification des événements DWM. Ces messages peuvent être utilisés pour surveiller les modifications telles que les modifications d’état de composition et les modifications de thème de couleur système.

- [**\_DWMCOLORIZATIONCOLORCHANGED WM**](wm-dwmcolorizationcolorchanged.md)
- [**\_DWMCOMPOSITIONCHANGED WM**](wm-dwmcompositionchanged.md)
- [**\_DWMNCRENDERINGCHANGED WM**](wm-dwmncrenderingchanged.md)
- [**\_DWMWINDOWMAXIMIZEDCHANGE WM**](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a>Désactivation de la composition DWM (Windows 7 et versions antérieures)

> [!WARNING]
> Les informations de cette section s’appliquent uniquement aux systèmes Windows 7 et versions antérieures.

Étant donné que DWM utilise l’unité de traitement graphique (GPU) pour la composition du bureau, votre application doit peut-être désactiver DWM pour des raisons de compatibilité. Les applications qui prennent le contrôle total du bureau, comme les jeux qui s’exécutent en mode plein écran, doivent déterminer si le DWM est activé et, si c’est le cas, le désactiver. Pour ce faire, deux fonctions sont nécessaires.

- [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

Un appel à [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) avec *FEnable* défini sur **DWM \_ EC \_ DISABLECOMPOSITION** désactive la composition DWM jusqu’à ce que le processus appelant soit arrêté ou que la composition ait été réactivée en appelant **DwmEnableComposition** avec *fEnable* défini sur **DWM \_ EC \_ ENABLECOMPOSITION**. La composition DWM redémarre automatiquement dès que toutes les applications qui ont une composition désactivée ont été arrêtées ou ont été réactivées manuellement en appelant **DwmEnableComposition**.

> [!NOTE]  
> Le DWM désactive automatiquement la composition lorsqu’une application tente de dessiner directement sur la surface d’affichage principale. La composition sera désactivée jusqu’à ce que la surface principale du périphérique soit libérée par cette application.
