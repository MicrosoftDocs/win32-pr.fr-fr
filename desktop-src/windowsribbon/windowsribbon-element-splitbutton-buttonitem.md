---
title: Propriété SplitButton. ButtonItem
description: Représente un conteneur pour un bouton ou un bouton bascule qui expose la commande par défaut d’un bouton partagé.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- Ruban Windows de la propriété SplitButton. ButtonItem
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf1e1cb908ce9a86f23f75d17bf2e76797997db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464674"
---
# <a name="splitbuttonbuttonitem-property"></a><span data-ttu-id="63516-104">Propriété SplitButton. ButtonItem</span><span class="sxs-lookup"><span data-stu-id="63516-104">SplitButton.ButtonItem property</span></span>

<span data-ttu-id="63516-105">Représente un conteneur pour un [bouton ou un](windowsribbon-controls-button.md) [bouton bascule](windowsribbon-controls-togglebutton.md) qui expose la commande par défaut d’un [bouton partagé](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="63516-105">Represents a container for a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) that exposes the default Command of a [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="63516-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="63516-106">Usage</span></span>

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a><span data-ttu-id="63516-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="63516-107">Attributes</span></span>

<span data-ttu-id="63516-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="63516-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="63516-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="63516-109">Child elements</span></span>



| <span data-ttu-id="63516-110">Élément</span><span class="sxs-lookup"><span data-stu-id="63516-110">Element</span></span>                                                               | <span data-ttu-id="63516-111">Description</span><span class="sxs-lookup"><span data-stu-id="63516-111">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="63516-112">**Button**</span><span class="sxs-lookup"><span data-stu-id="63516-112">**Button**</span></span>](windowsribbon-element-button.md)<br/>             | <span data-ttu-id="63516-113">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="63516-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="63516-114">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="63516-114">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/> | <span data-ttu-id="63516-115">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="63516-115">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="63516-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="63516-116">Parent elements</span></span>



| <span data-ttu-id="63516-117">Élément</span><span class="sxs-lookup"><span data-stu-id="63516-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="63516-118">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="63516-118">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="63516-119">Notes</span><span class="sxs-lookup"><span data-stu-id="63516-119">Remarks</span></span>

<span data-ttu-id="63516-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="63516-120">Optional.</span></span>

<span data-ttu-id="63516-121">Peut se produire au plus une fois pour chaque [**SplitButton**](windowsribbon-element-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="63516-121">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

<span data-ttu-id="63516-122">Chaque **SplitButton. ButtonItem** ne peut contenir qu’un seul élément enfant [**Button**](windowsribbon-element-button.md) ou [**ToggleButton**](windowsribbon-element-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="63516-122">Each **SplitButton.ButtonItem** can contain only one [**Button**](windowsribbon-element-button.md) or [**ToggleButton**](windowsribbon-element-togglebutton.md) child element.</span></span>

## <a name="examples"></a><span data-ttu-id="63516-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="63516-123">Examples</span></span>

<span data-ttu-id="63516-124">L’exemple suivant illustre le balisage de base pour le [bouton partagé](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="63516-124">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="63516-125">Cette section de code montre les déclarations de commande [**SplitButton**](windowsribbon-element-splitbutton.md) et **SplitButton. ButtonItem** , avec un [**groupe**](windowsribbon-element-group.md) associé qui fonctionne comme conteneur parent de l’élément **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="63516-125">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="63516-126">Cette section de code montre les déclarations de contrôle [**SplitButton**](windowsribbon-element-splitbutton.md) et **SplitButton. ButtonItem** .</span><span class="sxs-lookup"><span data-stu-id="63516-126">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** control declarations.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="63516-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63516-127">Requirements</span></span>



| <span data-ttu-id="63516-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63516-128">Requirement</span></span> | <span data-ttu-id="63516-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="63516-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="63516-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63516-130">Minimum supported client</span></span><br/> | <span data-ttu-id="63516-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63516-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="63516-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63516-132">Minimum supported server</span></span><br/> | <span data-ttu-id="63516-133">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63516-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63516-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63516-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63516-135">Contrôle de bouton partagé</span><span class="sxs-lookup"><span data-stu-id="63516-135">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





