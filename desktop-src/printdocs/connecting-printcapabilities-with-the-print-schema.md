---
description: En savoir plus sur le schéma PrintCapabilities général, qui couvre la structure, l’objectif et l’utilisation des différents types d’éléments.
ms.assetid: 2f6c51a3-003c-4d68-9e4d-9be5d325a477
title: Connexion de PrintCapabilities au schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661a8eb93c6f788381713c0c6620e8a09a53648f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118038"
---
# <a name="connecting-printcapabilities-with-the-print-schema"></a>Connexion de PrintCapabilities au schéma d’impression

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le schéma PrintCapabilities général couvre la structure, l’objectif et l’utilisation des différents types d’éléments. Elle spécifie l’attribut Name utilisé pour définir des instances spécifiques de chaque type d’élément. Il spécifie que les auteurs PrintCapabilities peuvent utiliser des instances d’éléments définies par les mots clés du schéma d’impression, ou ils peuvent introduire leurs propres instances définies en privé, à condition que ces instances définies de manière privée soient définies dans un espace de noms clairement identifié comme leur propre. (Les auteurs PrintCapabilities peuvent également utiliser des instances définies précédemment dans un autre espace de noms privé.)

Le document Mots clés du schéma d’impression définit les instances spécifiques de chaque type d’élément pouvant être utilisé dans les documents PrintCapabilities et dans des PrintTicket. Il documente également leur objectif et leur utilisation. Le document des mots clés du schéma d’impression définit également des instances de plusieurs types d’éléments, comme suit :

-   Instances de propriété et de sous-propriété qui résident à la racine du document PrintCapabilities

    -   Ces éléments décrivent les différents aspects et fonctionnalités de l’appareil et fournissent un vocabulaire commun pour la description des appareils.

-   Instances de propriété et de sous-propriété qui sont des enfants d’éléments de fonctionnalité

    -   Ces éléments décrivent différents aspects liés à une fonctionnalité spécifique.

-   Instances de propriété et de sous-propriété qui sont des enfants d’éléments option

    -   Ces éléments décrivent les différents aspects et fonctionnalités de l’appareil qui dépendent de l’option sélectionnée pour une fonctionnalité spécifique. Elles peuvent être remplacées par des instances de propriété situées à la racine du document PrintCapabilities, mais offrent des avantages supplémentaires dans certains cas. Pour plus d’informations, consultez [Ajout d’instances de propriété](adding-property-instances.md).

<!-- -->

-   Instances ScoredProperty

    -   Les instances ScoredProperty définissent la langue utilisée pour caractériser une option. Les instances ScoredProperty définies dans les mots clés du schéma d’impression permettent aux instances d’option écrites par de nombreuses parties différentes d’être portables pour de nombreux appareils, et d’être compréhensibles par tout autre pilote de périphérique ou tout autre fournisseur PrintCapabilities ou PrintTicket.

-   Instances de valeur ScoredProperty

    -   Ces instances de valeur sont fournies pour la même raison que les instances ScoredProperty sont fournies.

-   Instances de fonctionnalités

    -   Chaque option doit appartenir à une fonctionnalité spécifique, ce qui nécessite la définition de la fonctionnalité elle-même.

-   Instances ParameterDef

    -   Une instance ParameterDef fournie par des mots clés de schéma d’impression définit également une valeur pour chaque propriété qu’elle contient. Le fournisseur PrintCapabilities est libre de modifier les instances de valeur pour les instances de propriété qui peuvent être modifiées. Pour plus d’informations sur les instances de propriété qui peuvent être modifiées et celles qui ne peuvent pas être modifiées (elles sont immuables), consultez [éléments ParameterDef et ParameterInit](parameterdef-and-parameterinit-elements.md).

Il est important de noter que le schéma PrintCapabilities ne nomme aucune instance d’option. Les instances d’option se caractérisent uniquement par leurs instances ScoredProperty prises dans leur ensemble. Une idée fausse courante est que l’utilisation de l’attribut’name’pour définir une option identifie des instances d’option, mais cela est incorrect. Il n’est pas nécessaire que les éléments option soient uniques pour les instances d’option frères, ni l’attribut’name’pour définir une option requise.

Le document Mots clés du schéma d’impression définit un espace de noms standard auquel appartiennent tous les attributs de nom d’instance des schémas PrintCapabilities et PrintTicket. Toutes les balises de type d’élément et les attributs XML utilisés par les types d’éléments appartiennent également à cet espace de noms.

Pour chaque instance définie dans le schéma PrintCapabilities, le schéma PrintCapabilities spécifie à la fois l’attribut Name et l’emplacement de l’instance. Le fournisseur et le client doivent conserver les deux lors de l’utilisation de cette instance dans leur document PrintCapabilities ou PrintTicket.

Le document Mots clés du schéma d’impression désigne certaines instances comme obligatoires. Ces instances doivent apparaître dans chaque document PrintCapabilities et doivent être correctement initialisées avec des valeurs valides. Toutes les instances des mots clés du schéma d’impression qui ne sont pas désignés comme obligatoires sont facultatives.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



