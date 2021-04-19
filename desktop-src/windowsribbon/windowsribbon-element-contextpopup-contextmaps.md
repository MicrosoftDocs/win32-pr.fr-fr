---
title: ContextPopup. ContextMaps, propriété
description: Représente un conteneur pour les éléments ContextMap.
ms.assetid: 06dfd4ba-a1d8-48bb-b185-d265e007a820
keywords:
- Ruban Windows de la propriété ContextPopup. ContextMaps
topic_type:
- apiref
api_name:
- ContextPopup.ContextMaps
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034381c4af840219ff1d6dd4d7a73aa34f528915
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517319"
---
# <a name="contextpopupcontextmaps-property"></a><span data-ttu-id="72ee6-104">ContextPopup. ContextMaps, propriété</span><span class="sxs-lookup"><span data-stu-id="72ee6-104">ContextPopup.ContextMaps property</span></span>

<span data-ttu-id="72ee6-105">Représente un conteneur pour les éléments [**ContextMap**](windowsribbon-element-contextmap.md) .</span><span class="sxs-lookup"><span data-stu-id="72ee6-105">Represents a container for [**ContextMap**](windowsribbon-element-contextmap.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="72ee6-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="72ee6-106">Usage</span></span>

``` syntax
<ContextPopup.ContextMaps>
  child elements
</ContextPopup.ContextMaps>
```

## <a name="attributes"></a><span data-ttu-id="72ee6-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="72ee6-107">Attributes</span></span>

<span data-ttu-id="72ee6-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="72ee6-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="72ee6-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="72ee6-109">Child elements</span></span>



| <span data-ttu-id="72ee6-110">Élément</span><span class="sxs-lookup"><span data-stu-id="72ee6-110">Element</span></span>                                                           | <span data-ttu-id="72ee6-111">Description</span><span class="sxs-lookup"><span data-stu-id="72ee6-111">Description</span></span>                                        |
|-------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="72ee6-112">**ContextMap**</span><span class="sxs-lookup"><span data-stu-id="72ee6-112">**ContextMap**</span></span>](windowsribbon-element-contextmap.md)<br/> | <span data-ttu-id="72ee6-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="72ee6-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="72ee6-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="72ee6-114">Parent elements</span></span>



| <span data-ttu-id="72ee6-115">Élément</span><span class="sxs-lookup"><span data-stu-id="72ee6-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="72ee6-116">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="72ee6-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="72ee6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="72ee6-117">Remarks</span></span>

<span data-ttu-id="72ee6-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="72ee6-118">Optional.</span></span>

<span data-ttu-id="72ee6-119">Peut se produire au plus une fois pour chaque [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="72ee6-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="examples"></a><span data-ttu-id="72ee6-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="72ee6-120">Examples</span></span>

<span data-ttu-id="72ee6-121">L’exemple suivant illustre le balisage de base pour une vue [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="72ee6-121">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="72ee6-122">Cette section de code illustre une déclaration de contrôle **ContextPopup. ContextMaps** .</span><span class="sxs-lookup"><span data-stu-id="72ee6-122">This section of code shows a **ContextPopup.ContextMaps** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="72ee6-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72ee6-123">Requirements</span></span>



| <span data-ttu-id="72ee6-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72ee6-124">Requirement</span></span> | <span data-ttu-id="72ee6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="72ee6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="72ee6-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72ee6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="72ee6-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72ee6-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="72ee6-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72ee6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="72ee6-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72ee6-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72ee6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72ee6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ee6-131">Contrôle Popup du contexte</span><span class="sxs-lookup"><span data-stu-id="72ee6-131">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





