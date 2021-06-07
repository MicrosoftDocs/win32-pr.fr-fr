---
title: Tab (élément)
description: Représente un onglet principal ou contextuel.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Ruban fenêtres d’élément d’onglet
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 410326961df84f6ae62d3c43bee3e651c9533066
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443880"
---
# <a name="tab-element"></a><span data-ttu-id="634c2-104">Tab (élément)</span><span class="sxs-lookup"><span data-stu-id="634c2-104">Tab element</span></span>

<span data-ttu-id="634c2-105">Représente un onglet [principal](windowsribbon-controls-tab.md) ou [contextuel](windowsribbon-controls-tabgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="634c2-105">Represents a [core](windowsribbon-controls-tab.md) or [contextual](windowsribbon-controls-tabgroup.md) tab.</span></span>

## <a name="usage"></a><span data-ttu-id="634c2-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="634c2-106">Usage</span></span>

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a><span data-ttu-id="634c2-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="634c2-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="634c2-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="634c2-108">Attribute</span></span></th>
<th><span data-ttu-id="634c2-109">Type</span><span class="sxs-lookup"><span data-stu-id="634c2-109">Type</span></span></th>
<th><span data-ttu-id="634c2-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="634c2-110">Required</span></span></th>
<th><span data-ttu-id="634c2-111">Description</span><span class="sxs-lookup"><span data-stu-id="634c2-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="634c2-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="634c2-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="634c2-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="634c2-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="634c2-114">Non</span><span class="sxs-lookup"><span data-stu-id="634c2-114">No</span></span><br/></td>
<td><span data-ttu-id="634c2-115">Valide uniquement si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> est l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="634c2-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="634c2-116">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="634c2-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="634c2-117">Chaîne qui contient une liste d’entiers séparés par des virgules, comprise entre 0 et 31.</span><span class="sxs-lookup"><span data-stu-id="634c2-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="634c2-118">L’espace blanc est valide et ignoré.</span><span class="sxs-lookup"><span data-stu-id="634c2-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="634c2-119">Longueur maximale : 250 caractères.</span><span class="sxs-lookup"><span data-stu-id="634c2-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="634c2-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="634c2-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="634c2-121">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="634c2-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="634c2-122">Non</span><span class="sxs-lookup"><span data-stu-id="634c2-122">No</span></span><br/></td>
<td><span data-ttu-id="634c2-123">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="634c2-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="634c2-124">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="634c2-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="634c2-125">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="634c2-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="634c2-126">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="634c2-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="634c2-127">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="634c2-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="634c2-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="634c2-128">Child elements</span></span>



| <span data-ttu-id="634c2-129">Élément</span><span class="sxs-lookup"><span data-stu-id="634c2-129">Element</span></span>                                                                         | <span data-ttu-id="634c2-130">Description</span><span class="sxs-lookup"><span data-stu-id="634c2-130">Description</span></span>                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="634c2-131">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="634c2-131">**Group**</span></span>](windowsribbon-element-group.md)<br/>                         | <span data-ttu-id="634c2-132">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="634c2-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="634c2-133">**Tab. ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="634c2-133">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> | <span data-ttu-id="634c2-134">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="634c2-134">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="634c2-135">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="634c2-135">Parent elements</span></span>



| <span data-ttu-id="634c2-136">Élément</span><span class="sxs-lookup"><span data-stu-id="634c2-136">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="634c2-137">**Ruban. tabulations**</span><span class="sxs-lookup"><span data-stu-id="634c2-137">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/> |
| [<span data-ttu-id="634c2-138">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="634c2-138">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="634c2-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="634c2-139">Remarks</span></span>

<span data-ttu-id="634c2-140">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="634c2-140">Required.</span></span>

<span data-ttu-id="634c2-141">Doit se produire au moins une fois pour chaque élément [**ruban. Tabs**](windowsribbon-element-ribbon-tabs.md) ou [**TabGroup**](windowsribbon-element-tabgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="634c2-141">Must occur at least once for each [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) or [**TabGroup**](windowsribbon-element-tabgroup.md) element.</span></span>

<span data-ttu-id="634c2-142">L' **onglet** prend en charge les [modes d’application](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="634c2-142">**Tab** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="634c2-143">Si [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) est présent pour l’élément **Tab** , une entrée pour chaque élément de [**groupe**](windowsribbon-element-group.md) et sa taille idéale est requise sous **ScalingPolicy. IdealSizes**.</span><span class="sxs-lookup"><span data-stu-id="634c2-143">If [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) is present for the **Tab** element, then an entry for each [**Group**](windowsribbon-element-group.md) element and its ideal size is required under **ScalingPolicy.IdealSizes**.</span></span>

## <a name="examples"></a><span data-ttu-id="634c2-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="634c2-144">Examples</span></span>

<span data-ttu-id="634c2-145">L’exemple suivant illustre le balisage de base pour l’élément **Tab** .</span><span class="sxs-lookup"><span data-stu-id="634c2-145">The following example demonstrates the basic markup for the **Tab** element.</span></span>

<span data-ttu-id="634c2-146">Cette section de code montre les déclarations de commande d' **onglet** pour un onglet de **démarrage** .</span><span class="sxs-lookup"><span data-stu-id="634c2-146">This section of code shows the **Tab** Command declarations for a **Home** tab.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



<span data-ttu-id="634c2-147">Cette section de code montre les déclarations de contrôle d' **onglet** .</span><span class="sxs-lookup"><span data-stu-id="634c2-147">This section of code shows the **Tab** control declarations.</span></span>


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a><span data-ttu-id="634c2-148">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="634c2-148">Element information</span></span>

- <span data-ttu-id="634c2-149">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="634c2-149">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="634c2-150">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="634c2-150">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="634c2-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="634c2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="634c2-152">Contrôle Tab</span><span class="sxs-lookup"><span data-stu-id="634c2-152">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> <dt>

[<span data-ttu-id="634c2-153">Contrôle de groupe d’onglets</span><span class="sxs-lookup"><span data-stu-id="634c2-153">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="634c2-154">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="634c2-154">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

