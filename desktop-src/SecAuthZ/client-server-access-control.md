---
description: Une application serveur fournit des services aux clients.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Access Control client/serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534382"
---
# <a name="clientserver-access-control"></a>Access Control client/serveur

Une application serveur fournit des services aux clients. Par exemple, un serveur peut effectuer les services suivants pour le compte d’un client :

-   Enregistrer et récupérer des informations à partir d’une base de données privée
-   Accéder aux ressources réseau
-   Démarrer les [*processus*](/windows/desktop/SecGloss/p-gly) dans le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) du client sur l’ordinateur du serveur

Un serveur protégé contrôle l’accès à ses services. Windows fournit une prise en charge de la sécurité qui permet à un serveur d’effectuer les opérations suivantes :

-   Emprunter l’identité du contexte de [*sécurité*](/windows/desktop/SecGloss/s-gly)d’un client, ce qui amène le système à effectuer la plupart des contrôles d’accès et de [*privilège*](/windows/desktop/SecGloss/p-gly) sur le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) du client plutôt que sur le serveur
-   Enregistrer un client sur l’ordinateur du serveur
-   Se connecter aux ressources réseau à l’aide du contexte de sécurité du client
-   Créer des [*descripteurs de sécurité*](/windows/desktop/SecGloss/s-gly) pour protéger des objets privés
-   Déterminer si un descripteur de sécurité autorise l’accès à un client
-   Déterminer si un jeu de privilèges est activé dans le jeton d’un client
-   Générer des messages d’audit dans le journal des événements de sécurité pour enregistrer les tentatives d’accès par un client aux objets ou utiliser des privilèges

 

 
