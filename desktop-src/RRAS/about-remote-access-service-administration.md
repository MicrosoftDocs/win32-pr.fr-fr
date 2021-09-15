---
title: À propos de l’administration du service d’accès à distance
description: les systèmes d’exploitation Windows 2000 et versions ultérieures fournissent un ensemble de fonctions permettant d’administrer les autorisations et les ports des utilisateurs sur les serveurs RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- Routage et accès à distance service RRAS, administration RAS
- Routage et accès à distance service RRAS, administration RAS, Description
- Administration RAS RRAS
- Administration RAS RRAS, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413625"
---
# <a name="about-remote-access-service-administration"></a>À propos de l’administration du service d’accès à distance

les systèmes d’exploitation Windows 2000 et versions ultérieures fournissent un ensemble de fonctions permettant d’administrer les autorisations et les ports des utilisateurs sur les serveurs RAS. À l’aide de ces fonctions, vous pouvez développer une application d’administration de serveur RAS pour effectuer les tâches suivantes :

-   Énumérer les utilisateurs qui disposent d’un jeu d’autorisations RAS spécifié
-   Affecter ou révoquer des autorisations RAS pour un utilisateur spécifié
-   Énumérer les ports configurés sur un serveur RAS
-   Obtenir des informations et des statistiques sur un port spécifié sur un serveur RAS
-   Réinitialiser les compteurs de statistiques pour un port spécifié
-   Déconnecter un port spécifié

Vous pouvez également installer une DLL d’administration de serveur RAS pour auditer les connexions utilisateur et affecter des adresses IP aux utilisateurs distants. La DLL exporte un ensemble de fonctions que le serveur RAS appelle chaque fois qu’un utilisateur tente de se connecter ou de se déconnecter.

Cette documentation décrit les rubriques suivantes :

-   [comparaison de fonctions : Windows 2000 et RRAS redistributable](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [Administration des utilisateurs RAS](ras-user-administration.md)
-   [Administration du serveur et du port RAS](ras-server-and-port-administration.md)
-   [DLL d’administration RAS](ras-administration-dll.md)
-   [Configuration du registre des DLL d’administration RAS](ras-administration-dll-registry-setup.md)

 

 




