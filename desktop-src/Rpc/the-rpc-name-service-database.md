---
title: La base de données du service de noms RPC
description: Un service de noms est un service qui mappe des noms à des objets, et qui gère généralement les paires (nom, objet) d’une base de données.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- Appel de procédure distante RPC, description, base de données de service de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311413"
---
# <a name="the-rpc-name-service-database"></a>La base de données du service de noms RPC

Un service de noms est un service qui mappe des noms à des objets, et qui gère généralement les paires (nom, objet) d’une base de données. En règle générale, le nom est un nom logique facile à mémoriser et à utiliser par les utilisateurs. Par exemple, un service de noms permet à un utilisateur d’utiliser le nom logique « laserprinter ». Le service de noms mappe ce nom au nom spécifique au réseau utilisé par le serveur d’impression.

Pour utiliser une explication simplifiée, le service de noms RPC mappe un nom à un handle de liaison et gère les mappages (nom, handle de liaison) dans la base de données du service de noms RPC. Le service de noms RPC permet aux applications clientes d’utiliser un nom logique plutôt qu’une séquence de protocole et une adresse réseau spécifiques. L’utilisation du nom logique permet aux administrateurs réseau d’installer et de configurer plus facilement votre application distribuée.

Une entrée de base de données du service de noms RPC a l’un des attributs suivants : **serveur**, **groupe** ou **Profil**. Dans l’implémentation Microsoft, les entrées ne peuvent avoir qu’un seul attribut, de sorte que ces entrées sont également appelées des entrées de serveur, des entrées de groupe et des entrées de profil.

L’entrée de serveur se compose d’UUID d’interface, d’UUID d’objets (nécessaires lorsque le serveur implémente des points d’entrée multiples), d’une adresse réseau, d’une séquence de protocole et de toutes les informations de point de terminaison associées à des points de terminaison connus. Lorsqu’un point de terminaison dynamique est utilisé, les informations de point de terminaison sont conservées dans la base de données de mappage des points de terminaison et non dans la base de données du service de noms, et le point de terminaison est résolu comme tout autre point de terminaison dynamique. Les entrées de serveur sont gérées par des fonctions qui commencent par le préfixe « RpcNsBinding ».

L’entrée de groupe peut contenir des entrées de serveur ou d’autres entrées de groupe. Les entrées de groupe sont gérées par des fonctions qui commencent par le préfixe « RpcNsGroup ».

L’entrée de profil peut contenir des entrées de profil, de groupe ou de serveur. Les entrées de profil sont gérées par les fonctions qui commencent par le préfixe « RpcNsProfile ».

Cette section présente une vue d’ensemble de la base de données de service de noms dans les rubriques suivantes :

-   [Instructions pour les applications de service de noms](name-service-application-guidelines.md)
-   [Vue d’ensemble de l’entrée Service Name](an-overview-of-the-name-service-entry.md)
-   [Critères pour les entrées de service de nom](criteria-for-name-service-entries.md)
-   [Nettoyage de l’entrée du service de noms](name-service-entry-cleanup.md)
-   [Ce qui se passe lors d’une requête](what-happens-during-a-query.md)
-   [Utilisation de Microsoft Locator](using-microsoft-locator.md)
-   [Utilisation des service d’annuaire de cellules/service d’annuaires de cellules (CDS)](using-the-cell-directory-service-cds-.md)
-   [Syntaxe de nom](name-syntax.md)

 

 




