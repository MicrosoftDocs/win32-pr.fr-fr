---
title: ScalingPolicy. IdealSizes, propriété
description: Représente un conteneur de spécifications de mise à l’échelle pour le modèle SizeDefinition préféré, en fonction de la taille du ruban.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- Ruban Windows de la propriété ScalingPolicy. IdealSizes
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bf62cd0388b523f444c4a9cca226b58187212b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509742"
---
# <a name="scalingpolicyidealsizes-property"></a><span data-ttu-id="81639-104">ScalingPolicy. IdealSizes, propriété</span><span class="sxs-lookup"><span data-stu-id="81639-104">ScalingPolicy.IdealSizes property</span></span>

<span data-ttu-id="81639-105">Représente un conteneur de spécifications de mise à l’échelle pour le modèle [**SizeDefinition**](windowsribbon-element-sizedefinition.md) préféré, en fonction de la taille du ruban.</span><span class="sxs-lookup"><span data-stu-id="81639-105">Represents a container of scaling specifications for the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template, based on Ribbon size.</span></span>

## <a name="usage"></a><span data-ttu-id="81639-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="81639-106">Usage</span></span>

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a><span data-ttu-id="81639-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="81639-107">Attributes</span></span>

<span data-ttu-id="81639-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="81639-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="81639-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="81639-109">Child elements</span></span>



| <span data-ttu-id="81639-110">Élément</span><span class="sxs-lookup"><span data-stu-id="81639-110">Element</span></span>                                                 | <span data-ttu-id="81639-111">Description</span><span class="sxs-lookup"><span data-stu-id="81639-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="81639-112">**Scale**</span><span class="sxs-lookup"><span data-stu-id="81639-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/> | <span data-ttu-id="81639-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="81639-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="81639-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="81639-114">Parent elements</span></span>



| <span data-ttu-id="81639-115">Élément</span><span class="sxs-lookup"><span data-stu-id="81639-115">Element</span></span>                                                                 |
|-------------------------------------------------------------------------|
| [<span data-ttu-id="81639-116">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="81639-116">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="81639-117">Notes</span><span class="sxs-lookup"><span data-stu-id="81639-117">Remarks</span></span>

<span data-ttu-id="81639-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="81639-118">Optional.</span></span>

<span data-ttu-id="81639-119">Peut se produire au plus une fois pour chaque [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="81639-119">May occur at most once for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).</span></span>

<span data-ttu-id="81639-120">Si **ScalingPolicy. IdealSizes** est défini, une entrée de mise à l' [**échelle**](windowsribbon-element-scale.md) pour chaque élément de [**groupe**](windowsribbon-element-group.md) dans un élément de [**tabulation**](windowsribbon-element-tab.md) doit être présente.</span><span class="sxs-lookup"><span data-stu-id="81639-120">If **ScalingPolicy.IdealSizes** is defined, then a [**Scale**](windowsribbon-element-scale.md) entry for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element must be present.</span></span>

<span data-ttu-id="81639-121">**ScalingPolicy. IdealSizes** sont les dispositions de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) préférées pour un [**groupe**](windowsribbon-element-group.md) de contrôles.</span><span class="sxs-lookup"><span data-stu-id="81639-121">**ScalingPolicy.IdealSizes** are the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layouts for a [**Group**](windowsribbon-element-group.md) of controls.</span></span>

## <a name="examples"></a><span data-ttu-id="81639-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="81639-122">Examples</span></span>

<span data-ttu-id="81639-123">L’exemple suivant montre comment personnaliser l’apparence des contrôles dans un [**groupe**](windowsribbon-element-group.md) à l’aide de la fonctionnalité de disposition adaptative des modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de ruban.</span><span class="sxs-lookup"><span data-stu-id="81639-123">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="81639-124">Le manifeste [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) dans cet exemple spécifie une préférence **ScalingPolicy. IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pour chacun des quatre groupes de contrôles sur un onglet de **démarrage** . En outre, les éléments de mise à l' [**échelle**](windowsribbon-element-scale.md) sont spécifiés pour influencer le comportement de réduction, dans l’ordre de la taille décroissant, de chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="81639-124">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a **ScalingPolicy.IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
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



## <a name="requirements"></a><span data-ttu-id="81639-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81639-125">Requirements</span></span>



| <span data-ttu-id="81639-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81639-126">Requirement</span></span> | <span data-ttu-id="81639-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="81639-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="81639-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81639-128">Minimum supported client</span></span><br/> | <span data-ttu-id="81639-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81639-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="81639-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81639-130">Minimum supported server</span></span><br/> | <span data-ttu-id="81639-131">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81639-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81639-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81639-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81639-133">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="81639-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





