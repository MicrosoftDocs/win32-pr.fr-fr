---
title: Recherche du programme serveur
description: Une fois que l’exécution RPC côté client se connecte à un système hôte serveur demandé dans le handle de liaison, la bibliothèque Runtime RPC du client recherche le processus serveur.
ms.assetid: 0c863018-746a-4793-abe7-1838d988e0f4
keywords:
- Appel de procédure distante RPC, tâches, recherche du programme serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b822dbca1a927e13f01d7c91aa7c78267db4d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311525"
---
# <a name="finding-the-server-program"></a>Recherche du programme serveur

Une fois que l’exécution RPC côté client se connecte à un système hôte serveur demandé dans le handle de liaison, la bibliothèque Runtime RPC du client recherche le processus serveur. Pour ce faire, il interroge le mappage du point de terminaison sur le système hôte du serveur. Le mappage de point de terminaison contient des informations sur le point de terminaison sur lequel le serveur est à l’écoute.

 

 




