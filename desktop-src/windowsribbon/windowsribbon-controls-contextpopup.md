---
title: Menu contextuel contexte
description: Une fenêtre contextuelle contextuelle est le contrôle principal dans la vue ContextPopup de l’infrastructure de ruban Windows.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77441cc3cdcc9212d27d2230d76d2618f1831ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512741"
---
# <a name="context-popup"></a><span data-ttu-id="419b6-103">Menu contextuel contexte</span><span class="sxs-lookup"><span data-stu-id="419b6-103">Context Popup</span></span>

<span data-ttu-id="419b6-104">Une fenêtre contextuelle contextuelle est le contrôle principal dans la [**vue ContextPopup**](windowsribbon-element-contextpopup.md) de l’infrastructure de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="419b6-104">A Context Popup is the principal control in the [**ContextPopup View**](windowsribbon-element-contextpopup.md) of the Windows Ribbon framework.</span></span> <span data-ttu-id="419b6-105">Il s’agit d’un système de menu contextuel riche qui est exposé uniquement par l’infrastructure en tant qu’extension d’une implémentation de ruban ; l’infrastructure n’expose pas la fenêtre contextuelle de contexte en tant que contrôle indépendant.</span><span class="sxs-lookup"><span data-stu-id="419b6-105">It is a rich context menu system that is only exposed by the framework as an extension to a Ribbon implementation—the framework does not expose the Context Popup as an independent control.</span></span>

