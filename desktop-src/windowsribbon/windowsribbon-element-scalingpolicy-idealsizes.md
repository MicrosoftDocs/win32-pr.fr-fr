---
title: ScalingPolicy. IdealSizes, propriété
description: Représente un conteneur de spécifications de mise à l’échelle pour le modèle SizeDefinition préféré, en fonction de la taille du ruban.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- ScalingPolicy. IdealSizes, propriété Windows ruban
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500f6193411ed72b8858506816d9af4f82b1219680fa0537bf54b3daa7735211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439524"
---
# <a name="scalingpolicyidealsizes-property"></a>ScalingPolicy. IdealSizes, propriété

Représente un conteneur de spécifications de mise à l’échelle pour le modèle [**SizeDefinition**](windowsribbon-element-sizedefinition.md) préféré, en fonction de la taille du ruban.

## <a name="usage"></a>Usage

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                 | Description                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Scale**](windowsribbon-element-scale.md)<br/> | Peut se produire une ou plusieurs fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                 |
|-------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Remarques

Facultatif.

Peut se produire au plus une fois pour chaque [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).

Si **ScalingPolicy. IdealSizes** est défini, une entrée de mise à l' [**échelle**](windowsribbon-element-scale.md) pour chaque élément de [**groupe**](windowsribbon-element-group.md) dans un élément de [**tabulation**](windowsribbon-element-tab.md) doit être présente.

**ScalingPolicy. IdealSizes** sont les dispositions de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) préférées pour un [**groupe**](windowsribbon-element-group.md) de contrôles.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment personnaliser l’apparence des contrôles dans un [**groupe**](windowsribbon-element-group.md) à l’aide de la fonctionnalité de disposition adaptative des modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de ruban.

Le manifeste [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) dans cet exemple spécifie une préférence **ScalingPolicy. IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pour chacun des quatre groupes de contrôles sur un onglet de **démarrage** . En outre, les éléments de mise à l' [**échelle**](windowsribbon-element-scale.md) sont spécifiés pour influencer le comportement de réduction, dans l’ordre de la taille décroissant, de chaque groupe.


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

 

 





