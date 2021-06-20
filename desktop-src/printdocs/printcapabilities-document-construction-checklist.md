---
description: Cet article fournit une liste de vérification que les auteurs de documents PrintCapabilities peuvent utiliser pour créer un document PrintCapabilities qui décrit un appareil.
ms.assetid: 4b8fa1a4-6461-4722-861b-354f206b2a73
title: Liste de vérification de la construction de document PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee309c96cf7b2d70cb78f125e7783668fb2298da
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407112"
---
# <a name="printcapabilities-document-construction-checklist"></a>Liste de vérification de la construction de document PrintCapabilities

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le [Résumé des types d’éléments](summary-of-element-types.md) présente les différents éléments qui composent un document PrintCapabilities. Cette section fournit une liste de vérification que les auteurs de documents PrintCapabilities peuvent utiliser pour créer un document PrintCapabilities qui décrit un appareil.

1.  Identifiez tous les attributs d’appareil qui contribuent à la configuration de l’appareil. Pour chaque attribut d’appareil, déterminez s’il doit être représenté en tant que construction fonctionnalité/option ou en tant que construction de paramètre.

2.  Pour chaque fonctionnalité de l’appareil, déterminez si elle peut être représentée par une fonctionnalité définie dans les mots clés du schéma d’impression. Si ce n’est pas le cas, vous devez introduire une nouvelle fonctionnalité définie en privé (et un attribut de nom correspondant).

    -   Pour les instances de fonctionnalités définies par les mots clés du schéma d’impression, identifiez chacun des États disponibles auxquels cette fonctionnalité peut être définie. Chaque État correspond à une option de l’instance de fonctionnalité. Déterminez lequel de ces États correspond aux instances d’option définies par schéma d’impression associées à cette fonctionnalité et les États qui requièrent une instance d’option personnalisée. La rubrique [définitions d’option](option-definitions.md) présente des informations sur la façon de construire de nouvelles instances d’option et sur la façon de dériver de nouvelles instances d’option à partir d’instances d’option existantes.

    -   Pour les instances de fonctionnalités non standard, identifiez les caractéristiques qui peuvent être utilisées pour distinguer une option d’une autre. Représentent chaque caractéristique par un élément ScoredProperty et, dans chaque instance d’option, attribuez à chaque ScoredProperty une valeur spécifique à cette option. Assurez-vous qu’il y a suffisamment d’éléments ScoredProperty pour que chaque option d’une fonctionnalité donnée soit unique. Les instances de fonctionnalité et d’option non standard sont de leur nature non portable. Autrement dit, un autre pilote ne sera pas en mesure de trouver une fonctionnalité ou une option équivalente pour correspondre à une fonctionnalité ou une option non standard spécifiée dans le PrintTicket créé par votre pilote.

3.  Déterminez si une option doit contenir des éléments ParameterRef. Pour plus d’informations, consultez [constructions de paramètres](parameter-constructs.md) et éléments de référence de [paramètre](parameter-reference-elements.md).

4.  Pour les paramètres, déterminez si l’une des instances ParameterDef définies dans les mots clés du schéma d’impression est une correspondance appropriée. Dans ce cas, copiez l’instance ParameterDef à partir des mots clés du schéma d’impression et ajustez la valeur de chaque instance de propriété mutable pour le meilleur ajustement. Si aucune des instances ParameterDef dans les mots clés du schéma d’impression ne correspond à une correspondance appropriée, créez votre propre instance ParameterDef. Pour plus d’informations, consultez [paramètres dans le document PrintCapabilities](parameters-in-the-printcapabilities-document.md).

5.  Assurez-vous que toutes les instances Property et ScoredProperty requises par le document des mots clés du schéma d’impression sont présentes dans votre document PrintCapabilities, et qu’ils sont correctement initialisés.

6.  Ajoutez des instances de propriété et de sous-propriété supplémentaires selon vos besoins. Vous pouvez introduire des instances de propriété définies de manière privée si des aspects de l’appareil que vous devez caractériser ne sont pas couverts par les instances de propriété définies dans les mots clés du schéma d’impression.

7.  Observez la Convention d’espace de noms pour les attributs Name. Cela s’applique aux attributs de nom définis en privé, ainsi qu’à ceux définis dans les mots clés du schéma d’impression.

8.  Les enfants du même type d’élément ne peuvent pas s’imbriquer jusqu’à une profondeur de plus de 10 éléments. Cette règle s’applique indépendamment à chaque type d’élément qui peut être défini.

Notez que les fonctionnalités d’impression du document XML doivent être encodées au format UTF-8 ou UTF-16.

Notez que l’ensemble des instances Feature, option et ParameterDef signalées ne doit pas changer, quelle que soit la capture instantanée. Les instances ScoredProperty qui composent chaque instance d’option et la valeur assignée à chaque élément ScoredProperty ne doivent pas non plus changer. Il en va de même pour les instances de propriété qui composent chaque instance ParameterDef.

Pour obtenir la liste des instances de propriété supplémentaires qui doivent être fournies pour définir entièrement des constructions et des paramètres de fonctionnalité/option, consultez [ParameterDef](parameterdef.md) et [ParameterInit](parameterinit.md). Par exemple, chaque fonctionnalité doit spécifier son comportement d’interface utilisateur, en particulier s’il est possible de sélectionner exactement une ou plusieurs instances d’option pour chaque fonctionnalité à un moment donné. Le document Mots clés du schéma d’impression définit ces instances de propriété, où elles doivent apparaître dans le document PrintCapabilities, et quelles instances de valeur définies dans les mots clés de schéma d’impression sont disponibles.

Le fournisseur PrintCapabilities est chargé d’émettre la valeur appropriée pour toutes les instances de propriétés dépendantes de la configuration. Par exemple, si le taux d’impression dépend à la fois du mode colorimétrique et de la résolution utilisée, le fournisseur PrintCapabilities doit noter les paramètres de mode colorimétrique et de résolution spécifiés dans le PrintTicket fourni par le client, et doit signaler la valeur appropriée pour le taux d’impression. Notez que chaque instance ScoredProperty doit être à valeur unique ; son instance de valeur ne peut pas changer en cas de modification de la configuration de l’appareil.

Notez également que les instances de propriété définies dans les mots clés du schéma d’impression doivent apparaître à l’emplacement spécifié. Ils ne peuvent pas apparaître à des emplacements arbitraires dans un document PrintCapabilities. Les instances de propriété définies de manière privée peuvent apparaître n’importe où, même en tant que sous-propriétés dans des instances de propriété définies par schéma.

Notez qu’un conflit fonctionnel entre les paramètres est défini comme deux éléments de schéma d’impression non conflictuels qui ont une fonction similaire, mais qui sont des fonctionnalités différentes. Par exemple, JobDuplexAllDocumentsContiguously et DocumentDuplex ; tous deux représentent la fonction duplex de l’appareil, mais diffèrent dans l’application de la fonction, l’un s’applique à l’ensemble du travail de façon contiguë et l’autre à des documents. Dans le cas où deux éléments de ce type sont spécifiés, la priorité est déterminée par le producteur PrintCapabilities et le consommateur PrintTicket. Il incombe au producteur PrintCapabilities d’indiquer correctement les contraintes entre les éléments en conflit par le biais de l’attribut « contrainte ». Les éléments du schéma d’impression public qui présentent ce conflit sémantique sont identifiés dans leur définition.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



