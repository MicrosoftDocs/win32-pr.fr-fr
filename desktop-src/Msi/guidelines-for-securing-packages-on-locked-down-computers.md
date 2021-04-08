---
description: Pour aider à maintenir une installation logicielle sécurisée sur des ordinateurs verrouillés, respectez ces instructions lors de la création du package Windows Installer.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Sécurisation des packages sur les ordinateurs verrouillés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8380ad7e342d35bff80da4d4d86c37759a80a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866314"
---
# <a name="securing-packages-on-locked-down-computers"></a>Sécurisation des packages sur les ordinateurs verrouillés

Lorsque vous créez un package Windows Installer qui sera utilisé sur des ordinateurs verrouillés, vous respectez les instructions suivantes pour assurer la maintenance d’un environnement sécurisé lors de l’installation :

-   Testez la compatibilité de votre package avec la [stratégie système](system-policy.md)de l’ordinateur Windows Installer.
-   Veillez à ce que le package s’exécute avec tous les [niveaux d’interface utilisateur](user-interface-levels.md), aucun, de base, limité et complet.
-   Testez votre package sur des partitions NTFS, avec des privilèges [*élevés*](e-gly.md) et non élevés.
-   À compter de Windows Installer 3,0, la mise à [jour corrective du contrôle de compte d’utilisateur](user-account-control--uac--patching.md) permet aux utilisateurs non-administrateurs d’appliquer des correctifs aux applications installées dans le contexte par ordinateur. Testez votre package de correctifs sur Windows Vista et Windows XP pour l’installation par les utilisateurs disposant d’un accès administrateur et par des utilisateurs non-administrateurs.

 

 



