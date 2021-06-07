---
title: Élément InRibbonGallery
description: Représente la Galerie de In-Ribbon, un contrôle basé sur la galerie qui expose un sous-ensemble par défaut d’éléments directement dans le ruban. Tous les éléments restants sont affichés lorsque l’utilisateur clique sur un bouton de menu déroulant.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- Ruban des fenêtres d’élément InRibbonGallery
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a25b2ebb937d954adce58231fd8c6b3347a031a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443370"
---
# <a name="inribbongallery-element"></a>Élément InRibbonGallery

Représente la [Galerie dans le ruban](windowsribbon-controls-inribbongallery.md), un contrôle basé sur la galerie qui expose un sous-ensemble par défaut d’éléments directement dans le ruban. Tous les éléments restants sont affichés lorsque l’utilisateur clique sur un bouton de menu déroulant.

## <a name="usage"></a>Utilisation

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
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
<tr class="odd">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>Non<br/></td>
<td>Avec <em>ItemWidth</em>, détermine la taille de l’image d’élément affichée dans le contrôle Gallery. <br/>
<blockquote>
[!Note]<br />
S’applique uniquement aux galeries où la valeur de l’attribut <em>type</em> est égale à <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : Integer)<br/> </dt> <dd> La valeur par défaut est -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>Non<br/></td>
<td>Avec <em>ItemHeight</em>, détermine la taille de l’image d’élément affichée dans le contrôle Gallery. <br/>
<blockquote>
[!Note]<br />
S’applique uniquement aux galeries où la valeur de l’attribut <em>type</em> est égale à <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : Integer)<br/> </dt> <dd> La valeur par défaut est -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxColumns</strong><br/></td>
<td>xs:integer<br/></td>
<td>Non<br/></td>
<td>Spécifie le nombre maximal de colonnes que le <strong>InRibbonGallery</strong> affiche, par exemple, dans la liste déroulante <em>grande</em> disposition de groupe.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MaxColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>Non<br/></td>
<td>Spécifie le nombre maximal de colonnes que le <strong>InRibbonGallery</strong> affiche dans la disposition de groupe de <em>taille moyenne</em> , avant de passer à une <em>grande</em> disposition. <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxRows</strong><br/></td>
<td>xs:integer<br/></td>
<td>Non<br/></td>
<td>Spécifie le nombre maximal de lignes pour la disposition des éléments <strong>InRibbonGallery</strong> . <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : Integer)<br/> </dt> <dd> La valeur par défaut est 1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinColumnsLarge</strong><br/></td>
<td>xs:integer<br/></td>
<td>Non<br/></td>
<td>Spécifie le nombre minimal de colonnes que le <strong>InRibbonGallery</strong> affiche dans la <em>grande</em> disposition de groupe, avant de passer au mode <em>moyen</em>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MinColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>Non<br/></td>
<td>Spécifie le nombre minimal de colonnes que le <strong>InRibbonGallery</strong> affiche dans la disposition de groupe de <em>taille moyenne</em> , avant de basculer vers <em>Small</em>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>Non<br/></td>
<td>Spécifie l’emplacement d’affichage de l’étiquette de l’élément par rapport à l’image. <br/> Limité à l’une des valeurs suivantes :<br/> <br/>
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



| Élément                                                                                           | Description                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Activé**](windowsribbon-element-checkbox.md)<br/>                                     | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/> | Doit se produire exactement une fois<br/> <br/>     |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/> | Peut se produire au plus une fois<br/> <br/>      |
| [**Bouton**](windowsribbon-element-button.md)<br/>                                       | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                               | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                             | Peut se produire une ou plusieurs fois<br/> <br/> |



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
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 et versions ultérieures.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Remarques

facultatif.

Peut se produire au plus une fois pour chaque [**ControlGroup**](windowsribbon-element-controlgroup.md) ou élément de [**groupe**](windowsribbon-element-group.md) .

La capture d’écran suivante illustre le contrôle [de Galerie ruban dans le ruban](windowsribbon-controls-inribbongallery.md) de Microsoft Paint pour Windows 7.

![capture d’écran d’un contrôle de galerie dans le ruban dans le ruban Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour une [Galerie dans le ruban](windowsribbon-controls-inribbongallery.md).

Cette section de code montre les déclarations de commande **InRibbonGallery** , avec un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **InRibbonGallery** .


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



Cette section de code montre les déclarations de contrôle **InRibbonGallery** .


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a>Informations sur les éléments


* **Système minimal pris en charge**: Windows 7
* **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de galerie dans le ruban](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Utilisation des galeries](ribbon-controls-galleries.md)
</dt> <dt>

[Exemple de Galerie](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





