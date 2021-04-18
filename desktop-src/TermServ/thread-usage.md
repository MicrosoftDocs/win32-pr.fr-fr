---
title: Utilisation de threads
description: Vous devez ajuster et équilibrer l’utilisation des threads d’application pour un environnement multi-utilisateur, multiprocesseur Services Bureau à distance.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509582"
---
# <a name="thread-usage"></a>Utilisation de threads

Les threads offrent un moyen pratique d’autoriser une application à maximiser son utilisation des ressources du processeur dans un système, en particulier dans une configuration à plusieurs processeurs. Dans un environnement Services Bureau à distance, toutefois, plusieurs utilisateurs peuvent exécuter des applications multithread, et tous les threads de tous les utilisateurs sont en concurrence pour les ressources de processeur central de ce système. En tenant compte de cela, vous devez régler et équilibrer l’utilisation des threads d’application pour un environnement multi-utilisateur, multiprocesseur Services Bureau à distance. Alors qu’une application multithread mal conçue avec des threads inactifs ou inutilisés peut s’exécuter correctement sur un ordinateur client, la même application peut ne pas s’exécuter correctement sur un serveur Services Bureau à distance multi-utilisateur.

 

 




