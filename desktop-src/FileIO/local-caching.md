---
description: La mise en cache locale des données est une technique utilisée pour accélérer l’accès réseau aux fichiers de données. Cela implique la mise en cache des données sur les clients plutôt que sur des serveurs lorsque cela est possible.
ms.assetid: a7eb24b3-7e23-4798-8584-30a171fa4f04
title: Mise en cache locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8132bc51831db752422de1e3071ee3ef0b33a1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009920"
---
# <a name="local-caching"></a>Mise en cache locale

*La mise en cache locale* des données est une technique utilisée pour accélérer l’accès réseau aux fichiers de données. Cela implique la mise en cache des données sur les clients plutôt que sur des serveurs lorsque cela est possible.

L’effet de la mise en cache locale est qu’elle permet de combiner plusieurs opérations d’écriture sur la même région d’un fichier en une seule opération d’écriture sur le réseau. La mise en cache locale réduit le trafic réseau, car les données sont écrites une seule fois. Une telle mise en cache améliore le temps de réponse apparent des applications, car les applications n’attendent pas que les données soient envoyées sur le serveur via le réseau.

La mise en cache locale des données à lire peut s’avérer très rapide pour accélérer la lecture. Un exemple simple est une application qui accède aux données de manière séquentielle, par exemple le préprocesseur d’un compilateur. Dans ce cas, la couche réseau du système d’exploitation lit les données sur le réseau avant que l’application ne demande les données. Dans l’idéal, le réseau remet les données avant que l’application le demande à partir du système de fichiers, ce qui se traduit par une réponse quasi instantanée. Dans la pratique, cela se produit rarement, mais la lecture anticipée accélère les applications en anticipant la requête suivante.

La mise en cache locale peut également contribuer à réduire le trafic réseau en lisant une partie d’un fichier sur le réseau, puis en le conservant dans le cache local. Les opérations de lecture suivantes effectuées sur cette partie par l’application sont lues à partir du cache local.

Un type d’application pouvant tirer parti de la mise en cache locale est un fichier de commandes. Les processeurs de commandes lisent et exécutent un fichier de commandes une ligne à la fois. Pour chaque ligne, le processeur de commandes ouvre le fichier, effectue une recherche au début de la ligne, lit jusqu’à ce qu’il en a besoin, ferme le fichier, puis exécute la ligne. Chaque ligne entraîne une grande quantité de trafic réseau. Le trafic réseau peut être considérablement réduit en mettant en cache l’ensemble du fichier de commandes sur un client.

La mise en cache locale facilite également l’utilisation d’un autre problème lié aux réseaux, en particulier les réseaux qui effectuent des opérations sur les modems et autres canaux fins : temps de réponse lent. Les utilisateurs ne veulent pas attendre que les données soient récupérées sur le réseau, modifiées, puis réécrites. Avec la lecture anticipée et la mise en cache des écritures, il semble souvent que ces fonctions fonctionnent beaucoup plus rapidement qu’en réalité.

Un risque de mise en cache locale est que les données écrites ont uniquement une intégrité aussi importante que le client lui-même tant que les données sont mises en cache sur le client. En général, les données localement mises en cache doivent être vidées sur le serveur dès que possible. Avec les systèmes d’exploitation et la prise en charge du matériel modernes, tels que les onduleurs, le risque de perdre des données en cache localement est réduit. Mais le risque existe toujours et vous devez prendre en compte le compromis entre l’intégrité des données et la vitesse de réponse apparente et le compromis entre l’intégrité des données et le trafic réseau réduit.

 

 



