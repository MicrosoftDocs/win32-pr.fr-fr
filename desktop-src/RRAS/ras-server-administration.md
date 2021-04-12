---
title: Administration du serveur RAS
description: Windows NT Server 4,0 fournit un ensemble de fonctions permettant d’administrer les autorisations et les ports des utilisateurs sur les serveurs RAS Windows NT/Windows 2000.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Administration de serveur, RAS
- Administration, serveur RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197224"
---
# <a name="ras-server-administration"></a>Administration du serveur RAS

Windows NT Server 4,0 fournit un ensemble de fonctions permettant d’administrer les autorisations et les ports des utilisateurs sur les serveurs RAS Windows NT/Windows 2000. Windows 95 ne prend pas en charge ces fonctions. À l’aide de ces fonctions, vous pouvez développer une application d’administration de serveur RAS pour effectuer les tâches suivantes :

-   Énumérer les utilisateurs qui disposent d’un jeu d’autorisations RAS spécifié
-   Affecter ou révoquer des autorisations RAS pour un utilisateur spécifié
-   Énumérer les ports configurés sur un serveur RAS
-   Obtenir des informations et des statistiques sur un port spécifié sur un serveur RAS
-   Réinitialiser les compteurs de statistiques pour un port spécifié
-   Déconnecter un port spécifié

Vous pouvez également installer une DLL d’administration de serveur RAS pour auditer les connexions utilisateur et affecter des adresses IP aux utilisateurs distants. La DLL exporte un ensemble de fonctions que le serveur RAS appelle chaque fois qu’un utilisateur tente de se connecter ou de se déconnecter.

 

 




