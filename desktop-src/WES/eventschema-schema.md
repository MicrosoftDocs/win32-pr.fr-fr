---
title: Schéma d’événement
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: En savoir plus sur le schéma d’événement
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bfb26f6c71d544e0c0a6a4d833b40a5d15ae5485
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311126"
---
# <a name="event-schema"></a>Schéma d’événement

Le schéma d’événement définit les éléments et types suivants qui identifient les éléments et les attributs d’un événement enregistré :

-   [Éléments EventSchema](eventschema-elements.md)
-   [Types simples EventSchema](eventschema-simple-types.md)
-   [Types complexes EventSchema](eventschema-complex-types.md)

La section éléments contient les noms des éléments que vous trouverez dans les événements journalisés. Toutefois, pour obtenir les détails de chaque élément, consultez le type complexe qui contient l’élément.

le SDK Windows inclut le schéma dans le \\ fichier include \\ Event. xsd.

Vous pouvez utiliser ce schéma pour identifier les éléments et les attributs lors de l’appel de la fonction [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) pour afficher des sections ou des propriétés spécifiques de l’événement. Pour obtenir un exemple qui montre comment utiliser ce schéma lors du rendu des événements, consultez [rendu des événements](rendering-events.md).

outre le schéma d’événement, Windows journal des événements définit également les schémas suivants :

-   [Schéma EventManifest](eventmanifestschema-schema.md): définit les éléments et les types utilisés pour écrire un manifeste d’instrumentation.
-   [Schéma de requête](queryschema-schema.md): définit les éléments et les types utilisés pour écrire une requête afin de récupérer des événements à partir d’un ou plusieurs canaux.

 

 




