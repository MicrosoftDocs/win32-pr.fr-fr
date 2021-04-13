---
title: ToggleButton, élément
description: Représente un contrôle bouton bascule.
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- Ruban Windows de l’élément ToggleButton
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 652ea7b535f41cc3dbb40f25bbe49ab4fe52f5ff
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104314137"
---
# <a name="togglebutton-element"></a><span data-ttu-id="6b3d9-104">ToggleButton, élément</span><span class="sxs-lookup"><span data-stu-id="6b3d9-104">ToggleButton element</span></span>

<span data-ttu-id="6b3d9-105">Représente un contrôle [bouton bascule](windowsribbon-controls-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="6b3d9-105">Represents a [Toggle Button](windowsribbon-controls-togglebutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="6b3d9-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="6b3d9-106">Usage</span></span>

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="6b3d9-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="6b3d9-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b3d9-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="6b3d9-108">Attribute</span></span></th>
<th><span data-ttu-id="6b3d9-109">Type</span><span class="sxs-lookup"><span data-stu-id="6b3d9-109">Type</span></span></th>
<th><span data-ttu-id="6b3d9-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6b3d9-110">Required</span></span></th>
<th><span data-ttu-id="6b3d9-111">Description</span><span class="sxs-lookup"><span data-stu-id="6b3d9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b3d9-112"><strong>ApplicationDefaults. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="6b3d9-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="6b3d9-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="6b3d9-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="6b3d9-114">Non</span><span class="sxs-lookup"><span data-stu-id="6b3d9-114">No</span></span><br/></td>
<td><span data-ttu-id="6b3d9-115">Cet attribut est valide uniquement lorsque l’élément <strong>ToggleButton</strong> est un enfant de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6b3d9-115">This attribute is valid only when the <strong>ToggleButton</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="6b3d9-116">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6b3d9-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="6b3d9-117">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="6b3d9-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="6b3d9-118">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="6b3d9-118">Default.</span></span> <br/> </dd> <span data-ttu-id="6b3d9-119"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="6b3d9-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b3d9-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="6b3d9-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="6b3d9-121">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="6b3d9-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="6b3d9-122">Non</span><span class="sxs-lookup"><span data-stu-id="6b3d9-122">No</span></span><br/></td>
<td><span data-ttu-id="6b3d9-123">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6b3d9-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="6b3d9-124">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="6b3d9-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6b3d9-125">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="6b3d9-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="6b3d9-126">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="6b3d9-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="6b3d9-127">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="6b3d9-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="6b3d9-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6b3d9-128">Child elements</span></span>

<span data-ttu-id="6b3d9-129">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="6b3d9-129">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6b3d9-130">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6b3d9-130">Parent elements</span></span>



| <span data-ttu-id="6b3d9-131">Élément</span><span class="sxs-lookup"><span data-stu-id="6b3d9-131">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b3d9-132">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="6b3d9-132">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="6b3d9-133">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="6b3d9-133">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="6b3d9-134">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="6b3d9-134">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="6b3d9-135">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="6b3d9-135">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="6b3d9-136">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="6b3d9-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="6b3d9-137">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="6b3d9-137">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="6b3d9-138">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="6b3d9-138">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="6b3d9-139">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="6b3d9-139">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="6b3d9-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="6b3d9-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="6b3d9-141">Notes</span><span class="sxs-lookup"><span data-stu-id="6b3d9-141">Remarks</span></span>

<span data-ttu-id="6b3d9-142">Facultatif ou obligatoire, en fonction de l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="6b3d9-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="6b3d9-143">Peut se produire au plus une fois pour chaque élément [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6b3d9-143">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="6b3d9-144">Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="6b3d9-144">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="6b3d9-145">Exemples</span><span class="sxs-lookup"><span data-stu-id="6b3d9-145">Examples</span></span>

<span data-ttu-id="6b3d9-146">L’exemple suivant illustre le balisage de base pour l’élément **ToggleButton** .</span><span class="sxs-lookup"><span data-stu-id="6b3d9-146">The following example demonstrates the basic markup for the **ToggleButton** element.</span></span>

<span data-ttu-id="6b3d9-147">Cette section de code illustre une déclaration d’élément **ToggleButton** au sein de l’élément [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) .</span><span class="sxs-lookup"><span data-stu-id="6b3d9-147">This section of code shows a **ToggleButton** element declaration within the [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a><span data-ttu-id="6b3d9-148">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6b3d9-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="6b3d9-149">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b3d9-149">Minimum supported system</span></span><br/> | <span data-ttu-id="6b3d9-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6b3d9-150">Windows 7</span></span> |
| <span data-ttu-id="6b3d9-151">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="6b3d9-151">Can be empty</span></span>                        | <span data-ttu-id="6b3d9-152">Oui</span><span class="sxs-lookup"><span data-stu-id="6b3d9-152">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="6b3d9-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b3d9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b3d9-154">Bouton bascule</span><span class="sxs-lookup"><span data-stu-id="6b3d9-154">Toggle Button control</span></span>](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





