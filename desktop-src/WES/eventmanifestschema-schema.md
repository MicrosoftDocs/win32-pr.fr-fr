---
title: Schéma EventManifest
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 'En savoir plus sur : schéma EventManifest'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8b282a3570c7ddc510f55c012a13b9438108693a3b6abba06de08ce1da59d734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055847"
---
# <a name="eventmanifest-schema"></a>Schéma EventManifest

Le schéma EventManifest définit les éléments et types suivants que vous utilisez pour écrire un manifeste d’Instrumentation :

-   [Éléments EventManifestSchema](eventmanifestschema-elements.md)
-   [Types simples EventManifestSchema](eventmanifestschema-simple-types.md)
-   [Types complexes EventManifestSchema](eventmanifestschema-complex-types.md)

La section éléments contient les noms des éléments que vous utilisez dans votre manifeste ; Toutefois, pour obtenir les détails de chaque élément, consultez le type complexe qui contient l’élément.

Un manifeste d’instrumentation est un fichier XML qui définit un fournisseur d’événements, les canaux sur lesquels les événements sont écrits, les événements eux-mêmes, les critères de filtrage des événements tels que les niveaux, les tâches et les OpCodes, ainsi que les chaînes localisées utilisées lors du rendu des événements. La Convention consiste à utiliser. Man comme extension pour les fichiers manifeste. Pour plus d’informations sur l’écriture d’un manifeste, consultez [écriture d’un manifeste d’instrumentation](writing-an-instrumentation-manifest.md).

le SDK Windows inclut le schéma dans le \\ fichier include \\ eventic. xsd. Vous pouvez utiliser le XSD pour valider votre manifeste.

outre le schéma EventManifest, Windows journal des événements définit également les schémas suivants :

-   [Schéma d’événement](eventschema-schema.md): définit les éléments et les types utilisés pour le rendu d’un événement.
-   [Schéma de requête](queryschema-schema.md): définit les éléments et les types utilisés pour écrire une requête afin de récupérer des événements à partir d’un ou plusieurs canaux.

 

 




