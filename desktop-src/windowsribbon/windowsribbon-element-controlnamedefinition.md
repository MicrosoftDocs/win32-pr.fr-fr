---
title: Élément ControlNameDefinition
description: Représente le nom d’un contrôle dans un modèle de disposition SizeDefinition personnalisé.
ms.assetid: 94b724bd-a4e3-40e0-9cf0-3cc6a71100d2
keywords:
- Ruban des fenêtres d’élément ControlNameDefinition
topic_type:
- apiref
api_name:
- ControlNameDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14ec269ce51b0074b9a03f78aea218b482955d1b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312664"
---
# <a name="controlnamedefinition-element"></a><span data-ttu-id="759c9-104">Élément ControlNameDefinition</span><span class="sxs-lookup"><span data-stu-id="759c9-104">ControlNameDefinition element</span></span>

<span data-ttu-id="759c9-105">Représente le nom d’un contrôle dans un modèle de disposition [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personnalisé.</span><span class="sxs-lookup"><span data-stu-id="759c9-105">Represents a name of a control in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="759c9-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="759c9-106">Usage</span></span>

``` syntax
<ControlNameDefinition
  Name = "xs:positiveInteger or xs:string">
  child elements
</ControlNameDefinition>
```

## <a name="attributes"></a><span data-ttu-id="759c9-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="759c9-107">Attributes</span></span>



| <span data-ttu-id="759c9-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="759c9-108">Attribute</span></span>           | <span data-ttu-id="759c9-109">Type</span><span class="sxs-lookup"><span data-stu-id="759c9-109">Type</span></span>                                       | <span data-ttu-id="759c9-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="759c9-110">Required</span></span>      | <span data-ttu-id="759c9-111">Description</span><span class="sxs-lookup"><span data-stu-id="759c9-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------|--------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="759c9-112">**Nom**</span><span class="sxs-lookup"><span data-stu-id="759c9-112">**Name**</span></span><br/> | <span data-ttu-id="759c9-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="759c9-113">xs:positiveInteger or xs:string</span></span><br/> | <span data-ttu-id="759c9-114">Non</span><span class="sxs-lookup"><span data-stu-id="759c9-114">No</span></span><br/> | <span data-ttu-id="759c9-115"><dt> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="759c9-115"><dt> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="759c9-116">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="759c9-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="759c9-117">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="759c9-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="759c9-118">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="759c9-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="759c9-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="759c9-119">Child elements</span></span>



| <span data-ttu-id="759c9-120">Élément</span><span class="sxs-lookup"><span data-stu-id="759c9-120">Element</span></span>                              | <span data-ttu-id="759c9-121">Description</span><span class="sxs-lookup"><span data-stu-id="759c9-121">Description</span></span>                                        |
|--------------------------------------|----------------------------------------------------|
| <span data-ttu-id="759c9-122">**ControlNameDefinition**</span><span class="sxs-lookup"><span data-stu-id="759c9-122">**ControlNameDefinition**</span></span><br/> | <span data-ttu-id="759c9-123">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="759c9-123">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="759c9-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="759c9-124">Parent elements</span></span>



| <span data-ttu-id="759c9-125">Élément</span><span class="sxs-lookup"><span data-stu-id="759c9-125">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="759c9-126">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="759c9-126">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="759c9-127">Notes</span><span class="sxs-lookup"><span data-stu-id="759c9-127">Remarks</span></span>

<span data-ttu-id="759c9-128">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="759c9-128">Optional.</span></span>

<span data-ttu-id="759c9-129">Peut se produire une ou plusieurs fois pour chaque élément [**ControlNameMap**](windowsribbon-element-controlnamemap.md) .</span><span class="sxs-lookup"><span data-stu-id="759c9-129">May occur one or more times for each [**ControlNameMap**](windowsribbon-element-controlnamemap.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="759c9-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="759c9-130">Examples</span></span>

<span data-ttu-id="759c9-131">L’exemple de code suivant illustre le balisage de base pour un modèle de disposition personnalisé à quatre boutons [**SizeDefinition**](windowsribbon-element-sizedefinition.md) avec quatre éléments **ControlNameDefinition** .</span><span class="sxs-lookup"><span data-stu-id="759c9-131">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with four **ControlNameDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="759c9-132">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="759c9-132">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="759c9-133">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="759c9-133">Minimum supported system</span></span><br/> | <span data-ttu-id="759c9-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="759c9-134">Windows 7</span></span> |
| <span data-ttu-id="759c9-135">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="759c9-135">Can be empty</span></span>                        | <span data-ttu-id="759c9-136">Non</span><span class="sxs-lookup"><span data-stu-id="759c9-136">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="759c9-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="759c9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="759c9-138">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="759c9-138">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





