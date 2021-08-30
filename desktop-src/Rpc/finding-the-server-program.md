---
title: Recherche du programme serveur
description: Une fois que l’exécution RPC côté client se connecte à un système hôte serveur demandé dans le handle de liaison, la bibliothèque Runtime RPC du client recherche le processus serveur.
ms.assetid: 0c863018-746a-4793-abe7-1838d988e0f4
keywords:
- Appel de procédure distante RPC, tâches, recherche du programme serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4732bb1b47efc2614c79d5f36426c7d9f2118e2c9026f5a76aaf4b11ce54fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021219"
---
# <a name="finding-the-server-program"></a>Recherche du programme serveur

Une fois que l’exécution RPC côté client se connecte à un système hôte serveur demandé dans le handle de liaison, la bibliothèque Runtime RPC du client recherche le processus serveur. Pour ce faire, il interroge le mappage du point de terminaison sur le système hôte du serveur. Le mappage de point de terminaison contient des informations sur le point de terminaison sur lequel le serveur est à l’écoute.

 

 




