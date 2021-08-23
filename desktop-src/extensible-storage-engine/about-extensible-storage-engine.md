---
description: 'en savoir plus sur : à propos du moteur de Stockage Extensible'
title: à propos du moteur de Stockage Extensible
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 26a1d4d28f1d5957432202545ff94c4f18c37e5a521e0deadfdabfb72751adec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983869"
---
# <a name="about-extensible-storage-engine"></a>à propos du moteur de Stockage Extensible


_**s’applique à :** Exchange Server 2013 | Windows | Windows Serveurs_

## <a name="about-extensible-storage-engine"></a>à propos du moteur de Stockage Extensible

Le moteur ESE (Extensible Storage Engine) est un moteur de base de données qui stocke les informations dans une séquence logique. Les informations peuvent être récupérées de manière séquentielle ou en accédant à des index définis. Les mises à jour de la base de données sont implémentées avec une transaction afin de garantir des opérations sécurisées. Le moteur ESE permet un accès simultané à plusieurs bases de données, notamment des bases de données de fichiers journaux de transactions qui peuvent être utilisées pour la récupération du système. ESE est évolutif pour des applications volumineuses ou de petite taille. Les fonctionnalités suivantes sont disponibles avec l’interface de programmation d’applications (API) ESE :

  - Sauvegarde et restauration : une application peut créer des copies cohérentes de l’état des données pendant qu’elle est en ligne et modifie activement l’état des données.

  - Navigation dans les curseurs : l’application peut naviguer avec le curseur pour accéder aux données de manière séquentielle ou à l’aide d’index.

  - Base de données : collection de tables qui sont sauvegardées et restaurées en tant qu’unité unique.

  - Journalisation et récupération après incident : l’API ESE garantit que la cohérence des données définie par l’application est honorée même en cas de panne du système.

  - Tables : structure fondamentale de la base de données ESE utilisée pour stocker les données.

  - Transaction : le moteur de base de données ESE fournit des transactions (ACID) durables isolées cohérentes atomiques qui permettent aux applications de récupérer des données uniquement à partir d’États de données fiables et gèrent la cohérence des données en cas d’arrêt inattendu du processus ou d’arrêt du système.

  - Scalable : l’application peut créer des bases de données aussi volumineuses que 100 Go ou une taille de 1 Mo.

