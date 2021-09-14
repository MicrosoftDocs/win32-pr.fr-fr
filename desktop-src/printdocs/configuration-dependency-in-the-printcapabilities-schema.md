---
title: Dépendance de configuration PrintCapabilities
description: Les dépendances de configuration font référence au fait que certains éléments peuvent être modifiés ou même supprimés d’un document PrintCapabilities à la suivante.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20f01c8e7bd9a036a53048996ec5a38246471f67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118042"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>Dépendance de configuration dans le schéma PrintCapabilities

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le schéma PrintCapabilities correspond étroitement à l’infrastructure du schéma d’impression, en termes d’éléments utilisés et de la structure générale exprimée par les éléments parents et enfants. Les dépendances de configuration, qui se rapportent spécifiquement au PrintCapabilities, sont répertoriées ici comme une extension de l’infrastructure générale. Les dépendances de configuration font référence au fait que certains éléments, y compris leur contenu, peuvent être modifiés ou même supprimés d’un document PrintCapabilities à la suivante, en raison de dépendances sur la configuration. Même si un élément parent doit être indépendant de la configuration, ses éléments enfants peuvent avoir des dépendances. Ces dépendances sont exprimées à l’aide \* \* de constructions Switch/case dans les fichiers GPD.

En guise d’exemple de dépendance de configuration, prenez en compte les valeurs associées à chaque propriété dans le document PrintCapabilities. Chaque document PrintCapabilities peut différer dans les instances de propriété qui sont définies et dans les instances de valeur assignées à ces instances de propriété.



| Type d'élément                                                                                                                                                                             | Dépendance de configuration                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fonctionnalité <br/> Option<br/> ParameterInit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> Propriété<br/> ScoredProperty<br/> | Ces éléments ne doivent pas avoir de dépendances de configuration.<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | Les éléments ParameterDef et les éléments qu’ils contiennent dans n’importe quel niveau d’imbrication ne doivent pas avoir de dépendances de configuration.<br/>                                                                                        |
| Propriété <br/>                                                                                                                                                                     | Les éléments de propriété peuvent avoir des dépendances de configuration, sauf lorsqu’ils apparaissent dans les éléments ParameterDef.<br/>                                                                                                       |
| Valeur <br/>                                                                                                                                                                        | Les éléments de valeur qui apparaissent dans les éléments ScoredProperty ne doivent pas avoir de dépendances de configuration. Les éléments de valeur qui apparaissent dans un élément de propriété peuvent avoir des dépendances arbitraires sur la configuration.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




