---
title: Nettoyage des connexions inactives
description: Par défaut, les connexions dans le pool de threads ne sont pas fermées tant que l’ensemble de l’Association n’est pas arrêté.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc7a7d4cefcead53e9b92678867cd76ceb6fab7f1ab5f1a573cf75378cf2a5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020799"
---
# <a name="idle-connection-cleanup"></a>Nettoyage des connexions inactives

Par défaut, les connexions dans le pool de threads ne sont pas fermées tant que l’ensemble de l’Association n’est pas arrêté. Cette stratégie permet aux clients disposant d’un grand nombre de threads ou d’identités de sécurité d’effectuer des appels RPC au serveur de manière efficace. L’inconvénient est qu’une quantité insuffisante de ressources peut être engagée pour maintenir ces connexions. Pour gérer le processus, RPC fournit la fonction [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) . Cette fonction active le nettoyage des connexions inactives ; le client analyse régulièrement le pool de connexions et ferme les connexions qui n’ont pas été utilisées récemment. Si l’Association a conservé des handles de contexte, le nettoyage de la connexion inactive ferme toutes les connexions inactives, mais veille à ce qu’au moins une connexion reste ouverte, même si la connexion est inactive (sinon, le serveur reçoit des dépassements de contexte). Si l’Association n’a pas conservé de handles de contexte, le nettoyage de la connexion inactive ferme toutes les connexions inactives, même si cela ne laisse aucune connexion dans le pool.

sur Windows XP, l’exécution RPC effectue le suivi du nombre de connexions ouvertes dans une association et active automatiquement le nettoyage de la connexion inactive si le nombre de connexions dans une association dépasse un certain seuil.

 

 




