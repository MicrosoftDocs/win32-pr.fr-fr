---
title: Élément ScalingPolicy
description: Représente un conteneur pour la mise à l’échelle des spécifications.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- Ruban des fenêtres d’élément ScalingPolicy
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 812256b0ff329073eb516c6ab2eb7501db8de40d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444990"
---
# <a name="scalingpolicy-element"></a><span data-ttu-id="7c05a-104">Élément ScalingPolicy</span><span class="sxs-lookup"><span data-stu-id="7c05a-104">ScalingPolicy element</span></span>

<span data-ttu-id="7c05a-105">Représente un conteneur pour la mise à l’échelle des spécifications.</span><span class="sxs-lookup"><span data-stu-id="7c05a-105">Represents a container for scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="7c05a-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="7c05a-106">Usage</span></span>

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="7c05a-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="7c05a-107">Attributes</span></span>

<span data-ttu-id="7c05a-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="7c05a-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7c05a-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7c05a-109">Child elements</span></span>



| <span data-ttu-id="7c05a-110">Élément</span><span class="sxs-lookup"><span data-stu-id="7c05a-110">Element</span></span>                                                                                       | <span data-ttu-id="7c05a-111">Description</span><span class="sxs-lookup"><span data-stu-id="7c05a-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="7c05a-112">**Mise à l’échelle**</span><span class="sxs-lookup"><span data-stu-id="7c05a-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/>                                       | <span data-ttu-id="7c05a-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="7c05a-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="7c05a-114">**ScalingPolicy.IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="7c05a-114">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | <span data-ttu-id="7c05a-115">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="7c05a-115">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="7c05a-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7c05a-116">Parent elements</span></span>



| <span data-ttu-id="7c05a-117">Élément</span><span class="sxs-lookup"><span data-stu-id="7c05a-117">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="7c05a-118">**Tab. ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="7c05a-118">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7c05a-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="7c05a-119">Remarks</span></span>

<span data-ttu-id="7c05a-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7c05a-120">Required.</span></span>

<span data-ttu-id="7c05a-121">Doit être exécutée une fois pour chaque [**Tab. ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="7c05a-121">Must occur once for each [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span></span>

<span data-ttu-id="7c05a-122">L’élément **ScalingPolicy** contient un manifeste de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) et des déclarations de mise à l' [**échelle**](windowsribbon-element-scale.md) qui spécifient des préférences de disposition adaptative pour un ou plusieurs éléments de [**groupe**](windowsribbon-element-group.md) lorsque le ruban est redimensionné.</span><span class="sxs-lookup"><span data-stu-id="7c05a-122">The **ScalingPolicy** element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

<span data-ttu-id="7c05a-123">La liste des déclarations d' [**échelle**](windowsribbon-element-scale.md) doit être dans l’ordre décroissant des tailles valides (grande, moyenne, petite, contextuelle) pour le [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associé à l’élément de [**groupe**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="7c05a-123">The list of [**Scale**](windowsribbon-element-scale.md) declarations must be in descending order of valid sizes (Large, Medium, Small, Popup) for the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associated with the [**Group**](windowsribbon-element-group.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="7c05a-124">Il est fortement recommandé de spécifier des détails de stratégie de mise à l’échelle adéquats de sorte qu’un ruban puisse s’afficher sans barres de défilement lorsqu’il est redimensionné à une largeur de 300 pixels à 96 points par pouce (dpi).</span><span class="sxs-lookup"><span data-stu-id="7c05a-124">It is highly recommended that adequate scaling policy detail be specified such that a Ribbon is able to render without scroll bars when resized to a width of 300 pixels at 96 dots per inch (dpi).</span></span>

 

## <a name="examples"></a><span data-ttu-id="7c05a-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="7c05a-125">Examples</span></span>

<span data-ttu-id="7c05a-126">L’exemple suivant montre comment personnaliser l’apparence des contrôles dans un [**groupe**](windowsribbon-element-group.md) à l’aide de la fonctionnalité de disposition adaptative des modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de ruban.</span><span class="sxs-lookup"><span data-stu-id="7c05a-126">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="7c05a-127">Le manifeste **ScalingPolicy** dans cet exemple spécifie une préférence [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pour chacun des quatre groupes de contrôles sur un onglet de **démarrage** . En outre, les éléments de mise à l' [**échelle**](windowsribbon-element-scale.md) sont spécifiés pour influencer le comportement de réduction, dans l’ordre de la taille décroissant, de chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="7c05a-127">The **ScalingPolicy** manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="element-information"></a><span data-ttu-id="7c05a-128">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7c05a-128">Element information</span></span>

- <span data-ttu-id="7c05a-129">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c05a-129">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="7c05a-130">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="7c05a-130">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="7c05a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c05a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c05a-132">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="7c05a-132">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





