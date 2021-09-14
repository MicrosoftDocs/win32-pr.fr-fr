---
description: En savoir plus sur l’élément Value, qui associe un littéral à un type. Le type de données de la valeur doit être String, Integer, Decimal ou QName.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Valeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 345ef8a40b7c87db68259f2815b07cfda0e5bc57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117989"
---
# <a name="value"></a>Valeur

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un élément de valeur associe un littéral à un type.

## <a name="element-tag"></a>Balise d’élément

&lt;Valeur&gt;

## <a name="xml-attributes"></a>Attributs XML

Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.



| Attribut XML       | Détails                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xsi:type<br/> | Spécifie le type de données de la valeur, qui doit être l’un des types définis par XSD suivants : String, Integer, Decimal, QName. Si elle est manquante, le type de données par défaut est String.<br/> |



 

Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .

## <a name="element-information"></a>Informations sur les éléments

Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.



| Category                   | Détails                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Éléments parents<br/> | ParameterInit <br/> Propriété<br/> ScoredProperty<br/>                                                                                   |
| Éléments enfants<br/>  | Seul le contenu d’un caractère ou d’un entier est autorisé.<br/>                                                                                                |
| Élément This<br/>    | Le contenu null est autorisé. Le contenu des caractères doit être conforme à la syntaxe définie par le type de données.<br/> Les frères enfants en double ne sont pas autorisés.<br/> |



 

## <a name="configuration-dependencies"></a>Dépendances de configuration

Les éléments de valeur qui apparaissent dans l’élément ScoredProperty ne peuvent pas avoir de dépendances de configuration. Les éléments de valeur qui apparaissent dans les éléments de propriété peuvent avoir des dépendances arbitraires sur la configuration.

## <a name="element-usage"></a>Utilisation des éléments

Un élément de valeur peut apparaître dans une propriété ou un élément ScoredProperty. L’objectif de l’élément value est de représenter une valeur comme un type de données XML standard. Le type de données est spécifié en tant qu’attribut XML de l’élément Value, xsi : type. Notez que tous les types définis par XSD ou XML ne sont pas pris en charge. Pour obtenir la liste des types pris en charge, consultez [Résumé des types d’éléments](summary-of-element-types.md). Un élément de valeur ne peut contenir que du contenu de caractères. Rien d’autre ne peut apparaître en tant que contenu dans un élément de valeur.

> [!Note]  
> Certaines propriétés définies par le schéma d’impression et les éléments ScoredProperty ne contiennent pas d’élément Value, car leur objectif est simplement d’être des parents des sous-propriétés. Vous ne devez pas ajouter un élément de valeur à ces propriétés, comme celles-ci, les propriétés qui ne contiennent pas d’élément de valeur.

 

Pour se conformer à l’infrastructure du schéma d’impression, qui nécessite la présence d’un ou de plusieurs éléments de valeur dans les éléments qui prennent en charge des valeurs, une valeur absente ou non définie doit être représentée en présentant l’élément de valeur comme élément vide ; autrement dit, en tant que &lt; valeur &gt; &lt; /value &gt; .

## <a name="example"></a>Exemple

Définissez une valeur de type Decimal et initialisez-la sur « 128,5 ».

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




