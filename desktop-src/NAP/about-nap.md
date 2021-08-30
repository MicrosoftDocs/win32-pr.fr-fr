---
title: À propos de NAP
description: À propos de NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fcf0b653ae72dcae4bd62958b9b85e238af3e421b9ae18bb9faf58a2faa4db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891729"
---
# <a name="about-nap"></a>À propos de NAP

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La protection d’accès réseau (NAP) est conçue pour aider les administrateurs à maintenir l’intégrité des ordinateurs sur le réseau, ce qui, à son tour, permet de maintenir l’intégrité globale du réseau. Elle n’est pas conçue pour protéger un réseau contre les utilisateurs malveillants. Par exemple, si un ordinateur dispose de tous les logiciels et configurations requis par la stratégie d’accès réseau, l’ordinateur est considéré comme sain ou conforme, et il se verra accorder l’accès approprié au réseau. La protection d’accès réseau n’empêche pas un utilisateur autorisé avec un ordinateur conforme de télécharger un programme malveillant sur le réseau ou d’effectuer un autre comportement inapproprié.

Pour protéger l’accès à un réseau, une infrastructure réseau doit fournir les zones de fonctionnalités suivantes :

-   Validation de l’intégrité : détermine si les ordinateurs sont conformes aux spécifications d’intégrité du système.
-   Restriction réseau : restreint l’accès au réseau ou à la communication pour les clients qui ne sont pas conformes aux exigences d’intégrité du système.
-   Correction : fournit les mises à jour nécessaires pour permettre à l’ordinateur de corriger son état d’intégrité non conforme.
-   Conformité en cours : autorise l’accès au réseau tant que l’ordinateur de l’utilisateur répond aux exigences de la stratégie de contrôle d’intégrité.

Windows XP avec Service Pack 3 (SP3), Windows Vista et Windows Server 2008 fournissent des méthodes de contrainte de mise en conformité NAP pour la configuration des adresses DHCP (Dynamic Host configuration Protocol), les connexions de réseau privé virtuel (VPN) basées sur l’accès à distance, les connexions câblées et sans fil authentifiées par IEEE 802.1 x et les communications IPsec (Internet Protocol security). En outre, la plateforme NAP prend en charge une architecture via laquelle la validation d’intégrité, la restriction réseau, la mise à jour et la conformité continue sont prises en charge par des composants supplémentaires qui peuvent être fournis par des éditeurs de logiciels tiers ou par Microsoft.

La plateforme NAP comprend les composants suivants :

-   [Architecture du client NAP](nap-client-architecture.md)
-   [Architecture côté serveur NAP](nap-server-side-architecture.md)
-   [Communication entre le client NAP et le composant côté serveur](nap-client-and-server-side-component-communication.md)

le client NAP requiert Windows Vista, Windows XP avec SP3 ou Windows Server 2008. le serveur de stratégie de contrôle d’intégrité nap et les points de contrainte de mise en conformité nap pour la contrainte DHCP, VPN et IPsec nécessitent Windows server 2008.

 

 




