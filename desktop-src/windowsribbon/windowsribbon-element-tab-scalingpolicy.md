---
title: Propriété Tab. ScalingPolicy
description: Représente un conteneur pour les spécifications de mise à l’échelle des onglets.
ms.assetid: cc1e4a35-9348-459b-a2f1-25c34d49e5e8
keywords:
- propriété Tab. ScalingPolicy Windows ruban
topic_type:
- apiref
api_name:
- Tab.ScalingPolicy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11b98174ff5c3426a4805905f0aa7ada86d63a644f4245135bcede5c71d11e75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850794"
---
# <a name="tabscalingpolicy-property"></a>Propriété Tab. ScalingPolicy

Représente un conteneur pour les spécifications de mise à l’échelle des [onglets](windowsribbon-controls-tab.md) .

## <a name="usage"></a>Usage

``` syntax
<Tab.ScalingPolicy>
  child elements
</Tab.ScalingPolicy>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                 | Description                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/> | Doit se produire exactement une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                             |
|-----------------------------------------------------|
| [**Onglet**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Remarques

Facultatif.

Peut se produire au plus une fois pour chaque [**onglet**](windowsribbon-element-tab.md).

Les spécifications de mise à l’échelle décrivent le comportement de la taille et de la disposition des contrôles dans un [onglet](windowsribbon-controls-tab.md) lorsque le ruban est redimensionné.

## <a name="examples"></a>Exemples

L’exemple de code suivant montre un manifeste [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) qui spécifie une préférence [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pour chacun des quatre groupes de contrôles sur un onglet de **démarrage** . En outre, les éléments de mise à l' [**échelle**](windowsribbon-element-scale.md) sont spécifiés pour influencer le comportement de réduction, dans l’ordre de la taille décroissant, de chaque groupe.


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md)
</dt> </dl>

 

 





