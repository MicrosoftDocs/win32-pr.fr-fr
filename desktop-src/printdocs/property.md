---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Propriété (documents et impression)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321722"
---
# <a name="property-documents-and-printing"></a>Propriété (documents et impression)

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un élément de propriété déclare un appareil, une mise en forme de travail ou une autre propriété pertinente dont le nom est donné par son attribut de nom. Un élément de valeur est utilisé pour assigner une valeur à la propriété.

Une propriété peut être complexe, contenant éventuellement plusieurs sous-propriétés. Les sous-propriétés sont également représentées par des éléments de propriété.

## <a name="element-tag"></a>Balise d’élément

<Property>

## <a name="xml-attributes"></a>Attributs XML

Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.



| Attribut XML   | Détails                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contient l’attribut Name de la propriété, qui est soit une propriété standard, soit une propriété définie en privé. <br/> |



 

Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .

## <a name="element-information"></a>Informations sur les éléments

Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.



| Category                   | Détails                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Éléments parents<br/> | PrintCapabilities <br/> Fonctionnalité<br/> PrintTicket<br/> Option<br/> ParameterDef<br/> Propriété<br/> ScoredProperty<br/>                                                                                                                                                              |
| Éléments enfants<br/>  | Le système n’affecte pas l’importance à l’ordre des éléments. Si les clients choisissent d’ascriber une certaine importance dans l’ordre des éléments, ils sont libres de le faire. <br/> *Property* (une ou plusieurs) *valeur* (zéro ou plus)<br/> ou <br/> *Valeur* de la *propriété* (zéro ou plus) (un ou plusieurs)<br/> |
| Élément This<br/>    | Aucune donnée de caractères n’est autorisée.<br/> Les éléments de valeur enfants dupliqués qui sont des frères sont autorisés.<br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a>Dépendances de configuration

Une propriété peut avoir des dépendances de configuration, sauf lorsqu’elle apparaît dans un élément ParameterDef.

## <a name="element-usage"></a>Utilisation des éléments

En plus d’apparaître dans les éléments de fonctionnalité et d’option, les éléments de propriété peuvent apparaître au niveau racine des technologies sous-jacentes respectives. Le schéma d’impression définit un ensemble d’éléments de propriété qui peuvent être utilisés pour décrire un appareil de manière portable. Toutefois, si ces propriétés sont insuffisantes pour vos besoins en tant que fournisseur PrintCapabilities (généralement parce que l’appareil pris en charge a de nouveaux aspects non anticipés par le schéma d’impression), vous pouvez introduire vos propres éléments de propriété privés. Vous pouvez améliorer ou développer les informations fournies par une propriété publique en ajoutant une ou plusieurs sous-propriétés privées en tant que contenu d’élément de la propriété publique.

Les éléments de propriété sont définis à l’aide d’une balise d’élément XML, <Property> . Un nom est attribué à chaque propriété au moyen de son attribut Name. Le nom doit être un QName XML et doit être conforme à la Convention d’espace de noms. Pour plus d’informations, consultez [attributs XML](xml-attributes.md). L’attribut de nom de propriété et son emplacement dans la hiérarchie des éléments de propriété parents (s’il s’agit d’une sous-propriété) identifient de façon unique la propriété dans le document PrintCapabilities ou PrintTicket.

Une propriété peut contenir un ou plusieurs éléments de valeur, ou un ou plusieurs éléments de propriété enfants (appelés sous-propriétés), ou une combinaison des deux. Les sous-propriétés sont utiles lorsque la propriété elle-même est composée de plusieurs composants. Par exemple, une propriété « ConsumableColor » peut avoir des composants « C », « M » et « Y ».

## <a name="example"></a>Exemple

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




