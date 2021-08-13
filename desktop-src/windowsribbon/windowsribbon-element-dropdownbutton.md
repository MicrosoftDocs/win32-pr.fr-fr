---
title: Élément DropDownButton
description: Représente un contrôle de bouton de Drop-Down standard.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- élément DropDownButton Windows ruban
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3275e6de398c42d29424b2a1f9b0c750989357ef21c10d5db1e1680e7adb0836
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707267"
---
# <a name="dropdownbutton-element"></a>Élément DropDownButton

Représente un contrôle de [bouton](windowsribbon-controls-dropdownbutton.md) déroulant standard.

## <a name="usage"></a>Usage

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Valide uniquement si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> est l’élément parent.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne qui contient une liste d’entiers séparés par des virgules, comprise entre 0 et 31.<br/> L’espace blanc est valide et ignoré.<br/> Longueur maximale : 250 caractères. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS : positiveInteger ou XS : String<br/></td>
<td>Non<br/></td>
<td>Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)<br/> </dt> <dd> Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus. <br/> La valeur doit être unique dans le document XML du ruban. <br/> Longueur maximale : 100 caractères. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                             | Description                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**Activé**](windowsribbon-element-checkbox.md)<br/>                       | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Peut se produire une ou plusieurs fois<br/> <br/> |
| **DropDownButton**<br/>                                                       | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                     | Doit se produire au moins une fois<br/> <br/>    |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Peut se produire une ou plusieurs fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| **DropDownButton**<br/>                                                     |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Groupe**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Remarques

Facultatif ou obligatoire, en fonction de l’élément parent.

Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

**DropDownButton** prend en charge les [modes d’application](ribbon-applicationmodes.md) lorsqu’il est hébergé dans la colonne de gauche du menu de l’application.

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) et [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) ne sont pas des éléments enfants valides de **DropDownButton** lorsque **DropDownButton** est un descendant de [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour **DropDownButton**.

Cette section de code montre les déclarations de commande **DropDownButton** , avec un [**groupe**](windowsribbon-element-group.md) associé qui fonctionne comme conteneur parent de l’élément **DropDownButton** .


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



Cette section de code montre les déclarations de contrôle **DropDownButton** .


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a>Informations sur les éléments

* **système minimal pris en charge**: Windows 7
* **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de bouton déroulant](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

