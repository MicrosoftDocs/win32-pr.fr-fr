---
title: Élément ContextMap
description: Représente un mappage de paire ContextMenu et MiniToolbar.
ms.assetid: 84379578-24c6-4bf7-8dcf-8e21e5665d29
keywords:
- Ruban des fenêtres d’élément ContextMap
topic_type:
- apiref
api_name:
- ContextMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4754fc75ca09e39cdc7eabbeae2a0a2d2630c31f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443010"
---
# <a name="contextmap-element"></a><span data-ttu-id="870e9-104">Élément ContextMap</span><span class="sxs-lookup"><span data-stu-id="870e9-104">ContextMap element</span></span>

<span data-ttu-id="870e9-105">Représente un mappage de paire [**ContextMenu**](windowsribbon-element-contextmenu.md) et [**MiniToolbar**](windowsribbon-element-minitoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="870e9-105">Represents a [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) pair mapping.</span></span>

## <a name="usage"></a><span data-ttu-id="870e9-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="870e9-106">Usage</span></span>

``` syntax
<ContextMap
  CommandName = "xs:positiveInteger or xs:string"
  MiniToolbar = "xs:string"
  ContextMenu = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="870e9-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="870e9-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="870e9-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="870e9-108">Attribute</span></span></th>
<th><span data-ttu-id="870e9-109">Type</span><span class="sxs-lookup"><span data-stu-id="870e9-109">Type</span></span></th>
<th><span data-ttu-id="870e9-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="870e9-110">Required</span></span></th>
<th><span data-ttu-id="870e9-111">Description</span><span class="sxs-lookup"><span data-stu-id="870e9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="870e9-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="870e9-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="870e9-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="870e9-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="870e9-114">Non</span><span class="sxs-lookup"><span data-stu-id="870e9-114">No</span></span><br/></td>
<td><span data-ttu-id="870e9-115">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="870e9-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="870e9-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="870e9-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="870e9-117">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="870e9-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="870e9-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="870e9-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="870e9-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="870e9-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="870e9-120"><strong>ContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="870e9-120"><strong>ContextMenu</strong></span></span><br/></td>
<td><span data-ttu-id="870e9-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="870e9-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="870e9-122">Non</span><span class="sxs-lookup"><span data-stu-id="870e9-122">No</span></span><br/></td>
<td><span data-ttu-id="870e9-123">Doit correspondre à un nom <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em></em>existant.</span><span class="sxs-lookup"><span data-stu-id="870e9-123">Must correspond to an existing <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="870e9-124">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="870e9-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="870e9-125">Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="870e9-125">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="870e9-126"><strong>MiniToolbar</strong></span><span class="sxs-lookup"><span data-stu-id="870e9-126"><strong>MiniToolbar</strong></span></span><br/></td>
<td><span data-ttu-id="870e9-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="870e9-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="870e9-128">Non</span><span class="sxs-lookup"><span data-stu-id="870e9-128">No</span></span><br/></td>
<td><span data-ttu-id="870e9-129">Doit correspondre à un <em>nom</em>de <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> existant.</span><span class="sxs-lookup"><span data-stu-id="870e9-129">Must correspond to an existing <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="870e9-130">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="870e9-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="870e9-131">Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="870e9-131">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="870e9-132">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="870e9-132">Child elements</span></span>

<span data-ttu-id="870e9-133">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="870e9-133">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="870e9-134">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="870e9-134">Parent elements</span></span>



| <span data-ttu-id="870e9-135">Élément</span><span class="sxs-lookup"><span data-stu-id="870e9-135">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="870e9-136">**ContextPopup.ContextMaps**</span><span class="sxs-lookup"><span data-stu-id="870e9-136">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="870e9-137">Remarques</span><span class="sxs-lookup"><span data-stu-id="870e9-137">Remarks</span></span>

<span data-ttu-id="870e9-138">facultatif.</span><span class="sxs-lookup"><span data-stu-id="870e9-138">Optional.</span></span>

<span data-ttu-id="870e9-139">Peut se produire une ou plusieurs fois pour chaque [**ContextPopup. ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span><span class="sxs-lookup"><span data-stu-id="870e9-139">May occur one or more times for each [**ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span></span>

## <a name="examples"></a><span data-ttu-id="870e9-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="870e9-140">Examples</span></span>

<span data-ttu-id="870e9-141">L’exemple suivant illustre le balisage de base pour une vue [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="870e9-141">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="870e9-142">Cette section de code illustre un ensemble de déclarations de contrôle **ContextMap** .</span><span class="sxs-lookup"><span data-stu-id="870e9-142">This section of code shows a set of **ContextMap** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="870e9-143">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="870e9-143">Element information</span></span>


* <span data-ttu-id="870e9-144">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="870e9-144">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="870e9-145">**Peut être vide**: Oui</span><span class="sxs-lookup"><span data-stu-id="870e9-145">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="870e9-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="870e9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="870e9-147">Contrôle Popup du contexte</span><span class="sxs-lookup"><span data-stu-id="870e9-147">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