-   [<span data-ttu-id="419b6-106">Composants de la fenêtre contextuelle contextuelle</span><span class="sxs-lookup"><span data-stu-id="419b6-106">Components of the Context Popup</span></span>](#context-popup)
-   [<span data-ttu-id="419b6-107">Implémenter la fenêtre contextuelle de contexte</span><span class="sxs-lookup"><span data-stu-id="419b6-107">Implement the Context Popup</span></span>](#implement-the-context-popup)
    -   [<span data-ttu-id="419b6-108">balisage</span><span class="sxs-lookup"><span data-stu-id="419b6-108">Markup</span></span>](#markup)
    -   [<span data-ttu-id="419b6-109">Code</span><span class="sxs-lookup"><span data-stu-id="419b6-109">Code</span></span>](#code)
-   [<span data-ttu-id="419b6-110">Propriétés de la fenêtre contextuelle de contexte</span><span class="sxs-lookup"><span data-stu-id="419b6-110">Context Popup Properties</span></span>](#context-popup-properties)
-   [<span data-ttu-id="419b6-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="419b6-111">Related topics</span></span>](#related-topics)

## <a name="components-of-the-context-popup"></a><span data-ttu-id="419b6-112">Composants de la fenêtre contextuelle contextuelle</span><span class="sxs-lookup"><span data-stu-id="419b6-112">Components of the Context Popup</span></span>

<span data-ttu-id="419b6-113">La fenêtre contextuelle de contexte est un conteneur logique pour le menu contextuel et Mini-Toolbar sous-contrôles qui sont exposés via les éléments de balisage [**ContextMenu**](windowsribbon-element-contextmenu.md) et [**MiniToolbar**](windowsribbon-element-minitoolbar.md) , respectivement :</span><span class="sxs-lookup"><span data-stu-id="419b6-113">The Context Popup is a logical container for the Context Menu and Mini-Toolbar sub-controls that are exposed through the [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) markup elements, respectively:</span></span>

-   <span data-ttu-id="419b6-114">Le [**ContextMenu**](windowsribbon-element-contextmenu.md) expose un menu de commandes et de galeries.</span><span class="sxs-lookup"><span data-stu-id="419b6-114">The [**ContextMenu**](windowsribbon-element-contextmenu.md) exposes a menu of Commands and galleries.</span></span>
-   <span data-ttu-id="419b6-115">Le [**MiniToolbar**](windowsribbon-element-minitoolbar.md) expose une barre d’outils flottante de diverses commandes, galeries et contrôles complexes tels que le [contrôle de police](windowsribbon-controls-fontcontrol.md) et la [zone de liste déroulante](windowsribbon-controls-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="419b6-115">The [**MiniToolbar**](windowsribbon-element-minitoolbar.md) exposes a floating toolbar of various Commands, galleries, and complex controls such as the [Font Control](windowsribbon-controls-fontcontrol.md) and the [Combo Box](windowsribbon-controls-combobox.md).</span></span>

<span data-ttu-id="419b6-116">Chaque sous-contrôle peut apparaître au plus une fois dans un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="419b6-116">Each sub-control can appear at most once in a Context Popup.</span></span>

<span data-ttu-id="419b6-117">La capture d’écran suivante illustre la fenêtre contextuelle de contexte et ses sous-contrôles constitutifs.</span><span class="sxs-lookup"><span data-stu-id="419b6-117">The following screen shot illustrates the Context Popup and its constituent sub-controls.</span></span>

![capture d’écran avec légendes montrant les composants d’interface utilisateur contextuels du ruban.](images/controls/contextpopup.png)

<span data-ttu-id="419b6-119">La fenêtre contextuelle contextuelle est purement conceptuelle et n’expose pas les fonctionnalités d’interface utilisateur lui-même, telles que le positionnement ou le dimensionnement.</span><span class="sxs-lookup"><span data-stu-id="419b6-119">The Context Popup is purely conceptual and does not expose any UI functionality itself, such as positioning or sizing.</span></span>

> [!Note]  
> <span data-ttu-id="419b6-120">La fenêtre contextuelle s’affiche généralement en cliquant avec le bouton droit de la souris (ou en utilisant le raccourci clavier MAJ + F10) sur un objet qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="419b6-120">The Context Popup is typically displayed by right-clicking the mouse (or through the keyboard shortcut SHIFT+F10) on an object of interest.</span></span> <span data-ttu-id="419b6-121">Toutefois, les étapes nécessaires à l’affichage de la fenêtre contextuelle sont définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="419b6-121">However, the steps required to display the Context Popup are defined by the application.</span></span>

 

## <a name="implement-the-context-popup"></a><span data-ttu-id="419b6-122">Implémenter la fenêtre contextuelle de contexte</span><span class="sxs-lookup"><span data-stu-id="419b6-122">Implement the Context Popup</span></span>

<span data-ttu-id="419b6-123">De la même façon que les autres contrôles de l’infrastructure de ruban Windows, la fenêtre contextuelle est implémentée via un composant de balisage qui spécifie ses détails de présentation et un composant de code qui régit ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="419b6-123">In similar fashion to other Windows Ribbon framework controls, the Context Popup is implemented through a markup component that specifies its presentation details and a code component that governs its functionality.</span></span>

<span data-ttu-id="419b6-124">Le tableau suivant répertorie les contrôles qui sont pris en charge par chaque sous-contrôle contextuel de contexte.</span><span class="sxs-lookup"><span data-stu-id="419b6-124">The following table lists the controls that are supported by each Context Popup sub-control.</span></span>



| <span data-ttu-id="419b6-125">Contrôler</span><span class="sxs-lookup"><span data-stu-id="419b6-125">Control</span></span>                                                                  | <span data-ttu-id="419b6-126">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="419b6-126">Mini-Toolbar</span></span> | <span data-ttu-id="419b6-127">Menu contextuel</span><span class="sxs-lookup"><span data-stu-id="419b6-127">Context Menu</span></span> |
|--------------------------------------------------------------------------|--------------|--------------|
| [<span data-ttu-id="419b6-128">Button</span><span class="sxs-lookup"><span data-stu-id="419b6-128">Button</span></span>](windowsribbon-controls-button.md)                              | <span data-ttu-id="419b6-129">x</span><span class="sxs-lookup"><span data-stu-id="419b6-129">x</span></span>            | <span data-ttu-id="419b6-130">x</span><span class="sxs-lookup"><span data-stu-id="419b6-130">x</span></span>            |
| [<span data-ttu-id="419b6-131">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="419b6-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)                         | <span data-ttu-id="419b6-132">x</span><span class="sxs-lookup"><span data-stu-id="419b6-132">x</span></span>            | <span data-ttu-id="419b6-133">x</span><span class="sxs-lookup"><span data-stu-id="419b6-133">x</span></span>            |
| [<span data-ttu-id="419b6-134">Zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="419b6-134">Combo Box</span></span>](windowsribbon-controls-combobox.md)                         | <span data-ttu-id="419b6-135">x</span><span class="sxs-lookup"><span data-stu-id="419b6-135">x</span></span>            |              |
| [<span data-ttu-id="419b6-136">Bouton déroulant</span><span class="sxs-lookup"><span data-stu-id="419b6-136">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)            | <span data-ttu-id="419b6-137">x</span><span class="sxs-lookup"><span data-stu-id="419b6-137">x</span></span>            | <span data-ttu-id="419b6-138">x</span><span class="sxs-lookup"><span data-stu-id="419b6-138">x</span></span>            |
| [<span data-ttu-id="419b6-139">Sélecteur de couleurs déroulantes</span><span class="sxs-lookup"><span data-stu-id="419b6-139">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | <span data-ttu-id="419b6-140">x</span><span class="sxs-lookup"><span data-stu-id="419b6-140">x</span></span>            | <span data-ttu-id="419b6-141">x</span><span class="sxs-lookup"><span data-stu-id="419b6-141">x</span></span>            |
| [<span data-ttu-id="419b6-142">Galerie déroulante</span><span class="sxs-lookup"><span data-stu-id="419b6-142">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)          | <span data-ttu-id="419b6-143">x</span><span class="sxs-lookup"><span data-stu-id="419b6-143">x</span></span>            | <span data-ttu-id="419b6-144">x</span><span class="sxs-lookup"><span data-stu-id="419b6-144">x</span></span>            |
| [<span data-ttu-id="419b6-145">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="419b6-145">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | <span data-ttu-id="419b6-146">x</span><span class="sxs-lookup"><span data-stu-id="419b6-146">x</span></span>            |              |
| [<span data-ttu-id="419b6-147">Bouton aide</span><span class="sxs-lookup"><span data-stu-id="419b6-147">Help Button</span></span>](windowsribbon-controls-helpbutton.md)                     |              |              |
| [<span data-ttu-id="419b6-148">Galerie dans le ruban</span><span class="sxs-lookup"><span data-stu-id="419b6-148">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)          |              |              |
| [<span data-ttu-id="419b6-149">Spinner</span><span class="sxs-lookup"><span data-stu-id="419b6-149">Spinner</span></span>](windowsribbon-controls-spinner.md)                            |              |              |
| [<span data-ttu-id="419b6-150">Bouton partagé</span><span class="sxs-lookup"><span data-stu-id="419b6-150">Split Button</span></span>](windowsribbon-controls-splitbutton.md)                   | <span data-ttu-id="419b6-151">x</span><span class="sxs-lookup"><span data-stu-id="419b6-151">x</span></span>            | <span data-ttu-id="419b6-152">x</span><span class="sxs-lookup"><span data-stu-id="419b6-152">x</span></span>            |
| [<span data-ttu-id="419b6-153">Galerie de boutons partagés</span><span class="sxs-lookup"><span data-stu-id="419b6-153">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)    | <span data-ttu-id="419b6-154">x</span><span class="sxs-lookup"><span data-stu-id="419b6-154">x</span></span>            | <span data-ttu-id="419b6-155">x</span><span class="sxs-lookup"><span data-stu-id="419b6-155">x</span></span>            |
| [<span data-ttu-id="419b6-156">Bouton bascule</span><span class="sxs-lookup"><span data-stu-id="419b6-156">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)                 | <span data-ttu-id="419b6-157">x</span><span class="sxs-lookup"><span data-stu-id="419b6-157">x</span></span>            | <span data-ttu-id="419b6-158">x</span><span class="sxs-lookup"><span data-stu-id="419b6-158">x</span></span>            |



 

### <a name="markup"></a><span data-ttu-id="419b6-159">balisage</span><span class="sxs-lookup"><span data-stu-id="419b6-159">Markup</span></span>

<span data-ttu-id="419b6-160">Chaque sous-contrôle contextuel de contexte doit être déclaré individuellement dans le balisage.</span><span class="sxs-lookup"><span data-stu-id="419b6-160">Each Context Popup sub-control must be declared individually in markup.</span></span>

### <a name="mini-toolbar"></a><span data-ttu-id="419b6-161">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="419b6-161">Mini-Toolbar</span></span>

<span data-ttu-id="419b6-162">Lorsque vous ajoutez des contrôles à une mini-barre d’outils contextuelle contextuelle, les deux recommandations suivantes doivent être prises en compte :</span><span class="sxs-lookup"><span data-stu-id="419b6-162">When adding controls to a Context Popup Mini-Toolbar, the following two recommendations should be considered:</span></span>

-   <span data-ttu-id="419b6-163">Les contrôles doivent être hautement reconnaissables et fournir des fonctionnalités évidentes.</span><span class="sxs-lookup"><span data-stu-id="419b6-163">Controls should be highly recognizable and provide obvious functionality.</span></span> <span data-ttu-id="419b6-164">La familiarité est essentielle, car les étiquettes et les info-bulles ne sont pas exposées pour les contrôles de Mini-Toolbar.</span><span class="sxs-lookup"><span data-stu-id="419b6-164">Familiarity is key, as labels and tooltips are not exposed for Mini-Toolbar controls.</span></span>
-   <span data-ttu-id="419b6-165">Chaque commande exposée par un contrôle doit être présentée ailleurs dans l’interface ruban.</span><span class="sxs-lookup"><span data-stu-id="419b6-165">Each Command exposed by a control should be presented elsewhere in the ribbon UI.</span></span> <span data-ttu-id="419b6-166">Le Mini-Toolbar ne prend pas en charge la navigation au clavier.</span><span class="sxs-lookup"><span data-stu-id="419b6-166">The Mini-Toolbar does not support keyboard navigation.</span></span>

<span data-ttu-id="419b6-167">L’exemple suivant illustre le balisage de base pour un élément [**MiniToolbar**](windowsribbon-element-minitoolbar.md) qui contient trois contrôles [bouton](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="419b6-167">The following example demonstrates the basic markup for a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="419b6-168">Un élément [**MenuGroup**](windowsribbon-element-menugroup.md) est spécifié pour chaque ligne de contrôles dans la mini-barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="419b6-168">One [**MenuGroup**](windowsribbon-element-menugroup.md) element is specified for each row of controls in the Mini-Toolbar.</span></span>

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a><span data-ttu-id="419b6-169">Menu contextuel</span><span class="sxs-lookup"><span data-stu-id="419b6-169">Context Menu</span></span>

<span data-ttu-id="419b6-170">L’exemple suivant illustre le balisage de base pour un élément [**ContextMenu**](windowsribbon-element-contextmenu.md) qui contient trois contrôles [Button](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="419b6-170">The following example demonstrates the basic markup for a [**ContextMenu**](windowsribbon-element-contextmenu.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="419b6-171">Chaque ensemble de contrôles de l’élément [**MenuGroup**](windowsribbon-element-menugroup.md) est séparé par une barre horizontale dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="419b6-171">Each set of controls in the [**MenuGroup**](windowsribbon-element-menugroup.md) element is separated by a horizontal bar in the Context Menu.</span></span>

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



<span data-ttu-id="419b6-172">Bien qu’une fenêtre contextuelle de contexte puisse contenir au plus l’un de chaque sous-contrôle, plusieurs déclarations d’élément [**ContextMenu**](windowsribbon-element-contextmenu.md) et [**MiniToolbar**](windowsribbon-element-minitoolbar.md) dans le balisage du ruban sont valides.</span><span class="sxs-lookup"><span data-stu-id="419b6-172">Although a Context Popup can contain at most one of each sub-control, multiple [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element declarations in the Ribbon markup are valid.</span></span> <span data-ttu-id="419b6-173">Cela permet à une application de prendre en charge diverses combinaisons de menus contextuels et de contrôles de Mini-Toolbar, en fonction de critères définis par l’application, tels que le contexte de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="419b6-173">This allows an application to support various combinations of Context Menu and Mini-Toolbar controls, based on criteria defined by the application, such as workspace context.</span></span>

<span data-ttu-id="419b6-174">Pour plus d’informations, consultez l’élément [**ContextMap**](windowsribbon-element-contextmap.md) .</span><span class="sxs-lookup"><span data-stu-id="419b6-174">For more information, see the [**ContextMap**](windowsribbon-element-contextmap.md) element.</span></span>

<span data-ttu-id="419b6-175">L’exemple suivant illustre le balisage de base pour l’élément [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="419b6-175">The following example demonstrates the basic markup for the [**ContextPopup**](windowsribbon-element-contextpopup.md) element.</span></span>


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



### <a name="code"></a><span data-ttu-id="419b6-176">Code</span><span class="sxs-lookup"><span data-stu-id="419b6-176">Code</span></span>

<span data-ttu-id="419b6-177">Pour appeler un menu contextuel, la méthode [**IUIContextualUI :: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) est appelée lorsque la fenêtre de niveau supérieur de l’application du ruban reçoit une \_ notification WM CONTEXTMENU.</span><span class="sxs-lookup"><span data-stu-id="419b6-177">To invoke a Context Popup, the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method is called when the top-level window of the Ribbon application receives a WM\_CONTEXTMENU notification.</span></span>

<span data-ttu-id="419b6-178">Cet exemple montre comment gérer la notification WM \_ CONTEXTMENU dans la méthode WndProc () de l’application du ruban.</span><span class="sxs-lookup"><span data-stu-id="419b6-178">This example demonstrates how to handle the WM\_CONTEXTMENU notification in the WndProc() method of the Ribbon application.</span></span>


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



<span data-ttu-id="419b6-179">L’exemple suivant montre comment une application de ruban peut afficher la fenêtre contextuelle au niveau d’un emplacement spécifique à l’écran à l’aide de la méthode [**IUIContextualUI :: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) .</span><span class="sxs-lookup"><span data-stu-id="419b6-179">The following example demonstrates how a Ribbon application can show the Context Popup at a specific screen location using the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method.</span></span>

<span data-ttu-id="419b6-180">GetCurrentContext () a la valeur `cmdContextMap` définie dans l’exemple de balisage précédent.</span><span class="sxs-lookup"><span data-stu-id="419b6-180">GetCurrentContext() has a value of `cmdContextMap` as defined in the preceding markup example.</span></span>

<span data-ttu-id="419b6-181">g \_ pApplication est une référence à l’interface [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) .</span><span class="sxs-lookup"><span data-stu-id="419b6-181">g\_pApplication is a reference to the [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) interface.</span></span>


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



<span data-ttu-id="419b6-182">La référence à [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) peut être libérée avant la fermeture de la fenêtre contextuelle du contexte, comme indiqué dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="419b6-182">The reference to [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) can be released before the Context Popup is dismissed, as shown in the preceding example.</span></span> <span data-ttu-id="419b6-183">Toutefois, la référence doit être libérée à un moment donné pour éviter les fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="419b6-183">However, the reference must be released at some point to avoid memory leaks.</span></span>

> [!Caution]  
> <span data-ttu-id="419b6-184">L' Mini-Toolbar a un effet de fondu prédéfini basé sur la proximité du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="419b6-184">The Mini-Toolbar has a built-in fade effect that is based on the proximity of the mouse pointer.</span></span> <span data-ttu-id="419b6-185">Pour cette raison, il est recommandé d’afficher le Mini-Toolbar aussi près que possible du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="419b6-185">For this reason, it is recommended that the Mini-Toolbar be displayed as close to the mouse pointer as possible.</span></span> <span data-ttu-id="419b6-186">Dans le cas contraire, en raison des mécanismes d’affichage en conflit, le Mini-Toolbar peut ne pas s’afficher comme prévu.</span><span class="sxs-lookup"><span data-stu-id="419b6-186">Otherwise, due to the conflicting display mechanisms, the Mini-Toolbar may not render as expected.</span></span>

 

## <a name="context-popup-properties"></a><span data-ttu-id="419b6-187">Propriétés de la fenêtre contextuelle de contexte</span><span class="sxs-lookup"><span data-stu-id="419b6-187">Context Popup Properties</span></span>

<span data-ttu-id="419b6-188">Aucune clé de propriété n’est associée au contrôle contextuel contextuel.</span><span class="sxs-lookup"><span data-stu-id="419b6-188">There are no property keys associated with the Context Popup control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="419b6-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="419b6-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="419b6-190">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="419b6-190">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="419b6-191">Exemple ContextPopup</span><span class="sxs-lookup"><span data-stu-id="419b6-191">ContextPopup Sample</span></span>](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 