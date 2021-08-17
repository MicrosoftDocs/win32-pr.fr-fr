---
title: Menu contextuel contexte
description: une fenêtre contextuelle contextuelle est le contrôle principal dans la vue ContextPopup de l’infrastructure du ruban Windows.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15424aa8b2b82580218eb3663e4b157bce321fdde027e03101ce2cf38626aac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964411"
---
# <a name="context-popup"></a>Menu contextuel contexte

une fenêtre contextuelle contextuelle est le contrôle principal dans la [**vue ContextPopup**](windowsribbon-element-contextpopup.md) de l’infrastructure du ruban Windows. Il s’agit d’un système de menu contextuel riche qui est exposé uniquement par l’infrastructure en tant qu’extension d’une implémentation de ruban ; l’infrastructure n’expose pas la fenêtre contextuelle de contexte en tant que contrôle indépendant.

-   [Composants de la fenêtre contextuelle contextuelle](#context-popup)
-   [Implémenter la fenêtre contextuelle de contexte](#implement-the-context-popup)
    -   [balisage](#markup)
    -   [Code](#code)
-   [Propriétés de la fenêtre contextuelle de contexte](#context-popup-properties)
-   [Rubriques connexes](#related-topics)

## <a name="components-of-the-context-popup"></a>Composants de la fenêtre contextuelle contextuelle

La fenêtre contextuelle de contexte est un conteneur logique pour le menu contextuel et Mini-Toolbar sous-contrôles qui sont exposés via les éléments de balisage [**ContextMenu**](windowsribbon-element-contextmenu.md) et [**MiniToolbar**](windowsribbon-element-minitoolbar.md) , respectivement :

-   Le [**ContextMenu**](windowsribbon-element-contextmenu.md) expose un menu de commandes et de galeries.
-   Le [**MiniToolbar**](windowsribbon-element-minitoolbar.md) expose une barre d’outils flottante de diverses commandes, galeries et contrôles complexes tels que le [contrôle de police](windowsribbon-controls-fontcontrol.md) et la [zone de liste déroulante](windowsribbon-controls-combobox.md).

Chaque sous-contrôle peut apparaître au plus une fois dans un menu contextuel.

La capture d’écran suivante illustre la fenêtre contextuelle de contexte et ses sous-contrôles constitutifs.

![capture d’écran avec légendes montrant les composants d’interface utilisateur contextuels du ruban.](images/controls/contextpopup.png)

La fenêtre contextuelle contextuelle est purement conceptuelle et n’expose pas les fonctionnalités d’interface utilisateur lui-même, telles que le positionnement ou le dimensionnement.

> [!Note]  
> La fenêtre contextuelle s’affiche généralement en cliquant avec le bouton droit de la souris (ou en utilisant le raccourci clavier MAJ + F10) sur un objet qui vous intéresse. Toutefois, les étapes nécessaires à l’affichage de la fenêtre contextuelle sont définies par l’application.

 

## <a name="implement-the-context-popup"></a>Implémenter la fenêtre contextuelle de contexte

de la même façon que d’autres contrôles de l’infrastructure de ruban Windows, la fenêtre contextuelle est implémentée via un composant de balisage qui spécifie ses détails de présentation et un composant de code qui régit ses fonctionnalités.

Le tableau suivant répertorie les contrôles qui sont pris en charge par chaque sous-contrôle contextuel de contexte.



| Contrôler                                                                  | Mini-Toolbar | Menu contextuel |
|--------------------------------------------------------------------------|--------------|--------------|
| [Button](windowsribbon-controls-button.md)                              | x            | x            |
| [Case à cocher](windowsribbon-controls-checkbox.md)                         | x            | x            |
| [Zone de liste déroulante](windowsribbon-controls-combobox.md)                         | x            |              |
| [Bouton déroulant](windowsribbon-controls-dropdownbutton.md)            | x            | x            |
| [Sélecteur de couleurs déroulantes](windowsribbon-controls-dropdowncolorpicker.md) | x            | x            |
| [Galerie déroulante](windowsribbon-controls-dropdowngallery.md)          | x            | x            |
| [Contrôle de police](windowsribbon-controls-fontcontrol.md)                   | x            |              |
| [Bouton aide](windowsribbon-controls-helpbutton.md)                     |              |              |
| [Galerie dans le ruban](windowsribbon-controls-inribbongallery.md)          |              |              |
| [Spinner](windowsribbon-controls-spinner.md)                            |              |              |
| [Bouton partagé](windowsribbon-controls-splitbutton.md)                   | x            | x            |
| [Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md)    | x            | x            |
| [Bouton bascule](windowsribbon-controls-togglebutton.md)                 | x            | x            |



 

### <a name="markup"></a>balisage

Chaque sous-contrôle contextuel de contexte doit être déclaré individuellement dans le balisage.

### <a name="mini-toolbar"></a>Mini-Toolbar

Lorsque vous ajoutez des contrôles à une mini-barre d’outils contextuelle contextuelle, les deux recommandations suivantes doivent être prises en compte :

-   Les contrôles doivent être hautement reconnaissables et fournir des fonctionnalités évidentes. La familiarité est essentielle, car les étiquettes et les info-bulles ne sont pas exposées pour les contrôles de Mini-Toolbar.
-   Chaque commande exposée par un contrôle doit être présentée ailleurs dans l’interface ruban. Le Mini-Toolbar ne prend pas en charge la navigation au clavier.

L’exemple suivant illustre le balisage de base pour un élément [**MiniToolbar**](windowsribbon-element-minitoolbar.md) qui contient trois contrôles [bouton](windowsribbon-controls-button.md) .

> [!Note]  
> Un élément [**MenuGroup**](windowsribbon-element-menugroup.md) est spécifié pour chaque ligne de contrôles dans la mini-barre d’outils.

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a>Menu contextuel

L’exemple suivant illustre le balisage de base pour un élément [**ContextMenu**](windowsribbon-element-contextmenu.md) qui contient trois contrôles [Button](windowsribbon-controls-button.md) .

> [!Note]  
> Chaque ensemble de contrôles de l’élément [**MenuGroup**](windowsribbon-element-menugroup.md) est séparé par une barre horizontale dans le menu contextuel.

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



Bien qu’une fenêtre contextuelle de contexte puisse contenir au plus l’un de chaque sous-contrôle, plusieurs déclarations d’élément [**ContextMenu**](windowsribbon-element-contextmenu.md) et [**MiniToolbar**](windowsribbon-element-minitoolbar.md) dans le balisage du ruban sont valides. Cela permet à une application de prendre en charge diverses combinaisons de menus contextuels et de contrôles de Mini-Toolbar, en fonction de critères définis par l’application, tels que le contexte de l’espace de travail.

Pour plus d’informations, consultez l’élément [**ContextMap**](windowsribbon-element-contextmap.md) .

L’exemple suivant illustre le balisage de base pour l’élément [**ContextPopup**](windowsribbon-element-contextpopup.md) .


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a>Code

Pour appeler un menu contextuel, la méthode [**IUIContextualUI :: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) est appelée lorsque la fenêtre de niveau supérieur de l’application du ruban reçoit une \_ notification WM CONTEXTMENU.

Cet exemple montre comment gérer la notification WM \_ CONTEXTMENU dans la méthode WndProc () de l’application du ruban.


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



L’exemple suivant montre comment une application de ruban peut afficher la fenêtre contextuelle au niveau d’un emplacement spécifique à l’écran à l’aide de la méthode [**IUIContextualUI :: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) .

GetCurrentContext () a la valeur `cmdContextMap` définie dans l’exemple de balisage précédent.

g \_ pApplication est une référence à l’interface [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) .


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



La référence à [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) peut être libérée avant la fermeture de la fenêtre contextuelle du contexte, comme indiqué dans l’exemple précédent. Toutefois, la référence doit être libérée à un moment donné pour éviter les fuites de mémoire.

> [!Caution]  
> L' Mini-Toolbar a un effet de fondu prédéfini basé sur la proximité du pointeur de la souris. Pour cette raison, il est recommandé d’afficher le Mini-Toolbar aussi près que possible du pointeur de la souris. Dans le cas contraire, en raison des mécanismes d’affichage en conflit, le Mini-Toolbar peut ne pas s’afficher comme prévu.

 

## <a name="context-popup-properties"></a>Propriétés de la fenêtre contextuelle de contexte

Aucune clé de propriété n’est associée au contrôle contextuel contextuel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)
</dt> <dt>

[Exemple ContextPopup](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 