---
title: Scale, élément
description: Représente la préférence de taille et de disposition d’un groupe de contrôles via une paire groupe, SizeDefinition.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Ruban Windows de l’élément de mise à l’échelle
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3832d36a48b330b036fa287499f9db387335f87b
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104381440"
---
# <a name="scale-element"></a><span data-ttu-id="5c71c-104">Scale, élément</span><span class="sxs-lookup"><span data-stu-id="5c71c-104">Scale element</span></span>

<span data-ttu-id="5c71c-105">Représente la préférence de taille et de disposition d’un [**groupe**](windowsribbon-element-group.md) de contrôles via une paire {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}.</span><span class="sxs-lookup"><span data-stu-id="5c71c-105">Represents the size and layout preference of a [**Group**](windowsribbon-element-group.md) of controls through a {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} pair.</span></span>

## <a name="usage"></a><span data-ttu-id="5c71c-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="5c71c-106">Usage</span></span>

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a><span data-ttu-id="5c71c-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="5c71c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c71c-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="5c71c-108">Attribute</span></span></th>
<th><span data-ttu-id="5c71c-109">Type</span><span class="sxs-lookup"><span data-stu-id="5c71c-109">Type</span></span></th>
<th><span data-ttu-id="5c71c-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5c71c-110">Required</span></span></th>
<th><span data-ttu-id="5c71c-111">Description</span><span class="sxs-lookup"><span data-stu-id="5c71c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c71c-112"><strong>Groupe</strong></span><span class="sxs-lookup"><span data-stu-id="5c71c-112"><strong>Group</strong></span></span><br/></td>
<td><span data-ttu-id="5c71c-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="5c71c-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="5c71c-114">Oui</span><span class="sxs-lookup"><span data-stu-id="5c71c-114">Yes</span></span><br/></td>
<td><span data-ttu-id="5c71c-115">Doit correspondre à un <em>CommandName</em>de <a href="windowsribbon-element-group.md"><strong>groupe</strong></a> existant.</span><span class="sxs-lookup"><span data-stu-id="5c71c-115">Must correspond to an existing <a href="windowsribbon-element-group.md"><strong>Group</strong></a> <em>CommandName</em>.</span></span><br/> <br/><span data-ttu-id="5c71c-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="5c71c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="5c71c-117">Chaîne ou valeur entière comprise entre 2 et 59999, inclusive ou 0X2 et 0xea5f en hexadécimal, inclus.</span><span class="sxs-lookup"><span data-stu-id="5c71c-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="5c71c-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="5c71c-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="5c71c-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="5c71c-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c71c-120"><strong>Taille</strong></span><span class="sxs-lookup"><span data-stu-id="5c71c-120"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="5c71c-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="5c71c-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="5c71c-122">Oui</span><span class="sxs-lookup"><span data-stu-id="5c71c-122">Yes</span></span><br/></td>
<td><span data-ttu-id="5c71c-123">Cette valeur doit correspondre à l’une des tailles valides de l’attribut <em>SizeDefinition</em> du <a href="windowsribbon-element-group.md"><strong>groupe</strong></a> associé de contrôles spécifié dans <em>Group</em>.</span><span class="sxs-lookup"><span data-stu-id="5c71c-123">This value should correspond to one of the valid sizes for the <em>SizeDefinition</em> attribute of the associated <a href="windowsribbon-element-group.md"><strong>Group</strong></a> of controls specified in <em>Group</em>.</span></span> <br/> <span data-ttu-id="5c71c-124">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c71c-124">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="5c71c-125">
<dt><span></span><span></span><strong></strong> Messages</span><span class="sxs-lookup"><span data-stu-id="5c71c-125">
<dt><span></span><span></span><strong></strong> (Popup)</span></span><br/> </dt> <dd> <span data-ttu-id="5c71c-126">Mise en page de contrôle identique à <code>Large</code> , mais hébergée dans un volet contextuel ou une liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="5c71c-126">Identical control layout to <code>Large</code> but hosted in a pop-up or a drop-down pane.</span></span><br/> </dd> <span data-ttu-id="5c71c-127"><dt><span></span><span></span><strong></strong> Small</span><span class="sxs-lookup"><span data-stu-id="5c71c-127"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="5c71c-128">Petit modèle <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5c71c-128">Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="5c71c-129"><dt><span></span><span></span><strong></strong> Médias</span><span class="sxs-lookup"><span data-stu-id="5c71c-129"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="5c71c-130">Modèle de <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> moyen.</span><span class="sxs-lookup"><span data-stu-id="5c71c-130">Medium <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="5c71c-131"><dt><span></span><span></span><strong></strong> Conséquent</span><span class="sxs-lookup"><span data-stu-id="5c71c-131"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="5c71c-132">Modèle <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> volumineux.</span><span class="sxs-lookup"><span data-stu-id="5c71c-132">Large <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="5c71c-133">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5c71c-133">Child elements</span></span>

<span data-ttu-id="5c71c-134">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="5c71c-134">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="5c71c-135">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5c71c-135">Parent elements</span></span>



| <span data-ttu-id="5c71c-136">Élément</span><span class="sxs-lookup"><span data-stu-id="5c71c-136">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c71c-137">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="5c71c-137">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [<span data-ttu-id="5c71c-138">**ScalingPolicy.IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="5c71c-138">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5c71c-139">Notes</span><span class="sxs-lookup"><span data-stu-id="5c71c-139">Remarks</span></span>

<span data-ttu-id="5c71c-140">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="5c71c-140">Optional.</span></span>

<span data-ttu-id="5c71c-141">Peut se produire une ou plusieurs fois pour chaque [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) ou [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).</span><span class="sxs-lookup"><span data-stu-id="5c71c-141">May occur one or more times for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) or [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).</span></span>

<span data-ttu-id="5c71c-142">Chaque paire d’attributs (*Group*, *Size*) doit être unique.</span><span class="sxs-lookup"><span data-stu-id="5c71c-142">Each (*Group*, *Size*) attribute pair must be unique.</span></span>

## <a name="examples"></a><span data-ttu-id="5c71c-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="5c71c-143">Examples</span></span>

<span data-ttu-id="5c71c-144">L’exemple suivant montre comment personnaliser l’apparence des contrôles dans un [**groupe**](windowsribbon-element-group.md) à l’aide de la fonctionnalité de disposition adaptative des modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de ruban.</span><span class="sxs-lookup"><span data-stu-id="5c71c-144">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="5c71c-145">Le manifeste [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) dans cet exemple spécifie une préférence [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pour chacun des quatre groupes de contrôles sur un onglet de **démarrage** . En outre, les éléments de mise à l' **échelle** sont spécifiés pour influencer le comportement de réduction, dans l’ordre de la taille décroissant, de chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="5c71c-145">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, **Scale** elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="element-information"></a><span data-ttu-id="5c71c-146">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5c71c-146">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="5c71c-147">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c71c-147">Minimum supported system</span></span><br/> | <span data-ttu-id="5c71c-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c71c-148">Windows 7</span></span> |
| <span data-ttu-id="5c71c-149">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="5c71c-149">Can be empty</span></span>                        | <span data-ttu-id="5c71c-150">Oui</span><span class="sxs-lookup"><span data-stu-id="5c71c-150">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="5c71c-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c71c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c71c-152">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="5c71c-152">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





