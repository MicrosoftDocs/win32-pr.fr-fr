---
title: Élément GroupSizeDefinition
description: Représente la taille de disposition d’un groupe de contrôles dans un modèle personnalisé.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- Ruban des fenêtres d’élément GroupSizeDefinition
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cf166dbf428c9d17beb148887cc94be73dc11a0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106511265"
---
# <a name="groupsizedefinition-element"></a><span data-ttu-id="ea006-104">Élément GroupSizeDefinition</span><span class="sxs-lookup"><span data-stu-id="ea006-104">GroupSizeDefinition element</span></span>

<span data-ttu-id="ea006-105">Représente la taille de disposition d’un groupe de contrôles dans un modèle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="ea006-105">Represents a layout size for a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="ea006-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="ea006-106">Usage</span></span>

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="ea006-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="ea006-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea006-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="ea006-108">Attribute</span></span></th>
<th><span data-ttu-id="ea006-109">Type</span><span class="sxs-lookup"><span data-stu-id="ea006-109">Type</span></span></th>
<th><span data-ttu-id="ea006-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ea006-110">Required</span></span></th>
<th><span data-ttu-id="ea006-111">Description</span><span class="sxs-lookup"><span data-stu-id="ea006-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ea006-112"><strong>Taille</strong></span><span class="sxs-lookup"><span data-stu-id="ea006-112"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="ea006-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="ea006-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="ea006-114">Non</span><span class="sxs-lookup"><span data-stu-id="ea006-114">No</span></span><br/></td>
<td><span data-ttu-id="ea006-115">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea006-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="ea006-116">
<dt><span></span><span></span><strong></strong> Conséquent</span><span class="sxs-lookup"><span data-stu-id="ea006-116">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="ea006-117">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ea006-117">Default.</span></span> <br/> </dd> <span data-ttu-id="ea006-118"><dt><span></span><span></span><strong></strong> Médias</span><span class="sxs-lookup"><span data-stu-id="ea006-118"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="ea006-119"><dt><span></span><span></span><strong></strong> Small</span><span class="sxs-lookup"><span data-stu-id="ea006-119"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ea006-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ea006-120">Child elements</span></span>



| <span data-ttu-id="ea006-121">Élément</span><span class="sxs-lookup"><span data-stu-id="ea006-121">Element</span></span>                                                                                 | <span data-ttu-id="ea006-122">Description</span><span class="sxs-lookup"><span data-stu-id="ea006-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="ea006-123">**ColumnBreak**</span><span class="sxs-lookup"><span data-stu-id="ea006-123">**ColumnBreak**</span></span>](windowsribbon-element-columnbreak.md)<br/>                     | <span data-ttu-id="ea006-124">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="ea006-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ea006-125">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="ea006-125">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="ea006-126">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="ea006-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ea006-127">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="ea006-127">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="ea006-128">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="ea006-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ea006-129">**Haut**</span><span class="sxs-lookup"><span data-stu-id="ea006-129">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                     | <span data-ttu-id="ea006-130">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="ea006-130">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ea006-131">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ea006-131">Parent elements</span></span>



| <span data-ttu-id="ea006-132">Élément</span><span class="sxs-lookup"><span data-stu-id="ea006-132">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="ea006-133">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="ea006-133">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ea006-134">Notes</span><span class="sxs-lookup"><span data-stu-id="ea006-134">Remarks</span></span>

<span data-ttu-id="ea006-135">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="ea006-135">Optional.</span></span>

<span data-ttu-id="ea006-136">Peut se produire jusqu’à trois fois pour chaque élément [**SizeDefinition**](windowsribbon-element-sizedefinition.md) (une fois pour chaque *taille*).</span><span class="sxs-lookup"><span data-stu-id="ea006-136">May occur up to three times for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element (one time for each *Size*).</span></span>

## <a name="examples"></a><span data-ttu-id="ea006-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="ea006-137">Examples</span></span>

<span data-ttu-id="ea006-138">L’exemple de code suivant illustre un modèle personnalisé de base qui comprend les trois tailles de disposition de groupe qui doivent être définies avec l’élément **GroupSizeDefinition** lors de la création d’un modèle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="ea006-138">The following code example illustrates a basic custom template that includes the three group layout sizes that must be defined with the **GroupSizeDefinition** element when creating a custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="ea006-139">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ea006-139">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="ea006-140">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea006-140">Minimum supported system</span></span><br/> | <span data-ttu-id="ea006-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ea006-141">Windows 7</span></span> |
| <span data-ttu-id="ea006-142">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="ea006-142">Can be empty</span></span>                        | <span data-ttu-id="ea006-143">Non</span><span class="sxs-lookup"><span data-stu-id="ea006-143">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="ea006-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea006-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea006-145">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="ea006-145">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





