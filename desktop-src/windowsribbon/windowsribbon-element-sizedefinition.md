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
# <a name="sizedefinition-element"></a>Élément SizeDefinition

Représente un modèle de disposition personnalisé de contrôles de ruban.

## <a name="usage"></a>Utilisation

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
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
<td><strong>Nom</strong><br/></td>
<td>XS : positiveInteger ou XS : String ou XS : Token<br/></td>
<td>Oui<br/></td>
<td>Lorsque <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon. SizeDefinitions</strong></a> est le parent, sinon facultatif.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String ou XS : Token)<br/> </dt> <dd> Chaîne ou valeur entière comprise entre 2 et 59999, inclusive ou 0X2 et 0xea5f en hexadécimal, inclus. <br/> La valeur doit être unique dans le document XML du ruban. <br/> Longueur maximale : 100 caractères. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                             | Description                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [**ControlNameMap**](windowsribbon-element-controlnamemap.md)<br/>           | Peut se produire au plus une fois<br/> <br/>   |
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> | Doit se produire au moins une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                                   |
|-------------------------------------------------------------------------------------------|
| [**Groupe**](windowsribbon-element-group.md)<br/>                                   |
| [**Ruban. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a>Remarques

facultatif.

Peut se produire au plus une fois pour chaque élément de [**groupe**](windowsribbon-element-group.md) .

Peut se produire une ou plusieurs fois pour chaque élément [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .

Les [modèles de disposition](windowsribbon-templates.md) de l’infrastructure du ruban prédéfinis sont spécifiés avec l’attribut *SizeDefinition* de l’élément [**Group**](windowsribbon-element-group.md) .

Si un élément [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) correspondant n’est pas déclaré pour chaque élément de [**Groupe**](windowsribbon-element-group.md) dans un élément [**Tab**](windowsribbon-element-tab.md) , une erreur de validation se produit.

## <a name="examples"></a>Exemples

L’exemple de code suivant illustre un modèle personnalisé de base.


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



## <a name="element-information"></a>Informations sur les éléments


- **Système minimal pris en charge**: Windows 7 
- **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md)
</dt> </dl>

 

 





