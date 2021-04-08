---
title: Résolution des problèmes de connexion Internet
description: Dans ce scénario, un utilisateur tente d’accéder à www.msn.com à l’aide du protocole HTTPS, mais il ne peut pas se connecter. Vous pouvez utiliser les commandes netsh et Moniteur réseau pour collecter et afficher les traces afin de déterminer la raison de l’échec de la connexion.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753636c1186243a96e3cef5a4ab73244556daec4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839797"
---
# <a name="troubleshooting-internet-connections"></a>Résolution des problèmes de connexion Internet

Dans ce scénario, un utilisateur tente d’accéder à www.msn.com à l’aide du protocole HTTPS, mais il ne peut pas se connecter. Vous pouvez utiliser les commandes netsh et Moniteur réseau pour collecter et afficher les traces afin de déterminer la raison de l’échec de la connexion.

Tout d’abord, vous pouvez utiliser Netsh pour démarrer une trace. Tapez **netsh trace Start Scenario = internetclient tracefile = MSN. etl** démarre le suivi de tous les fournisseurs activés dans le cadre du scénario internetclient, en enregistrant les résultats dans un fichier nommé MSN. etl. Après avoir utilisé un navigateur Web pour tenter d’atteindre www.msn.com, la saisie de **netsh trace stop** se termine et met en corrélation le fichier de trace.

Vous pouvez ensuite ouvrir le fichier MSN. etl dans Moniteur réseau. Les événements sont regroupés par ID d’activité dans le volet gauche. L’utilisation de la description de filtre **. Contains (« MSN »)** affiche uniquement les événements qui incluent la chaîne « MSN » dans leur description de protocole.

![résolution des problèmes de connexion Internet à l’aide du moniteur réseau (1)](images/internetclient1.png)

Ensuite, vous pouvez examiner les événements dans le résumé des frames pour identifier un événement qui semble pertinent. Après avoir sélectionné l’événement, cliquez avec le bouton droit et pointez sur Rechercher des conversations, puis cliquez sur UTEvent pour sélectionner la conversation au niveau du UTEvent.

![résolution des problèmes de connexion Internet à l’aide du moniteur réseau (2)](images/internetclient2.png)

L’activité normalisée associée dans le volet gauche est ensuite mise en surbrillance, dans ce cas UTEvent ActivityID 397.

![résolution des problèmes de connexion Internet à l’aide du moniteur réseau (3)](images/internetclient3.png)

En utilisant Moniteur réseau pour afficher et filtrer les informations de trace, le nombre d’événements à examiner a été réduit de 1989 à 96.

 

 




