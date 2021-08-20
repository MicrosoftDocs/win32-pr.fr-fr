---
description: Cette rubrique n’est pas à jour. Pour plus d’informations, consultez la spécification du schéma d’impression.
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: Éléments ParameterDef et ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa945ad7fec484828bd81b2052f9b330d0e1679
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475125"
---
# <a name="parameterdef-and-parameterinit-elements"></a>Éléments ParameterDef et ParameterInit

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un élément ParameterDef diffère d’un élément ParameterInit en ce qu’il décrit la valeur qu’un élément ParameterInit peut contenir, tandis qu’un élément ParameterInit assigne une valeur au paramètre. Un élément ParameterDef se compose d’un ensemble spécifique d’éléments de propriété, qui sont des enfants de l’élément ParameterDef, qui spécifient le type de données, la valeur maximale, la valeur minimale et les valeurs par défaut des données, ainsi que d’autres informations. Ces éléments de propriété sont décrits plus loin dans cette rubrique.

Les éléments ParameterDef peuvent apparaître uniquement dans leur contexte autorisé. Pour la version initiale du schéma d’impression, ils peuvent se trouver au niveau racine du document PrintCapabilities. L’attribut Name de l’élément ParameterDef définit le nom du paramètre. Un attribut de nom unique doit être assigné à chaque élément ParameterDef dans le document PrintCapabilities.

> [!Note]
> pour imprimer des fonctionnalités fournisseurs de documents :
> 
> La signification d’un nom de paramètre est universelle ; autrement dit, si un élément ParameterDef dans un document PrintCapabilities a le même attribut Name (la chaîne formée à partir de l’espace de noms et le nom descriptif de l’élément ParameterDef) en tant qu’élément ParameterDef dans un autre document PrintCapabilities, il est supposé que ces deux éléments représentent le même concept et doivent être interprétés de la même manière. Par conséquent, un élément ParameterDef défini dans un PrintTicket pour un document PrintCapabilities peut être utilisé pour initialiser l’élément ParameterInit du même nom défini dans un document PrintCapabilities différent.

 

## <a name="relationship-to-xml-attributes"></a>Relation aux attributs XML

Comme c’est le cas pour tous les attributs Name, le nom du paramètre se présente sous la forme d’un QName XML. Une construction de paramètre définie par schéma a un nom qualifié par l’espace de noms public, formant l’attribut Name, tandis que l’attribut Name d’une construction de paramètre définie en privé est qualifié par un espace de noms privé qui est unique pour le créateur.

## <a name="relationship-between-parameterdef-and-property-element-types"></a>Relation entre les types d’éléments ParameterDef et Property

Les éléments ParameterDef définis dans les mots clés du schéma d’impression doivent être entièrement définis dans un document PrintCapabilities. Le document Mots clés du schéma d’impression fournit des valeurs nominales pour certains éléments de propriété d’un élément ParameterDef (par exemple, DefaultValue et autres), mais l’auteur d’un document PrintCapabilities est responsable de la définition des éléments de propriété restants. Dans tous les cas, tous les éléments de propriété doivent être définis explicitement dans un élément ParameterDef, y compris ceux qui sont définis dans les mots clés du schéma d’impression.

Certains éléments de propriété de chaque élément ParameterDef apparaissant dans les mots clés de schéma d’impression sont désignés comme *immuables*. Cela signifie que toutes les définitions de document PrintCapabilities des éléments ParameterDef définis par des mots clés de schéma d’impression doivent conserver ces éléments de propriété sans modification. Ces éléments de propriété immuables permettent aux constructions de paramètres d’être portables et non ambiguës dans tous les documents PrintCapabilities. Un exemple premier est l’unité utilisée dans un élément ParameterDef. Ces unités doivent être immuables pour promouvoir une compréhension cohérente de leur signification. Les éléments de propriété d’un ParameterDef qui sont désignés comme non immuables peuvent être redéfinis dans un document PrintCapabilities.

Un élément ParameterDef est composé des éléments de propriété suivants. Tout doit être présent, sauf indication contraire.




