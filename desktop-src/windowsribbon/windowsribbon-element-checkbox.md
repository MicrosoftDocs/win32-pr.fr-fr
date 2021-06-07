---
title: CheckBox, élément
description: Représente un contrôle de case à cocher.
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- Ruban Windows de l’élément CheckBox
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d9357337e569f43b14c34798c9c6e8da4b7b10b
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443040"
---
# <a name="checkbox-element"></a><span data-ttu-id="b7869-104">CheckBox, élément</span><span class="sxs-lookup"><span data-stu-id="b7869-104">CheckBox element</span></span>

<span data-ttu-id="b7869-105">Représente un contrôle de case [à cocher](windowsribbon-controls-checkbox.md) .</span><span class="sxs-lookup"><span data-stu-id="b7869-105">Represents a [Check Box](windowsribbon-controls-checkbox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="b7869-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="b7869-106">Usage</span></span>

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="b7869-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="b7869-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7869-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="b7869-108">Attribute</span></span></th>
<th><span data-ttu-id="b7869-109">Type</span><span class="sxs-lookup"><span data-stu-id="b7869-109">Type</span></span></th>
<th><span data-ttu-id="b7869-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b7869-110">Required</span></span></th>
<th><span data-ttu-id="b7869-111">Description</span><span class="sxs-lookup"><span data-stu-id="b7869-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7869-112"><strong>ApplicationDefaults. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="b7869-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="b7869-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="b7869-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="b7869-114">Non</span><span class="sxs-lookup"><span data-stu-id="b7869-114">No</span></span><br/></td>
<td><span data-ttu-id="b7869-115">Cet attribut est valide uniquement lorsque l’élément <strong>CheckBox</strong> est un enfant de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b7869-115">This attribute is valid only when the <strong>CheckBox</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="b7869-116">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7869-116">Restricted to one of the following values:</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b7869-117">La <strong>case à cocher</strong> ne prend pas en charge un État tertiaire ou indéterminé.</span><span class="sxs-lookup"><span data-stu-id="b7869-117">The <strong>CheckBox</strong> does not support a tertiary, or indeterminate, state.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="b7869-118">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="b7869-118">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="b7869-119">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="b7869-119">Default.</span></span> <br/> </dd> <span data-ttu-id="b7869-120"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="b7869-120"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7869-121"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="b7869-121"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="b7869-122">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="b7869-122">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="b7869-123">Non</span><span class="sxs-lookup"><span data-stu-id="b7869-123">No</span></span><br/></td>
<td><span data-ttu-id="b7869-124">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b7869-124">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="b7869-125">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="b7869-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b7869-126">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="b7869-126">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="b7869-127">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="b7869-127">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="b7869-128">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="b7869-128">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="b7869-129">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b7869-129">Child elements</span></span>

<span data-ttu-id="b7869-130">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="b7869-130">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b7869-131">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b7869-131">Parent elements</span></span>



| <span data-ttu-id="b7869-132">Élément</span><span class="sxs-lookup"><span data-stu-id="b7869-132">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7869-133">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="b7869-133">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="b7869-134">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="b7869-134">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="b7869-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="b7869-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="b7869-136">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="b7869-136">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="b7869-137">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="b7869-137">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="b7869-138">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="b7869-138">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="b7869-139">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="b7869-139">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="b7869-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="b7869-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="b7869-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="b7869-141">Remarks</span></span>

<span data-ttu-id="b7869-142">Facultatif ou obligatoire, en fonction de l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="b7869-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="b7869-143">Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="b7869-143">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="b7869-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="b7869-144">Examples</span></span>

<span data-ttu-id="b7869-145">L’exemple suivant illustre le balisage de base pour l’élément **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="b7869-145">The following example demonstrates the basic markup for the **CheckBox** element.</span></span>

<span data-ttu-id="b7869-146">Cette section de code montre les déclarations de commande de **case à cocher** .</span><span class="sxs-lookup"><span data-stu-id="b7869-146">This section of code shows the **CheckBox** Command declarations.</span></span>


```XML
<Command Name="cmdCheckBoxGroup"
         Symbol="cmdCheckBoxGroup"
         Comment="CheckBox Group"
         LabelTitle="CheckBoxGroup"/>
<Command Name="cmdCheckBox"
         Symbol="cmdCheckBox"
         Comment="CheckBox"
         LabelTitle="CheckBox"/>
```



<span data-ttu-id="b7869-147">Cette section de code montre les déclarations de contrôle **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="b7869-147">This section of code shows the **CheckBox** control declarations.</span></span>


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="b7869-148">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b7869-148">Element information</span></span>

* <span data-ttu-id="b7869-149">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7869-149">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="b7869-150">**Peut être vide**: Oui</span><span class="sxs-lookup"><span data-stu-id="b7869-150">**Can be empty**: Yes</span></span>


## <a name="see-also"></a><span data-ttu-id="b7869-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7869-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7869-152">Contrôle Check Box </span><span class="sxs-lookup"><span data-stu-id="b7869-152">Check Box control</span></span>](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 





