---
description: Obtenir des informations sur l’élément option. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Option
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f02f506c61353698bc4386541ea96dbf858790dd7c34c6d80b8dc2542c46a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098973"
---
# <a name="option"></a>Option

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un élément option contient tous les éléments Property et ScoredProperty associés à cette option.

## <a name="element-tag"></a>Balise d’élément

<Option>

## <a name="xml-attributes"></a>Attributs XML

Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.



| Attribut XML          | Détails                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| la<br/> | Cet attribut est facultatif pour un document PrintCapabilities.<br/> Cet attribut indique si l’option est disponible pour la sélection ou l’utilisation. Cet attribut XML peut être défini sur l’une des valeurs suivantes : None, PrintTicketSettings, AdminSetting ou DeviceSettings. <br/> Voir [attributs XML](xml-attributes.md)<br/> |
| name<br/>        | Contient le nom de l’option, soit une option standard, soit une option définie en privé. L’attribut XML est utilisé de cette façon afin de faire la différence entre les instances d’option. <br/>                                                                                                                                                        |



 

Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .

## <a name="element-information"></a>Informations sur les éléments

Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.



| Category                   | Détails                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Éléments parents<br/> | Fonctionnalité <br/>                                                                                                                                                                                                                                                                              |
| Éléments enfants<br/>  | *Property* (zéro, un ou plusieurs)<br/> *ScoredProperty* (zéro ou plus pour les options avec l’attribut XML’name'; une ou plusieurs options pour les options qui n’utilisent pas l’attribut XML’name' \* )<br/> \* seules les options publiques définies dans le schéma d’impression ne peuvent pas avoir d’attribut’name', tel que DocumentNUp)<br/> |
| Élément This<br/>    | Aucune donnée de caractères n’est autorisée.<br/> Les frères enfants en double ne sont pas autorisés.<br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a>Dépendances de configuration

Un élément de définition d’option ne peut pas avoir de dépendances de configuration.

## <a name="element-usage"></a>Utilisation des éléments

L’objectif de l’élément option consiste à caractériser l’un des États qu’un attribut de configuration d’appareil, représenté par un élément de fonctionnalité, peut supposer. Chaque définition d’élément option contient un ou plusieurs éléments ScoredProperty qui décrivent une caractéristique intrinsèque ou essentielle de cette option. Pour faciliter la portabilité et la préservation de l’intention, le schéma d’impression définit de nombreux éléments de fonctionnalités courants et divers éléments d’option pour chaque fonctionnalité. Il est donc important d’utiliser des éléments d’option d’impression définis par schéma, si possible, avant de créer vos propres définitions d’options. la compréhension du processus de définition des éléments d’Option fournit des insights utiles sur la façon dont le document PrintCapabilities et les des printticket sont utilisés dans les architectures d’impression Microsoft .NET Framework version 3,0 et Windows Vista.

## <a name="example"></a>Exemple

L’exemple suivant définit un nom pour l’option.

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




