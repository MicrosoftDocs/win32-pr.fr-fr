---
description: Décrit les fonctionnalités d’un redirecteur réseau.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Redirecteurs réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce8c887cba779fe3f6aee9811819c6638d926f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009895"
---
# <a name="network-redirectors"></a>Redirecteurs réseau

Un redirecteur réseau est un pilote de système de fichiers (ou FSD) qui fonctionne de la manière suivante :

-   En tant que client dans le cadre d’une opération d’e/s réseau en envoyant des demandes d’e/s aux serveurs et en traitant les réponses des serveurs.
-   En tant que serveur dans le cadre d’une opération d’e/s réseau en recevant des demandes d’e/s des serveurs et en traitant les demandes.

Il effectue toute l’interaction de bas niveau avec le serveur pour résoudre le nom de fichier fourni par l’application avec l’emplacement de la ressource sur le serveur distant. De cette façon, le redirecteur permet à l’application d’accéder aux ressources sur les serveurs distants et de les manipuler comme si elles se trouvaient sur l’ordinateur local.

Les redirecteurs fonctionnent entièrement en mode noyau. Cela offre les avantages suivants en matière de performances par rapport aux alternatives en mode utilisateur :

-   Il peut interagir avec les FSDs en mode noyau s’exécutant sur le serveur, tels que le serveur FSD, sans nécessiter de commutateurs de contexte de mode noyau à utilisateur et de mode utilisateur à noyau.
-   Il peut interagir en mode noyau avec le gestionnaire de cache sur le serveur pour mettre en cache les données d’e/s envoyées par le gestionnaire de cache du serveur sur le client.
-   Les fonctions d’API personnalisées pour les demandes d’e/s distantes et les modifications apportées aux fonctions d’e/s de fichier standard pour fournir cette fonctionnalité ne sont pas nécessaires.

 

 



