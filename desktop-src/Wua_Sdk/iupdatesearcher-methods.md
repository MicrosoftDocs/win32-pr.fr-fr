---
description: L’interface IUpdateSearcher définit les méthodes suivantes.
ms.assetid: 82735555-b23a-43b0-bf5b-a8cf72dc40d4
title: Méthodes IUpdateSearcher
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf2207f92fb0eae48b79641109e9218bc993f2048d5ec623ea1d476424457f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106470"
---
# <a name="iupdatesearcher-methods"></a>Méthodes IUpdateSearcher

L’interface [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) définit les méthodes suivantes.



| Méthode                                                              | Description                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)                   | Commence l’exécution d’une recherche asynchrone des mises à jour. La recherche utilise les options de recherche qui sont actuellement configurées. |
| [**EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)                       | Termine une recherche asynchrone des mises à jour.                                                                             |
| [**EscapeString**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-escapestring)                 | Convertit une chaîne en une chaîne qui peut être utilisée comme valeur littérale dans une chaîne de critères de recherche.                          |
| [**GetTotalHistoryCount**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-gettotalhistorycount) | Retourne le nombre d’événements de mise à jour sur l’ordinateur.                                                                      |
| [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-queryhistory)                | Interroge de manière synchrone l’ordinateur sur l’historique des événements de mise à jour.                                                      |
| [**Recherche**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search)                             | Effectue une recherche synchrone des mises à jour. La recherche utilise les options de recherche qui sont actuellement configurées.              |



 

 

 



