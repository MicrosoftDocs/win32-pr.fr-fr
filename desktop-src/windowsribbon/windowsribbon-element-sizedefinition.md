---
title: Élément SizeDefinition
description: Représente un modèle de disposition personnalisé de contrôles de ruban.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- Ruban des fenêtres d’élément SizeDefinition
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc68ac032459bed77d402ebd860886398748c874
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444800"
---
# <a name="sizedefinition-element"></a><span data-ttu-id="1a1ec-104">Élément SizeDefinition</span><span class="sxs-lookup"><span data-stu-id="1a1ec-104">SizeDefinition element</span></span>

<span data-ttu-id="1a1ec-105">Représente un modèle de disposition personnalisé de contrôles de ruban.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-105">Represents a custom layout template of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="1a1ec-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="1a1ec-106">Usage</span></span>

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="1a1ec-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="1a1ec-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a1ec-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="1a1ec-108">Attribute</span></span></th>
<th><span data-ttu-id="1a1ec-109">Type</span><span class="sxs-lookup"><span data-stu-id="1a1ec-109">Type</span></span></th>
<th><span data-ttu-id="1a1ec-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1a1ec-110">Required</span></span></th>
<th><span data-ttu-id="1a1ec-111">Description</span><span class="sxs-lookup"><span data-stu-id="1a1ec-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a1ec-112"><strong>Nom</strong></span><span class="sxs-lookup"><span data-stu-id="1a1ec-112"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="1a1ec-113">XS : positiveInteger ou XS : String ou XS : Token</span><span class="sxs-lookup"><span data-stu-id="1a1ec-113">xs:positiveInteger or xs:string or xs:token</span></span><br/></td>
<td><span data-ttu-id="1a1ec-114">Oui</span><span class="sxs-lookup"><span data-stu-id="1a1ec-114">Yes</span></span><br/></td>
<td><span data-ttu-id="1a1ec-115">Lorsque <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon. SizeDefinitions</strong></a> est le parent, sinon facultatif.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-115">When <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> is the parent, otherwise optional.</span></span><br/> <br/><span data-ttu-id="1a1ec-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String ou XS : Token)</span><span class="sxs-lookup"><span data-stu-id="1a1ec-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string or xs:token)</span></span><br/> </dt> <dd> <span data-ttu-id="1a1ec-117">Chaîne ou valeur entière comprise entre 2 et 59999, inclusive ou 0X2 et 0xea5f en hexadécimal, inclus.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="1a1ec-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="1a1ec-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="1a1ec-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1a1ec-120">Child elements</span></span>



| <span data-ttu-id="1a1ec-121">Élément</span><span class="sxs-lookup"><span data-stu-id="1a1ec-121">Element</span></span>                                                                             | <span data-ttu-id="1a1ec-122">Description</span><span class="sxs-lookup"><span data-stu-id="1a1ec-122">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="1a1ec-123">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="1a1ec-123">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/>           | <span data-ttu-id="1a1ec-124">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="1a1ec-124">May occur at most once</span></span><br/> <br/>   |
| [<span data-ttu-id="1a1ec-125">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="1a1ec-125">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> | <span data-ttu-id="1a1ec-126">Doit se produire au moins une fois</span><span class="sxs-lookup"><span data-stu-id="1a1ec-126">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1a1ec-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1a1ec-127">Parent elements</span></span>



| <span data-ttu-id="1a1ec-128">Élément</span><span class="sxs-lookup"><span data-stu-id="1a1ec-128">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a1ec-129">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="1a1ec-129">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                   |
| [<span data-ttu-id="1a1ec-130">**Ruban. SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="1a1ec-130">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1a1ec-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a1ec-131">Remarks</span></span>

<span data-ttu-id="1a1ec-132">facultatif.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-132">Optional.</span></span>

<span data-ttu-id="1a1ec-133">Peut se produire au plus une fois pour chaque élément de [**groupe**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="1a1ec-133">May occur at most once for each [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="1a1ec-134">Peut se produire une ou plusieurs fois pour chaque élément [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="1a1ec-134">May occur one or more times for each [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="1a1ec-135">Les [modèles de disposition](windowsribbon-templates.md) de l’infrastructure du ruban prédéfinis sont spécifiés avec l’attribut *SizeDefinition* de l’élément [**Group**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="1a1ec-135">Predefined Ribbon framework [layout templates](windowsribbon-templates.md) are specified with the *SizeDefinition* attribute of the [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="1a1ec-136">Si un élément [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) correspondant n’est pas déclaré pour chaque élément de [**Groupe**](windowsribbon-element-group.md) dans un élément [**Tab**](windowsribbon-element-tab.md) , une erreur de validation se produit.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-136">If a corresponding [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) element is not declared for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element, a validation error will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="1a1ec-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="1a1ec-137">Examples</span></span>

<span data-ttu-id="1a1ec-138">L’exemple de code suivant illustre un modèle personnalisé de base.</span><span class="sxs-lookup"><span data-stu-id="1a1ec-138">The following code example illustrates a basic custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="1a1ec-139">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1a1ec-139">Element information</span></span>


- <span data-ttu-id="1a1ec-140">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="1a1ec-140">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="1a1ec-141">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="1a1ec-141">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="1a1ec-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a1ec-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a1ec-143">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="1a1ec-143">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





