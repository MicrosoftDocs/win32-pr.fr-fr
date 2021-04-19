---
title: Limite de durée de recherche
description: Lorsque vous demandez une recherche sur un serveur qui se trouve sous une charge de travail lourde, vous pouvez demander au serveur de limiter la recherche à une limite de temps spécifiée.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- Temps de recherche limité par ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ff9de38a17fe6ebac4ebb045e2f8b896bc764
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513443"
---
# <a name="search-time-limit"></a>Limite de durée de recherche

Lorsque vous demandez une recherche sur un serveur qui se trouve sous une charge de travail lourde, vous pouvez demander au serveur de limiter la recherche à une limite de temps spécifiée. Par exemple, pour exécuter une application afin de générer un rapport hebdomadaire sur un serveur qui s’exécute presque, et pour éviter de maximiser le temps processeur et empêcher l’exécution d’autres tâches, vous pouvez définir la durée de la recherche sur une valeur faible et réexécuter l’application ultérieurement si elle ne parvient pas à générer le rapport.

Certains serveurs peuvent imposer leur propre limite de temps d’administration. Dans ce cas, si vous spécifiez une valeur de limite de temps de recherche supérieure à la limite de temps d’administration, le serveur ignore votre spécification et utilise plutôt sa limite de temps d’administration interne.

Pour plus d’informations sur l’utilisation de l’option de limite de temps de recherche avec une interface de recherche spécifique, consultez :

-   [Limite de temps du serveur avec IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Recherche avec OLE DB](searching-with-ole-db.md)

 

 




