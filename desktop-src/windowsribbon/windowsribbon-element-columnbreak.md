---
title: Élément ColumnBreak
description: Représente un séparateur vertical (visible ou masqué) dans les modèles de disposition SizeDefinition personnalisés.
ms.assetid: 5979d3e6-366b-4c47-810f-90fb8039af8d
keywords:
- Ruban des fenêtres d’élément ColumnBreak
topic_type:
- apiref
api_name:
- ColumnBreak
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5bff1682cdf55b44092a176abd6dc7e935220a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444840"
---
# <a name="columnbreak-element"></a><span data-ttu-id="61e33-104">Élément ColumnBreak</span><span class="sxs-lookup"><span data-stu-id="61e33-104">ColumnBreak element</span></span>

<span data-ttu-id="61e33-105">Représente un séparateur vertical (visible ou masqué) dans les modèles de disposition [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personnalisés.</span><span class="sxs-lookup"><span data-stu-id="61e33-105">Represents a vertical separator (visible or hidden) in custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout templates.</span></span>

## <a name="usage"></a><span data-ttu-id="61e33-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="61e33-106">Usage</span></span>

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="61e33-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="61e33-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61e33-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="61e33-108">Attribute</span></span></th>
<th><span data-ttu-id="61e33-109">Type</span><span class="sxs-lookup"><span data-stu-id="61e33-109">Type</span></span></th>
<th><span data-ttu-id="61e33-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="61e33-110">Required</span></span></th>
<th><span data-ttu-id="61e33-111">Description</span><span class="sxs-lookup"><span data-stu-id="61e33-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61e33-112"><strong>ShowSeparator</strong></span><span class="sxs-lookup"><span data-stu-id="61e33-112"><strong>ShowSeparator</strong></span></span><br/></td>
<td><span data-ttu-id="61e33-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="61e33-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="61e33-114">Non</span><span class="sxs-lookup"><span data-stu-id="61e33-114">No</span></span><br/></td>
<td><span data-ttu-id="61e33-115">Limité à l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="61e33-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="61e33-116">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="61e33-116">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="61e33-117">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="61e33-117">Default.</span></span> <br/> </dd> <span data-ttu-id="61e33-118"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="61e33-118"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="61e33-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="61e33-119">Child elements</span></span>

<span data-ttu-id="61e33-120">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="61e33-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="61e33-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="61e33-121">Parent elements</span></span>



| <span data-ttu-id="61e33-122">Élément</span><span class="sxs-lookup"><span data-stu-id="61e33-122">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="61e33-123">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="61e33-123">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="61e33-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="61e33-124">Remarks</span></span>

<span data-ttu-id="61e33-125">facultatif.</span><span class="sxs-lookup"><span data-stu-id="61e33-125">Optional.</span></span>

<span data-ttu-id="61e33-126">Peut se produire une ou plusieurs fois pour chaque élément [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="61e33-126">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="61e33-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="61e33-127">Examples</span></span>

<span data-ttu-id="61e33-128">L’exemple suivant illustre le balisage de base pour un élément **ColumnBreak** dans un modèle de disposition personnalisé à quatre boutons [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="61e33-128">The following example demonstrates the basic markup for a **ColumnBreak** element in a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span> <span data-ttu-id="61e33-129">**ColumnBreak** est uniquement spécifié pour le `Large` modèle.</span><span class="sxs-lookup"><span data-stu-id="61e33-129">The **ColumnBreak** is only specified for the `Large` template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="61e33-130">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="61e33-130">Element information</span></span>

* <span data-ttu-id="61e33-131">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="61e33-131">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="61e33-132">**Peut être vide**: Oui</span><span class="sxs-lookup"><span data-stu-id="61e33-132">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="61e33-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61e33-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61e33-134">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="61e33-134">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





