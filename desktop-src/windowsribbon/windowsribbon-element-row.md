---
title: Élément Row
description: Représente une ligne de contrôles dans un modèle de disposition SizeDefinition personnalisé.
ms.assetid: c3dac35f-3537-4eb7-b378-501ea88813f5
keywords:
- Ruban des fenêtres d’élément de ligne
topic_type:
- apiref
api_name:
- Row
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83a0a5a9e7908cc1c8cff688b3fefc1e8910b6a4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106509007"
---
# <a name="row-element"></a><span data-ttu-id="9b443-104">Élément Row</span><span class="sxs-lookup"><span data-stu-id="9b443-104">Row element</span></span>

<span data-ttu-id="9b443-105">Représente une ligne de contrôles dans un modèle de disposition SizeDefinition personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9b443-105">Represents a row of controls in a custom SizeDefinition layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="9b443-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="9b443-106">Usage</span></span>

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a><span data-ttu-id="9b443-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="9b443-107">Attributes</span></span>

<span data-ttu-id="9b443-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="9b443-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9b443-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9b443-109">Child elements</span></span>



| <span data-ttu-id="9b443-110">Élément</span><span class="sxs-lookup"><span data-stu-id="9b443-110">Element</span></span>                                                                                 | <span data-ttu-id="9b443-111">Description</span><span class="sxs-lookup"><span data-stu-id="9b443-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="9b443-112">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="9b443-112">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="9b443-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="9b443-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="9b443-114">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="9b443-114">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="9b443-115">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="9b443-115">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="9b443-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9b443-116">Parent elements</span></span>



| <span data-ttu-id="9b443-117">Élément</span><span class="sxs-lookup"><span data-stu-id="9b443-117">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b443-118">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="9b443-118">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9b443-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9b443-119">Remarks</span></span>

<span data-ttu-id="9b443-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="9b443-120">Optional.</span></span>

<span data-ttu-id="9b443-121">Peut se produire une ou plusieurs fois pour chaque élément [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="9b443-121">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="9b443-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="9b443-122">Examples</span></span>

<span data-ttu-id="9b443-123">L’exemple de code suivant illustre le balisage de base pour un modèle de disposition personnalisé à quatre boutons [**SizeDefinition**](windowsribbon-element-sizedefinition.md) avec différents éléments de **ligne** .</span><span class="sxs-lookup"><span data-stu-id="9b443-123">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **Row** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="9b443-124">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9b443-124">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="9b443-125">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b443-125">Minimum supported system</span></span><br/> | <span data-ttu-id="9b443-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b443-126">Windows 7</span></span> |
| <span data-ttu-id="9b443-127">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="9b443-127">Can be empty</span></span>                        | <span data-ttu-id="9b443-128">Non</span><span class="sxs-lookup"><span data-stu-id="9b443-128">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="9b443-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b443-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b443-130">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="9b443-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





