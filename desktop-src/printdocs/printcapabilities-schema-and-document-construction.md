---
title: Schémas et documents PrintCapabilities
description: Le schéma PrintCapabilities est destiné à éliminer la plupart des limitations des fonctions Win32 DevCaps.
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd79c81beceecea4a660fd2376a759e470670a414a7cad4a8ac26be086688e15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711619"
---
# <a name="printcapabilities-schema-and-document-construction"></a>Schéma PrintCapabilities et construction de document

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Les fonctions DevCaps Win32 actuelles (telles que GetDeviceCaps ou DeviceCapabilities, décrites dans la documentation du kit de développement logiciel (SDK) de Microsoft Platform) limitent sérieusement le type d’informations que les composants non pilotes peuvent obtenir, en ce qui concerne les fonctionnalités et les propriétés des périphériques d’impression. Il n’existe pas de prise en charge pour la publication des fonctionnalités des processeurs d’impression, ni de méthode pour énumérer les fonctionnalités non standard. Par conséquent, il n’existe aucun moyen pour un composant autre qu’un pilote de construire une interface utilisateur complète. En outre, le client ou l’application ne peut pas déterminer complètement les fonctionnalités des appareils ou des files d’attente d’impression au-delà de celles fournies par les fonctions Win32 DevCaps. Les fonctions actuelles ne sont pas extensibles, de sorte que les appareils ne peuvent pas publier de nouvelles propriétés ou fonctionnalités.

Le schéma PrintCapabilities est destiné à éliminer la plupart des limitations des fonctions Win32 DevCaps en fournissant un sur-ensemble des fonctionnalités offertes par ces fonctions. Si davantage de fonctionnalités sont nécessaires, un fournisseur du document PrintCapabilities peut étendre les mots clés du schéma d’impression, dans les contraintes de l’infrastructure du schéma d’impression, en ajoutant des instances d’éléments définies de manière privée. En raison de sa dépendance vis-à-vis du XML en tant que moyen d’échange, tout consommateur d’un document PrintCapabilities peut accéder à toutes les données du document sans restriction et sans se soucier de la compatibilité avec les différentes versions de système d’exploitation. Cette section décrit le schéma PrintCapabilities et détaille son utilisation.

Le public visé pour cette section comprend les groupes suivants :

-   Implémenteurs de l’interface de fournisseur PrintTicket/PrintCapabilities

-   Consommateurs de PrintCapabilities

-   Clients de l’interface du fournisseur PrintTicket/PrintCapabilities

La première catégorie de la liste précédente est appelée fournisseurs PrintCapabilities dans le reste de cette section. Les deuxième et troisième catégories sont appelées consommateurs PrintCapabilities.

## <a name="relationship-to-print-schema-and-printticket-schema"></a>Relation avec le schéma d’impression et le schéma PrintTicket

Les schémas PrintCapabilities et PrintTicket sont des parties spécialisées du schéma d’impression. Les principales différences structurelles entre ces sous-ensembles du schéma d’impression sont que le schéma PrintCapabilities inclut des instances Property et ParameterDef qui ne sont pas contenues dans le schéma PrintTicket, tandis que le schéma PrintTicket contient des instances Property et ParameterInit qui ne sont pas contenues dans le schéma PrintCapabilities. À l’exception de ces différences, les schémas PrintCapabilities et PrintTicket sont généralement mis en miroir l’un de l’autre dans le contenu, en partageant les fonctionnalités, les options, les ScoredProperty et les instances de valeur. Tout contenu partagé doit être tenu à jour. Par exemple, si une modification est apportée à la fonctionnalité PageMediaSize dans le schéma PrintCapabilities, la même modification doit être apportée dans le schéma PrintTicket.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



