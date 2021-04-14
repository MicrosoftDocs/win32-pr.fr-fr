---
title: Propriété Tab. ScalingPolicy
description: Représente un conteneur pour les spécifications de mise à l’échelle des onglets.
ms.assetid: cc1e4a35-9348-459b-a2f1-25c34d49e5e8
keywords:
- Ruban Windows de la propriété Tab. ScalingPolicy
topic_type:
- apiref
api_name:
- Tab.ScalingPolicy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46528e7b5957415db55f1a51dd6dafed7e1da98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466567"
---
# <a name="tabscalingpolicy-property"></a><span data-ttu-id="4ecc4-104">Propriété Tab. ScalingPolicy</span><span class="sxs-lookup"><span data-stu-id="4ecc4-104">Tab.ScalingPolicy property</span></span>

<span data-ttu-id="4ecc4-105">Représente un conteneur pour les spécifications de mise à l’échelle des [onglets](windowsribbon-controls-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="4ecc4-105">Represents a container for [Tab](windowsribbon-controls-tab.md) scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="4ecc4-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="4ecc4-106">Usage</span></span>

``` syntax
<Tab.ScalingPolicy>
  child elements
</Tab.ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="4ecc4-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="4ecc4-107">Attributes</span></span>

<span data-ttu-id="4ecc4-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="4ecc4-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4ecc4-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4ecc4-109">Child elements</span></span>



| <span data-ttu-id="4ecc4-110">Élément</span><span class="sxs-lookup"><span data-stu-id="4ecc4-110">Element</span></span>                                                                 | <span data-ttu-id="4ecc4-111">Description</span><span class="sxs-lookup"><span data-stu-id="4ecc4-111">Description</span></span>                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="4ecc4-112">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="4ecc4-112">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> | <span data-ttu-id="4ecc4-113">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="4ecc4-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="4ecc4-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4ecc4-114">Parent elements</span></span>



| <span data-ttu-id="4ecc4-115">Élément</span><span class="sxs-lookup"><span data-stu-id="4ecc4-115">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="4ecc4-116">**Onglet**</span><span class="sxs-lookup"><span data-stu-id="4ecc4-116">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4ecc4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4ecc4-117">Remarks</span></span>

<span data-ttu-id="4ecc4-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4ecc4-118">Optional.</span></span>

<span data-ttu-id="4ecc4-119">Peut se produire au plus une fois pour chaque [**onglet**](windowsribbon-element-tab.md).</span><span class="sxs-lookup"><span data-stu-id="4ecc4-119">May occur at most once for each [**Tab**](windowsribbon-element-tab.md).</span></span>

<span data-ttu-id="4ecc4-120">Les spécifications de mise à l’échelle décrivent le comportement de la taille et de la disposition des contrôles dans un [onglet](windowsribbon-controls-tab.md) lorsque le ruban est redimensionné.</span><span class="sxs-lookup"><span data-stu-id="4ecc4-120">Scaling specifications describe the size and layout behavior for the controls in a [Tab](windowsribbon-controls-tab.md) when the Ribbon is resized.</span></span>

## <a name="examples"></a><span data-ttu-id="4ecc4-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="4ecc4-121">Examples</span></span>

<span data-ttu-id="4ecc4-122">L’exemple de code suivant montre un manifeste [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) qui spécifie une préférence [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pour chacun des quatre groupes de contrôles sur un onglet de **démarrage** . En outre, les éléments de mise à l' [**échelle**](windowsribbon-element-scale.md) sont spécifiés pour influencer le comportement de réduction, dans l’ordre de la taille décroissant, de chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="4ecc4-122">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4ecc4-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ecc4-123">Requirements</span></span>



| <span data-ttu-id="4ecc4-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ecc4-124">Requirement</span></span> | <span data-ttu-id="4ecc4-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ecc4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4ecc4-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ecc4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4ecc4-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ecc4-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4ecc4-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ecc4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4ecc4-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ecc4-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ecc4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ecc4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ecc4-131">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="4ecc4-131">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





