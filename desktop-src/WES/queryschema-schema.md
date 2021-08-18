---
title: Schéma de requête
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 'En savoir plus sur : schéma de requête'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14beeaf8c4d739e490de972107fedf279e16e75b5401f63a709d43b03c338c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005169"
---
# <a name="query-schema"></a>Schéma de requête

Le schéma de requête définit les éléments et types suivants que vous pouvez utiliser pour écrire une requête XML structurée afin de récupérer des événements à partir d’un canal ou d’un fichier journal :

-   [Éléments QuerySchema](queryschema-elements.md)
-   [Types complexes QuerySchema](queryschema-complex-types.md)

La section éléments contient les noms des éléments que vous utilisez dans votre requête ; Toutefois, pour obtenir les détails de chaque élément, consultez le type complexe qui contient l’élément.

Une requête peut contenir une ou plusieurs expressions XPath utilisées pour inclure ou exclure un événement dans le jeu de résultats de la requête. Vous pouvez rechercher des événements à partir de plusieurs canaux ou fichiers journaux, mais vous ne pouvez pas mélanger des canaux et des fichiers journaux. Vous pouvez utiliser une requête dans toute fonction qui accepte un XPath (par exemple, les fonctions [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ). Chaque XPath que vous spécifiez est limité à 32 expressions. Pour obtenir un exemple, consultez [consommation d’événements](consuming-events.md).

le SDK Windows inclut le schéma dans le \\ fichier include \\ Query. xsd.

outre le schéma de requête, Windows journal des événements définit également les schémas suivants :

-   [Schéma EventManifest](eventmanifestschema-schema.md): définit les éléments et les types utilisés pour écrire un manifeste d’instrumentation.
-   [Schéma d’événement](eventschema-schema.md): définit les éléments et les types utilisés pour le rendu d’un événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Événements de consommation](consuming-events.md)
</dt> </dl>

 

 




