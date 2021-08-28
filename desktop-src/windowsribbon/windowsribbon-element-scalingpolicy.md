---
title: Élément ScalingPolicy
description: Représente un conteneur pour la mise à l’échelle des spécifications.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- élément ScalingPolicy Windows ruban
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 202112a24a74c9b20d429910fd0ee9447002ce7f2cb95133165fb968eaaf4f69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007469"
---
# <a name="scalingpolicy-element"></a>Élément ScalingPolicy

Représente un conteneur pour la mise à l’échelle des spécifications.

## <a name="usage"></a>Usage

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                       | Description                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Scale**](windowsribbon-element-scale.md)<br/>                                       | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | Peut se produire au plus une fois<br/> <br/>      |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                         |
|---------------------------------------------------------------------------------|
| [**Tab. ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Remarques

Obligatoire.

Doit être exécutée une fois pour chaque [**Tab. ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).

L’élément **ScalingPolicy** contient un manifeste de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) et des déclarations de mise à l' [**échelle**](windowsribbon-element-scale.md) qui spécifient des préférences de disposition adaptative pour un ou plusieurs éléments de [**groupe**](windowsribbon-element-group.md) lorsque le ruban est redimensionné.

La liste des déclarations d' [**échelle**](windowsribbon-element-scale.md) doit être dans l’ordre décroissant des tailles valides (grande, moyenne, petite, contextuelle) pour le [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associé à l’élément de [**groupe**](windowsribbon-element-group.md) .

> [!Note]  
> Il est fortement recommandé de spécifier des détails de stratégie de mise à l’échelle adéquats de sorte qu’un ruban puisse s’afficher sans barres de défilement lorsqu’il est redimensionné à une largeur de 300 pixels à 96 points par pouce (dpi).

 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment personnaliser l’apparence des contrôles dans un [**groupe**](windowsribbon-element-group.md) à l’aide de la fonctionnalité de disposition adaptative des modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de ruban.

Le manifeste **ScalingPolicy** dans cet exemple spécifie une préférence [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pour chacun des quatre groupes de contrôles sur un onglet de **démarrage** . En outre, les éléments de mise à l' [**échelle**](windowsribbon-element-scale.md) sont spécifiés pour influencer le comportement de réduction, dans l’ordre de la taille décroissant, de chaque groupe.


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



## <a name="element-information"></a>Informations sur les éléments

- **système minimal pris en charge**: Windows 7 
- **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md)
</dt> </dl>

 

 





