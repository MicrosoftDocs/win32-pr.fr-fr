---
description: Le gestionnaire de contrôle des services (SCM) gère une base de données des services installés et des services de pilotes, et fournit un moyen unifié et sécurisé de les contrôler.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: À propos des services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58bcd2058ec8f8de5cbe56a521e2d83919a17532c00dab175d93305edd3684d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126479"
---
# <a name="about-services"></a>À propos des services

Le [Gestionnaire de contrôle](service-control-manager.md) des services (SCM) gère une base de données des services installés et des services de pilotes, et fournit un moyen unifié et sécurisé de les contrôler. La base de données contient des informations sur la façon dont chaque service ou service de pilote doit être démarré. Il permet également aux administrateurs système de personnaliser les exigences de sécurité pour chaque service et ainsi de contrôler l’accès au service.

Les types de programmes suivants utilisent les fonctions fournies par le SCM.



| Type                          | Description                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Programme de service               | Programme qui fournit du code exécutable pour un ou plusieurs services. Les programmes de service utilisent des fonctions qui se connectent au SCM et envoient des informations d’État au SCM.                                                                                                                                                                          |
| Programme de configuration de service | Programme qui interroge ou modifie la base de données de services. Les programmes de configuration de service utilisent des fonctions qui ouvrent la base de données, installent ou suppriment des services dans la base de données, puis interrogent ou modifient les paramètres de configuration et de sécurité pour les services installés. Les programmes de configuration de service gèrent les services et les pilotes. |
| Programme de contrôle de service       | Programme qui démarre et contrôle les services et les services de pilotes. Les programmes de contrôle de service utilisent des fonctions qui envoient des demandes au SCM, qui exécute la demande.                                                                                                                                                                     |



 

Cette vue d’ensemble aborde les sujets suivants :

-   [Gestionnaire de contrôle des services](service-control-manager.md)
-   [Programmes de service](service-programs.md)
-   [Programmes de configuration de service](service-configuration-programs.md)
-   [Programmes de contrôle de service](service-control-programs.md)
-   [Comptes d’utilisateur de service](service-user-accounts.md)
-   [Services interactifs](interactive-services.md)
-   [Sécurité des services et droits d’accès](service-security-and-access-rights.md)
-   [Déboguer un service](debugging-a-service.md)
-   [Événements de déclencheur de service](service-trigger-events.md)

 

 



