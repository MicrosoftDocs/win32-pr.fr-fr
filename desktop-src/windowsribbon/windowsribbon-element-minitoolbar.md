---
title: Élément MiniToolbar
description: Représente une barre d’outils contextuelle.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- Ruban des fenêtres d’élément MiniToolbar
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb5e4a27d10fe5233f8e7059bc9da8ecfd2fa383
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100841"
---
# <a name="minitoolbar-element"></a><span data-ttu-id="c4dfc-104">Élément MiniToolbar</span><span class="sxs-lookup"><span data-stu-id="c4dfc-104">MiniToolbar element</span></span>

<span data-ttu-id="c4dfc-105">Représente une barre d’outils contextuelle.</span><span class="sxs-lookup"><span data-stu-id="c4dfc-105">Represents a contextual toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="c4dfc-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="c4dfc-106">Usage</span></span>

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a><span data-ttu-id="c4dfc-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="c4dfc-107">Attributes</span></span>



| <span data-ttu-id="c4dfc-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="c4dfc-108">Attribute</span></span>           | <span data-ttu-id="c4dfc-109">Type</span><span class="sxs-lookup"><span data-stu-id="c4dfc-109">Type</span></span>                 | <span data-ttu-id="c4dfc-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4dfc-110">Required</span></span>       | <span data-ttu-id="c4dfc-111">Description</span><span class="sxs-lookup"><span data-stu-id="c4dfc-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4dfc-112">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c4dfc-112">**Name**</span></span><br/> | <span data-ttu-id="c4dfc-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="c4dfc-113">xs:string</span></span><br/> | <span data-ttu-id="c4dfc-114">Oui</span><span class="sxs-lookup"><span data-stu-id="c4dfc-114">Yes</span></span><br/> | <span data-ttu-id="c4dfc-115"><dt> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="c4dfc-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="c4dfc-116">Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="c4dfc-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="c4dfc-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c4dfc-117">Child elements</span></span>



| <span data-ttu-id="c4dfc-118">Élément</span><span class="sxs-lookup"><span data-stu-id="c4dfc-118">Element</span></span>                                                         | <span data-ttu-id="c4dfc-119">Description</span><span class="sxs-lookup"><span data-stu-id="c4dfc-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="c4dfc-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="c4dfc-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="c4dfc-121">Doit se produire au moins une fois</span><span class="sxs-lookup"><span data-stu-id="c4dfc-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c4dfc-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c4dfc-122">Parent elements</span></span>



| <span data-ttu-id="c4dfc-123">Élément</span><span class="sxs-lookup"><span data-stu-id="c4dfc-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4dfc-124">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="c4dfc-124">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c4dfc-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c4dfc-125">Remarks</span></span>

<span data-ttu-id="c4dfc-126">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="c4dfc-126">Optional.</span></span>

<span data-ttu-id="c4dfc-127">Peut se produire une ou plusieurs fois pour chaque [**ContextPopup. MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span><span class="sxs-lookup"><span data-stu-id="c4dfc-127">May occur one or more times for each [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span></span>

<span data-ttu-id="c4dfc-128">Contrairement à l’élément [**ContextMenu**](windowsribbon-element-contextmenu.md) , le **MiniToolbar** reste visible lorsqu’un utilisateur clique sur un élément dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="c4dfc-128">Unlike the [**ContextMenu**](windowsribbon-element-contextmenu.md) element, the **MiniToolbar** remains visible when an item on the toolbar is clicked.</span></span>

<span data-ttu-id="c4dfc-129">S’il est affiché sans [**ContextMenu**](windowsribbon-element-contextmenu.md), le **MiniToolbar** disparaît lorsque le pointeur de la souris est déplacé.</span><span class="sxs-lookup"><span data-stu-id="c4dfc-129">If displayed without a [**ContextMenu**](windowsribbon-element-contextmenu.md), the **MiniToolbar** fades as the mouse pointer is moved away.</span></span>

> [!Note]  
> <span data-ttu-id="c4dfc-130">En raison de ce comportement de fondu, un [**ContextMenu**](windowsribbon-element-contextmenu.md) doit s’afficher à proximité du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="c4dfc-130">Due to this fading behavior, a [**ContextMenu**](windowsribbon-element-contextmenu.md) should be displayed in close proximity to the mouse pointer.</span></span>

 

<span data-ttu-id="c4dfc-131">Étant donné que les contrôles dans le **MiniToolbar** ne sont pas accessibles par le clavier, les commandes qu’ils exposent doivent être disponibles ailleurs dans l’interface ruban.</span><span class="sxs-lookup"><span data-stu-id="c4dfc-131">Because controls in the **MiniToolbar** are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="c4dfc-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="c4dfc-132">Examples</span></span>

<span data-ttu-id="c4dfc-133">L’exemple suivant illustre le balisage de base pour une vue [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="c4dfc-133">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="c4dfc-134">Cette section de code illustre un ensemble de déclarations de contrôle **MiniToolbar** .</span><span class="sxs-lookup"><span data-stu-id="c4dfc-134">This section of code shows a set of **MiniToolbar** control declarations.</span></span>


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="element-information"></a><span data-ttu-id="c4dfc-135">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c4dfc-135">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="c4dfc-136">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4dfc-136">Minimum supported system</span></span><br/> | <span data-ttu-id="c4dfc-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c4dfc-137">Windows 7</span></span> |
| <span data-ttu-id="c4dfc-138">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="c4dfc-138">Can be empty</span></span>                        | <span data-ttu-id="c4dfc-139">Non</span><span class="sxs-lookup"><span data-stu-id="c4dfc-139">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="c4dfc-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4dfc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4dfc-141">Contrôle Popup du contexte</span><span class="sxs-lookup"><span data-stu-id="c4dfc-141">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





