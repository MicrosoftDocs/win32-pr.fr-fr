---
title: ContextMenu, élément
description: Représente un contrôle de menu contextuel.
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- Ruban des fenêtres d’éléments ContextMenu
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c824e87c063fb863e79f10cb9755b74df36023f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678453"
---
# <a name="contextmenu-element"></a><span data-ttu-id="4432c-104">ContextMenu, élément</span><span class="sxs-lookup"><span data-stu-id="4432c-104">ContextMenu element</span></span>

<span data-ttu-id="4432c-105">Représente un contrôle de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="4432c-105">Represents a context menu control.</span></span>

## <a name="usage"></a><span data-ttu-id="4432c-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="4432c-106">Usage</span></span>

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a><span data-ttu-id="4432c-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="4432c-107">Attributes</span></span>



| <span data-ttu-id="4432c-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="4432c-108">Attribute</span></span>           | <span data-ttu-id="4432c-109">Type</span><span class="sxs-lookup"><span data-stu-id="4432c-109">Type</span></span>                 | <span data-ttu-id="4432c-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4432c-110">Required</span></span>       | <span data-ttu-id="4432c-111">Description</span><span class="sxs-lookup"><span data-stu-id="4432c-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4432c-112">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4432c-112">**Name**</span></span><br/> | <span data-ttu-id="4432c-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="4432c-113">xs:string</span></span><br/> | <span data-ttu-id="4432c-114">Oui</span><span class="sxs-lookup"><span data-stu-id="4432c-114">Yes</span></span><br/> | <span data-ttu-id="4432c-115"><dt> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="4432c-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="4432c-116">Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="4432c-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="4432c-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4432c-117">Child elements</span></span>



| <span data-ttu-id="4432c-118">Élément</span><span class="sxs-lookup"><span data-stu-id="4432c-118">Element</span></span>                                                         | <span data-ttu-id="4432c-119">Description</span><span class="sxs-lookup"><span data-stu-id="4432c-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="4432c-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="4432c-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="4432c-121">Doit se produire au moins une fois</span><span class="sxs-lookup"><span data-stu-id="4432c-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="4432c-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4432c-122">Parent elements</span></span>



| <span data-ttu-id="4432c-123">Élément</span><span class="sxs-lookup"><span data-stu-id="4432c-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4432c-124">**ContextPopup.ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="4432c-124">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4432c-125">Notes</span><span class="sxs-lookup"><span data-stu-id="4432c-125">Remarks</span></span>

<span data-ttu-id="4432c-126">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4432c-126">Optional.</span></span>

<span data-ttu-id="4432c-127">Peut se produire une ou plusieurs fois pour chaque [**ContextPopup. ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span><span class="sxs-lookup"><span data-stu-id="4432c-127">May occur one or more times for each [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4432c-128">Un **ContextMenu** ne peut pas héberger des contrôles de [zone de liste déroulante](windowsribbon-controls-combobox.md) ou d' [Spinner](windowsribbon-controls-spinner.md) .</span><span class="sxs-lookup"><span data-stu-id="4432c-128">A **ContextMenu** cannot host [Combo Box](windowsribbon-controls-combobox.md) or [Spinner](windowsribbon-controls-spinner.md) controls.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4432c-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="4432c-129">Examples</span></span>

<span data-ttu-id="4432c-130">L’exemple suivant illustre le balisage de base pour une vue [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="4432c-130">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="4432c-131">Cette section de code illustre un ensemble de déclarations de contrôle **ContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="4432c-131">This section of code shows a set of **ContextMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="4432c-132">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4432c-132">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="4432c-133">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4432c-133">Minimum supported system</span></span><br/> | <span data-ttu-id="4432c-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4432c-134">Windows 7</span></span> |
| <span data-ttu-id="4432c-135">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="4432c-135">Can be empty</span></span>                        | <span data-ttu-id="4432c-136">Non</span><span class="sxs-lookup"><span data-stu-id="4432c-136">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="4432c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4432c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4432c-138">Contrôle Popup du contexte</span><span class="sxs-lookup"><span data-stu-id="4432c-138">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





