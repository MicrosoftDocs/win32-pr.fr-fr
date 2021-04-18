---
title: ContextPopup. ContextMenus, propriété
description: Représente un conteneur pour les éléments ContextMenu.
ms.assetid: 92633689-a892-421e-a5fb-e494f4cd1ea8
keywords:
- Ruban Windows de la propriété ContextPopup. ContextMenus
topic_type:
- apiref
api_name:
- ContextPopup.ContextMenus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ef8ab053b9912f545c2aad931eb8ad9583ff62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509347"
---
# <a name="contextpopupcontextmenus-property"></a><span data-ttu-id="2cf66-104">ContextPopup. ContextMenus, propriété</span><span class="sxs-lookup"><span data-stu-id="2cf66-104">ContextPopup.ContextMenus property</span></span>

<span data-ttu-id="2cf66-105">Représente un conteneur pour les éléments [**ContextMenu**](windowsribbon-element-contextmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="2cf66-105">Represents a container for [**ContextMenu**](windowsribbon-element-contextmenu.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="2cf66-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="2cf66-106">Usage</span></span>

``` syntax
<ContextPopup.ContextMenus>
  child elements
</ContextPopup.ContextMenus>
```

## <a name="attributes"></a><span data-ttu-id="2cf66-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="2cf66-107">Attributes</span></span>

<span data-ttu-id="2cf66-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="2cf66-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2cf66-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2cf66-109">Child elements</span></span>



| <span data-ttu-id="2cf66-110">Élément</span><span class="sxs-lookup"><span data-stu-id="2cf66-110">Element</span></span>                                                             | <span data-ttu-id="2cf66-111">Description</span><span class="sxs-lookup"><span data-stu-id="2cf66-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="2cf66-112">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="2cf66-112">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/> | <span data-ttu-id="2cf66-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="2cf66-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2cf66-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2cf66-114">Parent elements</span></span>



| <span data-ttu-id="2cf66-115">Élément</span><span class="sxs-lookup"><span data-stu-id="2cf66-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="2cf66-116">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="2cf66-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2cf66-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2cf66-117">Remarks</span></span>

<span data-ttu-id="2cf66-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="2cf66-118">Optional.</span></span>

<span data-ttu-id="2cf66-119">Peut se produire au plus une fois pour chaque [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="2cf66-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2cf66-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="2cf66-120">Examples</span></span>

<span data-ttu-id="2cf66-121">L’exemple suivant illustre le balisage de base pour une vue [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="2cf66-121">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="2cf66-122">Cette section de code illustre une déclaration de contrôle **ContextPopup. ContextMenus** .</span><span class="sxs-lookup"><span data-stu-id="2cf66-122">This section of code shows a **ContextPopup.ContextMenus** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2cf66-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cf66-123">Requirements</span></span>



| <span data-ttu-id="2cf66-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cf66-124">Requirement</span></span> | <span data-ttu-id="2cf66-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cf66-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2cf66-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cf66-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf66-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cf66-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="2cf66-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cf66-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf66-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cf66-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2cf66-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cf66-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf66-131">Contrôle Popup du contexte</span><span class="sxs-lookup"><span data-stu-id="2cf66-131">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





