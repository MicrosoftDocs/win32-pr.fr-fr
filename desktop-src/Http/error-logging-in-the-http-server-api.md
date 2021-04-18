---
title: Enregistrement des erreurs dans l'API du serveur HTTP
description: Certains types d’erreurs sont gérés par l’API du serveur HTTP au lieu d’être retransmis à une application pour la gestion, car la fréquence de ces erreurs pourrait autrement saturer un journal des événements ou un gestionnaire d’applications.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API serveur HTTP, journalisation des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988d87a65c914625623c3f55d33a7f8cc9a4f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512026"
---
# <a name="error-logging-in-the-http-server-api"></a>Enregistrement des erreurs dans l'API du serveur HTTP

Certains types d’erreurs sont gérés par l’API du serveur HTTP au lieu d’être retransmis à une application pour la gestion, car la fréquence de ces erreurs pourrait autrement saturer un journal des événements ou un gestionnaire d’applications.

Les trois rubriques suivantes décrivent les différents aspects de la journalisation des erreurs de l’API du serveur HTTP :

-   [Configuration](configuring-http-server-api-error-logging.md) de Les paramètres de Registre contrôlent si l’API du serveur HTTP journalise des erreurs, la taille maximale autorisée des fichiers journaux et l’emplacement où les fichiers journaux sont enregistrés.
-   [Format du fichier journal](format-of-the-http-server-api-error-logs.md) L’API du serveur HTTP crée des fichiers journaux conformes aux conventions des fichiers journaux du World Wide Web Consortium (W3C) et peut être analysée à l’aide d’outils standard. Toutefois, contrairement aux fichiers journaux W3C, les fichiers journaux de l’API du serveur HTTP ne contiennent pas de noms de colonnes.
-   [Types d’erreurs consignées](types-of-errors-logged-by-the-http-server-api.md) L’API du serveur HTTP enregistre une série d’erreurs courantes.

 

 




