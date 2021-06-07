---
title: élément Group
description: Représente un contrôle de groupe qui fonctionne comme un conteneur pour un groupe d’éléments.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Ruban des fenêtres d’élément de groupe
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1162055491f61ae6feffa385bbc5015e4f1b66f0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442870"
---
# <a name="group-element"></a><span data-ttu-id="e6818-104">élément Group</span><span class="sxs-lookup"><span data-stu-id="e6818-104">Group element</span></span>

<span data-ttu-id="e6818-105">Représente un contrôle de [groupe](windowsribbon-controls-group.md) qui fonctionne comme un conteneur pour un groupe d’éléments.</span><span class="sxs-lookup"><span data-stu-id="e6818-105">Represents a [Group](windowsribbon-controls-group.md) control that functions as a container for a group of elements.</span></span>

## <a name="usage"></a><span data-ttu-id="e6818-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="e6818-106">Usage</span></span>

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a><span data-ttu-id="e6818-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="e6818-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6818-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="e6818-108">Attribute</span></span></th>
<th><span data-ttu-id="e6818-109">Type</span><span class="sxs-lookup"><span data-stu-id="e6818-109">Type</span></span></th>
<th><span data-ttu-id="e6818-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e6818-110">Required</span></span></th>
<th><span data-ttu-id="e6818-111">Description</span><span class="sxs-lookup"><span data-stu-id="e6818-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6818-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="e6818-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="e6818-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="e6818-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="e6818-114">Non</span><span class="sxs-lookup"><span data-stu-id="e6818-114">No</span></span><br/></td>
<td><span data-ttu-id="e6818-115"><dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="e6818-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e6818-116">Chaîne qui contient une liste d’entiers séparés par des virgules, comprise entre 0 et 31.</span><span class="sxs-lookup"><span data-stu-id="e6818-116">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="e6818-117">L’espace blanc est valide et ignoré.</span><span class="sxs-lookup"><span data-stu-id="e6818-117">White space is valid and ignored.</span></span><br/> <span data-ttu-id="e6818-118">Longueur maximale : 250 caractères.</span><span class="sxs-lookup"><span data-stu-id="e6818-118">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6818-119"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="e6818-119"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="e6818-120">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="e6818-120">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="e6818-121">Non</span><span class="sxs-lookup"><span data-stu-id="e6818-121">No</span></span><br/></td>
<td><span data-ttu-id="e6818-122">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e6818-122">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="e6818-123">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="e6818-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e6818-124">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="e6818-124">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="e6818-125">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="e6818-125">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="e6818-126">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="e6818-126">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6818-127"><strong>SizeDefinition</strong></span><span class="sxs-lookup"><span data-stu-id="e6818-127"><strong>SizeDefinition</strong></span></span><br/></td>
<td><span data-ttu-id="e6818-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="e6818-128">xs:string</span></span><br/></td>
<td><span data-ttu-id="e6818-129">Non</span><span class="sxs-lookup"><span data-stu-id="e6818-129">No</span></span><br/></td>
<td><span data-ttu-id="e6818-130">Lorsqu’il est spécifié, la valeur de <em>SizeDefinition</em> est limitée à l’un des <a href="windowsribbon-templates.md">modèles de disposition</a> définis par l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="e6818-130">When specified, the value of <em>SizeDefinition</em> is constrained to one of the <a href="windowsribbon-templates.md">layout templates</a> defined by the Ribbon framework.</span></span> <br/> <br/><span data-ttu-id="e6818-131">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="e6818-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e6818-132">Toute séquence de zéro ou plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="e6818-132">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="e6818-133">La longueur maximale est illimitée.</span><span class="sxs-lookup"><span data-stu-id="e6818-133">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e6818-134">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e6818-134">Child elements</span></span>



| <span data-ttu-id="e6818-135">Élément</span><span class="sxs-lookup"><span data-stu-id="e6818-135">Element</span></span>                                                                             | <span data-ttu-id="e6818-136">Description</span><span class="sxs-lookup"><span data-stu-id="e6818-136">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="e6818-137">**Button**</span><span class="sxs-lookup"><span data-stu-id="e6818-137">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="e6818-138">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e6818-139">**Activé**</span><span class="sxs-lookup"><span data-stu-id="e6818-139">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="e6818-140">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e6818-141">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="e6818-141">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="e6818-142">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e6818-143">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="e6818-143">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               | <span data-ttu-id="e6818-144">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e6818-145">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="e6818-145">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="e6818-146">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e6818-147">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="e6818-147">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="e6818-148">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e6818-149">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="e6818-149">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="e6818-150">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-150">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e6818-151">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="e6818-151">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="e6818-152">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e6818-152">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="e6818-153">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="e6818-153">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>         | <span data-ttu-id="e6818-154">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-154">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e6818-155">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="e6818-155">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/>           | <span data-ttu-id="e6818-156">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="e6818-156">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="e6818-157">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="e6818-157">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                         | <span data-ttu-id="e6818-158">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-158">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e6818-159">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="e6818-159">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="e6818-160">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-160">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e6818-161">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="e6818-161">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="e6818-162">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-162">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e6818-163">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="e6818-163">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="e6818-164">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="e6818-164">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e6818-165">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e6818-165">Parent elements</span></span>



| <span data-ttu-id="e6818-166">Élément</span><span class="sxs-lookup"><span data-stu-id="e6818-166">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="e6818-167">**/**</span><span class="sxs-lookup"><span data-stu-id="e6818-167">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e6818-168">Remarques</span><span class="sxs-lookup"><span data-stu-id="e6818-168">Remarks</span></span>

<span data-ttu-id="e6818-169">facultatif.</span><span class="sxs-lookup"><span data-stu-id="e6818-169">Optional.</span></span>

<span data-ttu-id="e6818-170">Peut se produire une ou plusieurs fois pour chaque élément [**Tab**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="e6818-170">May occur one or more times for each [**Tab**](windowsribbon-element-tab.md) element.</span></span>

<span data-ttu-id="e6818-171">L' [**onglet**](windowsribbon-element-tab.md) prend en charge les [modes d’application](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="e6818-171">[**Tab**](windowsribbon-element-tab.md) supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="e6818-172">Le balisage du ruban est valide uniquement lorsque les éléments enfants du **groupe** correspondent au modèle spécifié pour *SizeDefinition*.</span><span class="sxs-lookup"><span data-stu-id="e6818-172">The Ribbon markup is valid only when the child elements of **Group** correspond to the template specified for *SizeDefinition*.</span></span>

## <a name="examples"></a><span data-ttu-id="e6818-173">Exemples</span><span class="sxs-lookup"><span data-stu-id="e6818-173">Examples</span></span>

<span data-ttu-id="e6818-174">L’exemple de code suivant illustre l’utilisation d’un modèle personnalisé dans un **groupe**.</span><span class="sxs-lookup"><span data-stu-id="e6818-174">The following code example illustrates the use of a custom template in a **Group**.</span></span>


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="e6818-175">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e6818-175">Element information</span></span>

* <span data-ttu-id="e6818-176">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6818-176">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="e6818-177">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="e6818-177">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="e6818-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6818-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6818-179">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="e6818-179">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="e6818-180">Contrôle de groupe</span><span class="sxs-lookup"><span data-stu-id="e6818-180">Group control</span></span>](windowsribbon-controls-group.md)
</dt> <dt>

[<span data-ttu-id="e6818-181">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="e6818-181">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

