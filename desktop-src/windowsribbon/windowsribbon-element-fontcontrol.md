---
title: Élément FontControl
description: Représente un contrôle de police, qui est un conteneur spécialisé de contrôles individuels dédiés à la manipulation de polices.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- Ruban des fenêtres d’élément FontControl
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c9d900c2af4f7f8ba26f5ac8dbbdc0d055668d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443400"
---
# <a name="fontcontrol-element"></a>Élément FontControl

Représente un [contrôle de police](windowsribbon-controls-fontcontrol.md), qui est un conteneur spécialisé de contrôles individuels dédiés à la manipulation de polices.

## <a name="usage"></a>Utilisation

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
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
<td><strong>FontType</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Limité à l’une des valeurs suivantes : <br/> <br/>
<dt><span></span><span></span><strong></strong> (FontOnly)<br/> </dt> <dd> Par défaut. <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> La définition de l’attribut <em>FontType</em> pour <code>FontOnly</code> active les fonctionnalités suivantes :<br/>
<ul>
<li>Zone de liste déroulante <strong>famille de polices</strong> .</li>
<li>Zone de liste déroulante <strong>taille de police</strong> .</li>
<li><p>Boutons bascule <strong>gras</strong>, <strong>italique</strong>, <strong>souligné</strong>et <strong>barré</strong> .</p>
<blockquote>
[!Note]<br />
Les boutons de bascule <strong>barré</strong> et <strong>souligné</strong> s’affichent par défaut, mais peuvent être masqués en définissant les attributs <em>IsStrikethroughButtonVisible</em> et <em>IsUnderlineButtonVisible</em> sur <code>false</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (FontWithColor)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> La définition de l’attribut <em>FontType</em> pour <code>FontWithColor</code> active les fonctionnalités suivantes :<br/>
<ul>
<li>Zone de liste déroulante <strong>famille de polices</strong> .</li>
<li>Zone de liste déroulante <strong>taille de police</strong> .</li>
<li><strong>Agrandir la police</strong> et <strong>réduire</strong> la taille de police de police des boutons d’incrémentation et de décrémentation.</li>
<li><p>Boutons bascule <strong>gras</strong>, <strong>italique</strong>, <strong>souligné</strong>et <strong>barré</strong> .</p>
<blockquote>
[!Note]<br />
Les boutons de bascule <strong>barré</strong> et <strong>souligné</strong> s’affichent par défaut, mais peuvent être masqués en définissant les attributs <em>IsStrikethroughButtonVisible</em> et <em>IsUnderlineButtonVisible</em> sur <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Sélecteur de couleurs de <strong>couleur du texte</strong> .</li>
<li><p>Sélecteur de couleurs de <strong>couleur de mise en surbrillance du texte</strong> .</p>
<blockquote>
[!Note]<br />
Ce contrôle est masqué par défaut, mais il peut être affiché en affectant à l’attribut <em>IsHighlightButtonVisible</em> la valeur <code>true</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (RichFont)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> La définition de l’attribut <em>FontType</em> pour <code>RichFont</code> active les fonctionnalités suivantes :<br/>
<ul>
<li>Zone de liste déroulante <strong>famille de polices</strong> .</li>
<li>Zone de liste déroulante <strong>taille de police</strong> .</li>
<li><strong>Agrandir la police</strong> et <strong>réduire</strong> la taille de police de police des boutons d’incrémentation et de décrémentation.</li>
<li><p>Boutons bascule <strong>gras</strong>, <strong>italique</strong>, <strong>souligné</strong>et <strong>barré</strong> .</p>
<blockquote>
[!Note]<br />
Les boutons de bascule <strong>barré</strong> et <strong>souligné</strong> s’affichent par défaut et ne peuvent pas être masqués en définissant les attributs <em>IsStrikethroughButtonVisible</em> et <em>IsUnderlineButtonVisible</em> sur <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Sélecteur de couleurs de <strong>couleur du texte</strong> .</li>
<li><p>Sélecteur de couleurs de <strong>couleur de mise en surbrillance du texte</strong> .</p>
<blockquote>
[!Note]<br />
Ce contrôle s’affiche par défaut et ne peut pas être masqué en affectant à l’attribut <em>IsHighlightButtonVisible</em> la valeur <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Boutons bascule en <strong>indice</strong> et en <strong>exposant</strong> .</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsGrowShrinkButtonGroupVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td><strong>Windows 8 et versions ultérieures</strong><br/> Limité à l’une des valeurs suivantes : <br/>
<blockquote>
[!Note]<br />
Les boutons agrandir/rétrécir ne sont jamais affichés dans le <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd> Valeur par défaut lorsque la valeur de <em>FontType</em> est égale à <code>FontWithColor</code> ou <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd> Valeur par défaut lorsque la valeur de <em>FontType</em> est égale à <code>FontOnly</code> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsHighlightButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) : <br/>
<blockquote>
[!Note]<br />
La mise en surbrillance des couleurs n’est disponible qu’à partir d’un <strong>FontControl</strong> lorsque la valeur de l’attribut <em>FontType</em> est égale à <code>FontWithColor</code> ou <code>RichFont</code> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd> Valeur par défaut lorsque la valeur de <em>FontType</em> est égale à <code>FontWithColor</code> ou <code>RichFont</code> .<br/> Valide uniquement lorsque la valeur de <em>FontType</em> est égale à <code>FontWithColor</code> ou <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd> Valeur par défaut lorsque la valeur de <em>FontType</em> est égale à <code>FontOnly</code> .<br/> Valide uniquement lorsque la valeur de <em>FontType</em> est égale à <code>FontOnly</code> ou <code>FontWithColor</code> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsStrikethroughButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) : <br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd> Par défaut. <br/> </dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd> Valide uniquement lorsque la valeur de <em>FontType</em> est égale à <code>FontOnly</code> ou <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsUnderlineButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) : <br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd> Par défaut. <br/> </dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd> Valide uniquement lorsque la valeur de <em>FontType</em> est égale à <code>FontOnly</code> ou <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaximumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Non<br/></td>
<td>Taille maximale en points à afficher.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)<br/> </dt> <dd> Valeur entière comprise entre 1 et 9999 inclus.<br/> La valeur par défaut est <strong>9999</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinimumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Non<br/></td>
<td>Taille minimale du point à afficher.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger)<br/> </dt> <dd> Valeur entière comprise entre 1 et 9999 inclus.<br/> La valeur par défaut est <strong>1</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ShowTrueTypeOnly</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd> Affiche uniquement les polices TrueType et OpenType. <br/> </dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd> Par défaut. Aucune restriction n’est placée sur le type de polices affichées.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ShowVerticalFonts</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :<br/>
<blockquote>
[!Note]<br />
Les polices verticales sont précédées d’un symbole @ dans la liste des <strong>familles de polices</strong> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd> Par défaut. Affiche les polices verticales qui sont définies pour s' <strong>Afficher</strong> dans le panneau de configuration <strong>polices</strong> . <br/> </dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd> Permet à une application qui ne prend pas en charge le texte vertical de masquer les polices verticales qui sont définies pour s' <strong>Afficher</strong> dans le panneau de configuration <strong>polices</strong> .<br/>
<blockquote>
[!Note]<br />
Dans Windows Vista, le panneau de configuration des <strong>polices</strong> n’offre pas de fonctionnalité d' <strong>affichage</strong> ou de <strong>masquage</strong> . Dans ce cas, l’attribut <em>ShowVerticalFonts</em> doit avoir la valeur <code>False</code> .
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                               |
|-----------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/> |
| [**Groupe**](windowsribbon-element-group.md)<br/>               |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a>Remarques

facultatif.

Peut se produire au plus une fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md)ou [**MenuGroup**](windowsribbon-element-menugroup.md) .

Les attributs de commande **FontControl** déclarés dans le balisage, tels que [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), sont substitués par les attributs des contrôles individuels qui composent le **FontControl**.

Toute tentative de sélection d’un échantillon de couleur dans le sélecteur de couleurs d’un [contrôle de police](windowsribbon-controls-fontcontrol.md) peut entraîner une violation d’accès si aucun gestionnaire de commandes n’est associé au contrôle.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour les trois types de [contrôle de police](windowsribbon-controls-fontcontrol.md).

Cette section de code montre les déclarations de commande **FontControl** , chacune avec une déclaration de conteneur de [**groupe**](windowsribbon-element-group.md) .


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



Cette section de code montre les déclarations de contrôle **FontControl** où chaque **FontControl** et [**groupe**](windowsribbon-element-group.md) est déclaré dans un seul onglet.


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a>Informations sur les éléments

* **Système minimal pris en charge**: Windows 7
* **Peut être vide**: Oui



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Exemple FontControl](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





