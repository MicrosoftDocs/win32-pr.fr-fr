---
title: Barres de défilement plat
description: Microsoft Internet Explorer 4,0 a introduit une nouvelle technologie visuelle appelée barres de défilement plat.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e56db4ee987a6d8cdc7b185f5db0f8d89540453
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423889"
---
# <a name="flat-scroll-bars"></a>Barres de défilement plat

Microsoft Internet Explorer 4,0 a introduit une nouvelle technologie visuelle appelée barres de défilement plat. Fonctionnellement, les barres de défilement plat se comportent comme des barres de défilement standard. La différence est que vous pouvez personnaliser leur apparence dans une plus grande mesure par rapport aux barres de défilement standard.

L’illustration suivante montre une fenêtre qui contient une barre de défilement plate.

![capture d’écran d’une fenêtre qui contient une barre de défilement plate](images/flatsb.jpg)

> [!Note]  
> Les barres de défilement plat sont prises en charge par les versions 4,71 à 5,82 de Comctl32.dll. Les versions 6,00 et ultérieures de Comctl32.dll ne prennent pas en charge les barres de défilement plat.

 

## <a name="using-flat-scroll-bars"></a>Utilisation des barres de défilement plat

Cette section décrit comment implémenter des barres de défilement plates dans votre application.

### <a name="before-you-begin"></a>Avant de commencer

Pour utiliser les fonctions de barre de défilement plat, vous devez inclure commctrl. h dans vos fichiers sources et établir un lien avec Comctl32. lib.

### <a name="adding-flat-scroll-bars-to-a-window"></a>Ajout de barres de défilement plates à une fenêtre

Pour ajouter des barres de défilement plates à une fenêtre, appelez [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), en passant le handle à la fenêtre. Au lieu d’utiliser les fonctions de barre de défilement standard pour manipuler vos barres de défilement, vous devez utiliser la fonction FlatSB xxx équivalente \_ . Il existe des fonctions de barre de défilement plat pour définir et récupérer les informations de défilement, la plage et la position. Si les barres de défilement plat n’ont pas été initialisées pour votre fenêtre, l’API de barre de défilement plate sera différée aux fonctions standard correspondantes, si elles sont utilisées. Cela vous permet d’activer et de désactiver les barres de défilement plat sans avoir à écrire du code conditionnel.

Étant donné qu’une application a peut-être défini des métriques personnalisées pour ses barres de défilement plates, elles ne sont pas mises à jour automatiquement en cas de modification des mesures du système. Lorsque les mesures de la barre de défilement système changent, un message [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) est Broadcast, avec son *wParam* défini sur [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). Pour mettre à jour les barres de défilement plat avec les nouvelles métriques du système, les applications doivent gérer ce message et modifier les propriétés dépendantes de la barre de défilement plat de manière explicite.

Pour mettre à jour les propriétés de la barre de défilement, utilisez [**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop). Le fragment de code suivant modifie les propriétés dépendantes de la mesure de la barre de défilement plate en valeurs système actuelles.


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a>Amélioration des barres de défilement plat

[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) vous permet de modifier les barres de défilement plat pour personnaliser l’apparence de votre fenêtre. Pour les barres de défilement verticales, vous pouvez modifier la largeur de la barre et la hauteur des flèches de direction. Pour les barres de défilement horizontales, vous pouvez modifier la hauteur de la barre et la largeur des flèches de direction. Vous pouvez également modifier la couleur d’arrière-plan des barres de défilement horizontale et verticale.

[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) vous permet également de personnaliser le mode d’affichage des barres de défilement plates. En modifiant les \_ Propriétés WSB prop \_ VSTYLE et WSB \_ prop \_ HSTYLE, vous pouvez définir le type de barre de défilement que vous souhaitez utiliser. Trois styles sont disponibles.



|   Style                 |   Description                                                                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODE FSB d' \_ Encarta \_ | Une barre de défilement standard standard est affichée. Lorsque la souris se déplace sur un bouton de direction ou le curseur de défilement, cette partie de la barre de défilement s’affiche en 3D.             |
| \_mode plat \_ FSB    | Une barre de défilement standard standard est affichée. Lorsque la souris se déplace sur un bouton de direction ou le curseur de défilement, cette partie de la barre de défilement s’affiche dans les couleurs inversées. |
| \_mode normal \_ FSB | Une barre de défilement normale et non plate est affichée. Aucun effet visuel spécial ne sera appliqué.                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a>Supprimer des barres de défilement plat

Si vous souhaitez supprimer les barres de défilement plat de votre fenêtre, appelez la fonction [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) , en passant le handle à la fenêtre. Cette fonction supprime uniquement les barres de défilement plat de votre fenêtre au moment de l’exécution. Vous n’avez pas besoin d’appeler cette fonction lorsque votre fenêtre est détruite.

 

 