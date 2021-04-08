---
title: Élément ControlNameMap
description: Représente un conteneur pour les noms de contrôles dans un modèle de disposition SizeDefinition personnalisé.
ms.assetid: b4bceb90-a9a3-42d7-a85b-bf6e4e02784b
keywords:
- Ruban des fenêtres d’élément ControlNameMap
topic_type:
- apiref
api_name:
- ControlNameMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ca5338978be7f9ddf3432cbe1a0fb8d243d8c00
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841302"
---
# <a name="controlnamemap-element"></a><span data-ttu-id="4fe93-104">Élément ControlNameMap</span><span class="sxs-lookup"><span data-stu-id="4fe93-104">ControlNameMap element</span></span>

<span data-ttu-id="4fe93-105">Représente un conteneur pour les noms de contrôles dans un modèle de disposition [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4fe93-105">Represents a container for control names in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="4fe93-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="4fe93-106">Usage</span></span>

``` syntax
<ControlNameMap>
  child elements
</ControlNameMap>
```

## <a name="attributes"></a><span data-ttu-id="4fe93-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="4fe93-107">Attributes</span></span>

<span data-ttu-id="4fe93-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="4fe93-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4fe93-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4fe93-109">Child elements</span></span>



| <span data-ttu-id="4fe93-110">Élément</span><span class="sxs-lookup"><span data-stu-id="4fe93-110">Element</span></span>                                                                                 | <span data-ttu-id="4fe93-111">Description</span><span class="sxs-lookup"><span data-stu-id="4fe93-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="4fe93-112">**ControlNameDefinition**</span><span class="sxs-lookup"><span data-stu-id="4fe93-112">**ControlNameDefinition**</span></span>](windowsribbon-element-controlnamedefinition.md)<br/> | <span data-ttu-id="4fe93-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="4fe93-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="4fe93-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4fe93-114">Parent elements</span></span>



| <span data-ttu-id="4fe93-115">Élément</span><span class="sxs-lookup"><span data-stu-id="4fe93-115">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="4fe93-116">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="4fe93-116">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4fe93-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4fe93-117">Remarks</span></span>

<span data-ttu-id="4fe93-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4fe93-118">Optional.</span></span>

<span data-ttu-id="4fe93-119">Peut se produire au plus une fois pour chaque élément [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe93-119">May occur at most once for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="4fe93-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="4fe93-120">Examples</span></span>

<span data-ttu-id="4fe93-121">L’exemple de code suivant illustre le balisage de base pour un modèle de disposition personnalisé à quatre boutons [**SizeDefinition**](windowsribbon-element-sizedefinition.md) avec un élément **ControlNameMap** .</span><span class="sxs-lookup"><span data-stu-id="4fe93-121">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with a **ControlNameMap** element.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="4fe93-122">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4fe93-122">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="4fe93-123">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fe93-123">Minimum supported system</span></span><br/> | <span data-ttu-id="4fe93-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4fe93-124">Windows 7</span></span> |
| <span data-ttu-id="4fe93-125">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="4fe93-125">Can be empty</span></span>                        | <span data-ttu-id="4fe93-126">Non</span><span class="sxs-lookup"><span data-stu-id="4fe93-126">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="4fe93-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fe93-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe93-128">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="4fe93-128">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





