---
title: Élément ControlSizeDefinition
description: Représente le style de disposition d’un groupe de contrôles dans un modèle personnalisé.
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- Ruban des fenêtres d’élément ControlSizeDefinition
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ff5217c08b4ea6da1931b0c65501f912f2cc5dc
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443410"
---
# <a name="controlsizedefinition-element"></a><span data-ttu-id="baee7-104">Élément ControlSizeDefinition</span><span class="sxs-lookup"><span data-stu-id="baee7-104">ControlSizeDefinition element</span></span>

<span data-ttu-id="baee7-105">Représente le style de disposition d’un groupe de contrôles dans un modèle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="baee7-105">Represents the layout style of a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="baee7-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="baee7-106">Usage</span></span>

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="baee7-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="baee7-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="baee7-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="baee7-108">Attribute</span></span></th>
<th><span data-ttu-id="baee7-109">Type</span><span class="sxs-lookup"><span data-stu-id="baee7-109">Type</span></span></th>
<th><span data-ttu-id="baee7-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="baee7-110">Required</span></span></th>
<th><span data-ttu-id="baee7-111">Description</span><span class="sxs-lookup"><span data-stu-id="baee7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="baee7-112"><strong>NomContrôle</strong></span><span class="sxs-lookup"><span data-stu-id="baee7-112"><strong>ControlName</strong></span></span><br/></td>
<td><span data-ttu-id="baee7-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="baee7-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="baee7-114">Non</span><span class="sxs-lookup"><span data-stu-id="baee7-114">No</span></span><br/></td>
<td><span data-ttu-id="baee7-115"><dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="baee7-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="baee7-116">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="baee7-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="baee7-117">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="baee7-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="baee7-118">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="baee7-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="baee7-119"><strong>ImageSize</strong></span><span class="sxs-lookup"><span data-stu-id="baee7-119"><strong>ImageSize</strong></span></span><br/></td>
<td><span data-ttu-id="baee7-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="baee7-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="baee7-121">Non</span><span class="sxs-lookup"><span data-stu-id="baee7-121">No</span></span><br/></td>
<td><span data-ttu-id="baee7-122">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="baee7-122">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="baee7-123">
<dt><span></span><span></span><strong></strong> Conséquent</span><span class="sxs-lookup"><span data-stu-id="baee7-123">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="baee7-124"><dt><span></span><span></span><strong></strong> Small</span><span class="sxs-lookup"><span data-stu-id="baee7-124"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="baee7-125">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="baee7-125">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="baee7-126"><strong>IsImageVisible</strong></span><span class="sxs-lookup"><span data-stu-id="baee7-126"><strong>IsImageVisible</strong></span></span><br/></td>
<td><span data-ttu-id="baee7-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="baee7-127">Boolean</span></span><br/></td>
<td><span data-ttu-id="baee7-128">Non</span><span class="sxs-lookup"><span data-stu-id="baee7-128">No</span></span><br/></td>
<td><span data-ttu-id="baee7-129">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="baee7-129">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="baee7-130">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="baee7-130">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="baee7-131">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="baee7-131">Default.</span></span> <br/> </dd> <span data-ttu-id="baee7-132"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="baee7-132"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="baee7-133"><strong>IsLabelVisible</strong></span><span class="sxs-lookup"><span data-stu-id="baee7-133"><strong>IsLabelVisible</strong></span></span><br/></td>
<td><span data-ttu-id="baee7-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="baee7-134">Boolean</span></span><br/></td>
<td><span data-ttu-id="baee7-135">Non</span><span class="sxs-lookup"><span data-stu-id="baee7-135">No</span></span><br/></td>
<td><span data-ttu-id="baee7-136">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="baee7-136">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="baee7-137">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="baee7-137">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="baee7-138">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="baee7-138">Default.</span></span> <br/> </dd> <span data-ttu-id="baee7-139"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="baee7-139"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="baee7-140"><strong>IsPopup</strong></span><span class="sxs-lookup"><span data-stu-id="baee7-140"><strong>IsPopup</strong></span></span><br/></td>
<td><span data-ttu-id="baee7-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="baee7-141">Boolean</span></span><br/></td>
<td><span data-ttu-id="baee7-142">Non</span><span class="sxs-lookup"><span data-stu-id="baee7-142">No</span></span><br/></td>
<td><span data-ttu-id="baee7-143">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="baee7-143">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="baee7-144">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="baee7-144">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="baee7-145"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="baee7-145"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="baee7-146">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="baee7-146">Child elements</span></span>

<span data-ttu-id="baee7-147">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="baee7-147">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="baee7-148">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="baee7-148">Parent elements</span></span>



| <span data-ttu-id="baee7-149">Élément</span><span class="sxs-lookup"><span data-stu-id="baee7-149">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="baee7-150">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="baee7-150">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               |
| [<span data-ttu-id="baee7-151">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="baee7-151">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="baee7-152">**Ligne**</span><span class="sxs-lookup"><span data-stu-id="baee7-152">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="baee7-153">Remarques</span><span class="sxs-lookup"><span data-stu-id="baee7-153">Remarks</span></span>

<span data-ttu-id="baee7-154">facultatif.</span><span class="sxs-lookup"><span data-stu-id="baee7-154">Optional.</span></span>

<span data-ttu-id="baee7-155">Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md)ou [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="baee7-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md), or [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="baee7-156">Exemples</span><span class="sxs-lookup"><span data-stu-id="baee7-156">Examples</span></span>

<span data-ttu-id="baee7-157">L’exemple de code suivant illustre le balisage de base pour un modèle de disposition personnalisé à quatre boutons [**SizeDefinition**](windowsribbon-element-sizedefinition.md) avec différents éléments **ControlSizeDefinition** .</span><span class="sxs-lookup"><span data-stu-id="baee7-157">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **ControlSizeDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="baee7-158">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="baee7-158">Element information</span></span>

* <span data-ttu-id="baee7-159">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="baee7-159">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="baee7-160">**Peut être vide**: Oui</span><span class="sxs-lookup"><span data-stu-id="baee7-160">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="baee7-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baee7-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baee7-162">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="baee7-162">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





