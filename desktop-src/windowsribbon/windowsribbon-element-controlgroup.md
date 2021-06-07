---
title: Élément ControlGroup
description: Représente un groupe de contrôles dans un modèle de disposition SizeDefinition.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- Ruban des fenêtres d’élément ControlGroup
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d2b49612102d03003c2f61395a56647aaef4475
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442940"
---
# <a name="controlgroup-element"></a><span data-ttu-id="eb94e-104">Élément ControlGroup</span><span class="sxs-lookup"><span data-stu-id="eb94e-104">ControlGroup element</span></span>

<span data-ttu-id="eb94e-105">Représente un groupe de contrôles dans un modèle de disposition [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="eb94e-105">Represents a group of controls in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="eb94e-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="eb94e-106">Usage</span></span>

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
```

## <a name="attributes"></a><span data-ttu-id="eb94e-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="eb94e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb94e-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="eb94e-108">Attribute</span></span></th>
<th><span data-ttu-id="eb94e-109">Type</span><span class="sxs-lookup"><span data-stu-id="eb94e-109">Type</span></span></th>
<th><span data-ttu-id="eb94e-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="eb94e-110">Required</span></span></th>
<th><span data-ttu-id="eb94e-111">Description</span><span class="sxs-lookup"><span data-stu-id="eb94e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eb94e-112"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="eb94e-112"><strong>SequenceNumber</strong></span></span><br/></td>
<td><span data-ttu-id="eb94e-113">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="eb94e-113">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="eb94e-114">Non</span><span class="sxs-lookup"><span data-stu-id="eb94e-114">No</span></span><br/></td>
<td><span data-ttu-id="eb94e-115">Valide uniquement lorsque <a href="windowsribbon-element-group.md"><strong>Group</strong></a> est l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="eb94e-115">Valid only when <a href="windowsribbon-element-group.md"><strong>Group</strong></a> is the parent element.</span></span><br/> <span data-ttu-id="eb94e-116">Chaque <em>élément</em> de la variable doit être unique au sein d’un élément de <a href="windowsribbon-element-group.md"><strong>groupe</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="eb94e-116">Each <em>SequenceNumber</em> must be unique within a <a href="windowsribbon-element-group.md"><strong>Group</strong></a> element.</span></span> <span data-ttu-id="eb94e-117">Les valeurs de l’élément de <em>tâche doivent augmenter</em> pour chaque élément de <strong>groupe</strong> , mais n’ont pas besoin d’être séquentielles.</span><span class="sxs-lookup"><span data-stu-id="eb94e-117">The values for <em>SequenceNumber</em> should increase for each <strong>Group</strong> element, but do not need to be sequential.</span></span> <br/> <br/><span data-ttu-id="eb94e-118">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="eb94e-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="eb94e-119">Toute valeur entière positive comprise entre 1000 et 59999 inclus.</span><span class="sxs-lookup"><span data-stu-id="eb94e-119">Any positive integer value between 1000 and 59999, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="eb94e-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eb94e-120">Child elements</span></span>



| <span data-ttu-id="eb94e-121">Élément</span><span class="sxs-lookup"><span data-stu-id="eb94e-121">Element</span></span>                                                                                 | <span data-ttu-id="eb94e-122">Description</span><span class="sxs-lookup"><span data-stu-id="eb94e-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="eb94e-123">**Button**</span><span class="sxs-lookup"><span data-stu-id="eb94e-123">**Button**</span></span>](windowsribbon-element-button.md)<br/>                               | <span data-ttu-id="eb94e-124">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eb94e-125">**Activé**</span><span class="sxs-lookup"><span data-stu-id="eb94e-125">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                           | <span data-ttu-id="eb94e-126">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eb94e-127">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="eb94e-127">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                           | <span data-ttu-id="eb94e-128">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eb94e-129">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="eb94e-129">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="eb94e-130">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-130">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eb94e-131">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="eb94e-131">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>               | <span data-ttu-id="eb94e-132">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eb94e-133">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="eb94e-133">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>     | <span data-ttu-id="eb94e-134">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eb94e-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="eb94e-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>             | <span data-ttu-id="eb94e-136">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eb94e-137">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="eb94e-137">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                     | <span data-ttu-id="eb94e-138">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-138">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="eb94e-139">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="eb94e-139">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>             | <span data-ttu-id="eb94e-140">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eb94e-141">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="eb94e-141">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                             | <span data-ttu-id="eb94e-142">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eb94e-143">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="eb94e-143">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                     | <span data-ttu-id="eb94e-144">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eb94e-145">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="eb94e-145">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>       | <span data-ttu-id="eb94e-146">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="eb94e-147">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="eb94e-147">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                   | <span data-ttu-id="eb94e-148">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="eb94e-148">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="eb94e-149">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="eb94e-149">Parent elements</span></span>



| <span data-ttu-id="eb94e-150">Élément</span><span class="sxs-lookup"><span data-stu-id="eb94e-150">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| <span data-ttu-id="eb94e-151">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="eb94e-151">**ControlGroup**</span></span><br/>                                                         |
| [<span data-ttu-id="eb94e-152">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="eb94e-152">**Group**</span></span>](windowsribbon-element-group.md)<br/>                             |
| [<span data-ttu-id="eb94e-153">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="eb94e-153">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="eb94e-154">**Ligne**</span><span class="sxs-lookup"><span data-stu-id="eb94e-154">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="eb94e-155">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb94e-155">Remarks</span></span>

<span data-ttu-id="eb94e-156">facultatif.</span><span class="sxs-lookup"><span data-stu-id="eb94e-156">Optional.</span></span>

<span data-ttu-id="eb94e-157">Peut se produire une ou plusieurs fois pour chaque élément [**Group**](windowsribbon-element-group.md) ou **ControlGroup** .</span><span class="sxs-lookup"><span data-stu-id="eb94e-157">May occur one or more times for each [**Group**](windowsribbon-element-group.md) or **ControlGroup** element.</span></span>

<span data-ttu-id="eb94e-158">Si aucun numéro de séquence n’est fourni, les éléments sont rendus dans l’ordre spécifié dans le balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="eb94e-158">If no sequence numbers are supplied, elements are rendered in the order specified in the Ribbon markup.</span></span>

<span data-ttu-id="eb94e-159">Si [**Group**](windowsribbon-element-group.md) ou **ControlGroup** est l’élément parent, **ControlGroup** est imposé aux éléments enfants possibles suivants : [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md)</span><span class="sxs-lookup"><span data-stu-id="eb94e-159">If [**Group**](windowsribbon-element-group.md) or **ControlGroup** is the parent element then **ControlGroup** is constrained to the following possible child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md)</span></span>

<span data-ttu-id="eb94e-160">Dans le cas contraire, lorsque [**Row**](windowsribbon-element-row.md) ou [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) est le parent, le [**groupe**](windowsribbon-element-group.md) est soumis à l’élément enfant possible suivant : [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span><span class="sxs-lookup"><span data-stu-id="eb94e-160">Otherwise, when [**Row**](windowsribbon-element-row.md) or [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) is the parent, [**Group**](windowsribbon-element-group.md) is constrained to the following possible child element: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span></span>

## <a name="examples"></a><span data-ttu-id="eb94e-161">Exemples</span><span class="sxs-lookup"><span data-stu-id="eb94e-161">Examples</span></span>

<span data-ttu-id="eb94e-162">L’exemple de code suivant illustre le balisage de base pour un modèle de disposition personnalisé à quatre boutons [**SizeDefinition**](windowsribbon-element-sizedefinition.md) avec différents éléments de [**groupe**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="eb94e-162">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various [**Group**](windowsribbon-element-group.md) elements.</span></span>


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="eb94e-163">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="eb94e-163">Element information</span></span>

* <span data-ttu-id="eb94e-164">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="eb94e-164">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="eb94e-165">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="eb94e-165">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="eb94e-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb94e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb94e-167">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="eb94e-167">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





