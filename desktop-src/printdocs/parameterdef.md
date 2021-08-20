---
description: En savoir plus sur l’élément ParameterDef, qui définit les caractéristiques valides de l’entrée de paramètre. La valeur est entrée au moyen d’un élément ParameterInit.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d7a0c8b86a8fef2d71cae1135eadca2c361e2062555d80a3a19f862f94ad7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033977"
---
# <a name="parameterdef"></a>ParameterDef

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un élément ParameterDef définit les caractéristiques valides de l’entrée de paramètre. La valeur est entrée au moyen d’un élément ParameterInit.

## <a name="element-tag"></a>Balise d’élément

<ParameterDef>

## <a name="xml-attributes"></a>Attributs XML

Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.



| Attribut XML   | Détails                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Définit un nom unique pour le paramètre dans le contexte du document actif. Les attributs de nom de ParameterDef dupliqués rendent le document PrintCapabilities non valide.<br/> |



 

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
<td>PrintCapabilities <br/></td>
</tr>
<tr class="even">
<td>Éléments enfants<br/></td>
<td>Property (un ou plusieurs) ;<br/> Les éléments de propriété standard suivants doivent apparaître en tant que contenu d’un élément ParameterDef. <br/>
<ul>
<li>DataType <br/></li>
<li>DefaultValue <br/></li>
<li>Obligatoire <br/></li>
<li>MaxLength ou MaxValue<br/></li>
<li>MinLength ou MinValue<br/></li>
<li>Plusieurs <br/></li>
<li>Unité <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Élément This<br/></td>
<td>Aucune donnée de caractères n’est autorisée.<br/> Les frères enfants en double ne sont pas autorisés.<br/></td>
</tr>
</tbody>
</table>



 

\*Obligatoire lorsque DataType est un entier ou un nombre décimal. Facultatif quand DataType est une chaîne.

## <a name="configuration-dependencies"></a>Dépendances de configuration

Un ParameterDef et son contenu à n’importe quel niveau d’imbrication ne peuvent pas avoir de dépendances de configuration.

## <a name="example"></a>Exemples

L’exemple suivant définit tous les éléments de propriété requis pour ce paramètre. L’exemple de [ParameterInit](parameterinit.md) montre comment initialiser ce paramètre.

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




