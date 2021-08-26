---
title: Considérations sur la sécurité des hôtes d’appareils
description: L’utilisation de l’hôte d’appareil crée des problèmes de sécurité.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4e8cdce90cdc5801010833db4cb97c49487c16a3926bf235f126f33e1078f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008089"
---
# <a name="device-host-security-considerations"></a>Considérations sur la sécurité des hôtes d’appareils

L’utilisation de l’hôte d’appareil crée des problèmes de sécurité en raison des éléments suivants :

-   les appareils hébergés sur un ordinateur exécutant Windows XP envoient des annonces sur tous les réseaux.
-   les appareils hébergés sur un ordinateur exécutant Windows XP autorisent le contrôle des appareils à partir de tous les réseaux.

cela augmente le risque pour les particuliers, car les appareils tels qu’un lecteur multimédia ou un système de chauffage ou un appareil HVAC hébergé sur un ordinateur exécutant Windows XP sont visibles et peuvent être contrôlés à partir des points de contrôle en dehors du foyer.

Lorsque vous créez un appareil hébergé, vous devez prendre en considération certains problèmes de sécurité.

-   Pour réduire l’étendue de la découverte et de l’attaque des périphériques UPnP, la durée de vie de tous les messages SSDP est de 1. Cela signifie qu’un appareil inscrit est découvert uniquement par des points de contrôle sur le même réseau. Vous pouvez configurer une durée de vie plus élevée dans le registre.
-   L’inscription d’un appareil non en cours d’exécution nécessite la pré-inscription de l’appareil .dll avec COM, ce qui requiert des privilèges d’administrateur.
-   L’inscription d’un appareil en cours d’exécution nécessite un privilège administrateur, service local ou système local.
-   Lorsque l’hôte d’appareil est démarré, il est exécuté en tant que [LocalService](/windows/desktop/Services/localservice-account). Cela donne à l’appareil la possibilité de générer des audits et de lire la clé de Registre **HKEY \_ local \_ machine** . L’appareil a accès à **HKEY \_ Current \_ User**. Le compte LocalService peut utiliser des ressources auxquelles l’accès LocalService a été accordé, ainsi que celles qui accordent l’accès à AuthenticatedUser. L’appareil a accès limité au système de fichiers.
-   Les listes de contrôle d’accès du système de fichiers doivent être mises à jour pour autoriser l’accès [LocalService](/windows/desktop/Services/localservice-account) au répertoire de ressources.
-   Si votre appareil doit disposer d’un accès plus sécurisé, vous pouvez créer votre propre processus pour l’appareil et l’inscrire à l’aide de [**IUPnPRegistrar :: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

 

 