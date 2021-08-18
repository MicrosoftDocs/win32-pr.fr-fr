---
title: Administration du serveur RAS
description: Windows NT Server 4,0 fournit un ensemble de fonctions permettant d’administrer les autorisations et les ports des utilisateurs sur les serveurs RAS Windows NT/Windows 2000.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Administration de serveur, RAS
- Administration, serveur RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6760e8cc06e5c7b389d01f690497dc070974cada5e9a922ec5576e48b2a328fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789188"
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

 

 




