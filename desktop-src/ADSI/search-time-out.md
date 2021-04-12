---
title: Délai d’expiration de la recherche
description: Un client peut également imposer une limite de temps pendant laquelle il doit attendre qu’un serveur retourne le jeu de résultats.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- Rechercher dans le délai d’expiration ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309221"
---
# <a name="search-time-out"></a>Délai d’expiration de la recherche

Un client peut également imposer une limite de temps pendant laquelle il doit attendre qu’un serveur retourne le jeu de résultats. La valeur de l’option « délai de recherche » spécifie cette limite. Lorsque le serveur ne parvient pas à répondre à une requête dans le délai spécifié, le client peut arrêter la recherche et réessayer plus tard.

La propriété de délai d’attente est utile lorsqu’un client demande une recherche asynchrone. Dans une recherche asynchrone, le client effectue une demande, puis poursuit avec d’autres tâches en attendant que le serveur retourne les résultats. Il est possible que le serveur puisse passer en mode hors connexion sans en avertir le client. Dans ce cas, le client n’a aucun moyen de reconnaître que le serveur est en train de traiter la requête, ou s’il a cessé d’être en ligne. La propriété de délai d’attente fournit au client un contrôle sur ces instances.

Pour plus d’informations sur l’utilisation de l’option de délai d’attente de recherche avec une interface de recherche spécifique, consultez :

-   [Limite de temps du client avec IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Recherche avec OLE DB](searching-with-ole-db.md)

 

 




