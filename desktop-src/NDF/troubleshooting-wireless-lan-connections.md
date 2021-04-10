---
title: Résolution des problèmes de connexion LAN sans fil
description: Dans ce scénario, un utilisateur tente de se connecter à un réseau local sans fil, mais il n’est pas en mesure de se connecter. Vous pouvez utiliser les commandes netsh et Moniteur réseau pour collecter et afficher les traces afin de déterminer la raison de l’échec de la connexion.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55878afcee0091634415d4dbc465d1b143f46057
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029683"
---
# <a name="troubleshooting-wireless-lan-connections"></a>Résolution des problèmes de connexion LAN sans fil

Dans ce scénario, un utilisateur tente de se connecter à un réseau local sans fil, mais il n’est pas en mesure de se connecter. Vous pouvez utiliser les commandes netsh et Moniteur réseau pour collecter et afficher les traces afin de déterminer la raison de l’échec de la connexion.

Tout d’abord, vous pouvez utiliser Netsh pour démarrer une trace. Le fait de taper **netsh trace Start scénario = WLAN tracefile = wlanwpp. etl** démarre le suivi de tous les fournisseurs activés dans le cadre du scénario de réseau local sans fil, en enregistrant les résultats dans un fichier nommé wlanwpp. etl. Après une tentative de connexion au réseau local sans fil, la saisie de **netsh trace stop** se termine et met en corrélation le fichier de trace.

Vous pouvez ensuite ouvrir le fichier wlanwpp. etl dans Moniteur réseau. Les événements sont regroupés par ID d’activité dans le volet gauche.

![résolution des problèmes de connexion de réseau local sans fil à l’aide du moniteur réseau (1)](images/1wlan.png)

L’ETL contient de nombreux suivis provenant d’autres fournisseurs de réseau qui sont activés. Vous pouvez appliquer un filtre pour afficher uniquement les événements pertinents pour le fournisseur **\_ MicrosoftWindowsWlanAutoConfig WLAN** .

![résolution des problèmes de connexion de réseau local sans fil à l’aide du moniteur réseau (2)](images/2wlan.png)

Une fois le filtre appliqué, vous pouvez examiner les événements dans le résumé des frames pour identifier un événement qui semble pertinent. Après avoir sélectionné l’événement, cliquez avec le bouton droit et pointez sur Rechercher des conversations, puis cliquez sur netpair.

![résolution des problèmes de connexion de réseau local sans fil à l’aide du moniteur réseau (3)](images/3wlan.png)

Le développement des éléments sous un ID d’activité dans le volet gauche vous permet d’afficher tous les autres fournisseurs pertinents pour la tentative de connexion. Pour afficher les événements d’autres fournisseurs, tous les filtres sont supprimés en cliquant sur **supprimer** dans le volet **filtre d’affichage** . Les suivis peuvent être analysés en faisant défiler le résumé des frames, en sélectionnant des événements supplémentaires, le cas échéant, pour obtenir plus d’informations. Dans ce cas, le volet Détails du cadre fournit des informations indiquant que l’échec est dû à une défaillance de l’échange de clés, ce qui est probablement dû au fait que l’utilisateur a entré une clé de passe incorrecte.

 

 




