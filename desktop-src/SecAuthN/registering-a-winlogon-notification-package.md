---
description: Les informations sur les packages de notification Winlogon sont stockées dans le registre. Les entrées de Registre spécifient le nom du package de notification, le nom de la DLL qui implémente le package et les noms des fonctions qui gèrent les événements Winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Inscription d’un package de notifications Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa41948062458581d607b64432166b99ba4701865a3c7b593365c87342359ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919668"
---
# <a name="registering-a-winlogon-notification-package"></a>Inscription d’un package de notifications Winlogon

Les informations sur les packages de notification [*Winlogon*](../secgloss/w-gly.md) sont stockées dans le registre. Les entrées de Registre spécifient le nom du package de notification, le nom de la DLL qui implémente le package et les noms des fonctions qui gèrent les événements Winlogon.

Lorsque Winlogon démarre, il vérifie le registre et charge tous les packages de notification inscrits. Lorsqu’un événement se produit, Winlogon appelle la fonction de gestionnaire d’événements désignée pour chaque package. Plusieurs packages de notification d’événements peuvent être inscrits sur un système.

Pour inscrire votre package de notification, créez une clé de Registre nommée **Notify** en tant que sous-clé de la clé de Registre suivante et ajoutez les valeurs détaillées dans les [entrées de registre](registry-entries.md).

**HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**

 

 
