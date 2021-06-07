---
title: Élément SplitButtonGallery
description: Représente un contrôle de Galerie de boutons partagés avec un menu déroulant basé sur la Galerie.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- Ruban des fenêtres d’élément SplitButtonGallery
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5f8767135b9472acba333b1cdfa6ab102e9b7f4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444830"
---
# <a name="splitbuttongallery-element"></a>Élément SplitButtonGallery

Représente un contrôle de [Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md) avec un menu déroulant basé sur la Galerie.

## <a name="usage"></a>Utilisation

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
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
<tr class="odd">
<td><strong>HasLargeItems</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Détermine si la ressource d’image de grande taille ou de petite taille de la commande est affichée dans le contrôle Gallery. <br/>
<blockquote>
[!Note]<br />
S’applique uniquement aux galeries où la valeur de l’attribut <em>type</em> est égale à <code>Command</code> .
</blockquote>
<br/> Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd> Par défaut. <br/> </dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>Non<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS : Integer)<br/> </dt> <dd> La valeur par défaut est -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>Non<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS : Integer)<br/> </dt> <dd> La valeur par défaut est -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>Non<br/></td>
<td>Limité à l’une des valeurs suivantes :<br/> <br/>
<dt><span></span><span></span><strong></strong> Ballon<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Cuir<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Gauche<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Éviter<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Approprié<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Coin<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Type</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Limité à l’une des valeurs suivantes :<br/> <br/>
<dt><span></span><span></span><strong></strong> Contenus<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Commandes<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                 | Description                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                                               | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**Activé**](windowsribbon-element-checkbox.md)<br/>                                           | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                     | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | Doit se produire exactement une fois<br/> <br/>     |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | Peut se produire au plus une fois<br/> <br/>      |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                                   | Peut se produire une ou plusieurs fois<br/> <br/> |



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
<td><a href="windowsribbon-element-group.md"><strong>Groupe</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a><br/></td>
<td>Lorsqu’il est contenu dans un <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>. Cet élément est uniquement pris en charge sur le premier niveau et ne doit pas avoir d’éléments enfants.<br/> <br/></td>
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
<td><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Remarques

facultatif.

Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)ou [**SplitButton**](windowsribbon-element-splitbutton.md) .

**SplitButtonGallery** prend en charge les [modes d’application](ribbon-applicationmodes.md).

[Interface utilisateur \_ Le \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) de la valeur de la variable est utilisé par une application pour interroger l’État bascule du contrôle Button d’un **SplitButtonGallery**.

La capture d’écran suivante illustre le contrôle de [Galerie de bouton partagé](windowsribbon-controls-splitbuttongallery.md) du ruban dans Microsoft Paint pour Windows 7.

![capture d’écran d’un contrôle de Galerie de boutons partagés dans Microsoft Paint pour Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour la [bibliothèque de boutons partagés](windowsribbon-controls-splitbuttongallery.md).

Cette section de code montre les déclarations de commande **SplitButtonGallery** , avec un [**groupe**](windowsribbon-element-group.md) associé qui fonctionne comme conteneur parent de l’élément **SplitButtonGallery** .


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



Cette section de code montre les déclarations de contrôle **SplitButtonGallery** .


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="element-information"></a>Informations sur les éléments


- **Système minimal pris en charge**: Windows 7 
- **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de la Galerie des boutons partagés](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Utilisation des galeries](ribbon-controls-galleries.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[Exemple de Galerie](windowsribbon-gallerysample.md)
</dt> </dl>

 

