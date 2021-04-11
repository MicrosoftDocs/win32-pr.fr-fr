---
title: Élément ContextPopup
description: Représente le contrôle contextuel de contexte dans la vue ContextPopup.
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- Ruban des fenêtres d’élément ContextPopup
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4feb7c4fbd2ca538fe4d0c2b2584163ee8c9fcea
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030282"
---
# <a name="contextpopup-element"></a><span data-ttu-id="286d0-104">Élément ContextPopup</span><span class="sxs-lookup"><span data-stu-id="286d0-104">ContextPopup element</span></span>

<span data-ttu-id="286d0-105">Représente le contrôle [contextuel de contexte](windowsribbon-controls-contextpopup.md) dans la vue ContextPopup.</span><span class="sxs-lookup"><span data-stu-id="286d0-105">Represents the [Context Popup](windowsribbon-controls-contextpopup.md) control in the ContextPopup View.</span></span>

## <a name="usage"></a><span data-ttu-id="286d0-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="286d0-106">Usage</span></span>

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a><span data-ttu-id="286d0-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="286d0-107">Attributes</span></span>

<span data-ttu-id="286d0-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="286d0-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="286d0-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="286d0-109">Child elements</span></span>



| <span data-ttu-id="286d0-110">Élément</span><span class="sxs-lookup"><span data-stu-id="286d0-110">Element</span></span>                                                                                         | <span data-ttu-id="286d0-111">Description</span><span class="sxs-lookup"><span data-stu-id="286d0-111">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="286d0-112">**ContextPopup.ContextMaps**</span><span class="sxs-lookup"><span data-stu-id="286d0-112">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | <span data-ttu-id="286d0-113">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="286d0-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="286d0-114">**ContextPopup.ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="286d0-114">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> | <span data-ttu-id="286d0-115">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="286d0-115">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="286d0-116">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="286d0-116">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | <span data-ttu-id="286d0-117">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="286d0-117">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="286d0-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="286d0-118">Parent elements</span></span>



| <span data-ttu-id="286d0-119">Élément</span><span class="sxs-lookup"><span data-stu-id="286d0-119">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="286d0-120">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="286d0-120">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="286d0-121">Notes</span><span class="sxs-lookup"><span data-stu-id="286d0-121">Remarks</span></span>

<span data-ttu-id="286d0-122">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="286d0-122">Optional.</span></span>

<span data-ttu-id="286d0-123">Peut se produire au plus une fois pour chaque [**application. views**](windowsribbon-element-application-views.md).</span><span class="sxs-lookup"><span data-stu-id="286d0-123">May occur at most once for each [**Application.Views**](windowsribbon-element-application-views.md).</span></span>

## <a name="examples"></a><span data-ttu-id="286d0-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="286d0-124">Examples</span></span>

<span data-ttu-id="286d0-125">L’exemple suivant illustre le balisage de base pour une vue **ContextPopup** .</span><span class="sxs-lookup"><span data-stu-id="286d0-125">The following example demonstrates the basic markup for a **ContextPopup** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="286d0-126">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="286d0-126">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="286d0-127">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="286d0-127">Minimum supported system</span></span><br/> | <span data-ttu-id="286d0-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="286d0-128">Windows 7</span></span> |
| <span data-ttu-id="286d0-129">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="286d0-129">Can be empty</span></span>                        | <span data-ttu-id="286d0-130">Non</span><span class="sxs-lookup"><span data-stu-id="286d0-130">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="286d0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="286d0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="286d0-132">Contrôle Popup du contexte</span><span class="sxs-lookup"><span data-stu-id="286d0-132">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





