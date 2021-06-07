---
title: Élément ComboBox
description: Représente un contrôle de zone de liste déroulante.
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- Ruban des fenêtres d’élément de ComboBox
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60ad8866b655be587e0c3d0f123d8bc59b6b8a21
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443580"
---
# <a name="combobox-element"></a>Élément ComboBox

Représente un contrôle de [zone de liste déroulante](windowsribbon-controls-combobox.md) .

## <a name="usage"></a>Utilisation

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
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
<td><strong>CommandName</strong><br/></td>
<td>XS : positiveInteger ou XS : String<br/></td>
<td>Non<br/></td>
<td>Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)<br/> </dt> <dd> Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus. <br/> La valeur doit être unique dans le document XML du ruban. <br/> Longueur maximale : 100 caractères. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsAutoCompleteEnabled</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd> Par défaut. <br/> </dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsEditable</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd> Par défaut. <br/> </dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ResizeType</strong><br/></td>
<td>ComboBoxResizeType<br/></td>
<td>Non<br/></td>
<td><dt><span></span><span></span><strong></strong> (NoResize)<br/> </dt> <dd> Par défaut. <br/> </dd> <dt><span></span><span></span><strong></strong> (VerticalResize)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Groupe</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 et versions ultérieures.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Remarques

facultatif.

Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

Étant donné que la **zone de liste déroulante** est exclusivement une galerie d’éléments, elle ne prend pas en charge les éléments de commande. C’est également le seul contrôle de galerie qui ne prend pas en charge un espace de commande (une collection de commandes qui sont déclarées dans le balisage et répertoriées en bas d’une galerie d’éléments ou d’une bibliothèque de commandes). Pour plus d’informations, consultez [utilisation des galeries](ribbon-controls-galleries.md).

La capture d’écran suivante illustre un contrôle de [zone de liste déroulante](windowsribbon-controls-combobox.md) du ruban à partir de Windows Live Movie Maker.

![capture d’écran d’un contrôle de zone de liste déroulante dans le ruban Microsoft Paint.](images/controls/combobox.png)

## <a name="examples"></a>Exemples

Les exemples suivants illustrent le balisage de base de la **zone de liste déroulante**.

Cette section de code montre les déclarations de commande de **liste déroulante** , avec un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément de **zone de liste déroulante** .


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```



Cette section de code montre les déclarations de contrôle de **zone de liste déroulante** .


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a>Informations sur les éléments

* **Système minimal pris en charge**: Windows 7
* **Peut être vide**: Oui



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle Combo Box](windowsribbon-controls-combobox.md)
</dt> <dt>

[Exemple de Galerie](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





