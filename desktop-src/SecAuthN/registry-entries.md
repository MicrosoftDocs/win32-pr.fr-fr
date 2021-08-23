---
description: Explique les entrées de Registre pour les événements Winlogon.
ms.assetid: dbebe23f-84ff-4a3e-8b8c-fa3bda10fa57
title: Entrées de Registre (authentification)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 388cbe42d085543d5e7d4df1c9705504864b370cf94eb32f4025eaba12b89ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919445"
---
# <a name="registry-entries-authentication"></a>Entrées de Registre (authentification)

Pour que votre package puisse recevoir des notifications d’événements de [*Winlogon*](../secgloss/w-gly.md), vous devez fournir le nom du package, les noms des fonctions du gestionnaire d’événements dans le package, la dll responsable de l’implémentation du package, ainsi que des informations indiquant si la dll prend en charge les événements asynchrones et l’emprunt d’identité.

Vous devez créer la clé de Registre du package de notification en tant que sous-clé de

**HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Notify**

Le nom de la clé est généralement identique au nom de la DLL. Toutefois, ce n’est pas obligatoire. Le nom choisi pour votre package ne doit pas être en conflit avec les noms des autres packages de notification installés.

Dans la clé de Registre **Notify** , créez les valeurs de Registre suivantes si votre package contient une fonction de gestionnaire d’événements pertinente.



| Type de données du nom de la valeur \[\]                         | Description                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Asynchrone** \[ **Reg \_ Valeur DWORD**\]<br/>    | Indique si le package peut gérer les événements de façon asynchrone. Si cette valeur est définie sur 1, Winlogon appelle les fonctions du package dans un thread distinct. Sinon, elle ne l'a pas.<br/>                                                                                                                                                                                                                                 |
| **DllName** \[ **Reg \_ DÉVELOPPER \_ SZ**\]<br/>    | Nom de la DLL qui implémente le package de notification, par exemple : « Notify.dll ».<br/>                                                                                                                                                                                                                                                                                                                          |
| **Emprunter l’identité** \[ **Reg \_ Valeur DWORD**\]<br/>     | Indique si Winlogon doit emprunter l’identité du [*contexte*](../secgloss/c-gly.md) de sécurité de l’utilisateur connecté lorsqu’il appelle les fonctions du package de notification. Si cette valeur est définie sur 1, Winlogon utilise l’emprunt d’identité. Sinon, elle ne l'a pas.<br/>                                                                                                                    |
| **Verrou** \[ **Reg \_ SZ**\]<br/>               | Nom de la fonction qui gère les événements de verrouillage du bureau, par exemple : « WLEventLock ».<br/>                                                                                                                                                                                                                                                                                                                           |
| **Fermeture de session** \[ **Reg \_ SZ**\]<br/>             | Nom de la fonction qui gère les événements de fermeture de session, par exemple : « WLEventLogoff ».<br/>                                                                                                                                                                                                                                                                                                                               |
| **Ouverture de session** \[ **Reg \_ SZ**\]<br/>              | Nom de la fonction qui gère les événements d’ouverture de session, par exemple : « WLEventLogon ».<br/>                                                                                                                                                                                                                                                                                                                                 |
| **Arrêter** \[ **Reg \_ SZ**\]<br/>           | Nom de la fonction qui gère les événements d’arrêt, par exemple : « WLEventShutdown ».<br/>                                                                                                                                                                                                                                                                                                                           |
| **SmartCardLogonNotify** \[ **Valeur DWORD**\]<br/> | Indique si Winlogon doit générer une notification pour les événements de connexion à partir de cartes à puce. Si cette valeur est définie sur 1, Winlogon autorise les notifications par carte à puce. Sinon, elle ne l'a pas.<br/>                                                                                                                                                                                                                     |
| **StartScreenSaver** \[ **Reg \_ SZ**\]<br/>   | Nom de la fonction qui gère les événements de démarrage de l’écran de veille, par exemple : « WLEventStartScreenSaver ».<br/>                                                                                                                                                                                                                                                                                                          |
| **StartShell** \[ **Reg \_ SZ**\]<br/>         | Nom de la fonction qui gère les événements de démarrage de l’interpréteur de commandes, par exemple : « WLEventStartShell ».<br/> Un événement de démarrage de l’interpréteur de commandes se produit une fois que l’utilisateur s’est connecté, mais avant que le bureau n’apparaisse. Il diffère de l’événement Logon dans le fait que le [*contexte*](../secgloss/c-gly.md) de sécurité de l’utilisateur a été établi et que des ressources telles que des connexions réseau sont disponibles.<br/> |
| **Démarrage** \[ **Reg \_ SZ**\]<br/>            | Nom de la fonction qui gère les événements de démarrage du système, par exemple : « WLEventStartup ».<br/>                                                                                                                                                                                                                                                                                                                       |
| **StopScreenSaver** \[ **Reg \_ SZ**\]<br/>    | Nom de la fonction qui gère les événements d’arrêt de l’économiseur d’écran, par exemple : « WLEventStopScreenSaver ».<br/>                                                                                                                                                                                                                                                                                                            |
| **Déverrouiller** \[ **Reg \_ SZ**\]<br/>             | Nom de la fonction qui gère les événements de déverrouillage du bureau, par exemple : « WLEventUnlock ».<br/>                                                                                                                                                                                                                                                                                                                        |



 

 

 