| Nom de la propriété | Valeurs | Description | Immuable? | 
|---------------|--------|-------------|------------|
| DataType <br /> | entier <br /> Décimal<br /> string<br /> Pas de valeur par défaut.<br /> | Spécifie si la valeur de paramètre est un entier, un nombre à virgule flottante ou une chaîne de texte. La valeur d’un paramètre est exprimée dans le même format que le type de données XSD Basic correspondant ; autrement dit, sous la forme d’un entier, d’une valeur décimale ou d’une chaîne. <br /> | Yes<br /> | 
| DefaultValue <br /> | Type spécifié par la propriété DataType.<br /> Pas de valeur par défaut.<br /> | Spécifie la valeur à utiliser pour initialiser un contrôle de l’interface utilisateur.<br /><ul><li>ou <br /></li></ul>Spécifie la valeur à utiliser si l’élément de paramètre approprié est manquant dans PrintTicket.<br /> | No<br /> | 
| Obligatoire <br /> | Inconditionnelle : l’élément ParameterInit doit toujours être fourni. <br /> Conditional : l’élément ParameterInit est requis uniquement si le paramètre est référencé dans un élément option dans PrintTicket.<br /> DefaultValue : Conditional.<br /> | Indique qu’un élément ParameterInit doit apparaître explicitement. Si conditionnel, ParameterInit doit être initialisé si PrintTicket contient une option qui référence le paramètre.<br /> Utilisé par les clients de l’interface utilisateur et les fournisseurs PrintCapabilities ou PrintTicket. Notez que dans n’importe quelle contrainte, la propriété obligatoire de l’élément ParameterDef doit être définie sur inconditionnelle. ParameterDef doit avoir une valeur définie ; sinon, la valeur ou la contrainte dépendante n’a pas pu être évaluée.<br /> | No<br /> | 
| MaxLength <br /> | entier si la propriété DataType spécifie String.<br /> DefaultValue : aucune valeur maximale n’est appliquée.<br /> | Pour les paramètres à valeur de chaîne, spécifie la chaîne la plus longue autorisée. Les fournisseurs UI et PrintCapabilities ou PrintTicket utilisent cette propriété pour valider l’élément ParameterDef.<br /> | No<br /> | 
| MaxValue <br /> | entier si la propriété DataType spécifie un entier.<br /> Decimal si la propriété DataType spécifie Decimal.<br /> DefaultValue : aucune valeur maximale n’est appliquée.<br /> | Pour les éléments ParameterDef d’un entier ou d’une valeur décimale, définit la plus grande valeur autorisée.<br /> | No<br /> | 
| MinLength <br /> | entier si la propriété DataType spécifie String. <br /> DefaultValue : aucune valeur minimale n’est appliquée.<br /> | Pour les valeurs de chaîne, définit la chaîne la plus petite autorisée. Les fournisseurs UI et PrintCapabilities ou PrintTicket utilisent cette propriété pour valider l’élément ParameterDef.<br /> | No<br /> | 
| MinValue <br /> | entier si la propriété DataType spécifie un entier.<br /> Decimal si la propriété DataType spécifie Decimal.<br /> DefaultValue : aucune valeur minimale n’est appliquée.<br /> | Pour les paramètres de type entier ou décimal, définit la plus petite valeur autorisée. <br /> | Non<br /> | 
| Multiple <br /> | entier si la propriété DataType spécifie un entier.<br /> Decimal si la propriété DataType spécifie Decimal.<br /> DefaultValue : 1<br /> | Pour les paramètres de valeurs entières ou décimales, la valeur du paramètre doit être un multiple de ce nombre. Pour plus d’informations, consultez <a href="#notes-on-multiple">Remarques sur les multiples</a> suivants.<br /> | No<br /> | 
| Unité <br /> | valeur de chaîne indiquant les unités utilisées pour le paramètre.<br /> Pas de valeur par défaut.<br /> | Indique les unités dans lesquelles le paramètre est exprimé. Par exemple, les angles en dixièmes de degrés, les longueurs en microns, etc.<br /> | Yes<br /> | 




 

## <a name="notes-on-multiple"></a>Remarques sur plusieurs

Pour les éléments ParameterInit avec des valeurs entières ou décimales, la valeur de ParameterInit doit être un multiple de ce nombre. Par exemple, les éléments ParameterInit de valeurs décimales peuvent être limités à des dixièmes en affectant à cette propriété la valeur 0,1. Les éléments d’interface utilisateur utilisent cette propriété lorsqu’ils construisent des boîtes de dialogue et des contrôles d’interface utilisateur. En outre, le code de validation PrintTicket peut utiliser cette propriété pour arrondir la valeur d’un ParameterInit à la valeur la plus proche indiquée par multiple. Remarque : les pilotes de périphérique et les fournisseurs PrintCapabilities ne doivent pas supposer que les valeurs ParameterInit sont des multiples de cette valeur de propriété. Chaque fournisseur doit être en mesure d’arrondir des valeurs arbitraires à la valeur utilisable la plus proche en raison de la possibilité que différents fournisseurs spécifient des valeurs différentes et conflictuelles pour cette propriété.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




