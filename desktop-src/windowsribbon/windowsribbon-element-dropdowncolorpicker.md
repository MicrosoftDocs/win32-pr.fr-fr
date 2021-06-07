---
title: Élément DropDownColorPicker
description: Représente une Drop-Down couleur Pickercontrol qui, lorsque l’utilisateur clique dessus, affiche une palette d’échantillons de couleurs.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- Ruban des fenêtres d’élément DropDownColorPicker
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce2fd1d9ff12b56d87955304fad24af23209ff91
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442900"
---
# <a name="dropdowncolorpicker-element"></a>Élément DropDownColorPicker

Représente un contrôle de [Sélecteur de couleurs déroulant](windowsribbon-controls-dropdowncolorpicker.md)qui, lorsque l’utilisateur clique dessus, affiche une palette d’échantillons de couleurs.

## <a name="usage"></a>Utilisation

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
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
<td><strong>Copeaux</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Taille de chaque puce ou nuance de couleur. <br/> Limité à l’une des valeurs suivantes :<br/> <br/>
<dt><span></span><span></span><strong></strong> Small<br/> </dt> <dd> Chaque puce de couleur est un carré de pixel 11x11. <br/> </dd> <dt><span></span><span></span><strong></strong> Médias<br/> </dt> <dd> Chaque puce de couleur est un carré de 16 x 16 pixels. <br/> </dd> <dt><span></span><span></span><strong></strong> Conséquent<br/> </dt> <dd> Chaque puce de couleur est un carré de pixel 24x24. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ColorTemplate</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Modèles de disposition qui spécifient le type de <a href="windowsribbon-controls-dropdowncolorpicker.md">Sélecteur de couleur déroulant</a>. <br/> Limité à l’une des valeurs suivantes (si aucun attribut facultatif relatif à un <em>ColorTemplate</em> n’est déclaré, la vue par défaut est indiquée) :<br/> <br/>
<dt><span></span><span></span><strong></strong> (ThemeColors)<br/> </dt> <dd> Par défaut. <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> La définition de l’attribut <em>ColorTemplate</em> pour <code>ThemeColors</code> active les fonctionnalités suivantes :<br/>
<ul>
<li>Ancre SplitButton.</li>
<li>Le bouton couleur <strong>automatique</strong> est affiché par défaut.</li>
<li>Palette de <strong>couleurs du thème</strong> Windows.</li>
<li>Grille d’échantillons de <strong>couleurs standard</strong> .</li>
<li>La grille des échantillons de <strong>couleurs récentes</strong> est facultative.</li>
<li>Lanceur de boîte de dialogue <strong>couleurs supplémentaires</strong> .</li>
<li><strong>Aucun</strong> bouton de couleur de couleur n’est affiché par défaut.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (StandardColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> La définition de l’attribut <em>ColorTemplate</em> pour <code>StandardColors</code> active les fonctionnalités suivantes :<br/>
<ul>
<li>Ancre SplitButton.</li>
<li>Le bouton couleur <strong>automatique</strong> est affiché par défaut.</li>
<li>Grille d’échantillons de <strong>couleurs standard</strong> .</li>
<li>Lanceur de boîte de dialogue <strong>couleurs supplémentaires</strong> .</li>
<li><strong>Aucun</strong> bouton de couleur de couleur n’est affiché par défaut.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (HighlightColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> La définition de l’attribut <em>ColorTemplate</em> pour <code>HighlightColors</code> active les fonctionnalités suivantes :<br/>
<ul>
<li>Ancre SplitButton.</li>
<li>Grille d’échantillons de <strong>couleurs standard</strong> sans en-tête.</li>
<li><strong>Aucun</strong> bouton de couleur de couleur n’est affiché par défaut.</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Colonnes</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Non<br/></td>
<td>Nombre de colonnes de la puce de couleur (ou de l’échantillon).<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)<br/> </dt> <dd> Toute valeur entière positive comprise entre 1 et 256 inclus.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS : positiveInteger ou XS : String<br/></td>
<td>Non<br/></td>
<td>Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)<br/> </dt> <dd> Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus. <br/> La valeur doit être unique dans le document XML du ruban. <br/> Longueur maximale : 100 caractères. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsAutomaticColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Affiche (ou masque) le bouton de couleur <strong>automatique</strong> . <br/> Valide uniquement lorsque <code>StandardColors</code> ou <code>ThemeColors</code> est spécifié pour l’attribut <em>ColorTemplate</em> . <br/> Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsNoColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Affiche (ou masque) le bouton <strong>aucune couleur</strong> . <br/> Valide pour toutes les valeurs <em>ColorTemplate</em> .<br/> Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>RecentColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Non<br/></td>
<td>Nombre de lignes de la puce de couleur (ou de l’échantillon) dans la zone <strong>couleurs récentes</strong> . <br/> Valide uniquement lorsque <code>ThemeColors</code> est spécifié pour l’attribut <em>ColorTemplate</em> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)<br/> </dt> <dd> Toute valeur entière positive comprise entre 1 et 256 inclus.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>StandardColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Non<br/></td>
<td>Nombre de lignes de puce de couleur (ou d’échantillon) dans la zone de <strong>couleurs standard</strong> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)<br/> </dt> <dd> Toute valeur entière positive comprise entre 1 et 256 inclus.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ThemeColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Non<br/></td>
<td>Nombre de lignes de puce de couleur (ou d’échantillon) dans la zone de <strong>couleurs de thème</strong> .<br/> Valide uniquement lorsque <code>ThemeColors</code> est spécifié pour l’attribut <em>ColorTemplate</em> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)<br/> </dt> <dd> Toute valeur entière positive comprise entre 1 et 256 inclus.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>         |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Groupe**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Remarques

facultatif.

Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour les trois types de [sélecteurs de couleurs déroulants](windowsribbon-controls-dropdowncolorpicker.md).

Cette section de code montre les déclarations de commande pour trois éléments **DropDownColorPicker** .


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```



Cette section de code illustre les trois types de déclarations de contrôle **DropDownColorPicker** .


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a>Informations sur les éléments

* **Système minimal pris en charge**: Windows 7
* **Peut être vide**: Oui



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de sélecteur de couleurs déroulant](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[Exemple DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





