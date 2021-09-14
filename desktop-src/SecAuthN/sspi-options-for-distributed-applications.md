---
description: Options SSPI pour les applications distribuées
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: Options SSPI pour les applications distribuées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096346"
---
# <a name="sspi-options-for-distributed-applications"></a>Options SSPI pour les applications distribuées

Les développeurs disposent de nombreuses options pour créer des applications distribuées. SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) fournit une couche d’abstraction entre les protocoles de niveau application et les [*protocoles de sécurité*](../secgloss/s-gly.md). Les applications peuvent tirer parti des protocoles de sécurité SSPI de plusieurs façons :

-   Appelez les routines SSPI directement (pour les applications traditionnelles basées sur les Sockets).

    Les routines utilisent des messages de demande/réponse pour implémenter le [*protocole d’application*](../secgloss/a-gly.md) qui transmet les données liées à la sécurité SSPI.

-   Utilisez COM pour appeler des options de sécurité implémentées à l’aide de RPC authentifié et de SSPI à des niveaux inférieurs.

    Ces applications n’appellent pas directement les fonctions SSPI.

-   utilisez [Windows sockets 2](../winsock/windows-sockets-start-page-2.md) (winsock) avec l’interface winsock étendue pour permettre aux fournisseurs de transport d’utiliser les fonctionnalités de sécurité.

    Cette approche intègre le fournisseur SSP ( [*Security Support Provider*](../secgloss/s-gly.md) ) dans la pile réseau et fournit des services de sécurité et de transport par le biais d’une interface commune.

-   utilisez l' [API Windows internet Extensions](../wininet/portal.md) (WinInet) et une interface conçue pour prendre en charge les protocoles de sécurité internet, tels que le protocole SSL ( [*SSL (Secure Sockets Layer)*](../secgloss/s-gly.md) ).

    Les applications utilisent l’interface SSPI sur le fournisseur de sécurité de [canal sécurisé](secure-channel.md) (SChannel) pour implémenter la sécurité wininet. Schannel est l’implémentation Microsoft de SSL.

Plusieurs fonctions SSPI renvoient des horodatages qui représentent l’étendue de la durée de vie de divers objets. Les [*packages de sécurité*](../secgloss/s-gly.md) peuvent conserver du temps et fournir des horodatages de différentes façons, mais l’utilisation de l’heure locale simplifie le travail des applications qui utilisent des fonctions SSPI.

 

 
