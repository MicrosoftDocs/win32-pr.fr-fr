---
title: Utilisation de threads
description: Vous devez ajuster et équilibrer l’utilisation des threads d’application pour un environnement multi-utilisateur, multiprocesseur Services Bureau à distance.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22959c6950458c95670d71479a2efe04fdafea765048508b9bd371b0a215064d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869519"
---
# <a name="thread-usage"></a>Utilisation de threads

Les threads offrent un moyen pratique d’autoriser une application à maximiser son utilisation des ressources du processeur dans un système, en particulier dans une configuration à plusieurs processeurs. Dans un environnement Services Bureau à distance, toutefois, plusieurs utilisateurs peuvent exécuter des applications multithread, et tous les threads de tous les utilisateurs sont en concurrence pour les ressources de processeur central de ce système. En tenant compte de cela, vous devez régler et équilibrer l’utilisation des threads d’application pour un environnement multi-utilisateur, multiprocesseur Services Bureau à distance. Alors qu’une application multithread mal conçue avec des threads inactifs ou inutilisés peut s’exécuter correctement sur un ordinateur client, la même application peut ne pas s’exécuter correctement sur un serveur Services Bureau à distance multi-utilisateur.

 

 




