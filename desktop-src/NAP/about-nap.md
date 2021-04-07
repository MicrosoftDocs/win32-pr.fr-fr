---
title: À propos de NAP
description: À propos de NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671417"
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

Windows XP avec Service Pack 3 (SP3), Windows Vista et Windows Server 2008 fournissent des méthodes de contrainte de mise en conformité NAP pour la configuration des adresses DHCP (Dynamic Host Configuration Protocol), les connexions de réseau privé virtuel (VPN) basées sur l’accès à distance, les connexions câblées et sans fil authentifiées par IEEE 802.1 X et les communications basées sur la sécurité du protocole Internet. En outre, la plateforme NAP prend en charge une architecture via laquelle la validation d’intégrité, la restriction réseau, la mise à jour et la conformité continue sont prises en charge par des composants supplémentaires qui peuvent être fournis par des éditeurs de logiciels tiers ou par Microsoft.

La plateforme NAP comprend les composants suivants :

-   [Architecture du client NAP](nap-client-architecture.md)
-   [Architecture côté serveur NAP](nap-server-side-architecture.md)
-   [Communication entre le client NAP et le composant côté serveur](nap-client-and-server-side-component-communication.md)

Le client NAP requiert Windows Vista, Windows XP avec SP3 ou Windows Server 2008. Le serveur de stratégie de contrôle d’intégrité NAP et les points de contrainte de mise en conformité NAP pour la contrainte DHCP, VPN et IPsec nécessitent Windows Server 2008.

 

 




