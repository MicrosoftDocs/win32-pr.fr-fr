---
title: Élément SplitButton
description: Représente un contrôle de bouton partagé standard.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- élément SplitButton Windows ruban
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07bc97a3c75a16c1a11783a13514a8ab5b3478c6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622735"
---
# <a name="splitbutton-element"></a>Élément SplitButton

Représente un contrôle de [bouton partagé](windowsribbon-controls-splitbutton.md) standard.

## <a name="usage"></a>Utilisation

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
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
<td>Valide uniquement si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> est l’élément parent.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne qui contient une liste d’entiers séparés par des virgules, comprise entre 0 et 31.<br/> L’espace blanc est valide et ignoré.<br/> Longueur maximale : 250 caractères. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS : positiveInteger ou XS : String<br/></td>
<td>No<br/></td>
<td>Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)<br/> </dt> <dd> Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus. <br/> La valeur doit être unique dans le document XML du ruban. <br/> Longueur maximale : 100 caractères. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                   | Description                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                                 | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                             | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                 | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/>       | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>               | Peut se produire une ou plusieurs fois<br/> <br/> |
| **SplitButton**<br/>                                                                | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md)<br/> | Peut se produire au plus une fois<br/> <br/>      |
| [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)<br/> | Peut se produire au plus une fois<br/> <br/>      |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>         | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                     | Peut se produire une ou plusieurs fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Groupe**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| **SplitButton**<br/>                                                        |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Remarques

Optionnel.

Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton** ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

**SplitButton** prend en charge les [modes d’application](ribbon-applicationmodes.md) lorsqu’il est hébergé dans la colonne de gauche du menu de l’application.

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) et [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) ne sont pas des éléments enfants valides de [**DropDownButton**](windowsribbon-element-dropdownbutton.md) lorsque **DropDownButton** est un descendant de [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).

[**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) doit se produire une seule fois si les éléments suivants ne sont pas présents en tant qu’éléments enfants de **SplitButton**:

-   [**Bouton**](windowsribbon-element-button.md)
-   [**CheckBox**](windowsribbon-element-checkbox.md)
-   [**DropDownButton**](windowsribbon-element-dropdownbutton.md)
-   [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)
-   [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)
-   **SplitButton**
-   [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)
-   [**ToggleButton**](windowsribbon-element-togglebutton.md)

Ces contrôles sont traités comme des éléments enfants d’un seul élément [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) par défaut.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour le [bouton partagé](windowsribbon-controls-splitbutton.md).

Cette section de code montre les déclarations de commande **SplitButton** , avec un [**groupe**](windowsribbon-element-group.md) associé qui fonctionne comme conteneur parent pour l’élément **SplitButton** .


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



Cette section de code montre les déclarations de contrôle **SplitButton** .


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

- **système minimal pris en charge**: Windows 7 
- **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de bouton partagé](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

