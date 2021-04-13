---
title: Scale, élément
description: Représente la préférence de taille et de disposition d’un groupe de contrôles via une paire groupe, SizeDefinition.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Ruban Windows de l’élément de mise à l’échelle
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3832d36a48b330b036fa287499f9db387335f87b
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104381440"
---
# <a name="scale-element"></a>Scale, élément

Représente la préférence de taille et de disposition d’un [**groupe**](windowsribbon-element-group.md) de contrôles via une paire {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}.

## <a name="usage"></a>Utilisation

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Type</th>
<th>Obligatoire</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Groupe</strong><br/></td>
<td>XS : positiveInteger ou XS : String<br/></td>
<td>Oui<br/></td>
<td>Doit correspondre à un <em>CommandName</em>de <a href="windowsribbon-element-group.md"><strong>groupe</strong></a> existant.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)<br/> </dt> <dd> Chaîne ou valeur entière comprise entre 2 et 59999, inclusive ou 0X2 et 0xea5f en hexadécimal, inclus. <br/> La valeur doit être unique dans le document XML du ruban. <br/> Longueur maximale : 100 caractères. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Taille</strong><br/></td>
<td>xs:string<br/></td>
<td>Oui<br/></td>
<td>Cette valeur doit correspondre à l’une des tailles valides de l’attribut <em>SizeDefinition</em> du <a href="windowsribbon-element-group.md"><strong>groupe</strong></a> associé de contrôles spécifié dans <em>Group</em>. <br/> Limité à l’une des valeurs suivantes : <br/> <br/>
<dt><span></span><span></span><strong></strong> Messages<br/> </dt> <dd> Mise en page de contrôle identique à <code>Large</code> , mais hébergée dans un volet contextuel ou une liste déroulante.<br/> </dd> <dt><span></span><span></span><strong></strong> Small<br/> </dt> <dd> Petit modèle <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> .<br/> </dd> <dt><span></span><span></span><strong></strong> Médias<br/> </dt> <dd> Modèle de <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> moyen.<br/> </dd> <dt><span></span><span></span><strong></strong> Conséquent<br/> </dt> <dd> Modèle <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> volumineux.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a>Notes

Optionnel.

Peut se produire une ou plusieurs fois pour chaque [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) ou [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).

Chaque paire d’attributs (*Group*, *Size*) doit être unique.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment personnaliser l’apparence des contrôles dans un [**groupe**](windowsribbon-element-group.md) à l’aide de la fonctionnalité de disposition adaptative des modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de ruban.

Le manifeste [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) dans cet exemple spécifie une préférence [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pour chacun des quatre groupes de contrôles sur un onglet de **démarrage** . En outre, les éléments de mise à l' **échelle** sont spécifiés pour influencer le comportement de réduction, dans l’ordre de la taille décroissant, de chaque groupe.


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



|                                     |           |
|-------------------------------------|-----------|
| Système minimal pris en charge<br/> | Windows 7 |
| Peut être vide                        | Oui       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md)
</dt> </dl>

 

 





