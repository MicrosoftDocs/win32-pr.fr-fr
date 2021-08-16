---
title: Élément ControlGroup
description: Représente un groupe de contrôles dans un modèle de disposition SizeDefinition.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- élément ControlGroup Windows ruban
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1777bd469b6bf07530881f9c20888d69fe98117ecbdeba4f3f5557f01ced172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117851025"
---
# <a name="controlgroup-element"></a>Élément ControlGroup

Représente un groupe de contrôles dans un modèle de disposition [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

## <a name="usage"></a>Usage

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
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
<td><strong>SequenceNumber</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Non<br/></td>
<td>Valide uniquement lorsque <a href="windowsribbon-element-group.md"><strong>Group</strong></a> est l’élément parent.<br/> Chaque <em>élément</em> de la variable doit être unique au sein d’un élément de <a href="windowsribbon-element-group.md"><strong>groupe</strong></a> . Les valeurs de l’élément de <em>tâche doivent augmenter</em> pour chaque élément de <strong>groupe</strong> , mais n’ont pas besoin d’être séquentielles. <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)<br/> </dt> <dd> Toute valeur entière positive comprise entre 1000 et 59999 inclus.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                 | Description                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                               | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**Activé**](windowsribbon-element-checkbox.md)<br/>                           | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                           | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>               | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/>     | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>             | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                     | Peut se produire au plus une fois<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>             | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                             | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                     | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>       | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                   | Peut se produire une ou plusieurs fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                             |
|-------------------------------------------------------------------------------------|
| **ControlGroup**<br/>                                                         |
| [**Groupe**](windowsribbon-element-group.md)<br/>                             |
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> |
| [**Ligne**](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a>Remarques

Facultatif.

Peut se produire une ou plusieurs fois pour chaque élément [**Group**](windowsribbon-element-group.md) ou **ControlGroup** .

Si aucun numéro de séquence n’est fourni, les éléments sont rendus dans l’ordre spécifié dans le balisage du ruban.

Si [**Group**](windowsribbon-element-group.md) ou **ControlGroup** est l’élément parent, **ControlGroup** est imposé aux éléments enfants possibles suivants : [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md)

Dans le cas contraire, lorsque [**Row**](windowsribbon-element-row.md) ou [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) est le parent, le [**groupe**](windowsribbon-element-group.md) est soumis à l’élément enfant possible suivant : [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).

## <a name="examples"></a>Exemples

L’exemple de code suivant illustre le balisage de base pour un modèle de disposition personnalisé à quatre boutons [**SizeDefinition**](windowsribbon-element-sizedefinition.md) avec différents éléments de [**groupe**](windowsribbon-element-group.md) .


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

* **système minimal pris en charge**: Windows 7
* **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md)
</dt> </dl>

 

 





