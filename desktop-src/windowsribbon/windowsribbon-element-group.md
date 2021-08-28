---
title: élément Group
description: Représente un contrôle de groupe qui fonctionne comme un conteneur pour un groupe d’éléments.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- élément de groupe Windows ruban
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86d12ddb781ecf7e1effba1cade8eb00e92fe20b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631367"
---
# <a name="group-element"></a>élément Group

Représente un contrôle de [groupe](windowsribbon-controls-group.md) qui fonctionne comme un conteneur pour un groupe d’éléments.

## <a name="usage"></a>Utilisation

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
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
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne qui contient une liste d’entiers séparés par des virgules, comprise entre 0 et 31.<br/> L’espace blanc est valide et ignoré.<br/> Longueur maximale : 250 caractères. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS : positiveInteger ou XS : String<br/></td>
<td>No<br/></td>
<td>Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)<br/> </dt> <dd> Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus. <br/> La valeur doit être unique dans le document XML du ruban. <br/> Longueur maximale : 100 caractères. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>SizeDefinition</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Lorsqu’il est spécifié, la valeur de <em>SizeDefinition</em> est limitée à l’un des <a href="windowsribbon-templates.md">modèles de disposition</a> définis par l’infrastructure du ruban. <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Toute séquence de zéro ou plusieurs caractères.<br/> La longueur maximale est illimitée.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                             | Description                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>               | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Peut se produire au plus une fois<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>         | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/>           | Peut se produire au plus une fois<br/> <br/>      |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                         | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Peut se produire une ou plusieurs fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                             |
|-----------------------------------------------------|
| [**Onglet**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Remarques

Optionnel.

Peut se produire une ou plusieurs fois pour chaque élément [**Tab**](windowsribbon-element-tab.md) .

L' [**onglet**](windowsribbon-element-tab.md) prend en charge les [modes d’application](ribbon-applicationmodes.md).

Le balisage du ruban est valide uniquement lorsque les éléments enfants du **groupe** correspondent au modèle spécifié pour *SizeDefinition*.

## <a name="examples"></a>Exemples

L’exemple de code suivant illustre l’utilisation d’un modèle personnalisé dans un **groupe**.


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a>Informations sur les éléments

* **système minimal pris en charge**: Windows 7
* **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md)
</dt> <dt>

[Contrôle de groupe](windowsribbon-controls-group.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

