---
description: Les informations sur les packages de notification Winlogon sont stockées dans le registre. Les entrées de Registre spécifient le nom du package de notification, le nom de la DLL qui implémente le package et les noms des fonctions qui gèrent les événements Winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Inscription d’un package de notifications Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202718"
---
# <a name="registering-a-winlogon-notification-package"></a>Inscription d’un package de notifications Winlogon

Les informations sur les packages de notification [*Winlogon*](../secgloss/w-gly.md) sont stockées dans le registre. Les entrées de Registre spécifient le nom du package de notification, le nom de la DLL qui implémente le package et les noms des fonctions qui gèrent les événements Winlogon.

Lorsque Winlogon démarre, il vérifie le registre et charge tous les packages de notification inscrits. Lorsqu’un événement se produit, Winlogon appelle la fonction de gestionnaire d’événements désignée pour chaque package. Plusieurs packages de notification d’événements peuvent être inscrits sur un système.

Pour inscrire votre package de notification, créez une clé de Registre nommée **Notify** en tant que sous-clé de la clé de Registre suivante et ajoutez les valeurs détaillées dans les [entrées de registre](registry-entries.md).

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**

 

 
