---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Fonctionnalité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89655181563e2da3a8d4841b1d90ecd4e6ac07
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106531267"
---
# <a name="feature"></a>Fonctionnalité

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un élément Feature contient une liste complète des éléments option et Property qui décrivent entièrement un attribut d’appareil, un paramètre de mise en forme de tâche ou d’autres caractéristiques pertinentes.

## <a name="element-tag"></a>Balise d’élément

<Feature>

## <a name="xml-attributes"></a>Attributs XML

Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.



| Attribut XML   | Détails                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| name<br/> | Contient le nom de la fonctionnalité, qu’il s’agisse d’une fonctionnalité standard ou d’une fonctionnalité définie en privé. <br/> |



 

Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .

## <a name="element-information"></a>Informations sur les éléments

Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Éléments parents<br/></td>
<td>PrintCapabilities <br/> PrintTicket <br/> Fonctionnalité<br/></td>
</tr>
<tr class="even">
<td>Éléments enfants<br/></td>
<td>Un des groupes suivants :<br/>
<ul>
<li><em>Fonctionnalité</em> (zéro ou plus)<br/></li>
<li><em>Option</em> (une ou plusieurs)<br/></li>
<li><em>Property</em> (zéro, un ou plusieurs)<br/></li>
</ul>
ou <br/>
<ul>
<li><em>Fonctionnalité</em> (une ou plusieurs)<br/></li>
<li><em>Option</em> (zéro, un ou plusieurs)<br/></li>
<li><em>Property</em> (zéro, un ou plusieurs)<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Élément This<br/></td>
<td>Aucune donnée de caractères n’est autorisée.<br/> Les éléments d’option enfants dupliqués qui sont des frères sont autorisés. Raccourcis d’attribut de nom en double autorisés. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a>Dépendances de configuration

Les éléments de fonctionnalité ne peuvent pas avoir de dépendances de configuration.

## <a name="element-usage"></a>Utilisation des éléments

### <a name="relationship-to-xml-attributes"></a>Relation aux attributs XML

Dans la représentation fonctionnalité/option, un attribut d’appareil est représenté par un élément de fonctionnalité. L’attribut d’appareil est identifié de manière unique par l’attribut Name dans l’élément Feature de l’attribut de périphérique, comme dans l’exemple suivant. Dans cet exemple, l’attribut d’appareil est Resolution.

``` syntax
<Feature name="Resolution" />
```

Le schéma d’impression définit un ensemble d’attributs de nom pour certaines instances de fonctionnalité. Ces attributs de nom servent à identifier un ensemble d’instances de fonctionnalités prédéfinies associées à des attributs d’appareil configurables spécifiques. Ces noms d’instances de fonctionnalités doivent être utilisés chaque fois que cela est possible, car ils augmentent la portabilité de votre document PrintCapabilities et les des PrintTicket dérivés de ceux-ci. Les instances de fonctionnalités définies de manière privée peuvent être introduites si certains attributs d’appareil ne correspondent à aucune des instances de fonctionnalités définies par schéma. Pour plus d’informations sur la syntaxe des attributs de nom et les conventions qui s’appliquent aux noms définis par le schéma et à la définition privée, consultez [attributs XML](xml-attributes.md).

### <a name="relationship-to-option-element"></a>Relation avec l’élément option

Chacun des États possibles est représenté par un élément option. Chaque définition d’option contient un ou plusieurs éléments ScoredProperty, qui, ensemble, décrivent de façon unique ou caractérisent l’État représenté. La technique utilisée pour créer des définitions d’options est décrite dans [définitions d’options](option-definitions.md). Tous les éléments d’option associés à un élément de fonctionnalité particulier résident en tant qu’éléments enfants de l’élément de fonctionnalité.

### <a name="subfeatures"></a>Sous-composants

L’infrastructure du schéma d’impression permet également de regrouper les éléments de fonctionnalité de manière hiérarchique. Autrement dit, un élément Feature peut lui-même contenir un ou plusieurs éléments de fonctionnalités enfants (sous-fonctionnalités). Cela peut être utile pour organiser des éléments de fonctionnalités connexes ou pour des éléments de fonctionnalité qui contrôlent les aspects d’une fonctionnalité d’appareil. Par exemple, un appareil qui prend en charge l’agrafage. Un tel appareil peut offrir à l’utilisateur la possibilité de localiser l’agrafe, par exemple dans l’angle supérieur gauche, dans le coin supérieur droit, dans le bord supérieur ou sur le bord gauche. L’interface utilisateur de cet appareil doit être en mesure de présenter l’utilisateur avec les choix de niveau le plus élevé en premier, ce qui, dans ce cas, s’il faut utiliser l’agrafage. Une fois que l’utilisateur a décidé d’utiliser l’agrafage, il doit être présenté avec un deuxième niveau de choix, l’emplacement de l’agrafe. Une hiérarchie de fonctionnalités ajoute la structure supplémentaire qui rend cette interface utilisateur possible. L’infrastructure du schéma d’impression permet aux sous-fonctionnalités d’avoir leurs propres sous-fonctionnalités enfants, ce qui autorise un niveau illimité d’imbrication.

L’infrastructure du schéma d’impression permet également aux éléments d’option d’apparaître au même niveau que les sous-fonctionnalités ; autrement dit, en tant que frères dans le même élément de fonctionnalité parent. Cela permet à l’utilisateur de prendre la décision de haut niveau (s’il faut utiliser l’agrafage) avant d’effectuer les sélections de sous-fonctionnalités. Pour cet exemple, l’élément de fonctionnalité racine, « agrafe », peut contenir deux éléments option, « on » et « OFF », ainsi qu’une sous-fonctionnalité nommée « StapleLocation ».

## <a name="example"></a>Exemple

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




