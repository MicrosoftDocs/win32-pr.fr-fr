---
title: Vue d’ensemble du DWM en arrière-plan
description: L’un des effets de signature Gestionnaire de fenêtrage (DWM) est une zone non cliente translucide et floue. Les API DWM permettent aux applications d’appliquer ces effets à la zone cliente de leurs fenêtres de niveau supérieur.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Gestionnaire de fenêtrage (DWM), effet de flou-arrière-plan
- DWM (Gestionnaire de fenêtrage), effet de flou
- effet Flou-arrière-plan
- effet translucide
- effet de transparence transparent
- Gestionnaire de fenêtrage (DWM), effet translucide
- DWM (Gestionnaire de fenêtrage), effet translucide
- Gestionnaire de fenêtrage (DWM), effet de transparence transparent
- DWM (Gestionnaire de fenêtrage), effet de transparence transparent
- Gestionnaire de fenêtrage (DWM), extension du frame de fenêtre dans la zone cliente
- DWM (Gestionnaire de fenêtrage), extension du frame de fenêtre dans la zone cliente
- extension du frame de fenêtre dans la zone cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7b357719ea3aa5a4853a933350ee2dda417842777354e2bbf1711e1cbeff1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456078"
---
# <a name="dwm-blur-behind-overview"></a>Vue d’ensemble du DWM en arrière-plan

L’un des effets de signature Gestionnaire de fenêtrage (DWM) est une zone non cliente translucide et floue. Les API DWM permettent aux applications d’appliquer ces effets à la zone cliente de leurs fenêtres de niveau supérieur.

> [!Note]  
> Windows Vista Édition familial basique ne prend pas en charge l’effet de transparence transparent. les zones qui s’affichent généralement avec l’effet de transparence sur les autres éditions de Windows sont rendues opaques.
> à partir de Windows 8, l’appel de cette fonction n’entraîne pas l’effet de flou, en raison d’un changement de style dans la manière dont les fenêtres sont affichées.


 

Cette rubrique décrit les scénarios de flou de client suivants que le DWM active.

-   [Ajout d’un flou à une région spécifique de la zone cliente](#adding-blur-to-a-specific-region-of-the-client-area)
-   [Extension du frame de fenêtre dans la zone cliente](#extending-the-window-frame-into-the-client-area)
-   [Rubriques connexes](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a>Ajout d’un flou à une région spécifique de la zone cliente

Une application peut appliquer l’effet de flou derrière la région cliente entière de la fenêtre ou à une sous-région spécifique. Cela permet aux applications d’ajouter un chemin d’accès et des barres de recherche stylisés qui sont visuellement séparés du reste de l’application.

L’API utilisée dans ce scénario est la fonction [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) , qui utilise le [**brouilleur de DWM derrière les constantes**](dwm-bb-constants.md) et la structure [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) .

L’exemple de fonction suivant, `EnableBlurBehind` , illustre comment appliquer l’effet Flou-arrière à la fenêtre entière.


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



Notez que la **valeur null** est spécifiée dans le paramètre *hRgnBlur* . Cela indique au DWM d’appliquer le flou derrière la fenêtre entière.

L’image suivante illustre l’effet de flou-behind appliqué à la fenêtre entière.

![effet Flou-behind appliqué à une fenêtre](images/dwm-blurbehindwindow.png)

Pour appliquer le flou derrière une sous-région, appliquez un handle de région valide (HRGN) au membre **hRgnBlur** de la structure [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) et ajoutez l’indicateur **DWM \_ BB \_ BLURREGION** au membre **dwFlags** .

Lorsque vous appliquez l’effet Flou-arrière à une sous-région de la fenêtre, le canal alpha de la fenêtre est utilisé pour la zone non floue. Cela peut provoquer une transparence inattendue dans la région non floue d’une fenêtre. Par conséquent, soyez vigilant lorsque vous appliquez un effet de flou à une sous-région.

## <a name="extending-the-window-frame-into-the-client-area"></a>Extension du frame de fenêtre dans la zone cliente

Une application peut étendre le flou du frame de fenêtre dans la zone cliente. Cela est utile lorsque vous appliquez l’effet de flou derrière une fenêtre avec une barre d’outils ancrée ou séparez visuellement les contrôles du reste d’une application. Cette fonctionnalité est exposée par la fonction [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .

Pour activer le flou à l’aide de [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), utilisez la structure [**Margins**](/windows/win32/api/uxtheme/ns-uxtheme-margins) pour indiquer la quantité à étendre dans la zone cliente. L’exemple de fonction suivant, `ExtendIntoClientBottom` , active ou désactive l’extension floue en bas du frame non client dans la zone cliente.


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



L’image suivante illustre l’effet de flou-behind étendu dans le bas de la zone cliente.

![image qui montre l’effet de flou-behind étendu au bas d’une zone cliente](images/dwm-extendedbottom.png)

Également disponible par le biais de la méthode [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) , il s’agit de l’effet « feuille de verre », où l’effet de flou est appliqué à la surface entière de la fenêtre sans bordure visible de la fenêtre. L’exemple suivant illustre cet effet lorsque la zone cliente est rendue sans bordure de fenêtre.


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



L’image suivante illustre le flou-en arrière-plan dans le style de fenêtre « feuille de verre ».

![image illustrant l’effet de flou-arrière dans le style de fenêtre « feuille de verre »](images/dwm-sheetofglass.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble du Gestionnaire de fenêtres du Bureau](dwm-overview.md)
</dt> <dt>

[Activer et contrôler la composition du Gestionnaire de fenêtrage](composition-ovw.md)
</dt> <dt>

[Considérations sur les performances et meilleures pratiques](bestpractices-ovw.md)
</dt> </dl>

 

 