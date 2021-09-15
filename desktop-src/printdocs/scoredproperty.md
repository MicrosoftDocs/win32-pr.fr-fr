---
description: Recherche des informations sur l’élément ScoredProperty. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ad42d49e65fffebad0aec7730ab8ce85f41876
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519460"
---
# <a name="scoredproperty"></a>ScoredProperty

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un élément ScoredProperty déclare une propriété qui est intrinsèque à une définition d’option. Ces propriétés doivent être comparées lors de l’évaluation de la précision qu’une option demandée correspond à une option prise en charge par l’appareil.

## <a name="element-tag"></a>Balise d’élément

&lt;ScoredProperty&gt;

## <a name="xml-attributes"></a>Attributs XML

Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.



| Attribut XML   | Détails                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contient l’attribut Name de ScoredProperty, soit une propriété standard, soit une propriété définie en privé. <br/> |



 

Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .

## <a name="element-information"></a>Informations sur les éléments

Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.



| Category                   | Détails                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Éléments parents<br/> | *Option*<br/> *ScoredProperty*<br/>                                                                                                                          |
| Éléments enfants<br/>  | Vous pouvez soit utiliser<br/> *ParameterRef* (un)<br/> ou<br/> *Valeur* (un)<br/> *Property* (zéro, un ou plusieurs)<br/> *ScoredProperty* (zéro ou plus)<br/> |
| Élément This<br/>    | Aucune donnée de caractères n’est autorisée.<br/> Les frères enfants en double ne sont pas autorisés.<br/>                                                                        |



 

## <a name="configuration-dependencies"></a>Dépendances de configuration

Un élément ScoredProperty ne peut pas avoir de dépendances de configuration.

## <a name="example"></a>Exemple

Déclarez un élément ScoredProperty nommé MediaSizeWidth avec la valeur 11.

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




