---
title: ContextPopup. MiniToolbars, propriété
description: Représente un conteneur pour les éléments MiniToolbar.
ms.assetid: 5c17e070-0520-44e6-a066-476107691205
keywords:
- Ruban Windows de la propriété ContextPopup. MiniToolbars
topic_type:
- apiref
api_name:
- ContextPopup.MiniToolbars
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e85e6b170b4b7408a17687bd26725e9183161
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466570"
---
# <a name="contextpopupminitoolbars-property"></a><span data-ttu-id="bbf14-104">ContextPopup. MiniToolbars, propriété</span><span class="sxs-lookup"><span data-stu-id="bbf14-104">ContextPopup.MiniToolbars property</span></span>

<span data-ttu-id="bbf14-105">Représente un conteneur pour les éléments [**MiniToolbar**](windowsribbon-element-minitoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf14-105">Represents a container for [**MiniToolbar**](windowsribbon-element-minitoolbar.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="bbf14-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="bbf14-106">Usage</span></span>

``` syntax
<ContextPopup.MiniToolbars>
  child elements
</ContextPopup.MiniToolbars>
```

## <a name="attributes"></a><span data-ttu-id="bbf14-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="bbf14-107">Attributes</span></span>

<span data-ttu-id="bbf14-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="bbf14-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bbf14-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bbf14-109">Child elements</span></span>



| <span data-ttu-id="bbf14-110">Élément</span><span class="sxs-lookup"><span data-stu-id="bbf14-110">Element</span></span>                                                             | <span data-ttu-id="bbf14-111">Description</span><span class="sxs-lookup"><span data-stu-id="bbf14-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="bbf14-112">**MiniToolbar**</span><span class="sxs-lookup"><span data-stu-id="bbf14-112">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/> | <span data-ttu-id="bbf14-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="bbf14-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="bbf14-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bbf14-114">Parent elements</span></span>



| <span data-ttu-id="bbf14-115">Élément</span><span class="sxs-lookup"><span data-stu-id="bbf14-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="bbf14-116">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="bbf14-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bbf14-117">Notes</span><span class="sxs-lookup"><span data-stu-id="bbf14-117">Remarks</span></span>

<span data-ttu-id="bbf14-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="bbf14-118">Optional.</span></span>

<span data-ttu-id="bbf14-119">Peut se produire au plus une fois pour chaque [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="bbf14-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="bbf14-120">Étant donné que les contrôles dans le [**MiniToolbar**](windowsribbon-element-minitoolbar.md) ne sont pas accessibles par le clavier, les commandes qu’ils exposent doivent être disponibles ailleurs dans l’interface ruban.</span><span class="sxs-lookup"><span data-stu-id="bbf14-120">Because controls in the [**MiniToolbar**](windowsribbon-element-minitoolbar.md) are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="bbf14-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="bbf14-121">Examples</span></span>

<span data-ttu-id="bbf14-122">L’exemple suivant illustre le balisage de base pour une vue [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf14-122">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="bbf14-123">Cette section de code illustre la déclaration de contrôle **ContextPopup. MiniToolbars** .</span><span class="sxs-lookup"><span data-stu-id="bbf14-123">This section of code shows the **ContextPopup.MiniToolbars** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="bbf14-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbf14-124">Requirements</span></span>



| <span data-ttu-id="bbf14-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbf14-125">Requirement</span></span> | <span data-ttu-id="bbf14-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbf14-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bbf14-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbf14-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf14-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbf14-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bbf14-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbf14-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf14-130">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbf14-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbf14-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbf14-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf14-132">Contrôle Popup du contexte</span><span class="sxs-lookup"><span data-stu-id="bbf14-132">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





