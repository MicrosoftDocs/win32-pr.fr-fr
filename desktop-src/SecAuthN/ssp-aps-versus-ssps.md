---
description: Explique les différences entre les fournisseurs de services partagés/APs et les SSP.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APs et SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952633"
---
# <a name="sspaps-vs-ssps"></a>SSP/APs et SSP

Les [*packages de sécurité*](../secgloss/s-gly.md) sont déployés dans l’un des types de bibliothèques de liens dynamiques (dll) suivants :

-   [SSP/APs](#sspaps-vs-ssps)
-   [SSP](#sspaps-vs-ssps)

Le fait qu’un package de sécurité se trouve dans un [*package d’authentification*](../secgloss/a-gly.md) /fournisseur de support de sécurité (SSP/AP) ou une dll SSP ( [*Security Support Provider*](../secgloss/s-gly.md) ) est déterminé par les types de services de sécurité qu’il fournit et dans quelle mesure il doit être intégré à l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA). Ces différences déterminent également l’API implémentée dans un package de sécurité personnalisé.

## <a name="sspaps"></a>SSP/APs

Un fournisseur de services partagés/AP est une DLL qui contient un ou plusieurs [*packages de sécurité*](../secgloss/s-gly.md) et peut fonctionner en tant que fournisseur de services partagés pour les applications client/serveur et comme [package d’authentification](authentication-packages.md) pour les applications d’ouverture de session. Pour fonctionner dans ces deux rôles, les services SSP/APs sont chargés dans l’espace de processus LSA au démarrage du système et peuvent également être chargés dans des processus d’application client/serveur.

Les packages de sécurité SSP/AP personnalisés doivent implémenter les [fonctions implémentées par le SSP/APS en mode utilisateur](authentication-functions.md)et les [fonctions implémentées par SSP/APS](authentication-functions.md). Ces implémentations de fonction peuvent utiliser les fonctions de prise en charge LSA pour offrir des fonctionnalités de sécurité avancées telles que la création de jetons, la prise en charge des [*informations d’identification supplémentaires*](../secgloss/s-gly.md) et l’authentification directe.

Si un package de sécurité SSP/AP personnalisé fournit la gamme complète des fonctions d' [*intégrité*](../secgloss/i-gly.md) et de confidentialité des messages, il implémente également les [fonctions implémentées par le SSP/APS en mode utilisateur](authentication-functions.md).

## <a name="ssps"></a>SSP

Un SSP est une DLL qui contient un ou plusieurs packages de sécurité fournissant une connexion authentifiée, une intégrité de message et des services de chiffrement de message aux applications client/serveur. Les SSP implémentent des fonctions SSPI ( [Security Support Provider Interface](sspi.md) ). Les applications peuvent accéder aux packages de sécurité dans un SSP en appelant directement les fonctions SSPI. Les SSP sont chargés dans les processus client et serveur. ils ne sont pas intégrés à l’autorité LSA.

 

 
