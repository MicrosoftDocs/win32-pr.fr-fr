---
title: Administration des utilisateurs RAS
description: Un serveur RAS utilise une base de données de comptes d’utilisateur qui contient des informations sur un ensemble de comptes d’utilisateur.
ms.assetid: b58767b0-9b76-4d43-953a-ea772643745e
keywords:
- Administration RAS RRAS, administration des utilisateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 742bf3e357ef813a60c67f991b6e5829879d3e1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512523"
---
# <a name="ras-user-administration"></a>Administration des utilisateurs RAS

Un serveur RAS utilise une base de données de comptes d’utilisateur qui contient des informations sur un ensemble de comptes d’utilisateur. Les informations incluent les privilèges RAS d’un utilisateur, qui sont un ensemble d’indicateurs binaires qui déterminent comment le serveur RAS répond quand l’utilisateur appelle pour se connecter. Les fonctions d’administration du serveur RAS localisent la base de données des comptes d’utilisateur et obtiennent et définissent les privilèges RAS pour les comptes d’utilisateur.

Un serveur RAS peut faire partie d’un domaine du système d’exploitation ou il peut être un ordinateur autonome qui exécute la version serveur ou professionnel du système d’exploitation. Pour un serveur qui fait partie d’un domaine, la base de données de comptes d’utilisateur est stockée sur le serveur qui est le contrôleur de domaine principal (PDC). Un serveur autonome stocke sa propre base de données de compte d’utilisateur local. Pour obtenir le nom du serveur qui stocke la base de données de comptes d’utilisateur utilisée par un serveur RAS spécifié, vous pouvez appeler la fonction [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) . Vous pouvez ensuite utiliser le nom du serveur de comptes d’utilisateur dans un appel à la fonction [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) pour énumérer les utilisateurs dans une base de données de comptes d’utilisateur. Vous pouvez également utiliser le nom du serveur dans les appels aux fonctions [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) et [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) pour obtenir et définir les privilèges RAS pour un compte d’utilisateur spécifié.

Les fonctions [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) et [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) utilisent la structure de l' [**\_ utilisateur RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) pour spécifier les privilèges RAS d’un utilisateur et le numéro de téléphone de rappel. Les privilèges RAS indiquent les informations suivantes :

-   Si l’utilisateur peut établir une connexion à distance au serveur ou au domaine auquel le serveur appartient.
-   Si l’utilisateur établit une connexion par le biais d’un rappel, dans lequel le serveur RAS se bloque, puis rappelle à l’utilisateur d’établir la connexion.

Chaque compte d’utilisateur spécifie l’un des indicateurs suivants pour indiquer les privilèges de rappel de l’utilisateur.



| Valeur                      | Signification                                                                                                                                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ Nocallback        | Le serveur RAS ne rappelle pas l’utilisateur pour établir une connexion.                                                                                                                                                                                                          |
| RASPRIV \_ AdminSetCallback  | Lorsque l’utilisateur appelle, le serveur RAS se bloque et appelle un numéro de téléphone de rappel prédéfini stocké dans la base de données des comptes d’utilisateur. Le membre **szPhoneNumber** de la structure de l' [**\_ utilisateur RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) contient le numéro de téléphone de l’utilisateur appelant.                       |
| RASPRIV \_ CallerSetCallback | Lorsque l’utilisateur appelle, le serveur RAS offre la possibilité de spécifier un numéro de téléphone auquel rappeler l’utilisateur. L’utilisateur peut également choisir de se connecter immédiatement sans rappeler. Le membre **szPhoneNumber** contient un nombre par défaut que l’utilisateur peut remplacer. |



 

 

 