---
title: Délai d’expiration de la recherche
description: Un client peut également imposer une limite de temps pendant laquelle il doit attendre qu’un serveur retourne le jeu de résultats.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- Rechercher dans le délai d’expiration ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e99b287c1bc0ba0da5e39b579c4a454eae821cf2c443930a5ae0376412e2c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082303"
---
# <a name="search-time-out"></a>Délai d’expiration de la recherche

Un client peut également imposer une limite de temps pendant laquelle il doit attendre qu’un serveur retourne le jeu de résultats. La valeur de l’option « délai de recherche » spécifie cette limite. Lorsque le serveur ne parvient pas à répondre à une requête dans le délai spécifié, le client peut arrêter la recherche et réessayer plus tard.

La propriété de délai d’attente est utile lorsqu’un client demande une recherche asynchrone. Dans une recherche asynchrone, le client effectue une demande, puis poursuit avec d’autres tâches en attendant que le serveur retourne les résultats. Il est possible que le serveur puisse passer en mode hors connexion sans en avertir le client. Dans ce cas, le client n’a aucun moyen de reconnaître que le serveur est en train de traiter la requête, ou s’il a cessé d’être en ligne. La propriété de délai d’attente fournit au client un contrôle sur ces instances.

Pour plus d’informations sur l’utilisation de l’option de délai d’attente de recherche avec une interface de recherche spécifique, consultez :

-   [Limite de temps du client avec IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Recherche avec OLE DB](searching-with-ole-db.md)

 

 




