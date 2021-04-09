---
description: Répertorie les événements de notification Winlogon.
ms.assetid: 48b0f389-5b3c-4b13-ad23-a8bc6bcd1850
title: Événements de notification Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58827dc2699c92dfc3a814d2366608e1bd3fb662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862390"
---
# <a name="winlogon-notification-events"></a>Événements de notification Winlogon

[*Winlogon*](../secgloss/w-gly.md) peut informer votre package de notification des événements suivants.



| Événement                               | Description                                                                                                                                                                                                                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Verrou**<br/>                 | Cet événement se produit lorsque l’utilisateur verrouille la station de travail.<br/>                                                                                                                                                                                                                                                   |
| **Fermeture**<br/>               | Cet événement se produit lorsqu’un utilisateur se déconnecte du système. L’événement de **déconnexion** est exécuté de façon synchrone, même si les paramètres de Registre du package de notification indiquent qu’il peut gérer les événements de façon asynchrone.<br/>                                                                                         |
| **Ouverture de session**<br/>                | Cet événement se produit lorsqu’un utilisateur se connecte au système.<br/> Notez que l’événement **Logon** se produit avant la restauration des connexions réseau de l’utilisateur. Si votre gestionnaire d’événements nécessite l’accès aux connexions réseau de l’utilisateur, il doit gérer l’événement **StartShell** à la place de l’événement **Logon** .<br/> |
| **Arrêter**<br/>             | Cet événement se produit juste avant l’arrêt du système.<br/>                                                                                                                                                                                                                                                     |
| **SmartCardLogonNotify**<br/> | Cet événement se produit lorsqu’un utilisateur ouvre une session sur le système à l’aide d’une carte à puce.<br/>                                                                                                                                                                                                                                   |
| **StartScreenSaver**<br/>     | Cet événement se produit lorsque l’économiseur d’écran a démarré. En règle générale, cela se produit une fois qu’un utilisateur a été inactif pendant un laps de temps défini.<br/> Les fonctions qui gèrent cet événement ne doivent pas afficher une interface utilisateur. La notification d’événement **StartScreenSaver** est fournie à titre d’information uniquement.<br/> |
| **StartShell**<br/>           | Cet événement se produit une fois que l’utilisateur s’est connecté au système, que des connexions réseau ont été établies et que le programme d’interpréteur de commandes spécifié par l’utilisateur (généralement l’Explorateur Windows) a été démarré.<br/>                                                                                                                |
| **Startup**<br/>              | Cet événement se produit lorsque le système est démarré ou redémarré.<br/>                                                                                                                                                                                                                                               |
| **StopScreenSaver**<br/>      | Cet événement se produit lorsque l’économiseur d’écran s’est arrêté. Cela se produit généralement en cas d’activité du clavier ou de la souris.<br/> Les fonctions qui gèrent cet événement ne doivent pas afficher une interface utilisateur. La notification d’événement **StopScreenSaver** est fournie à titre d’information uniquement.<br/>                  |
| **Bloquer**<br/>               | Cet événement se produit lorsque l’utilisateur déverrouille la station de travail ou lorsqu’un administrateur système remplace le verrou et déconnecte l’utilisateur.<br/>                                                                                                                                                                         |



 

 

 
