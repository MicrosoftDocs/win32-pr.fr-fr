---
title: Types complexes de schéma EventManifest
description: Voici les types complexes définis par le schéma EventManifest.
ms.assetid: 25facfdd-3846-4215-9b84-a833d86c39ef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d952a98bea78bab18f76da091a392e4b6247ca5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510010"
---
# <a name="eventmanifest-schema-complex-types"></a>Types complexes de schéma EventManifest

Voici les types complexes définis par le schéma EventManifest.



| Type complexe                                                                                       | Description                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BitMapType**](eventmanifestschema-bitmaptype-complextype.md)                                   | Définit une liste de mappages nom/valeur entre les valeurs de bits et les valeurs de chaîne.<br/>                                                                                                                                                  |
| [**BitMapValueType**](eventmanifestschema-bitmapvaluetype-complextype.md)                         | Définit le mappage entre une valeur de bit et une valeur de chaîne.<br/>                                                                                                                                                                  |
| [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)                         | Définit une liste de canaux auxquels les fournisseurs peuvent enregistrer des événements.<br/>                                                                                                                                                                |
| [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)                   | Définit les propriétés du fichier journal qui stocke le canal, par exemple sa capacité et s’il est séquentiel ou circulaire.<br/>                                                                                                |
| [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)             | Définit les propriétés de journalisation pour la session utilisée par le canal.<br/>                                                                                                                                                        |
| [**ChannelType**](eventmanifestschema-channeltype-complextype.md)                                 | Définit un canal auquel les fournisseurs peuvent enregistrer des événements.<br/>                                                                                                                                                                         |
| [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md)                   | Définit un élément de données que vous souhaitez inclure avec l’événement.<br/>                                                                                                                                                                 |
| [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)                           | Définit une liste d’événements que votre fournisseur peut journaliser.<br/>                                                                                                                                                                         |
| [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)                 | Définit un événement que votre fournisseur peut écrire.<br/>                                                                                                                                                                               |
| [**EventsType**](eventmanifestschema-eventstype-complextype.md)                                   | Contient une liste de fournisseurs définis dans le manifeste.<br/>                                                                                                                                                               |
| [**FilterType**](eventmanifestschema-filtertype-complextype.md)                                   | Définit un filtre de données utilisé par une session pour filtrer les événements en fonction des données d’événement.<br/>                                                                                                                                              |
| [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)                           | Définit une liste de filtres qu’un contrôleur ETW peut passer à votre fournisseur pour limiter davantage les événements qu’il écrit.<br/>                                                                                                       |
| [**ImportChannelType**](eventmanifestschema-importchanneltype-complextype.md)                     | Identifie un canal qui a été défini par un autre fournisseur ou dans un manifeste qui contient une section de métadonnées.<br/>                                                                                                            |
| [**InputType**](eventmanifestschema-inputtype-complextype.md)                                     | Définit un type de données d’entrée.<br/>                                                                                                                                                                                                  |
| [**InputTypeListType**](eventmanifestschema-inputtypelisttype-complextype.md)                     | Définit une liste de types d’entrée.<br/>                                                                                                                                                                                               |
| [**InstrumentationManifestType**](eventmanifestschema-instrumentationmanifesttype-complextype.md) | Définit le type de base pour l’élément [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) .<br/>                                                                                                |
| [**InstrumentationType**](eventmanifestschema-instrumentationtype-complextype.md)                 | Définit le contenu de la section d’instrumentation du manifeste.<br/>                                                                                                                                                         |
| [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)                         | Définit une liste de mots clés qui classent les événements.<br/>                                                                                                                                                                           |
| [**KeywordType**](eventmanifestschema-keywordtype-complextype.md)                                 | Définit un mot clé qui identifie une catégorie d’événements.<br/>                                                                                                                                                                      |
| [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)                             | Définit une liste de niveaux de gravité qui spécifient le niveau de détail d’un événement.<br/>                                                                                                                                                    |
| [**LevelType**](eventmanifestschema-leveltype-complextype.md)                                     | Définit une valeur de gravité qui détermine le niveau de détail des événements journalisés.<br/>                                                                                                                                           |
| [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)                       | Définit un groupe de ressources localisées que vous référencez dans votre manifeste.<br/>                                                                                                                                                  |
| [**MapType**](eventmanifestschema-maptype-complextype.md)                                         | Définit une liste de paires nom/valeur.<br/>                                                                                                                                                                                          |
| [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)                               | Définit les types de métadonnées que vous pouvez définir dans la section métadonnées du manifeste.<br/>                                                                                                                                      |
| [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)                           | Définit une liste de requêtes nommées qui interrogent la chaîne de message d’événement pour obtenir une valeur et effectuent une action spécifiée si elle est trouvée.<br/>                                                                                                     |
| [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)                           | Définit une liste d’OpCodes utilisés pour identifier les opérations d’un composant de l’application.<br/>                                                                                                                        |
| [**OpcodeType**](eventmanifestschema-opcodetype-complextype.md)                                   | Définit une opération dans un composant de l’application.<br/>                                                                                                                                                                  |
| [**OutputType**](eventmanifestschema-outputtype-complextype.md)                                   | Définit un type de données de sortie qui détermine la façon dont les données sont restituées.<br/>                                                                                                                                                        |
| [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md)                   | Définit une liste de paires d’expressions régulières utilisées pour modifier la chaîne de message.<br/>                                                                                                                                        |
| [**PatternMapType**](eventmanifestschema-patternmaptype-complextype.md)                           | Définit un mappage entre deux expressions régulières. Une expression est utilisée pour rechercher une chaîne correspondante dans la chaîne de message, tandis que l’autre est utilisée pour modifier la chaîne avant que le service la replace dans la chaîne de message.<br/> |
| [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md)                 | Définit les expressions régulières utilisées pour rechercher une chaîne correspondante dans la chaîne de message et la modifier.<br/>                                                                                                                           |
| [**ProviderType**](eventmanifestschema-providertype-complextype.md)                               | Définit un fournisseur et les métadonnées qu’il utilise pour définir ses événements.<br/>                                                                                                                                                       |
| [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md)                         | Définit une liste de chaînes localisées que vous pouvez référencer dans votre manifeste.<br/>                                                                                                                                                 |
| [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md)               | Définit une structure qui inclut un ou plusieurs éléments de données que vous souhaitez inclure avec l’événement.<br/>                                                                                                                            |
| [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md)         | Définit un événement spécifique à la tâche que votre fournisseur peut journaliser.<br/>                                                                                                                                                                    |
| [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)                               | Définit une liste de tâches utilisées pour identifier les composants d’une application.<br/>                                                                                                                                          |
| [**TaskType**](eventmanifestschema-tasktype-complextype.md)                                       | Définit un composant ou un sous-composant d’une application.<br/>                                                                                                                                                                       |
| [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md)                       | Modèle qui définit les données à inclure avec un événement.<br/>                                                                                                                                                                   |
| [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md)                       | Définit une liste de modèles qui spécifient les données à inclure avec les événements.<br/>                                                                                                                                                |
| [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)                               | Définit les types utilisés dans le manifeste.<br/>                                                                                                                                                                             |
| [**ValueMapType**](eventmanifestschema-valuemaptype-complextype.md)                               | Définit une liste de mappages nom/valeur entre les valeurs entières et les valeurs de chaîne.<br/>                                                                                                                                              |
| [**ValueMapValueType**](eventmanifestschema-valuemapvaluetype-complextype.md)                     | Définit le mappage entre une valeur entière et une valeur de chaîne.<br/>                                                                                                                                                             |
| [**XmlType**](eventmanifestschema-xmltype-complextype.md)                                         | Définit un fragment XML.<br/>                                                                                                                                                                                                     |
| [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)                         | Définit une liste de types de sortie que le service utilise pour déterminer comment restituer un type de données d’entrée.<br/>                                                                                                                             |



 

 

 





