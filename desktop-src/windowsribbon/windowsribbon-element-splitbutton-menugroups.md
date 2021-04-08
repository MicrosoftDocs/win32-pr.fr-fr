---
title: Propriété SplitButton. MenuGroups
description: Représente un conteneur pour un ensemble d’éléments de menu déroulants dans un contrôle de bouton partagé standard.
ms.assetid: 6328ad49-037b-4cd5-90f6-b91646e260ee
keywords:
- Ruban Windows de la propriété SplitButton. MenuGroups
topic_type:
- apiref
api_name:
- SplitButton.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8af4639040d6b6302b4d2b5761d750074389a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741461"
---
# <a name="splitbuttonmenugroups-property"></a><span data-ttu-id="77f9d-104">Propriété SplitButton. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="77f9d-104">SplitButton.MenuGroups property</span></span>

<span data-ttu-id="77f9d-105">Représente un conteneur pour un ensemble d’éléments de menu déroulants dans un contrôle de [bouton partagé](windowsribbon-controls-splitbutton.md) standard.</span><span class="sxs-lookup"><span data-stu-id="77f9d-105">Represents a container for a set of drop-down menu items in a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="77f9d-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="77f9d-106">Usage</span></span>

``` syntax
<SplitButton.MenuGroups>
  child elements
</SplitButton.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="77f9d-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="77f9d-107">Attributes</span></span>

<span data-ttu-id="77f9d-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="77f9d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="77f9d-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="77f9d-109">Child elements</span></span>



| <span data-ttu-id="77f9d-110">Élément</span><span class="sxs-lookup"><span data-stu-id="77f9d-110">Element</span></span>                                                         | <span data-ttu-id="77f9d-111">Description</span><span class="sxs-lookup"><span data-stu-id="77f9d-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="77f9d-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="77f9d-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="77f9d-113">Doit se produire au moins une fois</span><span class="sxs-lookup"><span data-stu-id="77f9d-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="77f9d-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="77f9d-114">Parent elements</span></span>



| <span data-ttu-id="77f9d-115">Élément</span><span class="sxs-lookup"><span data-stu-id="77f9d-115">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="77f9d-116">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="77f9d-116">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="77f9d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="77f9d-117">Remarks</span></span>

<span data-ttu-id="77f9d-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="77f9d-118">Optional.</span></span>

<span data-ttu-id="77f9d-119">Peut se produire au plus une fois pour chaque [**SplitButton**](windowsribbon-element-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="77f9d-119">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

## <a name="examples"></a><span data-ttu-id="77f9d-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="77f9d-120">Examples</span></span>

<span data-ttu-id="77f9d-121">L’exemple suivant illustre le balisage de base pour le [bouton partagé](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="77f9d-121">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="77f9d-122">Cette section de code montre les déclarations de commande [**SplitButton**](windowsribbon-element-splitbutton.md) et **SplitButton. MenuGroups** , avec un [**groupe**](windowsribbon-element-group.md) associé qui fonctionne comme conteneur parent de l’élément **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="77f9d-122">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="77f9d-123">Cette section de code montre les déclarations de contrôle [**SplitButton**](windowsribbon-element-splitbutton.md) et **SplitButton. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="77f9d-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** control declarations.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="77f9d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77f9d-124">Requirements</span></span>



| <span data-ttu-id="77f9d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77f9d-125">Requirement</span></span> | <span data-ttu-id="77f9d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="77f9d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="77f9d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77f9d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="77f9d-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77f9d-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="77f9d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77f9d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="77f9d-130">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77f9d-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77f9d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77f9d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f9d-132">Contrôle de bouton partagé</span><span class="sxs-lookup"><span data-stu-id="77f9d-132">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





