---
title: Élément MenuGroup
description: Représente un conteneur de contrôles à afficher dans une galerie, un menu ou une barre d’outils.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- Ruban des fenêtres d’élément MenuGroup
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95cbda43fe2f652888a7b84539752b5d671868c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442850"
---
# <a name="menugroup-element"></a>Élément MenuGroup

Représente un conteneur de contrôles à afficher dans une galerie, un menu ou une barre d’outils.

## <a name="usage"></a>Utilisation

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
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
<td><strong>Classe</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Spécifie la taille et le style de disposition des éléments dans l’interface utilisateur du menu.<br/> Une ressource d’image peut être fournie en deux tailles (grande et petite) et associée à l’élément dans le balisage à l’aide des éléments de propriété <a href="windowsribbon-element-command-largeimages.md"><strong>Command. LargeImages</strong></a> et <a href="windowsribbon-element-command-smallimages.md"><strong>Command. SmallImages</strong></a> . Si une seule image est fournie, l’infrastructure la redimensionne si nécessaire.<br/> Limité à l’une des valeurs suivantes :<br/> <br/>
<dt><span></span><span></span><strong></strong> (StandardItems)<br/> </dt> <dd> Par défaut. <br/> Style : petites images et texte en surbrillance.<br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <dt><span></span><span></span><strong></strong> (MajorItems)<br/> </dt> <dd> Style : grande image et texte en gras.<br/>
<blockquote>
[!Note]<br />
Si <strong>MenuGroup</strong> est un enfant de <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, l’attribut de <em>classe</em> est ignoré et un style <code>MajorItems</code> est appliqué par l’infrastructure.
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
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
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Peut se produire au plus une fois<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Peut se produire une ou plusieurs fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/>                             |
| [**ContextMenu**](windowsribbon-element-contextmenu.md)<br/>                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [**MiniToolbar**](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a>Remarques

Obligatoire.

Doit se produire au moins une fois pour chaque élément [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery. MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery. MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md)ou [**SplitButtonGallery. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) .

Si [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) est l’élément parent, **MenuGroup** est soumis aux éléments enfants suivants : [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).

Si [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery. MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery. MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)ou [**SplitButtonGallery. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) est l’élément parent, **MenuGroup** est alors soumis aux éléments enfants suivants : [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md).

Si [**MiniToolbar**](windowsribbon-element-minitoolbar.md) est l’élément parent, **MenuGroup** est soumis aux éléments enfants suivants : [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md).

L’attribut Class n’est pas requis quand [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) est l’élément parent. L’infrastructure applique une valeur de MajorItems pour l’attribut de classe.

Lorsque [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) est l’élément parent, l’attribut de classe n’est pas requis.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour le [**SplitButton**](windowsribbon-element-splitbutton.md) avec un élément **MenuGroup** .

Cette section de code montre les déclarations de commande [**SplitButton**](windowsribbon-element-splitbutton.md) et **MenuGroup** avec une grande ressource d’image. Un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **SplitButton** est également déclaré.


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



Cette section de code montre les déclarations de contrôle [**SplitButton**](windowsribbon-element-splitbutton.md) et **MenuGroup** avec `StandardItems` et `MajorItems` .


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a>Informations sur les éléments

* **Système minimal pris en charge**: Windows 7
* **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Spécification des ressources d’image du ruban](windowsribbon-imageformats.md)
</dt> <dt>

[Groupe de menus](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





