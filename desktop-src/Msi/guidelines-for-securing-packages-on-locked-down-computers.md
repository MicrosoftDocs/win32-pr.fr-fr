---
description: pour aider à maintenir une installation logicielle sécurisée sur des ordinateurs verrouillés, respectez ces instructions lors de la création du package Windows Installer.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Sécurisation des packages sur les ordinateurs verrouillés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bcdb2770e165a8b0d99fbc2088ec4c3b113e5befa180a7d6d2598eee866a5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315299"
---
# <a name="securing-packages-on-locked-down-computers"></a>Sécurisation des packages sur les ordinateurs verrouillés

lorsque vous créez un package Windows Installer qui sera utilisé sur des ordinateurs verrouillés, vous respectez les instructions suivantes pour assurer la maintenance d’un environnement sécurisé lors de l’installation :

-   testez la compatibilité de votre package avec la [stratégie système](system-policy.md)de l’ordinateur Windows Installer.
-   Veillez à ce que le package s’exécute avec tous les [niveaux d’interface utilisateur](user-interface-levels.md), aucun, de base, limité et complet.
-   Testez votre package sur des partitions NTFS, avec des privilèges [*élevés*](e-gly.md) et non élevés.
-   à compter de Windows Installer 3,0, la mise à [jour corrective du contrôle de compte d’utilisateur](user-account-control--uac--patching.md) permet aux utilisateurs non-administrateurs d’appliquer des correctifs aux applications installées dans le contexte par ordinateur. testez votre package de correctifs sur Windows Vista et Windows XP pour l’installation par les utilisateurs disposant d’un accès administrateur et par des utilisateurs non-administrateurs.

 

 



