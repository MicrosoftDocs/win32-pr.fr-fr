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
ms.openlocfilehash: 7d642cd209b3e00e2c63f7376e321132a1c0e686
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445020"
---
# <a name="row-element"></a><span data-ttu-id="2f375-104">Élément Row</span><span class="sxs-lookup"><span data-stu-id="2f375-104">Row element</span></span>

<span data-ttu-id="2f375-105">Représente une ligne de contrôles dans un modèle de disposition SizeDefinition personnalisé.</span><span class="sxs-lookup"><span data-stu-id="2f375-105">Represents a row of controls in a custom SizeDefinition layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="2f375-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="2f375-106">Usage</span></span>

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a><span data-ttu-id="2f375-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="2f375-107">Attributes</span></span>

<span data-ttu-id="2f375-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="2f375-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2f375-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2f375-109">Child elements</span></span>



| <span data-ttu-id="2f375-110">Élément</span><span class="sxs-lookup"><span data-stu-id="2f375-110">Element</span></span>                                                                                 | <span data-ttu-id="2f375-111">Description</span><span class="sxs-lookup"><span data-stu-id="2f375-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="2f375-112">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="2f375-112">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="2f375-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="2f375-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2f375-114">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="2f375-114">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="2f375-115">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="2f375-115">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2f375-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2f375-116">Parent elements</span></span>



| <span data-ttu-id="2f375-117">Élément</span><span class="sxs-lookup"><span data-stu-id="2f375-117">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f375-118">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="2f375-118">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2f375-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="2f375-119">Remarks</span></span>

<span data-ttu-id="2f375-120">facultatif.</span><span class="sxs-lookup"><span data-stu-id="2f375-120">Optional.</span></span>

<span data-ttu-id="2f375-121">Peut se produire une ou plusieurs fois pour chaque élément [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="2f375-121">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="2f375-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="2f375-122">Examples</span></span>

<span data-ttu-id="2f375-123">L’exemple de code suivant illustre le balisage de base pour un modèle de disposition personnalisé à quatre boutons [**SizeDefinition**](windowsribbon-element-sizedefinition.md) avec différents éléments de **ligne** .</span><span class="sxs-lookup"><span data-stu-id="2f375-123">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **Row** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="2f375-124">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2f375-124">Element information</span></span>




* <span data-ttu-id="2f375-125">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f375-125">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="2f375-126">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="2f375-126">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="2f375-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f375-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f375-128">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="2f375-128">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





