---
description: L’interface IUpdateSearcher définit les méthodes suivantes.
ms.assetid: 82735555-b23a-43b0-bf5b-a8cf72dc40d4
title: Méthodes IUpdateSearcher
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462cbd371546743bab836ed1cdc2479e30f13612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514638"
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



 

 

 



