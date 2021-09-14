---
description: Un package de notification Winlogon est une DLL qui exporte les fonctions qui gèrent les événements Winlogon. Par exemple, lorsqu’un utilisateur se connecte au système, Winlogon appelle la fonction de gestionnaire d’événements Logon du package de notification pour fournir des informations sur l’événement.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Création d’un package de notifications Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096446"
---
# <a name="creating-a-winlogon-notification-package"></a>Création d’un package de notifications Winlogon

Un package de notification [*Winlogon*](/windows/desktop/SecGloss/w-gly) est une dll qui exporte les fonctions qui gèrent les événements Winlogon. Par exemple, lorsqu’un utilisateur se connecte au système, Winlogon appelle la fonction de gestionnaire d’événements Logon du package de notification pour fournir des informations sur l’événement.

Les noms des fonctions de gestionnaire d’événements implémentées dans un package de notification sont laissés au développeur. Winlogon vérifie le registre pour obtenir les noms des fonctions de gestionnaire d’événements. Par exemple, un package de notification peut implémenter la fonction de gestionnaire d’événements LOGON, `WLEventLogon` tandis qu’un autre peut utiliser `HandleLogonEvent` .

Vous n’avez pas à implémenter et à inscrire des gestionnaires d’événements pour chaque événement Winlogon, uniquement pour les événements qui sont utiles à votre application. Chaque fonction de gestionnaire d’événements doit utiliser le prototype de fonction décrit dans [prototype de fonction du gestionnaire d’événements](event-handler-function-prototype.md). Ce prototype a un seul paramètre : une structure d' [**\_ \_ informations de notification wlx**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) qui contient des détails sur l’événement.

Winlogon ignore la sortie des fonctions de gestionnaire d’événements. Si la gestion d’un événement nécessite l’interaction avec Winlogon, utilisez les [fonctions de prise en charge de Winlogon](authentication-functions.md).

Pour utiliser votre package de notification Winlogon, la DLL doit être copiée dans le dossier% SystemRoot% \\ system32, et une mise à jour du registre doit être effectuée pour le package de notification. Pour plus d’informations sur la mise à jour du Registre, consultez [inscription d’un package de notification Winlogon](registering-a-winlogon-notification-package.md).

 

 
