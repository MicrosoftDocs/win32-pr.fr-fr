---
title: Enregistrement des erreurs dans l'API du serveur HTTP
description: Certains types d’erreurs sont gérés par l’API du serveur HTTP au lieu d’être retransmis à une application pour la gestion, car la fréquence de ces erreurs pourrait autrement saturer un journal des événements ou un gestionnaire d’applications.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API serveur HTTP, journalisation des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c92c071929b61020b456d8ecabc81ebc0f05503c2f385b235afc323cf8dea33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130679"
---
# <a name="error-logging-in-the-http-server-api"></a>Enregistrement des erreurs dans l'API du serveur HTTP

Certains types d’erreurs sont gérés par l’API du serveur HTTP au lieu d’être retransmis à une application pour la gestion, car la fréquence de ces erreurs pourrait autrement saturer un journal des événements ou un gestionnaire d’applications.

Les trois rubriques suivantes décrivent les différents aspects de la journalisation des erreurs de l’API du serveur HTTP :

-   [Configuration](configuring-http-server-api-error-logging.md) de Les paramètres de Registre contrôlent si l’API du serveur HTTP journalise des erreurs, la taille maximale autorisée des fichiers journaux et l’emplacement où les fichiers journaux sont enregistrés.
-   [Format du fichier journal](format-of-the-http-server-api-error-logs.md) L’API du serveur HTTP crée des fichiers journaux conformes aux conventions des fichiers journaux du World Wide Web Consortium (W3C) et peut être analysée à l’aide d’outils standard. Toutefois, contrairement aux fichiers journaux W3C, les fichiers journaux de l’API du serveur HTTP ne contiennent pas de noms de colonnes.
-   [Types d’erreurs consignées](types-of-errors-logged-by-the-http-server-api.md) L’API du serveur HTTP enregistre une série d’erreurs courantes.

 

 




