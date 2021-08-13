---
title: Limite de durée de recherche
description: Lorsque vous demandez une recherche sur un serveur qui se trouve sous une charge de travail lourde, vous pouvez demander au serveur de limiter la recherche à une limite de temps spécifiée.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- Temps de recherche limité par ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b666b41db67872cd418cca2d4ef2e3d766fbc1a1d1c1a2d9945eec7dfceb2429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690514"
---
# <a name="search-time-limit"></a>Limite de durée de recherche

Lorsque vous demandez une recherche sur un serveur qui se trouve sous une charge de travail lourde, vous pouvez demander au serveur de limiter la recherche à une limite de temps spécifiée. Par exemple, pour exécuter une application afin de générer un rapport hebdomadaire sur un serveur qui s’exécute presque, et pour éviter de maximiser le temps processeur et empêcher l’exécution d’autres tâches, vous pouvez définir la durée de la recherche sur une valeur faible et réexécuter l’application ultérieurement si elle ne parvient pas à générer le rapport.

Certains serveurs peuvent imposer leur propre limite de temps d’administration. Dans ce cas, si vous spécifiez une valeur de limite de temps de recherche supérieure à la limite de temps d’administration, le serveur ignore votre spécification et utilise plutôt sa limite de temps d’administration interne.

Pour plus d’informations sur l’utilisation de l’option de limite de temps de recherche avec une interface de recherche spécifique, consultez :

-   [Limite de temps du serveur avec IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Recherche avec OLE DB](searching-with-ole-db.md)

 

 




